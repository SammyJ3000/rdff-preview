# AI Engineering: Career Curriculum (v3)

**Goal:** Become a genuine AI engineer: someone who can design, build, test, deploy and support AI systems, and can honestly call themselves one. Selling workshops and integrations to local businesses comes **out of** these skills; it isn't the curriculum.

**Time:** 8–10 hrs/week. **Honest timeline: about 6 months** to the point where "AI engineer" is a fair title (Phases 1–3 done, three deployed projects on GitHub). It's a career, not a 6-week course.

**Sources:** Sajjaad Khader's AI engineer roadmap (the *what*) · Nick Saraev's AI learning method (the *how*) · my Interviewer gap analysis (where I started).

---

## Anti-drift rules (read at the start of every session)

1. **This file is the source of truth.** Every session starts with: *"Which milestone am I on?"* and ends by ticking something off.
2. **Every session produces code I wrote or changed and can explain.** A session that's only talk doesn't count.
3. **My existing tools are case studies, not the curriculum.** They come in at set points (marked 📁) to show a concept in the real world, then I move on.
4. **Sales/pitch practice: at most one session per phase.** Everything else is engineering.
5. **New ideas go in the Parking Lot** (bottom of this file), not into the plan.
6. **AI as tutor, not ghostwriter, while learning.** I write the first version myself, then AI reviews it (Checker). I use agents to write code for a skill only after I've done it by hand once.
7. **End of each phase: the no-AI rebuild.** I rebuild a small version of the phase project with no AI help. If I can't, I'm not done with the phase.

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

**Project 1:** a command-line tool that pulls data from a free public API (e.g. weather or companies data), stores it in SQLite, answers questions about it, and has tests. **On GitHub.**

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

**Project 2:** an enquiry triage tool. Messy incoming messages (emails or texts) → model extracts structured fields → validated → routed/stored in SQLite → drafted reply. Includes cost tracking and tests.

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

**Project 3:** a document Q&A assistant (RAG) over a realistic small-business document set, **with an eval suite and a published accuracy score**, deployed with a web endpoint.
**Project 4:** an agent that completes a multi-step business task using my own MCP server, with human approval on risky actions.

---

## Phase 4: Proof and career (weeks 23–26, then ongoing)

- **Capstone:** one complete system for a real (or realistic) client: data in, AI in the right places, deterministic logic elsewhere, evals, deployed, documented.
- **Portfolio:** a GitHub profile with Projects 1–4 + capstone, each with a README explaining the architecture, decisions and eval results.
- **Case studies:** my existing client work + the quote tool, written up properly.
- **Visibility:** post what I build (LinkedIn), go to local meetups.
- **Optional credential:** one recognised certificate if it helps, but the portfolio is the proof.
- *Now* I package workshops and integrations, from real skill.

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

## Progress log

| Date | Phase / skill | What I built or did | Ticked? |
|---|---|---|---|
| 2026-11-01 | Interviewer + Mapmaker | Gap analysis; plan v1→v3 | ✅ |
| 2026-11-01 | 📁 Quote tool (early case study) | Learned: LLM vs deterministic code, schema validation, human-in-the-loop, evals, data provenance | ✅ (concepts only; hands-on comes in Phase 2) |

---

## Parking Lot (ideas that are NOT part of the current plan)

- Pitch for the AmSpec/Andrew follow-up: "how does it get its data?" answer (drafted 2026-11-01)
- Workshop and offer packaging → Phase 4
