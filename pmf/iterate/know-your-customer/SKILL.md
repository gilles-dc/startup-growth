---
name: know-your-customer
description: Check whether the founders know their customer as well as the interview transcripts do. The AI asks each founder ten questions on the customer's day, tools, spending and words, then scores them, with the quote for every miss. Also sets up an agent that analyses every new interview transcript (Granola, a Drive folder) with a fixed template, checks every quote and proposes assumption-board changes, or runs the same prompt by hand after each call. Use after interviews, before the next calls, or for "quiz me on my customer", "learning debt", "analyse every new interview". Workshop slide I1. Part of the pmf skills; reads pmf/product-info.md.
---

# Know your customer (I1) — does the team know the customer?

Goal: every founder can explain the customer from memory, and every new interview adds to the evidence without anyone having to remember it.

## What you need

- **Chat only:** Quiz yourself on your customer; Every new interview, analysed by hand, with the same prompt run after each interview.
- **Runs on its own:** Claude Cowork scheduled tasks or Claude Code routines (Every new interview, analysed); Slack for the digests.

## Before you start

Read `pmf/product-info.md`, `pmf/assumptions.md`, `pmf/synthesis.md` and `pmf/tests/` if they exist (also check the project root, or a file attached to the conversation).

**If there is no product-info.md,** offer two routes and let the founder pick: run `pmf` first (seven questions, and every pmf skill reads the file it writes), or go straight on. Straight on: ask these in one message, and say short answers are fine:
1. What is the product, in one sentence, and who is it for?
2. What did you believe at the start, one line each: the customer, the problem, the promise, the product, the price?
3. What have you done since: how many interviews, which tests, which numbers? Attach the transcripts, notes or results you have.

Label the answers HYPOTHESIS. Answer 2 is the starting assumption board that new interviews are checked against. At the end, output them as a short `product-info.md` for the founder to save.

Each heading says how the technique works (chat · research · build · analyse · simulate) and, when it needs one, which building block: skill (it uses another skill), connector (it uses a connector) or schedule (runs on its own).

**Step by step.** If the founder asks to be taken through a technique, do one step at a time and stop at every hand-off. Each technique that needs the founder to act marks its steps: **Now** (what you do), **Your turn** (what the founder does; then stop and wait), **Resume** (the sentence that picks it up, in this chat or a new one), **Then** (what follows). At every stop, add one line to `product-info.md`: "Waiting for: [what], since [date]. To resume: Use know-your-customer to continue [the technique]." When you read a `product-info.md` that has a Waiting for line, start there: ask whether it has come in.

---

## Quiz yourself on your customer · chat · 5 min

> You have my customer interviews: [transcripts / synthesis]. Quiz me: 10 questions about my customer: their day, their tools, what they pay for, the words they use, what they said word for word. Don't give hints. At the end, score me and show what I got wrong, with the quote.

Run it with every founder on the team. Under 7/10: reread the transcripts before the next call. If the AI knows the customer better than the team does, the team has learning debt (Steve Blank's term): any founder should be able to explain the customer, their workflow, the evidence, the economics and the contradictions without opening a laptop.

## More techniques

### Every new interview, analysed · analyse · schedule

Only automate a method that already works by hand; automating a bad process makes it fail faster. Set up with Claude Cowork scheduled tasks or Claude Code routines (the founder approves the schedule and the connectors). Agents write drafts and digests; they never send, launch or spend.

Every new transcript updates the evidence, without the founder opening anything. Trigger: a new transcript (Granola, a Drive folder) or a daily schedule.

> When a new transcript appears in [Granola / folder]: analyse it with the per-interview template from `interview-synthesis` (P5), verify every quote, append to pmf/interviews/, and propose assumption-board changes with quotes. Post a 5-line summary to [Slack / doc].
(Seen at: Caitlin Sullivan on Aakash Gupta's podcast: 1 survey + 5 transcripts in under 2 minutes.)

By hand (no schedule, no transcript connector): after each interview, the founder attaches the transcript, or pastes it, and runs the same prompt in the chat. The summary comes back in the chat for the founder to share.

**Step by step:**
1. **Now:** write the prompt, the trigger and the connectors it reads, for approval. By hand: the prompt to save.
2. **Your turn:** approve the schedule and switch it on (a Claude Cowork scheduled task or a Claude Code routine). By hand: hold the next interview. **Stop.**
3. **Resume:** attach the new transcript (on a schedule, nothing) and say: "continue the interview analysis". After every interview, the same sentence.
4. **Then:** the analysis, every quote checked, and the proposed board changes for the founder to approve (Update the assumption board, in `pivot-or-persevere` (I2)).

---

## Output and hand-off

The quiz score and what each founder got wrong, in the chat; each analysed interview in `pmf/interviews/`; proposed changes to `pmf/assumptions.md`, for the founder to approve; updated `pmf/product-info.md`. If you can't write files, output the changed sections as a markdown block for the founder to save. Next: `pivot-or-persevere` (I2) to approve the board changes and decide what changes, or `interview-script` (P4) for more conversations.

## Rules (from pmf)

Nothing is evidence until a real person did something. Every number has a source or says GUESS. Every quote is verbatim or says PARAPHRASE. Never send, publish, launch, charge or spend without approval of the exact action. Update product-info.md and assumptions.md after every step. Change one thing per cycle.

---
Part of *Fast-Tracking Product-Market Fit with AI* by Gilles De Clerck (gillesdc.com).
