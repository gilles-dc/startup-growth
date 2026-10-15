---
name: pmf-problem
description: Validate whether a startup's problem is real, frequent and costly, with AI — first from sources, then from conversations. Use when running deep research on a problem, mining reviews, Reddit, forums or YouTube for pain points, pricing the cost of a problem, turning research into interview questions, writing or fixing an interview script, rehearsing, recruiting interviewees, comparing synthetic personas with real interviews, running AI-moderated interviews, synthesising transcripts with verified quotes, or asking for commitment. Part of the pmf-* set; reads pmf/product-info.md.
---

# PMF · Problem — is it a real problem?

Goal: the customer's world without the product, in their words, with numbers. First from sources, then from conversations with the people who have the problem. This is the qualitative stage: research makes the hypotheses checkable, and interviews put them in front of real people.

## What you need

- **Chat only:** I, J, K, L, M, N, R, S, T.
- **Free:** your AI's research mode (A, B, G), the last30days skill (C; Reddit, HN and GitHub need no key), YouTube transcripts (H), Claude Code (E, F), free tiers of Granola, Fireflies or Otter (Q), Tally (T), Gmail drafts and Calendly (O).
- **Paid, optional:** Apify scraper runs (D, pay per run), AI interviewer tools (P, e.g. UserCall from $89/month).
- **Blocked to a plain web fetch:** Capterra and G2 (anti-bot protection), Google Play and YouTube (pages built in JavaScript), most of Reddit. Use the connector named in each technique; pasting by hand is the last resort.

## Before you start

Read `pmf/product-info.md`, `pmf/assumptions.md` and `pmf/interview-questions.md` if they exist. If the first two don't exist, run the `pmf-loop` setup, or ask: product, customer, problem in their words, what they do today instead. Ask how many interviews the founder has done so far.

Recommend the techniques that fit the founder's situation. A typical first pass: **A + B + C → I → K**, then **L → M → O → Q → R**.

Each heading says how the technique works (chat · research · build · analyse · simulate) and, when it needs one, which building block: skill (it uses another skill), connector (it uses a connector) or schedule (runs on its own).

---

# Part 1 · From sources

## A. Research with sources you can check · research · 10 min

Deep research you can check line by line. Use the research tool available (Claude Research, web search) and follow this brief exactly:

> Research [problem] for [ICP].
> First, show me your research plan. Wait for my OK.
> Source priority: 1. primary data, studies, filings · 2. industry reports · 3. news · 4. social posts (opinion only, never as fact).
> End with a source table: claim · number · source URL · the exact sentence it comes from. If you can't find a source, write UNKNOWN. Don't estimate. Separate what was measured from what is someone's opinion. List what you could not find.

If you could not open a source page yourself (only a search snippet), mark its row NOT VERIFIED.

**Check:** the founder opens three links and reads the sentence. If one isn't there, treat every number in the report as a guess until checked. (Deloitte refunded part of a $290k Australian government contract in 2025 over a report citing papers and a court quote that don't exist.)

Seen at: Torsten Walbaum, Growth Unhinged (Aug 2025): plan first, source priorities, source table.

## B. Two research tools, side by side · research

1. Run the brief from A in two tools (e.g. Claude Research and ChatGPT deep research).
2. Paste both reports in and run:
> List every claim only one report makes, and every number the two reports disagree on, with both sources. Then list what both reports failed to find.
3. Disagreements and joint gaps go to technique K.

## C. What people said this month · research · skill

What people said about the problem this month, ranked by engagement.
- If the `last30days` skill is installed (mvanhorn/last30days-skill): run `/last30days [problem in plain words]`.
- Otherwise search with these strings and analyse the threads:
```
site:reddit.com "I wish there was" [topic]
site:reddit.com "is there a tool that" [task]
site:reddit.com "how do you guys" [task]
"[competitor] alternative"
"[competitor]" "switched to"
```
> For each thread: each pain mentioned · the exact quote · the username · what they say they use today. Only from the text.

Note for the founder: Reddit is restricting API access from November 2026 (RSS ends 13 Nov 2026, broader public API access in 2027), so Reddit-based tools and monitors may stop working.

## D. Competitors’ bad reviews, via Apify · research · connector

The 1–2 star reviews of what the customer uses today, in bulk.

**With a scraping connector (Apify, Bright Data, Firecrawl):** find the scraper for G2 / Capterra / Trustpilot / App Store / Google Play / Amazon, run it on the current solution and its two main competitors. Check the cost of a scraper run before starting a big one and tell the founder.
Apify has ready-made review scrapers for most of these sites; its free plan ($5 of credit a month) covers a few hundred reviews.
**Without a scraper:** ask the founder to paste 50–100 reviews. A plain web fetch can't open Capterra, G2 or Google Play, and cuts quotes short.

> Below are [N] reviews of [competitor], from [source].
> 1. Group the complaints into themes. For each: how many reviews mention it, and 3 quotes copied word for word.
> 2. For each theme: what the reviewer was trying to get done when it went wrong (the broken promise).
> 3. Who writes the angriest reviews: role, company size, use case, where stated.
> Only use what is in the reviews. If something isn't stated, write "not stated".

**Check:** Ctrl-F three quotes in the source. If one isn't there, redo it.

## E. Have the AI write your scraper · build (Claude Code)

When there's too much to read by hand: have Claude Code write a script that collects every post, comment or review about the problem from a source the founder is allowed to collect from. Respect terms of service and rate limits; avoid personal data. The result is thousands of rows to work with, ready for F.

Seen at: Amir Klein (monday.com), How I AI, Oct 2025: a 34,000-row Reddit dataset, built with no coding background.

## F. Sort every post by pain · analyse

1. Label every item with a cheap, fast model: pain type · segment · intensity · current workaround.
2. Reason over the labelled table with a strong model: clusters, counts, the strongest quote per cluster with a link.

Brute-forcing everything through the strongest model is what makes this expensive. Seen at: Claire Vo, How I AI, Sept 2026: ~200,000 classifications for about $4 with a cheap classifier, then a frontier model for reasoning.

## G. Rate your idea on six dimensions · research · skill

A check that admits what it couldn't find. Rate: problem frequency · problem severity · current spend · competition · willingness to switch · reachability of the ICP. Each HIGH / MED / LOW or **INSUFFICIENT DATA**, with citations. INSUFFICIENT DATA is the useful answer: that's where the founder goes and talks to people.

Seen at: Eddie Larsen's `/validate` skill (Medium, May 2026).

## H. Watch their workarounds on YouTube · research

People film their workaround and explain it out loud. Not yet tested end to end.
1. Search YouTube: "how I [task] in Excel / Notion / Google Sheets", or how they handle the problem today ("no-show policy salon"). Pick the 5 most-viewed.
2. Give the links to Gemini, which watches YouTube videos, picture and sound. Keep to videos under about 20 minutes: on a 45-minute video Gemini has invented details that weren't there (Caitlin Sullivan, Dec 2025). A plain web fetch gets empty transcripts; copying "Show transcript" by hand is the fallback.
> These are transcripts of people showing how they [task] today. For each video: the steps in order · the tools · how long it takes, if they say · every workaround · every moment they complain, sigh or apologise, quoted.

The workaround is the competitor you have to beat. The complaints are your copy.

## I. Price the problem · analyse

A cost-of-problem model where every assumption is a row.
> Build a cost-of-problem model for [ICP] with [problem], as a table: assumption · value · unit · source URL or GUESS · how I could check it in one interview question. Last row: total cost per customer per year, as a formula of the rows above.

If you can write files, save it as `pmf/problem-cost.csv` with working formulas. **Check:** count the GUESS rows. That's the interview agenda.

## J. Argue against yourself · chat · 5 min

> Here is my problem statement: [paste]. You are the customer I describe. You're busy and not convinced. Give me the 7 strongest reasons this problem isn't worth paying to solve. For each: what I'd need to see or hear in an interview to prove you wrong.

Add the seven to `pmf/interview-questions.md`. This output is a list of things to find out. It is no evidence.

## K. Turn research into interview questions · chat

The research's job is to make the next interview sharper.
1. Every UNKNOWN, every single-source claim, every opinion, every disagreement from B, every GUESS from I → one question.
2. Rewrite each as a question about the last time it happened ("Tell me about the last time you…"). Never ask about the future ("Would you…").
3. Save to `pmf/interview-questions.md`; the interview script (L) picks them up.

Then update `pmf/product-info.md` with what the research changed. Research that changes nothing was reading.

---

# Part 2 · From conversations

## L. Interview script · chat · skill

A script built on a method, then fixed by the founder.
- If an interview skill is installed (phuryn/pm-skills `interview-script`, or a Mom Test skill), generate the script with it from `product-info.md`.
- Otherwise, generate or fix it with this prompt:
> Here is my interview script: [paste, or "none yet"]. Using the rules of The Mom Test (Rob Fitzpatrick): flag every question that is leading, hypothetical ("would you…"), about the future, or about my idea. Rewrite each one into a question about something they did in the past. Add 3 questions about the last time [problem] happened. Add the questions from pmf/interview-questions.md. Output the final script only, in order.

Remove any question that asks the customer to design the solution. **Check:** if a question can be answered with "yes, probably", it's still wrong.

Seen at: Michele Hansen, Deploy Empathy (Feb 2025), on Chaz Yoon (Milled.com): a script in minutes, which still asked customers to brainstorm solutions until he removed those questions.

## M. Rehearse the interview · chat · 10 min

> Play [ICP persona from product-info.md]. You're busy, polite and not interested in new tools. You have [problem], but you've learned to live with it. Answer only what I ask; don't volunteer anything. If I ask a hypothetical question, give a vague, agreeable answer, the way real people do. After 10 questions, stop and tell me which questions got a real story and which got an opinion.

Nothing the persona says is evidence. It trains the interviewer.

## N. AI personas vs real people · simulate

1. Build 5 AI personas of the ICP from `product-info.md`. Interview each with the script. Write their consensus to `pmf/synthetic.md`.
2. The founder does at least 10 real interviews, recorded with permission, ideally half in person.
3. Compare: where did the personas agree with real people? Where were they wrong? Write it down.
4. Feed the real answers back into the personas. **The live interviews grade the synthetic ones, never the reverse.**

Why: NN/g (2024) found synthetic users claimed to have completed every course; a real user had completed three of seven. A Columbia mega-study (2026, 19 studies, 164 outcomes) found an average correlation of r = 0.20 between digital twins and the real people. Brand, Israeli & Ngwe (HBS) found GPT's willingness to pay matched humans for a known feature but needed real human data for new features, which is exactly the startup case.

Seen at: Steve Blank, Lean LaunchPad redesign (Sept 2026).

## O. Interview invites in your Gmail drafts · chat · connector

For each person on the list (`pmf/lists/`, from `pmf-customer`):
> Here is a person: [name, role, company, recent post or news]. Write a 3-sentence message asking for 20 minutes to learn how they handle [task] today. Reference their post or news in the first sentence. Don't mention a product, a startup or AI. No flattery. End with a specific day and time.

- With a scheduling connector (Calendly): add a single-use booking link per person.
- With email (Gmail via Zapier or Google Workspace): create **drafts only**. The founder reads, edits and sends.
- Never automate LinkedIn messaging. Never send on the founder's behalf.

**Check:** would the founder answer this message themselves? If not, don't send it.

## P. AI interviewer · simulate

Only once the script works with real people. An AI interviewer runs voice interviews in parallel; the founder reads the transcripts.
- Self-serve options exist (e.g. UserCall); enterprise ones (Listen Labs, Outset, Strella, Conveo) are priced for larger companies; openinterviewer is open source.
- Participants must be told they're speaking with an AI.
- Read the full transcripts as well as the summaries. It adds to the founder's own interviews; it never replaces them.

## Q. Patterns across interviews · analyse · skill

1. Get transcripts: a meeting-transcript connector (Granola, Fireflies, Otter), a folder of files, or pasted text.
2. **One interview per pass.** For each, using a fixed template: context · the story of the last time · current workaround · what they spent (money, time) · quotes (verbatim, with timestamp) · surprises. Save the template as a skill once it works, so every interview gets the same treatment.
3. **Then synthesise across interviews:**
> Make a table: pain · how many people mentioned it · strongest quote (word for word, with name) · what they do about it today · did they spend money or time on it (yes / no / not said). Sort by the last column. Then list every surprise: things people said that I didn't ask about. Then: what did people say that contradicts [hypotheses from assumptions.md]?
4. If NotebookLM is an option for the founder: uploading transcripts there gives answers that link to the exact line. Running Claude and ChatGPT side by side as two readers also shows where one of them over-reads.

## R. Check every quote · analyse · 5 min (mandatory)

Run on every synthesis before anyone uses it:
> For every quote in the analysis: find it in the transcripts; label it VERIFIED (word for word), PARAPHRASE (meaning kept, words changed) or NOT FOUND; for VERIFIED give speaker and timestamp; for PARAPHRASE give the real words. Then rewrite the analysis using only VERIFIED quotes.

Report the count of NOT FOUNDs to the founder. Teresa Torres found about 30% of ChatGPT's quotes from her interviews were inaccurate or absent (Product Talk, Oct 2025); Caitlin Sullivan's verification pass is the fix (Lenny's Newsletter, Feb 2026).

## S. Ask for a commitment · chat

Interest says yes. Commitment signs. End every good call with an ask in one of these currencies: time (a weekly call), data (access to their files), reputation (an introduction), money (a deposit, a letter of intent, a paid pilot).
> Draft a one-page pilot agreement between [startup] and [customer company]: 6 weeks · what we deliver · what they commit (data access, a weekly 30-minute call, a named contact) · price [€X] or free in exchange for a case study · what happens after, if it works. Plain language, one page.

Log every commitment in the Evidence table of `product-info.md`, with its strength: curiosity · interest · commitment · payment.

## T. The price question · analyse

Only to people who already described the problem. Four questions (Van Westendorp), in a form (Tally / Typeform connector if available):
1. At what price would it be so cheap you'd doubt the quality?
2. At what price would it be a bargain?
3. At what price would it start to feel expensive?
4. At what price would it be too expensive to consider?

With responses: compute the acceptable price range and optimal price point, plot the four curves (code), flag inconsistent responses. Small samples give rough ranges; say so.

---

## Output and hand-off

Write the Problem section of `pmf/product-info.md` in this format:

- **The what:** [who] has [problem], with numbers: how big, how often, how much it costs, what they resort to now.
- **The why:** why the problem exists: what current solutions offer and why that falls short; the structural gap.

Each line EVIDENCE (source) or HYPOTHESIS. Interview notes go in `pmf/interviews/`, the synthesis in `pmf/synthesis.md` (verified quotes only). Update `pmf/assumptions.md` and the Evidence table. Next: `pmf-solution` to shape the promise, or `pmf-iterate` if the interviews changed what you believe.

## Rules (from pmf-loop)

Nothing is evidence until a real person did something. Every number has a source or says GUESS. Every quote is verbatim or says PARAPHRASE. Never send, publish, launch, charge or spend without approval of the exact action. Update product-info.md and assumptions.md after every step. Change one thing per cycle. Interview recordings are personal data: get consent, store them carefully, and don't upload them to tools the interviewee didn't agree to.

---
Part of *Fast-Tracking Product-Market Fit with AI* by Gilles De Clerck (gillesdc.com).
