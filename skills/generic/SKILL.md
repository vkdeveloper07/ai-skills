---

name: medium-ai-digest
description: >
  Fetch AI and LLM articles from the user's Medium Daily Digest emails and export
  them as a downloadable .md file.
  Trigger this skill whenever the user asks to: pull AI/LLM articles from Medium
  digest, fetch today's/this week's Medium digest for AI content, "get me AI
  articles from Medium", "summarize my Medium digest", "extract LLM posts from my
  Medium email", or any phrasing around reading, collecting, or downloading Medium
  newsletter content related to AI, machine learning, LLMs, or similar tech topics.
  Use this skill even if the user says things like "check my Medium email" or
  "what's in my Medium digest today".
compatibility: "Requires Gmail MCP (connected), web_search + web_fetch, create_file/bash_tool, present_files"
---

# Medium AI Digest Skill

Pulls AI and LLM-relevant articles from the user's Medium Daily Digest email(s), fetches each article's full content,
and saves everything to a formatted Markdown file the user can download.

---

## Step 1 — Find the Medium Digest email(s)

Use the Gmail MCP `search_threads` tool with this query to find recent Medium digest emails:

```text
from:medium.com newer_than:7d
```

> **Note**: `from:noreply@medium.com` is unreliable — `from:medium.com` matches all Medium sending addresses. If the user specified a particular day or date range, adjust `newer_than` (e.g., `newer_than:1d` for today only, `newer_than:14d` for two weeks).

Retrieve up to **3 recent threads** — the most recent one is usually enough, but grab a few in case the user wants broader coverage.

Use `get_message` (not `get_thread`) with `messageFormat: PLAIN_TEXT` to load the email body. Plain text is much more compact and contains all the information you need — author names, titles, teasers, and article ID tracking URLs.

---

## Step 2 — Extract article titles and links from the email body

Medium Digest emails are HTML. The body (in `get_thread` results) may be:

* A raw HTML string inside a `parts` payload
* Base64-encoded (look for `data` fields — decode if needed using `atob()` logic or by running a small bash snippet)

Parse the email to extract a list of:

* **Title** — the article heading text
* **URL** — the `href` pointing to the Medium article (typically `https://medium.com/...`)
* **Subtitle/teaser** — any short description present under the title (optional, used for filtering)

> **Tip**: Medium digest links are often wrapped in tracking redirects (e.g., `https://email.medium.com/...`). These redirect to the real article URL. You do NOT need to follow them before filtering — use the title/teaser text for filtering, then fetch the final article content directly via the real Medium URL or by following the redirect with `web_fetch`.

---

## Step 3 — Filter for AI and LLM relevance

Score each article against this keyword list (case-insensitive match on title + teaser + publication name).

**Critical**: Use **whole-word matching** (regex word boundaries `\b...\b` or equivalent) for short keywords like `AI`, `ML`, `LLM`, `RAG`, `NLP`. Without this, "AI" matches inside "available", "thumbnail", "tail", etc. — leading to false positives.

**Strong signals** (whole-word match on title/teaser → include):
`\bAI\b`, `artificial intelligence`, `\bLLM\b`, `large language model`, `\bGPT\b`, `ChatGPT`, `Claude`, `Gemini`, `Llama`,
`OpenAI`, `Anthropic`, `machine learning`, `deep learning`, `neural network`, `transformer`,
`\bRAG\b`, `retrieval-augmented`, `vector database`, `embedding`, `fine-tuning`, `fine-tune`,
`prompt engineering`, `prompt caching`, `generative AI`, `diffusion model`, `Stable Diffusion`, `multimodal`,
`\bagent\b`, `agentic`, `copilot`, `foundation model`, `\bRLHF\b`, `alignment`, `\bMLOps\b`

**Publication name bonus** — if the publication is one of these, treat it as a strong signal even if the title is vague:
`AI Advances`, `Towards AI`, `AI Engineer Daily`, `The Batch`, `Towards Data Science`, `Better Programming`

**Weak signals** (two or more → include):
`\bmodel\b`, `training`, `inference`, `\bNLP\b`, `automation`, `prediction`, `Python`

If an article matches no keywords and is not in an AI publication, exclude it.

Aim to include **up to 10 articles** per digest run. If there are more matches than 10, prefer articles matching strong signals.

---

## Step 4 — Fetch full article content

For each filtered article:

1. **Search first** — call `web_search` with the article title and author name (e.g., `"Causal LLMs next frontier Agentic Reasoning Debmalya Biswas"`). This is required because `web_fetch` can only access URLs that appeared in a prior search result or were provided by the user.
2. From the search results, identify the Medium article URL (typically `medium.com/p/{id}`, `<publication>.medium.com/...`, or a publication mirror like `aiadvances.org/...`). Pick the most direct article link.
3. Call `web_fetch` on that URL with `html_extraction_method: markdown`.
4. Extract readable content — title, author, publication, body text. Strip navigation, sidebars, clap buttons, and boilerplate ("Sign in", "Become a member", etc.).
5. If the article is member-only, you will still get the introduction and metadata. Include what's available and add a paywall note.

Work through articles **sequentially** — one search + one fetch per article.

---

## Step 5 — Build the Markdown file

Assemble a single `.md` file with this structure:

```markdown
# Medium AI Digest — [Date]

> Automatically extracted from your Medium Daily Digest email.
> [N] AI/LLM articles found.

---

## Table of Contents
- [Article Title 1](#anchor-1)
- [Article Title 2](#anchor-2)
...

---

## [Article Title 1] {#anchor-1}

**Author:** [Name] | **Publication:** [Publication name, if any]
**Link:** [URL]

[Full article body, cleaned up as plain text / Markdown paragraphs]

---

## [Article Title 2] {#anchor-2}
...
```

### Formatting rules

* Convert bullet points and numbered lists to Markdown format
* Preserve code blocks with triple backticks if present
* Strip HTML tags, ad banners, and "Become a member" callouts
* For paywalled articles: include title + author + link + a note: `> ⚠️ This article requires a Medium membership to read in full.`
* Date in the header = date of the digest email, not today's date (unless they match)

---

## Step 6 — Save and present

1. Write the file to `/mnt/user-data/outputs/medium-ai-digest-[YYYY-MM-DD].md`
2. Call `present_files` with that path so the user gets a download card.
3. In your reply, briefly summarise:

   * How many total articles were in the digest
   * How many matched the AI/LLM filter
   * A one-line list of the article titles that were included

---

## Edge cases

| Situation                                                                         | Handling                                                                                                                       |
| --------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------ |
| No Medium digest found in last 7 days                                             | Tell the user, suggest checking if they're subscribed to Medium Daily Digest                                                   |
| All articles are paywalled                                                        | Include titles/links with paywall notice; mention the user may want to open them in their browser while logged in to Medium    |
| Digest email body is not parseable                                                | Try fetching the email as plain text; if still failing, report what was found and ask user for a copy-paste                    |
| User asks for a specific topic narrower than "AI/LLM" (e.g., "only RAG articles") | Apply an additional post-filter after the main AI filter using the user's specific keywords                                    |
| User specifies a date range (e.g., "last week's digest")                          | Adjust the Gmail query's `newer_than` / `older_than` parameters accordingly; merge multiple digest emails into one output file |

---

## Notes

* **Privacy**: Article content is fetched at runtime — nothing is cached or stored beyond the `.md` file.
* **Rate limits**: Medium occasionally rate-limits crawlers. If a `web_fetch` returns a 429 or robot-challenge page, include the article title and link in the output with a note that it couldn't be fetched automatically.
* **Member-only content**: The skill cannot bypass Medium's paywall. It will faithfully note which articles it could and couldn't access.
