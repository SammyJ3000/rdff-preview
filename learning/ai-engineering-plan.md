# AI Engineering Sprint: 10 Weeks to Selling with Confidence

> **LOCKED PLAN (set 2026-11-01).** 10 weeks × 8–10 hrs/week. Start **Mon 2 Nov 2026** → readiness test **w/c 4 Jan 2027** → start selling workshops.
> **No changes to this plan until the end-of-sprint review.** New ideas go in the Parking Lot. This applies to Claude too: if something seems off, Claude asks a question instead of rewriting the plan.

**Why this plan exists:** when Andrew asked how my quote tool gets its data, I couldn't explain it. I want to understand AI systems properly, with hands-on skills, before I sell workshops. But I want to get to selling in weeks, not months.

**Sources:** Sajjaad Khader's AI engineer roadmap (what to learn) · Nick Saraev's AI learning method (how to learn) · my Interviewer gap analysis (where I started).

---

## The rules

1. **Every session produces something I built or changed and can explain.** Talk-only sessions don't count.
2. **AI is my tutor, not my ghostwriter.** I write the first version; AI reviews it (Checker). I let an agent write code for a skill only after I've done it by hand once.
3. **Redo without help.** After any explanation, I go back to the start and do it myself. (Nick: this is only 10–15% more time and makes the biggest difference.)
4. **My existing tools are case studies (📁),** one session each, at set points. They're not the curriculum.
5. **No selling during the sprint.** I *can* go to BNI/Chamber meetings to **listen** and note the questions owners ask. Those go into my Hard Questions list.
6. **Ideas → Parking Lot.** Not into the plan.

---

## The 10 weeks

Each week: **learn** (main resource) → **build** (the week's project) → **check** (Nick's loop) → **tick it off**.

### Week 1: Terminal, Git, first Python
- **Learn:** CS50P Lecture 0 (Functions, Variables) + MIT *Missing Semester* (shell + Git lectures).
- **Build:** create a GitHub repo `ai-sprint`. Write small scripts from the CS50P problem set **myself**. Commit and push each one.
- **Done when:** I can make a repo, commit, push, and write a Python function without help.

### Week 2: Python I'll actually use
- **Learn:** CS50P Lectures 1–3 (conditionals, loops, exceptions). Reference: *Automate the Boring Stuff* chapters on lists, dictionaries and files.
- **Build:** a script that reads a CSV/JSON file of fake leads, cleans it, and saves a new file.
- **Done when:** I can use lists and dictionaries, loops, try/except, and read/write files and JSON.

### Week 3: APIs and data
- **Learn:** HTTP basics (requests/responses, status codes 200/401/429/500, API keys in `.env`). SQLBolt (SQL, ~3 hrs).
- **Build:** pull real local businesses from a free API (e.g. Companies House) → store in SQLite → query by area and industry.
- **Done when:** I can call an API from Python, handle errors, keep keys secret, and SELECT/WHERE/JOIN.

### Week 4: How LLMs work + my first API calls
- **Learn:** Karpathy, *Intro to Large Language Models* (1-hr talk). Anthropic courses on GitHub (`anthropics/courses`): **API fundamentals**.
- **Build:** a script that sends text to Claude and gets back a summary + action items. Count tokens and calculate the cost for 500 emails/month.
- **Done when:** I can explain tokens, context windows, temperature and why models hallucinate, and make API calls with error handling.

### Week 5: Prompting, context and structured output
- **Learn:** Anthropic **prompt engineering tutorial**; Pydantic basics (validation).
- **Build:** an **enquiry extractor**. Messy customer messages → model returns JSON (name, job type, urgency, budget) → validated → invalid answers rejected and flagged.
- 📁 **Case study (1 session): my quote tool.** Read `engine/` and the design doc's hard rule: *"the LLM never performs arithmetic and never sees a price."* Trace one quote through the code.
- **Done when:** I can explain why you separate the LLM (language) from deterministic code (numbers), and build validated structured output.

### Week 6: Tool use + automation
- **Learn:** Anthropic **tool use** course. One automation platform (n8n *or* Make, pick one): triggers, actions, webhooks.
- **Build:** (a) let Claude call two of my own Python functions, by hand, with no framework. (b) An automation: new enquiry → my week 5 extractor → Google Sheet + drafted reply waiting for approval.
- 📁 **Case study (1 session): missed-call text-back.** Map every step, webhook and failure point.
- **Done when:** I can explain function calling, webhooks, and the difference between an automation and an agent.

### Week 7: RAG ("AI that knows our documents")
- **Learn:** DeepLearning.AI short course on RAG (one only). Optional: Chip Huyen, *AI Engineering*, RAG chapter.
- **Build:** RAG **from scratch** over a sample business's documents (handbook, price list, FAQs): chunk → embed → store → retrieve → answer **with sources**.
- **Done when:** I can draw how RAG works and explain where it fails. (RAG supplies information; it doesn't guarantee correct answers.)

### Week 8: Evals and reliability
- **Learn:** Hamel Husain, *Your AI Product Needs Evals*.
- **Build:** a **20-question test set** for my week 7 assistant. Score it, improve it, re-score. Add failure handling (what happens when the API is down or there's no answer).
- 📁 **Case study (1 session): quote tool tests.** Run the tests in `tests/golden/`, change a day rate on purpose, and watch them catch it.
- **Done when:** I can explain "garbage in, garbage out," why deterministic doesn't mean correct, and how to measure an AI system.

### Week 9: Agents, MCP, privacy and cost
- **Learn:** Anthropic, *Building Effective Agents*; DeepLearning.AI *MCP: Build Rich-Context AI Apps with Anthropic*; UK GDPR basics for small businesses (ICO); the data policies of the AI tools I use; Ollama docs.
- **Build:** (a) connect Claude to 2–3 tools via MCP and complete a multi-step task with an approval step. (b) Run a local model with Ollama and compare it with Claude. (c) Write a one-page **"How AI tools handle your data"** sheet and a monthly **cost estimate template**.
- **Done when:** I can explain agents vs automations, what MCP is (and isn't), using data vs training on it, and what a system costs per month.

### Week 10: Consolidate + readiness test
- **No-AI rebuild:** rebuild a small version of the week 5 extractor or week 7 RAG with **no AI help**.
- **Diagnostician:** *"Here are all my mistakes from the sprint. What misunderstanding do they share?"* Fix the root.
- **Sparring:** the AI plays 3 skeptical business owners (privacy, cost, "AI makes things up").
- **Take the readiness test (below).** Pass → start selling. Fail on something → one more week on just that topic.

---

## Readiness test (the finish line)

I start selling workshops when I can:
- [ ] Explain these out loud, without notes, in under 2 minutes each: LLMs and hallucination, tokens and cost, APIs, structured output, the LLM-vs-code split, RAG, evals, agents vs automations, MCP, data privacy
- [ ] Score **80%+** on an Examiner quiz across all 10 weeks
- [ ] Complete the no-AI rebuild
- [ ] Answer my **Hard Questions list** (20+ real owner questions) confidently
- [ ] Demo one thing I built (extractor, RAG assistant or quote tool) **and explain how it works and where the data comes from**: the Andrew test

---

## How every session runs (Nick Saraev's method)

| Session | Time | What happens |
|---|---|---|
| 1. New material | 2 hrs | Main resource → **Explainer** for anything unclear → write the code myself |
| 2. Practice | 2 hrs | Exercises → **Checker**: *"Here's my code and why. Find what's wrong. Don't rewrite it."* → **redo without help** |
| 3. Build | 2 hrs | The week's project → break it on purpose → fix it |
| 4. Consolidate | 1.5–2 hrs | **Socratic** (*"ask me questions until I find what I don't understand"*) → **Examiner** (*"quiz me, harder each time, until I'm guessing"*) → **Listener** (explain out loud / draw / write, AI grades it) → **Clerk** (notes → flashcards) → tick the week |
| Daily | 10 min | Anki review |

---

## After the sprint (from week 11)
- **Sell:** talks + "use AI well and safely" workshops, from real understanding.
- **Keep learning 3–5 hrs/week:** deeper material in `parked-career-curriculum.md` (deployment, Docker, deeper RAG/agents, Chip Huyen's book). Small client integrations once I've built and supported a couple.

---

## Progress log

| Week | Dates | Built / did | Done? |
|---|---|---|---|
| Pre-sprint | 1 Nov | Interviewer gap analysis; quote tool explained (LLM vs code, validation, human check, evals, data provenance) | ✅ |
| 1 | 2–8 Nov | | |
| 2 | 9–15 Nov | | |
| 3 | 16–22 Nov | | |
| 4 | 23–29 Nov | | |
| 5 | 30 Nov–6 Dec | | |
| 6 | 7–13 Dec | | |
| 7 | 14–20 Dec | | |
| 8 | 21–27 Dec | (Christmas: allow a light week) | |
| 9 | 28 Dec–3 Jan | | |
| 10 | 4–10 Jan | Readiness test | |

## Hard Questions list (add from meetings and sparring)
1. How does it get its data, and how does it work? (Andrew)
2.

## Parking Lot
- Follow up with Andrew after the sprint, using the demo + explanation
- Workshop outline and pricing → week 10 / after the sprint
