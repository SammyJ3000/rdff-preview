# AI for Business: Personal Learning Plan (v2: after the Interviewer)

**Goal:** Be credible in front of skeptical local business owners (Chamber of Commerce, BNI). Teach practical AI use first, sell workshops next, and sell integrations only once I can explain, test and support what I build.

**Time:** 6–10 hrs/week. Launch in a few weeks.

**Sources:** Sajjaad Khader, *How to Become a $300K AI Engineer in 2026* (what to learn) · Nick Saraev, *How I Learn Complex Skills & Difficult Subjects So Fast with AI* (how to learn) · my Interviewer session (where I actually am).

---

## Where I am (Interviewer result)

> My ability to **build** with AI is well ahead of my ability to **explain, verify and support** what I've built.

**Strengths:** paid client work, tools I use daily, connected external data, turning business problems into product ideas, I know why context and project rules matter, I can spot commercially useful problems (missed leads, slow quoting, scattered information, admin).

**Gaps, ranked:**
1. How data moves through a tool (APIs, storage, what happens when a connection fails)
2. Privacy & security (using data vs training on it, permissions, keys, storage, provider policies)
3. Reliability & safe limits (fixed scripts fail too; testing, failure alerts, human approval)
4. LLMs vs RAG vs factual accuracy (rule-based prices vs AI-generated prices)
5. Real operating costs (my £20–£50/month estimate isn't backed up yet)
6. Prompting & context limits (adding another rule doesn't fix everything)
7. Automation vs agents vs MCP (the right vocabulary and the limits)

**Misconception to kill first:** *"An automation can't make mistakes because it does the same thing every time."* If an automation does the same thing every time, it also makes the same mistake every time.

**Skip for now:** training models, maths, transformer internals, fine-tuning, running my own model infrastructure, complex multi-agent systems, building custom MCP servers, learning every automation platform, model-comparison rabbit holes, "I can integrate your whole business" claims.

---

## The big change: learn everything through ONE demo

Instead of six separate topics, every week takes **the RD Forever Fitness demo** apart from a different angle. By week 6 I can explain one real tool completely, covering data, privacy, failures, cost and accuracy. That's the credibility. It's also what Nick means by *production over consumption*: I learn by doing things to a real tool, not by watching videos about one.

## Offer stages (don't skip ahead)

| Stage | What I sell | When |
|---|---|---|
| 1 | Free talks + "how to use ChatGPT/Claude/Copilot well" sessions | **Now.** This uses strengths I already have. |
| 2 | Paid hands-on workshops (staff using AI safely) | After Week 3 (privacy covered) |
| 3 | Small, supervised integrations (human approves outputs) | After Week 6, starting with a narrow, tested tool |
| 4 | Unattended integrations with sensitive data or customer commitments | Later, once I have case studies and proper testing |

---

## The weekly learning loop (Nick Saraev's method)

1. **Explain** (Explainer): *"Explain [topic] using the RD Forever Fitness demo as the example, at business-owner level, then junior-developer level."*
2. **Redo without help.** After any explanation, go back to the start and do or explain it myself with no AI. It only adds 10–15% more time and makes the biggest difference. Nodding along to an explanation means I've only read about it, not learned it.
3. **Socratic:** *"Don't give me answers. Ask me questions about [topic] until I find what I don't know."*
4. **Build / Check:** do the week's task, then *"Here's my work and reasoning. Find what's wrong or missing and any faster way. Don't rewrite it."*
5. **Listener:** explain the week's topic three ways: **talk** (voice memo, as if to a BNI room), **draw** (quick sketch), **write** (short version). Then *"Grade all three against [source]. What did I miss or get wrong?"*
6. **Examiner:** *"Quiz me one question at a time, each harder than the last, until I start guessing. Then tell me my level."*
7. **Clerk:** *"Turn my notes into a clean outline + flashcards. Don't add anything I didn't write."* Put the cards into Anki and review them for 10 min/day.

**Running "hard questions" list:** every week, add the 5 hardest questions a skeptical owner could ask about that topic, then answer them out loud without notes.

**Rule against over-reliance:** before asking an agent to build or fix anything, write down how I think it works. Afterwards, explain back what it did.

---

## The 6 weeks

### Week 1: Trace the data (Gap 1)
- Draw the full journey of one enquiry through the RD Forever Fitness demo: customer → form/message → API call(s) → my app → AI model (if any) → storage → reply.
- For every arrow, note **what data moves, where it's stored, who can see it, and what happens if that step fails.**
- Learn just enough about APIs to follow it: requests and responses, API keys, JSON, status codes (200/401/429/500), webhooks.
- **Redo without help:** redraw the diagram from memory.
- **Proof:** a one-page data-flow diagram of the demo, which I can explain in 2 minutes.

### Week 2: Make it reliable (Gap 3 + the misconception)
- Write **10–20 test cases** for the gym demo (booking form + chat assistant): known questions or bookings → the correct reply (including edge cases, missing info, silly inputs). Run them.
- Break it on purpose: turn off a connection, send duplicate enquiries, feed it bad data. What happens?
- Add (or design) **failure handling:** an alert to a person, no duplicate actions, and **human approval before anything risky goes to a customer (injury advice, under-18s, refunds).**
- **Proof:** a test sheet with results, plus a plain-English answer to "what happens when it goes wrong?"

### Week 3: Privacy & security (Gap 2) → unlocks paid workshops
- Using data vs training on data; consumer vs business/API plans; provider data-retention policies (read the actual ones for the tools I use).
- API key handling, access permissions, where data is stored and whether it's encrypted, least-privilege access.
- UK GDPR basics for small businesses (ICO guidance): lawful basis, what data a tool collects, retention, telling customers.
- Local models are **one** option, not a requirement. Separate repositories don't protect customer data by themselves.
- **Proof:** a one-page "How this tool handles your data" sheet for the demo, plus a simple AI usage policy template for staff (good workshop material).

### Week 4: LLMs, RAG & accuracy (Gaps 4 + 6)
- The difference between training a model, putting information in its context, and retrieving documents (RAG). RAG supplies relevant information; it doesn't guarantee correct answers.
- **Rules vs generation:** answers matched by fixed rules (as the demo chat does now) need different checks from answers an AI writes freely, e.g. prices, timetables, injury advice. Decide which parts of my demo should be rules and which should be AI.
- Context windows, missing information, conflicting instructions: why adding another rule doesn't reliably fix a failure, and why the week 2 tests matter.
- **Proof:** a "where AI is and isn't used in this tool, and why" explanation.

### Week 5: Real costs + the right vocabulary (Gaps 5 + 7)
- Build a real monthly cost sheet from the actual providers: model calls (tokens × price), messaging/SMS, phone numbers, hosting, automation platform, plus **my support time.** Do it for low, typical and busy months.
- Automation vs agent vs MCP: which steps follow fixed rules and which let a model choose actions. Scheduling or spawning agents doesn't by itself make something an agent. MCP is a standard way to connect tools; it doesn't make them safe or reliable.
- **Proof:** a reusable cost-estimate template, and a one-minute explanation of "automation vs agent."

### Week 6: Package it and spar
- Write the three offers (talk → workshop → supervised integration) with honest scope.
- **Sparring partner (sales calls):** give the AI a rough outline of my call. Then *"Play a skeptical [accountant / trades owner / estate agent] at BNI. Push back hard on privacy, cost and reliability. Answers must be under 30 seconds. Afterwards, tell me where I was vague."* Run it against 3 personas.
- **Diagnostician:** *"Here are all my quiz and sparring mistakes [paste]. What underlying misunderstanding do they share?"* Fix the root cause, not each mistake.
- **Proof:** a 10-minute demo walkthrough covering what it does, the data flow, privacy, testing, failures and costs.

---

## After week 6
- Every client job → a short case study ("saved X hrs/week for a local Y").
- Post what I'm building on LinkedIn; the people in my local network will see it.
- Keep Anki going; add one new topic a month (deeper automation, RAG builds, agents).
- Move to Stage 4 offers only with case studies + a testing routine I trust.
