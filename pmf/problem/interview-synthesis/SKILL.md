---
name: interview-synthesis
description: Synthesise customer interviews with AI and check every quote against the transcripts. Use when you have interview transcripts or notes (Granola, Fireflies, Otter, files or pasted text) and want one summary per interview, a table of pains across all of them, the surprises, what contradicts your assumptions, every quote labelled VERIFIED, PARAPHRASE or NOT FOUND, or a Van Westendorp price question for the people you interviewed. Workshop slide P5. Part of the pmf skills; reads pmf/product-info.md.
---

# Interview synthesis (P5) — what did the interviews tell us?

Goal: the customer's world without the product, in their words, with numbers, from conversations with the people who have the problem: one pass per interview, then the patterns across them, using only quotes checked against the transcripts.

## What you need

- **Chat only:** Check every quote, The price question (asked by voice, or pasted into any form tool); Patterns across interviews from pasted transcripts or notes.
- **Free:** free tiers of Granola, Fireflies or Otter (Patterns across interviews), Tally (The price question).

## Before you start

Read `pmf/product-info.md` and `pmf/assumptions.md` if they exist (also check the project root, or a file attached to the conversation). If they don't exist, run the `pmf` setup, or ask: product, customer, problem in their words, what they do today instead. Ask how many interviews the founder has done so far.

**If there is no product-info.md,** offer two routes and let the founder pick: run `pmf` first (seven questions, and every pmf skill reads the file it writes), or go straight on. Straight on: ask these in one message, and say short answers are fine:
1. What is the product or idea, in one sentence?
2. Who has the problem? Role, company type or life situation.
3. What is the problem, in the words your customer would use?
4. What do they do today about it? Name the tools, competitors or workarounds: their reviews and videos are the research.
5. How many people with the problem have you talked to so far? Any notes or recordings?

Label the answers HYPOTHESIS. At the end, output them as a short `product-info.md` for the founder to save.

Recommend the techniques that fit the founder's situation. A typical first pass in the problem stage: Research with sources you can check + Two research tools + What people said this month (`social-listener`, P1) → Price the problem → Turn research into interview questions (`interview-script`, P4), then the Interview script → Interview invites → Patterns across interviews → Check every quote (this skill).

Each heading says how the technique works (chat · research · build · analyse · simulate) and, when it needs one, which building block: skill (it uses another skill), connector (it uses a connector) or schedule (runs on its own).

**Step by step.** If the founder asks to be taken through a technique, do one step at a time and stop at every hand-off. Each technique that needs the founder to act marks its steps: **Now** (what you do), **Your turn** (what the founder does; then stop and wait), **Resume** (the sentence that picks it up, in this chat or a new one), **Then** (what follows). At every stop, add one line to `product-info.md`: "Waiting for: [what], since [date]. To resume: Use interview-synthesis to continue [the technique]." When you read a `product-info.md` that has a Waiting for line, start there: ask whether it has come in.

---

## Patterns across interviews · analyse · skill

1. Get transcripts: a meeting-transcript connector (Granola, Fireflies, Otter), a folder of files, or pasted text.
2. **One interview per pass.** For each, using a fixed template: context · the story of the last time · current workaround · what they spent (money, time) · quotes (verbatim, with timestamp) · surprises. Save the template as a skill once it works, so every interview gets the same treatment.
3. **Then synthesise across interviews:**
> Make a table: pain · how many people mentioned it · strongest quote (word for word, with name) · what they do about it today · did they spend money or time on it (yes / no / not said). Sort by the last column. Then list every surprise: things people said that I didn't ask about. Then: what did people say that contradicts [hypotheses from assumptions.md]?
4. If NotebookLM is an option for the founder: uploading transcripts there gives answers that link to the exact line. Running Claude and ChatGPT side by side as two readers also shows where one of them over-reads.
5. Check every quote, below, before anyone uses the synthesis.

**Step by step:**
1. **Now:** with a transcript connector, read the transcripts and go straight on. Otherwise say how to get them out: the recording tool's export, or typed notes.
2. **Your turn (no connector):** put the transcripts or notes in one folder, one file per interview. **Stop.**
3. **Resume:** attach the files and say: "continue the interview patterns".
4. **Then:** one pass per interview, the table across them, then Check every quote.

### Check every quote · analyse · 5 min (mandatory)

Run on every synthesis before anyone uses it:
> For every quote in the analysis: find it in the transcripts; label it VERIFIED (word for word), PARAPHRASE (meaning kept, words changed) or NOT FOUND; for VERIFIED give speaker and timestamp; for PARAPHRASE give the real words. Then rewrite the analysis using only VERIFIED quotes.

Report the count of NOT FOUNDs to the founder. Teresa Torres found about 30% of ChatGPT's quotes from her interviews were inaccurate or absent (Product Talk, Oct 2025); Caitlin Sullivan's verification pass is the fix (Lenny's Newsletter, Feb 2026).

## More techniques

### The price question · analyse

Only to people who already described the problem. Four questions (Van Westendorp), in a form (Tally / Typeform connector if available):
1. At what price would it be so cheap you'd doubt the quality?
2. At what price would it be a bargain?
3. At what price would it start to feel expensive?
4. At what price would it be too expensive to consider?

No forms connector: output the four questions ready to paste into any form tool (Google Forms, Tally, Typeform, Microsoft Forms), each with a number answer in the founder's currency. Or ask them by voice at the end of the interview and note the four prices per person in one sheet.

**Step by step:**
1. **Now:** write the four questions (a draft in the form tool, or the paste-ready text) and the message that goes with them, for approval.
2. **Your turn:** send them to the people who already described the problem, and wait for the answers. **Stop.**
3. **Resume:** attach the export or the sheet and say: "continue the price question". With the forms connector, read the answers directly.
4. **Then:** the range, the four curves and the flags below.

With responses: compute the acceptable price range and optimal price point, plot the four curves (code), flag inconsistent responses. Small samples give rough ranges; say so.

---

## Output and hand-off

Write the Problem section of `pmf/product-info.md` in this format:

- **The what:** [who] has [problem], with numbers: how big, how often, how much it costs, what they resort to now.
- **The why:** why the problem exists: what current solutions offer and why that falls short; the structural gap.

Each line EVIDENCE (source) or HYPOTHESIS. Interview notes go in `pmf/interviews/`, the synthesis in `pmf/synthesis.md` (verified quotes only). Update `pmf/assumptions.md` and the Evidence table. If you can't write files, output the changed sections as a markdown block for the founder to save. Next: the solution stage, from `competitive-analysis` (S1) to `value-proposition-generator` (S4), to shape the promise, or `pivot-or-persevere` (I2) if the interviews changed what you believe.

## Rules (from pmf)

Nothing is evidence until a real person did something. Every number has a source or says GUESS. Every quote is verbatim or says PARAPHRASE. Never send, publish, launch, charge or spend without approval of the exact action. Update product-info.md and assumptions.md after every step. Change one thing per cycle. Interview recordings are personal data: get consent, store them carefully, and don't upload them to tools the interviewee didn't agree to.

---
Part of *Fast-Tracking Product-Market Fit with AI* by Gilles De Clerck (gillesdc.com).
