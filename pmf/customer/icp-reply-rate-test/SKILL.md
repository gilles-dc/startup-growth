---
name: icp-reply-rate-test
description: Let reply rates pick a startup's first customer. Writes five variants of the customer, each a different role, life stage, company type or trigger, ten people per variant, one three-line message per variant with the same ask, and a reply tracker; the variant with the highest reply rate is where to start. Use when a founder is torn between several possible customers, wants to test their ICP, pick a first segment or beachhead, or compare outreach reply rates. Workshop slide C4. Part of the pmf skills; reads pmf/product-info.md.
---

# ICP reply-rate test (C4) — which customer do I start with?

Goal: an ICP the founder can test, and the variant of the customer that is readiest to talk, picked by reply rate.

## What you need

- **Chat only:** the whole test. You write; the founder sends the messages from their own accounts.
- The ten people per variant come from `prospect-list-builder` (C3), which lists its own free and paid options.

## Before you start

Read `pmf/product-info.md` and `pmf/assumptions.md` (also check the project root, or a file attached to the conversation).

**If there is no product-info.md,** offer two routes and let the founder pick: run `pmf` first (seven questions, and every pmf skill reads the file it writes), or go straight on. Straight on: ask these in one message, and say short answers are fine:
1. What is the product, in one sentence?
2. Who is it for? B2B: the role, the type and size of company, the countries. B2C: the person, their situation, where they live.
3. What problem does it solve, in their words, and what do they do today instead?
4. What event makes the problem urgent for them right now?
5. What evidence do you have so far: conversations, sign-ups, people who said yes?

Label the answers HYPOTHESIS. At the end, output them as a short `product-info.md` for the founder to save.

Each heading says how the technique works (chat · research · build · analyse · simulate) and, when it needs one, which building block: skill (it uses another skill), connector (it uses a connector) or schedule (runs on its own).

**Step by step.** If the founder asks to be taken through a technique, do one step at a time and stop at every hand-off. Each technique that needs the founder to act marks its steps: **Now** (what you do), **Your turn** (what the founder does; then stop and wait), **Resume** (the sentence that picks it up, in this chat or a new one), **Then** (what follows). At every stop, add one line to `product-info.md`: "Waiting for: [what], since [date]. To resume: Use icp-reply-rate-test to continue [the technique]." When you read a `product-info.md` that has a Waiting for line, start there: ask whether it has come in.

---

## Five first customers, picked by reply rate · chat · 10 min

Let reply rates pick the first customer instead of the founder's gut.

**When:** after the ICP. From the ICP and its hand-off, distil five variants of the customer, each a different angle on the problem: a different role, life stage, company type or trigger. Reply rates show which variant is readiest to talk, and so where to start. Also useful before the ICP, when the founder is torn between customers.

Prompt (run it yourself with the founder's product and ICP):

> My product: [one sentence]. My ICP: [the summary]. Write 5 variants of this customer that could each be the right first customer, as different as possible: different role, life stage or company type, and a different trigger. For each: who, specifically · their trigger (the event that makes the problem urgent for them) · their angle on the problem, in one line · where I'd find 10 of them this week.

Then:
1. Build a list of 10 people per variant (`prospect-list-builder` (C3); for consumers, the people who posted about the problem). Say how many each variant already has from `prospect-list-builder`.
2. Write one three-line message per variant, aimed at that variant's angle, with the same ask in all five (20 minutes to learn how they handle [task]) so the reply rates compare. No pitch. Write it in the customer's language. Show all five messages.
3. The founder sends them (never you). Track replies per variant in `pmf/icp-test.md`.
4. The highest reply rate becomes the variant to start with. Ten per variant is a first read: if the top two are within two replies of each other, send ten more to each before deciding.

**Check:** the decision is made on reply rate per variant, not on which one sounds best.

**Step by step:**
1. **Now:** the five variants, ten people per variant, the five messages and the reply tracker in `pmf/icp-test.md`.
2. **Your turn:** send the messages yourself, from your own accounts. Give it a week, and log every reply against its variant. **Stop.**
3. **Resume:** attach `icp-test.md` (or paste the reply counts per variant) and say: "continue the first-customer test".
4. **Then:** the variant to start with, or ten more messages each if the top two are close.

---

## Output and hand-off

- Track replies in `pmf/icp-test.md`, one row per variant.
- Update `pmf/product-info.md` (Customer section) with the variant to start with, and `pmf/assumptions.md` (persona rows).
- If you can't write files, output the changed sections as a markdown block for the founder to save, and the tracker as a table to paste into a sheet.
- Next: describe the winning variant in five dimensions with `icp` (C1), if it isn't yet. Then the problem stage: is the problem real for these people? Research it with `social-listener` (P1), then book the conversations with `interview-script` (P4).

## Rules (from pmf)

Nothing is evidence until a real person did something. Every number has a source or says GUESS. Every quote is verbatim or says PARAPHRASE. Never send, publish, launch, charge or spend without approval of the exact action. Update product-info.md and assumptions.md after every step. Change one thing per cycle.

---
Part of *Fast-Tracking Product-Market Fit with AI* by Gilles De Clerck (gillesdc.com).
