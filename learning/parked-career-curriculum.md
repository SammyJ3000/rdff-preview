> **PARKED on 2026-11-01.** This is the long-term deeper curriculum for AFTER the 10-week sprint (week 11 onwards, 3–5 hrs/week). Do not use it during the sprint.

# AI Engineering: Career Curriculum (v3)

**Goal:** A long-term career as an AI engineer: someone who can design, build, test, deploy and support AI systems, with foundations that compound over years. **The engineering curriculum below is the career.** Selling services is optional income alongside it, never a replacement for it.

**Two tracks, run in parallel:**
- **Engineering track (~70% of my time, 6–7 hrs/week):** the curriculum below. This is what compounds.
- **Selling track (~30%, 2–3 hrs/week):** meetings, talks and client work, offering **only what my skills currently support** (see the Offer Ladder).

**Honest timeline:** about 6 months to Phase 3, the point where "AI engineer" is a fair description and I can sell bigger builds with confidence. Until then: "AI consultant" or "I help businesses put AI to work."

**Sources:** Sajjaad Khader's AI engineer roadmap (the *what*) · Nick Saraev's AI learning method (the *how*) · my Interviewer gap analysis (where I started).

---

## Anti-drift rules (read at the start of every session)

1. **This file is the source of truth.** Every session starts with: *"Which milestone am I on?"* and ends by ticking something off.
2. **Every session produces code I wrote or changed and can explain.** A session that's only talk doesn't count.
3. **My existing tools are case studies, not the curriculum.** They come in at set points (marked 📁) to show a concept in the real world, then I move on.
4. **Study sessions are engineering.** Selling happens in the field (meetings, calls, client work), not in study sessions. Pitch practice is at most one study session per phase.
5. **New ideas go in the Parking Lot** (bottom of this file), not into the plan.
6. **AI as tutor, not ghostwriter, while learning.** I write the first version myself, then AI reviews it (Checker). I use agents to write code for a skill only after I've done it by hand once.
7. **End of each phase: the no-AI rebuild.** I rebuild a small version of the phase project with no AI help. If I can't, I'm not done with the phase.

8. **Sell only what the Offer Ladder says I've unlocked.** No promising builds I can't yet support.

---

## Offer Ladder (what I can honestly sell, by phase)

| Unlocked after | I can sell | Why it's honest |
|---|---|---|
| **Now** | Free talks; paid "use AI well and safely" workshops for teams (ChatGPT/Claude/Copilot, prompting, an AI usage policy) | A year of real use plus client work already supports this |
| **Phase 1** | Simple no-code automations (Zapier/Make/n8n), set up and supported | I understand APIs, data and failures well enough to fix them |
| **Phase 2** | Small AI integrations: enquiry triage, document extraction, drafting tools, with structured output, validation and a human check | I can build, read and debug them myself |
| **Phase 3** | Bigger builds: document Q&A (RAG) assistants, agents connected to business tools, deployed and measured with evals | I can test, deploy, monitor and support them |
| **Phase 4+** | Ongoing retainers, higher-ticket systems, case-study-led selling | A track record |

---

## Phase 1: Foundations (weeks 1–6)

*Changed from v1: I'm learning Python properly. Not to computer-science depth, but well enough to write, read and debug real code myself. An AI engineer who can't read the code their agent wrote can't support it.*

| Skill | Done when I can... |
|---|---|
| Terminal + Git/GitHub | Create a repo, commit, branch, push, open a PR without help |
| Python core | Write functions, use lists/dicts, loops, conditionals, error handling (try/except) |
| Files + JSON | Read/write files; load, change and save JSON |
| Packages + environments | Set up a project with `uv`, install packages, explain what a virtual environment is |
| HTTP + APIs | Call a REST API with `requests`, handle status codes (200/401/429/500), use API keys safely via `.env` |
| SQL basics (SQLite) | Create a table, INSERT, SELECT/WHERE/JOIN from Python |
| Testing basics | Write and run simple `pytest` tests |

**Project 1:** a lead-list builder. It pulls local businesses from a free public API (e.g. the Companies House API), stores them in SQLite, filters by area and industry, and has tests. A real foundation skill, and useful for my own prospecting.

---

## Phase 2: Working with models (weeks 7–12)

| Skill | Done when I can... |
|---|---|
| How LLMs work | Explain tokens, context windows, temperature, training vs inference, why they hallucinate |
| LLM APIs | Call the Anthropic and OpenAI APIs from Python; handle errors, retries, streaming |
| Context engineering | Write system prompts; manage what goes in the context and why |
| Structured output + validation | Get JSON from a model, validate it with Pydantic, reject bad output |
| Tool use / function calling | Let a model call my Python functions, by hand, with no framework |
| Cost | Count tokens and calculate cost per request and per month |
| Local models | Run a model with Ollama and call it from Python; compare quality, speed and cost |

📁 **Case study (1 session): my quote tool.** It's a live example of "the LLM does language, deterministic code does maths" plus schema validation. Read `engine/` and trace one quote through the code.

**Project 2 (sellable):** an enquiry triage tool, the kind of thing I'd sell after Phase 2. Messy incoming messages (emails or texts) → model extracts structured fields → validated → routed/stored in SQLite → drafted reply. Includes cost tracking and tests.

---

## Phase 3: Shipping AI systems (weeks 13–22)

| Skill | Done when I can... |
|---|---|
| Embeddings + vector search | Explain embeddings; build similarity search by hand |
| RAG from scratch | Chunk → embed → store → retrieve → generate, without a framework first |
| RAG with tools | Rebuild it with a vector DB (e.g. Chroma/pgvector) and explain the trade-offs |
| Evals | Build a golden test set, measure accuracy/hallucination, use LLM-as-judge carefully |
| Agents | Build an agent loop by hand (goal → tool calls → observe → repeat), with limits and human approval |
| MCP | Build a simple MCP server that exposes my own tools to Claude |
| Web backend | Wrap a system in a FastAPI endpoint |
| Deployment | Containerise with Docker basics and deploy to a hosting service; use secrets properly |
| Reliability + governance | Logging, failure handling, retries, model routing (cheap vs strong model), privacy basics (UK GDPR) |

📁 **Case study (1 session): missed-call text-back.** Webhooks, third-party APIs (telephony/SMS), and what happens when a step fails.
📁 **Case study (1 session): quote tool evals.** Its `tests/golden/` folder is a real golden dataset. Run the tests, break a rate on purpose, watch them catch it.

**Project 3 (sellable):** a document Q&A assistant (RAG), e.g. "ask our staff handbook / price list / policies," **with an eval suite and a measured accuracy score**, deployed with a web endpoint. My Phase 3 demo for clients.
**Project 4 (sellable):** an agent that completes a multi-step business task (e.g. enquiry → check calendar → draft booking → wait for approval) using my own MCP server.

---

## Phase 4: Proof and compounding (weeks 23–26, then ongoing)

- **Capstone = a real paid client build:** data in, AI in the right places, deterministic logic elsewhere, evals, deployed, documented, supported.
- **Case studies:** every client job written up (problem → what I built → measured result). These replace a CV.
- **Demo library:** Projects 2–4 + the quote tool, each ready to show in 5 minutes and explain technically if asked.
- **Visibility:** post what I build (LinkedIn), speak at local meetings.
- **Keep compounding:** one new skill per quarter (e.g. voice agents, fine-tuning basics, more advanced evals), picked from the Parking Lot, never more than one at a time.
- **Optional:** a job or contract role later, if I ever want one. The same foundations make that possible.

---

## Where to learn it (ONE main resource per phase; finish it before adding anything)

Rule: one **main** course per phase. "Reference" items are for looking things up, not extra courses. When stuck, use AI as the Explainer before reaching for a new resource.

**Phase 1: Foundations**
- **Main:** CS50's Introduction to Programming with Python (CS50P, Harvard, free: cs50.harvard.edu/python). Do the problem sets; they're the "production" Nick talks about.
- Terminal + Git: *The Missing Semester of Your CS Education* (MIT, free): the shell, Git and editor lectures only.
- SQL: SQLBolt (free, interactive, ~3 hrs).
- Reference: *Automate the Boring Stuff with Python* (free online) for practical scripts, files, JSON and APIs.

**Phase 2: Working with models**
- **Main:** Anthropic's courses on GitHub (github.com/anthropics/courses, free): API fundamentals → prompt engineering tutorial → real-world prompting → tool use. All in Python notebooks.
- Concepts: Andrej Karpathy's *Intro to Large Language Models* (1-hr YouTube talk); 3Blue1Brown's neural networks / transformers videos for intuition (no maths needed).
- Reference: Anthropic and OpenAI API docs; Pydantic docs (validation); Ollama docs (local models).

**Phase 3: Shipping AI systems**
- **Main (the field's textbook):** Chip Huyen, *AI Engineering* (O'Reilly, 2025). Read alongside building, one chapter per topic: RAG, agents, evals, deployment.
- Short, hands-on (free): DeepLearning.AI short courses. Pick only the one matching the current skill: RAG, evaluation, agents/tool use, and *MCP: Build Rich-Context AI Apps with Anthropic*.
- Agents: Anthropic's article *Building Effective Agents* (read before building Project 4).
- Evals: Hamel Husain's blog posts on LLM evals (start with *Your AI Product Needs Evals*).
- Deployment: FastAPI's official tutorial; Docker's "Get started" guide.
- Optional structured alternative (paid): DataCamp's AI Engineer track, recommended in Sajjaad's video.

**Phase 4+: Keep compounding**
- Hugging Face's free courses (LLM course, Agents course) when going deeper on open models.
- Pick one new topic per quarter from the Parking Lot.

---

## How every session runs (Nick Saraev's method)

1. **Name it:** what skill and milestone is this? (Check the tables above.)
2. **Explain** (Explainer): *"Explain [skill] at beginner level, then junior-developer level, with a real example."*
3. **Touch it:** write code. I write it first; AI is the **Checker**: *"Here's my code and why. Find what's wrong. Don't rewrite it."*
4. **Redo without help:** rebuild or re-explain it from scratch without AI.
5. **Socratic + Examiner:** *"Ask me questions until I find what I don't understand"* → *"Quiz me, each question harder, until I'm guessing."*
6. **Listener:** explain it out loud / draw it / write it, and have AI grade it against the source.
7. **Clerk:** notes → flashcards → Anki, 10 min/day.
8. **Tick the milestone** in this file.

**Every 4 weeks, Diagnostician:** *"Here are my mistakes from the last month. What misunderstanding do they share?"*

---

## A typical week (8–10 hrs)

| Session | Time | What happens |
|---|---|---|
| 1 | 2 hrs | **New material:** main resource lesson → Explainer for anything unclear → write the code yourself |
| 2 | 2 hrs | **Practice:** problem set / project work → Checker reviews your code → redo without help |
| 3 | 2 hrs | **Project:** build the phase project → break it on purpose → fix it |
| 4 | 1.5 hrs | **Consolidate:** Socratic + Examiner quiz → Listener (explain out loud) → Clerk makes flashcards → tick milestones |
| Daily | 10 min | Anki review |

## Progress log

| Date | Phase / skill | What I built or did | Ticked? |
|---|---|---|---|
| 2026-11-01 | Interviewer + Mapmaker | Gap analysis; plan v1→v3 | ✅ |
| 2026-11-01 | 📁 Quote tool (early case study) | Learned: LLM vs deterministic code, schema validation, human-in-the-loop, evals, data provenance | ✅ (concepts only; hands-on comes in Phase 2) |

---

## Parking Lot (ideas that are NOT part of the current plan)

- Pitch for the AmSpec/Andrew follow-up: "how does it get its data?" answer (drafted 2026-11-01)
- Workshop content and pricing → selling track (unlocked **now**)
