# AI Engineering for Business: 6-Week Learning Plan

**Goal:** Understand AI systems well enough to (1) teach business owners at Chamber of Commerce / BNI meetings, (2) sell workshops, and (3) scope and deliver AI integrations, all without overclaiming.

**Built from:**
- *How to Become a $300K AI Engineer in 2026* (Sajjaad Khader): **what** to learn
- *How I Learn Complex Skills & Difficult Subjects So Fast with AI* (Nick Saraev): **how** to learn it

**Time budget:** about 6 hours/week for 6 weeks (about 36 hours), then 1–2 hours/week to keep it fresh.

---

## 1. First, adjust the roadmap to your goal

Sajjaad's roadmap is built to get someone **hired as a software engineer at a big tech company**. You're doing something different: **advising and implementing for small businesses**. So some of it matters a lot more for you, and some of it barely matters.

| Roadmap item | Verdict for you | Why |
|---|---|---|
| **Python** | **Read it, don't master it** (~4 hrs) | Your agents write it. You need to read a script, roughly follow what it does, and notice when it's wrong. Learning it in depth would take months and wouldn't help you sell. |
| **SQL** | **Concepts only** (~1 hr) | Know what a database is and what SELECT / WHERE / JOIN do. Your clients' data mostly lives in spreadsheets, CRMs and accounting tools. |
| **APIs** | **Must know** | Every integration you sell is an API connection. You have to explain it simply and make a call yourself. |
| **Context engineering** | **Core skill: go deep** | This is where your year of hands-on use already pays off. System prompts, master prompts, Projects / Custom GPTs / Gems. It's also your workshop content. |
| **AI APIs (OpenAI / Anthropic)** | **Must know** | Keys, tokens, pricing, rate limits. You'll need these to quote integration jobs. |
| **Running your own models (Hugging Face)** | **Light, but keep it** (~2 hrs) | Running a local model (e.g. with Ollama) gives you a strong answer to *"Does my data leave the building?"* |
| **RAG** | **Must know, core skill** | "A chatbot that knows *our* documents" is the most common SMB integration request. |
| **Agents + MCP** | **Must know** | You already use agents. Learn the vocabulary and the limits so you can explain them to clients and scope work. |
| **Docker / AWS / GCP** | **Know what they are, skip the skills** | You'll mostly deliver through no-code / managed tools. Deep deployment skills are for engineers. |
| **Evals + governance (cost, model routing)** | **Must know, in plain English** | "How do we know it's right?" and "What will it cost per month?" are the two questions every owner asks. |
| **Level 4: landing the job** | **Replace** | You don't need a résumé. You need **case studies, demos and a clear offer** (see Week 6). |

### What the video leaves out (and your clients *will* ask about)
1. **Data privacy & security**: what happens to data typed into ChatGPT, business vs consumer plans, data-protection law (GDPR / UK GDPR or your local equivalent), training opt-outs.
2. **Limitations & hallucinations**: when *not* to use AI. Being honest about this builds trust faster than anything else.
3. **No-code automation**: Zapier, Make, n8n. Most small-business "AI integrations" are really workflows built in these tools.
4. **The tools they already pay for**: Microsoft 365 Copilot and Gemini in Google Workspace. "Get value from what you already have" is an easy first sale.

### On the credibility worry
Don't call yourself an "AI engineer." To a skeptical business owner, that title is a claim they'll try to disprove. Something like **"AI implementation consultant"** or **"I help local businesses put AI to work"** is honest, and it's what they're actually buying. They're won over by a **live demo on their kind of business**, a **plain-English explanation**, and **a result you got for a client**, not by a title. This plan is designed to give you all three.

---

## 2. How you'll learn (Nick Saraev's method, applied)

**Core principle:** you learn by **producing** (recalling, explaining, predicting, building), not by **consuming** (watching, rereading). Production takes more effort, but you forget far less of it. So no tutorial binges: every session ends with you *producing* something.

### The AI roles you'll use (copy-paste prompts)

| Role | When | Prompt to use |
|---|---|---|
| **Interviewer** | Day 1 | *"Interview me one question at a time to find out what I already know about how LLMs, APIs, RAG, agents and automation work. My goal is to teach and sell AI to small businesses. After 10–15 questions, summarize my gaps."* |
| **Mapmaker** | Day 1 | *"Using my gaps and this plan [paste], adjust the 6-week curriculum. Flag anything I can skip."* |
| **Explainer (right level)** | Each new concept | *"Explain [concept] three ways: to a 12-year-old, to a business owner, to a junior developer. Then give one real small-business example."* |
| **Socratic questioner** | After each explanation | *"Don't explain. Ask me questions that make me reason my way to how [concept] works. Correct me only when I'm stuck."* |
| **Examiner** | End of each week | *"Quiz me on this week's topics: 10 questions, mixed difficulty, one at a time. Make them harder when I get them right (keep me at the edge of what I know). Score me at the end."* |
| **Checker** | When you build things | *"Here's what I built and why [paste]. Don't fix it. Critique my reasoning and tell me what I misunderstood."* |
| **Listener** | 2–3× per week | Record yourself (voice memo) explaining a topic as if to a BNI room, transcribe it, then: *"Compare my explanation to [source]. What did I get wrong, leave out, or make too vague?"* |
| **Diagnostician** | End of weeks 3 and 6 | *"Here are all my quiz mistakes so far [paste]. What underlying misconceptions keep causing them?"* |
| **Sparring partner** | Weeks 5–6 | *"Play a skeptical 55-year-old accountant at a BNI meeting who thinks AI is hype and worries about client confidentiality. Push back hard on my pitch. Afterwards, tell me where I was vague."* |
| **Clerk** | End of each session | *"Turn these messy notes into a clean outline and 10 flashcards (question → answer)."* Import the cards into Anki. |

**Spaced repetition:** 10 minutes a day reviewing your flashcards in Anki. This keeps what you learn in week 1 from fading by week 6.

**Watch out for over-reliance:** Nick's GPS analogy applies here. If an agent does everything, you understand nothing. Rule: **before you ask an agent to build something, write down how you think it should work. Afterwards, explain back what it did.**

### Each weekly cycle (about 6 hrs)
1. **Explain** (1 hr): explainer + 1–2 short resources
2. **Question** (1 hr): Socratic loop
3. **Build** (2.5 hrs): a small hands-on project
4. **Teach back** (1 hr): listener: record a 3-minute explanation for business owners
5. **Test** (30 min): examiner quiz + clerk → flashcards

---

## 3. The 6 weeks

### Week 1: How LLMs actually work + context engineering
**Concepts:** tokens, context window, training vs. inference, why models hallucinate, temperature, system prompts, master prompts, Projects / Custom GPTs / Gems.
**Build:** a master prompt for one business type (e.g. an estate agent). Build it as a Claude Project or Custom GPT with their tone, services and FAQs, and test it with 10 realistic tasks.
**Proof for businesses:** a 3-minute "Why AI makes things up, and how to stop it" explanation. This becomes your first meeting talk.

### Week 2: APIs, and reading code without fear
**Concepts:** what an API is (Sajjaad's bank/ATM analogy is a good one to borrow), API keys, requests/responses, JSON, tokens = cost, rate limits. Python and SQL basics: just enough to read.
**Build:** with your agent's help, a script that reads a text file and sends it to the Anthropic or OpenAI API for a 3-sentence summary plus action items (the video's own starter project). **You** annotate every line in plain English before running it.
**Also:** work out the monthly API cost of that script for a business processing 500 emails/month.
**Proof:** a cost-estimate template you can reuse when quoting.

### Week 3: No-code automation + the tools businesses already own
**Concepts:** triggers, actions, webhooks; Zapier vs Make vs n8n; Copilot in M365 and Gemini in Workspace.
**Build:** an automation in Make or n8n: new web-form lead → AI drafts a personalized reply → saves it to Gmail drafts + logs to a Google Sheet.
**Proof:** a screen recording of it running. This is your best demo for BNI. **Diagnostician check-in at the end of this week.**

### Week 4: RAG ("a chatbot that knows *our* stuff")
**Concepts:** chunking, embeddings, vector databases, retrieval, why RAG beats "just paste it in" at scale, where RAG fails.
**Build:** start no-code (a Claude Project / Custom GPT with uploaded docs), then a real RAG chatbot over a sample business's documents (policies, price list, FAQs) using a no-code tool or a simple agent-built script. Try to break it: ask questions the docs don't answer.
**Proof:** a "staff handbook assistant" demo plus a one-page explainer of how it works and its limits.

### Week 5: Agents, MCP, and local models
**Concepts:** what makes something an agent (tools + loop + goal), MCP, agent failure modes, human-in-the-loop, local models and privacy.
**Build:** connect an agent to 2–3 tools via MCP (e.g. email + calendar + a doc) and have it complete a multi-step task. Install Ollama and run a small model locally. Compare its quality and speed against Claude/ChatGPT.
**Sparring:** start sessions with the skeptical-business-owner role-play.
**Proof:** a clear "what agents can and can't safely do for your business today" talk.

### Week 6: Reliability, cost, privacy, and packaging it to sell
**Concepts:** evals (test sets, hallucination checks), monitoring, model routing (cheap model for easy tasks, expensive for hard), data-privacy basics, writing an AI usage policy.
**Build:** a 20-question test set for your Week 4 chatbot. Score it, improve the prompt, re-score. Then draft a one-page AI usage policy template for a small business.
**Package your offer:**
- **Free:** 20-minute meeting talk ("5 things you can do with AI tomorrow")
- **Workshop:** half-day hands-on ("Get your team using AI safely")
- **Integration:** discovery call → scoped automation/chatbot → monthly support
**Final sparring:** run your whole pitch against 3 different skeptical personas. **Final diagnostician review.**

---

## 4. After the 6 weeks
- **Keep learning by doing client work.** Every integration teaches more than a course.
- **Write up every win as a short case study** ("Saved X hours/week for a local Y"). These do the credibility work a certificate can't.
- **Build in public a little.** Sajjaad's point applies locally too: post what you're building on LinkedIn. The people in your BNI room will see it.
- **Optional credential:** if you want something to point to, a short vendor course (e.g. Anthropic's or DeepLearning.AI's free short courses) is enough. Results matter more to SMB owners.
- **Maintenance:** 1–2 hrs/week: keep up with Anki, try one new tool, update your demos.

## 5. Where to start (today)
1. Run the **Interviewer** prompt (20 min).
2. Run the **Mapmaker** prompt with this plan pasted in.
3. Install **Anki**.
4. Start Week 1.
