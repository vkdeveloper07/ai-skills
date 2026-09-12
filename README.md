The example of medium-ai-digest skill


# Medium AI Digest — September 10–12, 2026

> Pulled from your last 3 Medium Daily Digest emails (Sep 10, Sep 11, Sep 12)  
> **30 total articles scanned · 10 matched the AI/LLM filter**  
> 🔥 Must Read · ⭐ Recommended · _(no badge)_ Worth a skim

---

## 🔥 Top Picks

_Highest-scoring articles from this digest — open these first._

| | Article | Author | Claps |
|---|---------|--------|-------|
| 🔥 | **Why AI Sucks at These Programming Languages** | Jose Crespo, PhD | 1.3K |
| ⭐ | **The Obvious Ways To Spot Someone Secretly Writing With AI** | Matt Lillywhite | 17.8K |
| ⭐ | **AI Images Look Perfect. Until You Notice This.** | HalfJourney Lab | 6.3K |
| ⭐ | **Mark Cuban Just Confirmed the Absurdity of the AI Bubble** | srgg6701 | 2.4K |
| ⭐ | **What Should Programmers Do While the AI Writes Code?** | Scott Batson | 1.1K |
| ⭐ | **Build a Second Brain in 15 Minutes: Just Markdown, Git, and an AI Agent** | Roan Brasil Monteiro | 798 |

---

## Table of Contents

1. 🔥 [Why AI Sucks at These Programming Languages](#1-why-ai-sucks-at-these-programming-languages) — _C++, Haskell, Rust, Verilog and VHDL expose semantic contexts AI can't handle_
2. ⭐ [The Obvious Ways To Spot Someone Secretly Writing With AI](#2-the-obvious-ways-to-spot-someone-secretly-writing-with-ai) — _The real giveaways have nothing to do with em-dashes_
3. ⭐ [AI Images Look Perfect. Until You Notice This.](#3-ai-images-look-perfect-until-you-notice-this) — _AI models visual effects without understanding their physical causes_
4. ⭐ [Mark Cuban Just Confirmed the Absurdity of the AI Bubble](#4-mark-cuban-just-confirmed-the-absurdity-and-grim-reality-of-the-ai-bubble) — _CEOs follow the herd; powerful AI still needs armies of human experts_
5. ⭐ [What Should Programmers Do While the AI Writes Code?](#5-what-should-programmers-do-while-the-ai-writes-code) — _Hint: not start another AI coding loop_
6. ⭐ [Build a Second Brain in 15 Minutes: Just Markdown, Git, and an AI Agent](#6-build-a-second-brain-in-15-minutes-just-markdown-git-and-an-ai-agent) — _No database, no server, no subscription — just .md files and Claude Code_
7. ⭐ [SQL vs NoSQL: Understand Databases in 5 Minutes](#7-sql-vs-nosql-understand-databases-in-5-minutes) — _5 types of databases explained for AI context_
8. ⭐ [How to Build an AI Agent Harness 2.0](#8-how-to-build-an-ai-agent-harness-20-and-engineer-better-than-99-of-developers) — _The verification loop that keeps agents from going off the rails_
9. [WebMCP: The Future of AI-Native Websites](#9-webmcp-the-future-of-ai-native-websites) — _A new protocol layer that lets AI agents interact with the web natively_
10. [How AI Models Improve Without Simply Getting Bigger](#10-how-ai-models-improve-without-simply-getting-bigger) — _Data, architecture, compute, feedback and context: the five levers_

---

## 1. 🔥 Why AI Sucks at These Programming Languages

**Author:** Jose Crespo, PhD | **Publication:** AI Advances  
**Read time:** 10 min | **Claps:** 1,300 | **Responses:** 61 | **Date:** Sep 10

| | Link |
|---|---|
| 📰 **Original** | https://medium.com/p/f35c14ac4a8e |
| 🔓 **Unlocked** | https://freedium.cfd/https://medium.com/p/f35c14ac4a8e |

> **TL;DR:** AI generates convincing-looking code in any language, but fails silently in languages where correctness depends on nested semantic contexts invisible in the code itself — making C++, Rust, Haskell, Verilog, and VHDL the places human developers remain indispensable.

**Key takeaways:**
- AI learns what code *looks like*, not how it *means* — in C++ a single line's correctness can depend on name lookup, ADL, template instantiation, value categories, and object lifetimes that are nowhere near that line. AI is blind to those layers.
- The real threat model is not "AI writes bad code you can see" but "AI writes code that compiles, passes tests, and is semantically wrong" — the bug lives several context layers away from the surface.
- Languages that encode most semantics *visibly* (Python, Go) are being automated much faster than those that hide it (C++, Haskell, Rust) — choose your niche accordingly.
- "The line of code is only the visible surface. The real semantics live underneath. And that is exactly where current AI sucks." This isn't a fixable prompt problem — it's a mathematical gap that requires a different AI architecture.
- For developers: if your work lives in languages with rich hidden semantic structure, your career runway is longer than the AI-doom headlines suggest. Learn to articulate *why* a piece of nested context is important — that's your moat.

---

## 2. ⭐ The Obvious Ways To Spot Someone Secretly Writing With AI

**Author:** Matt Lillywhite | **Publication:** The Daily Draft  
**Read time:** 7 min | **Claps:** 17,800 | **Responses:** 637 | **Date:** Sep 12

| | Link |
|---|---|
| 📰 **Original** | https://medium.com/p/f36ce8d4d715 |
| 🔓 **Unlocked** | https://freedium.cfd/https://medium.com/p/f36ce8d4d715 |

> **TL;DR:** Most "AI tells" that people flag — similes, metaphors, structured formatting — are just good writing; the actual signals worth watching are output velocity, lack of subject-matter specificity, and the author's inability to defend their work in depth.

**Key takeaways:**
- The internet has convinced itself that similes, metaphors, transitions, and clean structure are "AI tells" — but these are standard literary techniques that humans have used for decades. Calling them out as AI is embarrassing for the caller.
- The real tell is *unrealistic output velocity* — a writer consistently publishing the equivalent of multiple novels per month while holding a demanding full-time job and still sounding endlessly polished is a meaningful signal.
- Specificity is the other test: AI-generated content tends to stay at the level of general claims. A human expert drops concrete details, precise numbers, and edge cases that AI would have to be specifically prompted to include.
- The irony of AI detection hysteria: the more people believe generic writing is AI-generated, the more they disincentivise the careful, polished writing that used to be a hallmark of quality.
- This article itself went viral (17.8K claps) because it challenged a widespread assumption — it's a useful read for anyone in content-heavy professions worried about perception.

---

## 3. ⭐ AI Images Look Perfect. Until You Notice This.

**Author:** HalfJourney Lab | **Publication:** Independent  
**Read time:** 11 min | **Claps:** 6,300 | **Responses:** 159 | **Date:** Sep 10

| | Link |
|---|---|
| 📰 **Original** | https://medium.com/p/42a3cbd8585b |
| 🔓 **Unlocked** | https://freedium.cfd/https://medium.com/p/42a3cbd8585b |

> **TL;DR:** AI images fool the eyes but trip the subconscious because they render visual effects — shadows, reflections, blur — without the physical causes that would produce those effects in reality; the article introduces the ISLP framework to prompt for physics-consistent images.

**Key takeaways:**
- The key insight: AI learns visual *patterns*, not physical *causation*. A real photograph has shadows because of a light source; an AI image has a shadow because shadows tend to appear in similar scenes. The light source and shadow are decoupled — and your brain detects this without being able to name it.
- "There are effects without a cause." This is the single diagnostic for fake images: look for a shadow with no caster, a reflection that doesn't match the subject's pose, a blur pattern that doesn't fit the depth of field.
- Background text is still a reliable tell in 2026 — foreground text has improved dramatically, but text three layers back (a shop sign down the street, a book spine on a shelf) still garbles.
- The ISLP framework (Illumination, Surface, Light, Physics) is a prompting structure to force AI image generators to reason about physical cause-and-effect — dramatically improves photorealism at the cost of more verbose prompts.
- Practical checklist for spotting AI images: (1) trace every shadow to its source, (2) check reflections match the subject's actual pose, (3) zoom into background text, (4) look for light that has no origin.

---

## 4. ⭐ Mark Cuban Just Confirmed the Absurdity and Grim Reality of the AI Bubble

**Author:** srgg6701 | **Publication:** Predict  
**Read time:** 8 min | **Claps:** 2,400 | **Responses:** 71 | **Date:** Sep 10

| | Link |
|---|---|
| 📰 **Original** | https://medium.com/p/cb6c21e9f310 |
| 🔓 **Unlocked** | https://freedium.cfd/https://medium.com/p/cb6c21e9f310 |

> **TL;DR:** Cuban — the man who hedged his way out of the dot-com crash — is now warning that companies adopting AI without understanding what it actually does will be the ones that get wiped out; behind the slick demos, real AI deployments still require large expert teams to function.

**Key takeaways:**
- Cuban's tell for whether AI is as smart as the marketing claims: count the humans the company hired to make it work. If it takes an army of PhDs to run the "autonomous" system, the system is not autonomous — it's expensive automation with a better press release.
- CEOs are buying AI because peer pressure and board expectations have replaced due diligence. "If the CEO has no clue what exactly AI does in their company, start to think about another job. Your company is going to be challenged."
- The dot-com parallel is instructive: Cuban didn't deny the internet was real — he just knew the valuations were irrational. The same logic applies to AI infrastructure CAPEX today: the technology is real, the ROI timelines are not.
- The article's uncomfortable conclusion: the AI bubble won't pop because AI is fake — it'll pop because real AI costs far more to deploy reliably than the demos suggested, and most companies are only now discovering this in production.
- For practitioners: the gap between "AI vendor demo" and "AI in production at scale" is where careers are made. Learn to live in that gap.

---

## 5. ⭐ What Should Programmers Do While the AI Writes Code?

**Author:** Scott Batson | **Publication:** Independent  
**Read time:** 4 min | **Claps:** 1,100 | **Responses:** 52 | **Date:** Sep 10

| | Link |
|---|---|
| 📰 **Original** | https://medium.com/p/a2ce2e6de88e |
| 🔓 **Unlocked** | https://freedium.cfd/https://medium.com/p/a2ce2e6de88e |

> **TL;DR:** When AI agents handle implementation, the highest-leverage thing a developer can do isn't start another AI coding loop — it's invest the gap time in architecture, testing strategy, and the kind of deep system thinking that AI cannot parallelize.

**Key takeaways:**
- The mistake most developers make when an AI agent is running: they immediately start another AI coding loop. This creates parallelism without oversight — two agents, neither fully reviewed, compounding each other's errors.
- The time AI buys you is most valuable when spent on the meta-layer: reviewing architecture decisions, writing specs for the next task, running manual test cases on the last output. None of these things can be AI-accelerated without risk.
- Article argues this is the developer's new core skill: becoming a "gap manager" — someone who knows exactly what quality checks to run in the 5–20 minutes an agent is implementing, so nothing compounds unchecked.
- Don't mistake activity for productivity. Starting more AI loops looks productive; pausing to actually read and understand the last agent's output *is* productive.

---

## 6. ⭐ Build a Second Brain in 15 Minutes: Just Markdown, Git, and an AI Agent

**Author:** Roan Brasil Monteiro | **Publication:** Independent  
**Read time:** 7 min | **Claps:** 798 | **Responses:** 26 | **Date:** Sep 10

| | Link |
|---|---|
| 📰 **Original** | https://medium.com/p/c9d74ba992bb |
| 🔓 **Unlocked** | https://freedium.cfd/https://medium.com/p/c9d74ba992bb |

> **TL;DR:** The COG (Cognition + Obsidian + Git) system gives you a persistent, versioned AI memory using nothing but markdown files, git history, and any AI agent with file-system access — no external database, no subscription, no vendor lock-in.

**Key takeaways:**
- The entire architecture is three things: a folder of `.md` files (your knowledge vault), git for versioned history, and an AI agent (Claude Code, Cursor, Kiro, Gemini CLI, or Codex) that can read and write those files. Everything else is optional.
- The git layer is the killer feature: unlike cloud-based AI memory systems, every change to your notes is versioned, diffable, and fully exportable. You own the data in a format that will be readable in 20 years.
- Obsidian is optional but recommended as a human-readable UI on top of the vault — you can also just use any text editor. The vault is just a folder; Obsidian doesn't lock you in.
- A `CLAUDE.md` file at the vault root acts as the agent's configuration — it tells the AI how your notes are structured, what conventions you use, and what kinds of tasks it should help with. This is what makes the agent context-aware across sessions.
- The 15-minute setup is real: `git clone`, `npx install`, create your `CLAUDE.md`, start chatting. No auth flows, no cloud setup, no monthly fee for the infrastructure layer.

---

## 7. ⭐ SQL vs NoSQL: Understand Databases in 5 Minutes

**Author:** Shreyas Naphad | **Publication:** Towards AI  
**Read time:** 5 min | **Claps:** 564 | **Responses:** 5 | **Date:** Sep 12

| | Link |
|---|---|
| 📰 **Original** | https://medium.com/p/6701bf5b7932 |
| 🔓 **Unlocked** | https://freedium.cfd/https://medium.com/p/6701bf5b7932 |

> **TL;DR:** A fast-read overview of when to reach for SQL vs the five major NoSQL patterns — useful context for anyone designing data infrastructure for AI/ML systems that need to scale beyond relational storage.

**Key takeaways:**
- The five NoSQL types (document, key-value, column-family, graph, time-series) each solve a different scaling problem — don't pick NoSQL as a monolith, pick the type that matches your access pattern.
- For AI/ML pipelines: vector databases (pgvector, Pinecone, Weaviate) are a sixth type the article likely covers, and they've largely become the missing data infrastructure primitive for retrieval-augmented generation.
- SQL still wins when you have structured data, complex joins, and ACID guarantees matter — e.g., transactional data feeding an AI audit trail.
- The article's practical framing ("understand in 5 minutes") makes it a useful primer to share with non-engineers when justifying infrastructure choices for AI products.

---

## 8. ⭐ How to Build an AI Agent Harness 2.0 and Engineer Better Than 99% of Developers

**Author:** Sachin Kasana | **Publication:** CodeToDeploy  
**Read time:** 9 min | **Claps:** 370 | **Responses:** 8 | **Date:** Sep 10

| | Link |
|---|---|
| 📰 **Original** | https://medium.com/p/028e4fc01b50 |
| 🔓 **Unlocked** | https://freedium.cfd/https://medium.com/p/028e4fc01b50 |

> **TL;DR:** The "harness" around an AI coding agent — the verification loop, context management, and structured task handoffs — matters more than the model itself; most devs focus on prompts and miss the orchestration layer that determines whether the agent's output is trustworthy.

**Key takeaways:**
- "Your AI agent just finished a coding task" — but without a harness, there's no guarantee the output meets your spec, doesn't break existing tests, or aligns with your architecture. The harness is the V-model verification layer the agent doesn't have by default.
- Core components of a Harness 2.0: (1) structured input spec → (2) agent implementation → (3) automated verification (tests + linting) → (4) human review trigger if tests fail → (5) structured output report. The agent never grades its own homework.
- Context management is the second pillar: most agent failures happen not because the model is weak, but because the context window filled with irrelevant history. A good harness prunes context aggressively between subtasks.
- The 99th percentile edge is not about model choice — it's about being the developer who has built the scaffolding to *trust* the agent's output rather than spot-check it.

---

## 9. WebMCP: The Future of AI-Native Websites

**Author:** Vijayasekhar Deepak | **Publication:** Independent  
**Read time:** 5 min | **Claps:** 324 | **Responses:** 10 | **Date:** Sep 10

| | Link |
|---|---|
| 📰 **Original** | https://medium.com/p/fcf11c189b37 |
| 🔓 **Unlocked** | https://freedium.cfd/https://medium.com/p/fcf11c189b37 |

> **TL;DR:** WebMCP extends the Model Context Protocol to the open web, letting AI agents interact with websites through a standardised tool interface instead of brittle browser automation — a shift from "AI that scrapes" to "AI that calls."

**Key takeaways:**
- Current web agents (browser automation, Playwright scrapers) are fragile because they depend on DOM structure that changes with every redesign. WebMCP exposes a stable API surface that survives layout changes.
- The analogy is REST APIs for machines: WebMCP is to AI agents what the REST convention was to web services — a shared contract that decouples consumers from implementation details.
- Early adoption is primarily in AI-native products (Claude, Gemini, Copilot) where the vendor controls both sides of the integration. Open web adoption will follow as the spec matures.
- Worth watching if you're building products that expect AI agents as users/clients — designing a WebMCP endpoint alongside your REST API is relatively low effort and future-proofs your API surface.

---

## 10. How AI Models Improve Without Simply Getting Bigger

**Author:** Nikki | **Publication:** AI Advances  
**Read time:** 16 min | **Claps:** 190 | **Responses:** 0 | **Date:** Sep 10

| | Link |
|---|---|
| 📰 **Original** | https://medium.com/p/48be767591c7 |
| 🔓 **Unlocked** | https://freedium.cfd/https://medium.com/p/48be767591c7 |

> **TL;DR:** A deep-dive on the five improvement levers beyond raw parameter count — data quality, architecture innovation, compute efficiency, human feedback loops, and expanded context — with practical implications for what "better AI" actually means in 2026.

**Key takeaways:**
- Scale is not the only axis: most of the post-GPT-4 gains have come from data curation, RLHF quality, and architectural tweaks — not just adding more parameters. Knowing which lever was used matters for predicting where the next gains will come from.
- Data quality beats data quantity at the frontier: a carefully curated 500B token corpus now regularly outperforms a noisily scraped 5T token corpus on benchmark tasks. The "more data" assumption is increasingly wrong.
- Architecture innovations (sparse MoE, state-space models, hybrid attention) are producing models that run faster and cheaper without sacrificing quality — meaningful for anyone building cost-sensitive AI products.
- Human feedback is the least understood lever: RLHF and its variants (DPO, RLAIF) essentially encode human preferences into model weights. The article likely discusses how the *quality* of that feedback determines the model's alignment, not just its capability.
- Context length expansion (128K → 1M+ tokens) is changing what counts as "model intelligence" — tasks that required chaining multiple calls now happen in a single inference, collapsing entire workflow categories.

---

*Generated by the Medium AI Digest skill · Sep 12, 2026*  
*Sources: Medium Daily Digest emails (Sep 10 & Sep 12, 2026) · Filters: AI/LLM keyword matching with word-boundary detection · Scoring: clap count + response count + keyword density + publication tier*
