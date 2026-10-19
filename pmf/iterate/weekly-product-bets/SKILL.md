---
name: weekly-product-bets
description: Every Monday, read last week's product metrics, new interview notes, test results and the team channel, and propose five specific bets, ranked, each with the evidence behind it, the test to run and the result that would change the plan. Finds the biggest drop in the funnel first, ranks what people did above what they asked for, and lists requests from outside the ICP separately. Runs on its own as a Claude Cowork scheduled task or Claude Code routine, or by hand from exports each Monday. Use for "what should we test next?", "Monday bets", "weekly product ideas". Workshop slide I3. Part of the pmf skills; reads pmf/product-info.md.
---

# Weekly product bets (I3) — what do we try next?

Goal: make the loop run without the founder having to remember it: every Monday, five ranked bets from the week's evidence.

## What you need

- **Chat only:** Monday: five ideas to test, by hand, with the same prompt run on a fixed day.
- **Runs on its own:** Claude Cowork scheduled tasks or Claude Code routines; Slack for the digests.

## Before you start

Read `pmf/product-info.md`, `pmf/assumptions.md`, `pmf/synthesis.md` and `pmf/tests/` if they exist (also check the project root, or a file attached to the conversation).

**If there is no product-info.md,** offer two routes and let the founder pick: run `pmf` first (seven questions, and every pmf skill reads the file it writes), or go straight on. Straight on: ask these in one message, and say short answers are fine:
1. What is the product, in one sentence, and who is it for?
2. What have you done since you started: how many interviews, which tests, which numbers? Attach the transcripts, notes or results you have.
3. What decision are you facing right now?

Label the answers HYPOTHESIS. At the end, output them as a short `product-info.md` for the founder to save.

Each heading says how the technique works (chat · research · build · analyse · simulate) and, when it needs one, which building block: skill (it uses another skill), connector (it uses a connector) or schedule (runs on its own).

**Step by step.** If the founder asks to be taken through a technique, do one step at a time and stop at every hand-off. Each technique that needs the founder to act marks its steps: **Now** (what you do), **Your turn** (what the founder does; then stop and wait), **Resume** (the sentence that picks it up, in this chat or a new one), **Then** (what follows). At every stop, add one line to `product-info.md`: "Waiting for: [what], since [date]. To resume: Use weekly-product-bets to continue [the technique]." When you read a `product-info.md` that has a Waiting for line, start there: ask whether it has come in.

---

## Monday: five ideas to test · analyse · schedule

Only automate a method that already works by hand; automating a bad process makes it fail faster. Set up with Claude Cowork scheduled tasks or Claude Code routines (the founder approves the schedule and the connectors). Agents write drafts and digests; they never send, launch or spend.

Every Monday, the agent reads the week's data and proposes what to try next.

> Every Monday 8:00: read last week's product metrics [analytics connector], new interview notes, test results and [Slack channel]. Propose 5 specific bets, ranked, each with the evidence behind it and the test to run. Post before the team meeting.

How to pick the bets:
1. **Find the biggest drop** in this week's funnel, and look for its cause in the notes and messages.
2. **Rank the evidence:** what people did (metrics, payments, drop-offs) outweighs what they asked for. Several voices from the ICP outweigh one loud voice from a segment you don't serve.
3. **Each bet:** the evidence, with the line it comes from · the test to run · the result that would change the plan.
4. **Five bets, ranked.** Pick one to run first and say why; say which others can run alongside without touching the product.
5. **Requests from outside the ICP** (for example a feature only bigger customers want) are a question about who the customer is: list them separately, never as a bet.

(Seen at: Charles Cook, PostHog, Apr 2026 — he acts on about one in five; Jenny Wen, Anthropic, Mar 2026 — "3 vetted product ideas" every Monday.)

By hand (no schedule, no connectors): every Monday, the founder attaches last week's funnel export from the analytics tool, the new interview notes and test results, and the week's messages from the team channel, copied into one file. Run the same prompt on them.

**Step by step:**
1. **Now:** write the prompt and list what it reads, for approval. By hand: list the exports to bring each Monday.
2. **Your turn:** approve the schedule and switch it on. By hand: wait for Monday and gather the exports. **Stop.**
3. **Resume:** attach the exports (on a schedule, nothing) and say: "continue the Monday bets". Every Monday after, the same sentence.
4. **Then:** five bets, ranked, picked as above.

---

## Output and hand-off

Five bets, ranked, posted where the founder chose (Slack, a doc) or in the chat; the requests from outside the ICP listed apart; updated `pmf/product-info.md`. If you can't write files, output the changed sections as a markdown block for the founder to save. Next: run the first bet's test; take what it shows to `pivot-or-persevere` (I2). Requests from outside the ICP go to `icp` (C1), as a question about who the customer is.

## Rules (from pmf)

Nothing is evidence until a real person did something. Every number has a source or says GUESS. Every quote is verbatim or says PARAPHRASE. Never send, publish, launch, charge or spend without approval of the exact action. Update product-info.md and assumptions.md after every step. Change one thing per cycle.

---
Part of *Fast-Tracking Product-Market Fit with AI* by Gilles De Clerck (gillesdc.com).
