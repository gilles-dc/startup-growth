---
name: interview-script
description: Write or fix a customer interview script with AI, using The Mom Test. Use when turning research into interview questions, asking about the last time a problem happened, removing leading or hypothetical questions, pricing the cost of a problem, arguing against your own problem statement, drafting interview invites as Gmail drafts, setting up an AI interviewer, or asking for a commitment or a pilot agreement at the end of a call. Workshop slide P4. Part of the pmf skills; reads pmf/product-info.md.
---

# Interview script (P4) — what do I ask, and whom?

Goal: a numbered interview script built on a method, with every open question from the research turned into a question about the last time it happened. This is where the problem stage moves from sources to conversations with the people who have the problem.

## What you need

- **Chat only:** Turn research into interview questions, Interview script, Price the problem, Argue against yourself, Ask for a commitment; Interview invites with the invites sent by hand.
- **Free:** Gmail drafts and Calendly (Interview invites).
- **Paid, optional:** AI interviewer tools (AI interviewer, e.g. UserCall from $89/month).

## Before you start

Read `pmf/product-info.md`, `pmf/assumptions.md` and `pmf/interview-questions.md` if they exist (also check the project root, or a file attached to the conversation). If the first two don't exist, run the `pmf` setup, or ask: product, customer, problem in their words, what they do today instead. Ask how many interviews the founder has done so far.

**If there is no product-info.md,** offer two routes and let the founder pick: run `pmf` first (seven questions, and every pmf skill reads the file it writes), or go straight on. Straight on: ask these in one message, and say short answers are fine:
1. What is the product or idea, in one sentence?
2. Who has the problem? Role, company type or life situation.
3. What is the problem, in the words your customer would use?
4. What do they do today about it? Name the tools, competitors or workarounds: their reviews and videos are the research.
5. How many people with the problem have you talked to so far? Any notes or recordings?

Label the answers HYPOTHESIS. At the end, output them as a short `product-info.md` for the founder to save.

Recommend the techniques that fit the founder's situation. A typical first pass in the problem stage: Research with sources you can check + Two research tools + What people said this month (`social-listener`, P1) → Price the problem → Turn research into interview questions (this skill), then the Interview script → Interview invites → Patterns across interviews → Check every quote (`interview-synthesis`, P5).

Each heading says how the technique works (chat · research · build · analyse · simulate) and, when it needs one, which building block: skill (it uses another skill), connector (it uses a connector) or schedule (runs on its own).

**Step by step.** If the founder asks to be taken through a technique, do one step at a time and stop at every hand-off. Each technique that needs the founder to act marks its steps: **Now** (what you do), **Your turn** (what the founder does; then stop and wait), **Resume** (the sentence that picks it up, in this chat or a new one), **Then** (what follows). At every stop, add one line to `product-info.md`: "Waiting for: [what], since [date]. To resume: Use interview-script to continue [the technique]." When you read a `product-info.md` that has a Waiting for line, start there: ask whether it has come in.

---

## Interview script · chat · skill

A script built on a method, then fixed by the founder. Two steps: first the research becomes questions, then the questions become a script.

### 1. Turn research into interview questions · chat

The research's job is to make the next interview sharper.
1. Every UNKNOWN, every single-source claim, every opinion, every disagreement from the two research reports in `social-listener` (P1), every GUESS from Price the problem → one question.
2. Rewrite each as a question about the last time it happened ("Tell me about the last time you…"). Never ask about the future ("Would you…").
3. Save to `pmf/interview-questions.md`; the script in the next step picks them up.

Then update `pmf/product-info.md` with what the research changed. Research that changes nothing was reading.

### 2. Write or fix the script · chat · skill

- If an interview skill is installed (phuryn/pm-skills `interview-script`, or a Mom Test skill), generate the script with it from `product-info.md`.
- Otherwise, generate or fix it with this prompt:
> Here is my interview script: [paste, or "none yet"]. Using the rules of The Mom Test (Rob Fitzpatrick): flag every question that is leading, hypothetical ("would you…"), about the future, or about my idea. Rewrite each one into a question about something they did in the past. Add 3 questions about the last time [problem] happened. Add the questions from pmf/interview-questions.md. Output the final script only, in order.

Remove any question that asks the customer to design the solution. Mark each question in words as **must ask** or **optional** (skip if short on time), never with symbols, and number every question. **Check:** if a question can be answered with "yes, probably", it's still wrong.

Seen at: Michele Hansen, Deploy Empathy (Feb 2025), on Chaz Yoon (Milled.com): a script in minutes, which still asked customers to brainstorm solutions until he removed those questions.

## More techniques

### Price the problem · analyse

A cost-of-problem model where every assumption is a row.
> Build a cost-of-problem model for [ICP] with [problem], as a table: assumption · value · unit · source URL or GUESS · how I could check it in one interview question. Last row: total cost per customer per year, as a formula of the rows above.

If you can write files, save it as `pmf/problem-cost.csv` with working formulas. **Check:** count the GUESS rows. That's the interview agenda.

### Argue against yourself · chat · 5 min

> Here is my problem statement: [paste]. You are the customer I describe. You're busy and not convinced. Give me the 7 strongest reasons this problem isn't worth paying to solve. For each: what I'd need to see or hear in an interview to prove you wrong.

Add the seven to `pmf/interview-questions.md`. This output is a list of things to find out. It is no evidence.

### Interview invites in your Gmail drafts · chat · connector

For each person on the list (`pmf/lists/`, from `prospect-list-builder`, C3):
> Here is a person: [name, role, company, recent post or news]. Write a 3-sentence message asking for 20 minutes to learn how they handle [task] today. Reference their post or news in the first sentence. Don't mention a product, a startup or AI. No flattery. End with a specific day and time.

- With a scheduling connector (Calendly): add a single-use booking link per person.
- With email (Gmail via Zapier or Google Workspace): create **drafts only**. The founder reads, edits and sends.
- Never automate LinkedIn messaging. Never send on the founder's behalf.

No email connector: output each invite as plain text; the founder pastes it into their own email or a LinkedIn message and sends it by hand.

**Check:** would the founder answer this message themselves? If not, don't send it.

**Step by step:**
1. **Now:** one invite per person, as Gmail drafts or as text, each with a day and time or a booking link.
2. **Your turn:** read, edit and send each one yourself, and book the calls. Run the interviews with the Interview script; record only with consent. **Stop.**
3. **Resume:** attach the transcripts or notes and say: "continue the interviews".
4. **Then:** in `interview-synthesis` (P5), one pass per interview and the patterns (Patterns across interviews), then the quote check (Check every quote).

### AI interviewer · simulate

This shows how far the chain can be automated: the Interview script, the people from `prospect-list-builder` (C3), the Interview invites, and an AI that runs the interviews. Recommendation: do the interviews yourself. Use this only once the script works with real people. An AI interviewer runs voice interviews in parallel; the founder reads the transcripts.
- Self-serve options exist (e.g. UserCall); enterprise ones (Listen Labs, Outset, Strella, Conveo) are priced for larger companies; openinterviewer is open source.
- Participants must be told they're speaking with an AI.
- Read the full transcripts as well as the summaries. It adds to the founder's own interviews; it never replaces them.

**Step by step:**
1. **Now:** prepare the Interview script and the list of people for the tool, and the line that tells them they'll speak with an AI.
2. **Your turn:** set up the tool, send the invites and wait for the interviews to come in. **Stop.**
3. **Resume:** attach the transcripts and say: "continue the AI interviews".
4. **Then:** in `interview-synthesis` (P5), the patterns (Patterns across interviews) and the quote check (Check every quote), on the full transcripts.

### Ask for a commitment · chat

Interest says yes. Commitment signs. End every good call with an ask in one of these currencies: time (a weekly call), data (access to their files), reputation (an introduction), money (a deposit, a letter of intent, a paid pilot).
> Draft a one-page pilot agreement between [startup] and [customer company]: 6 weeks · what we deliver · what they commit (data access, a weekly 30-minute call, a named contact) · price [€X] or free in exchange for a case study · what happens after, if it works. Plain language, one page.

Log every commitment in the Evidence table of `product-info.md`, with its strength: curiosity · interest · commitment · payment.

**Step by step:**
1. **Now:** write the ask for the end of the call and the pilot agreement, for approval.
2. **Your turn:** make the ask at the end of each good call, and send the agreement to whoever says yes. **Stop.**
3. **Resume:** say who agreed to what, and say: "continue the commitments".
4. **Then:** each one logged in the Evidence table, with its strength.

---

## Output and hand-off

Turn research into interview questions and Argue against yourself add to `pmf/interview-questions.md`. Price the problem writes `pmf/problem-cost.csv`. Commitments go in the Evidence table of `pmf/product-info.md`. Where the research changed the problem, update the Problem section of `pmf/product-info.md` in this format:

- **The what:** [who] has [problem], with numbers: how big, how often, how much it costs, what they resort to now.
- **The why:** why the problem exists: what current solutions offer and why that falls short; the structural gap.

Each line EVIDENCE (source) or HYPOTHESIS. Update `pmf/assumptions.md`. If you can't write files, output the changed sections as a markdown block for the founder to save. Next: run the interviews, then `interview-synthesis` (P5) for the patterns and the quote check.

## Rules (from pmf)

Nothing is evidence until a real person did something. Every number has a source or says GUESS. Every quote is verbatim or says PARAPHRASE. Never send, publish, launch, charge or spend without approval of the exact action. Update product-info.md and assumptions.md after every step. Change one thing per cycle. Interview recordings are personal data: get consent, store them carefully, and don't upload them to tools the interviewee didn't agree to.

---
Part of *Fast-Tracking Product-Market Fit with AI* by Gilles De Clerck (gillesdc.com).
