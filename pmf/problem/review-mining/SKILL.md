---
name: review-mining
description: Mine the bad reviews of what a startup's customers use today, with AI. Use when collecting 1–2 star reviews from G2, Capterra, Trustpilot, the App Store, Google Play or Amazon, running an Apify review scraper, grouping competitors' complaints into themes with counts and word-for-word quotes, finding the broken promise behind each complaint, or finding out who writes the angriest reviews. Works from pasted reviews too. Workshop slide P2. Part of the pmf skills; reads pmf/product-info.md.
---

# Review mining (P2) — what do people hate about what they use today?

Goal: the 1–2 star reviews of what the customer uses today, in bulk, grouped into themes with counts and quotes word for word. This is the qualitative stage: research makes the hypotheses checkable, and interviews put them in front of real people.

## What you need

- **Chat only:** 50–100 reviews, pasted.
- **Free:** Apify's free plan ($5 of credit a month), or another scraping connector (Bright Data, Firecrawl).
- **Paid, optional:** Apify scraper runs (pay per run).
- **Blocked to a plain web fetch:** Capterra and G2 (anti-bot protection), Google Play and YouTube (pages built in JavaScript), most of Reddit. Use the connector named in each technique; pasting by hand is the last resort.

## Before you start

Read `pmf/product-info.md` and `pmf/assumptions.md` if they exist (also check the project root, or a file attached to the conversation). If they don't exist, run the `pmf` setup, or ask: product, customer, problem in their words, what they do today instead.

**If there is no product-info.md,** offer two routes and let the founder pick: run `pmf` first (seven questions, and every pmf skill reads the file it writes), or go straight on. Straight on: ask these in one message, and say short answers are fine:
1. What is the product or idea, in one sentence?
2. Who has the problem? Role, company type or life situation.
3. What is the problem, in the words your customer would use?
4. What do they do today about it? Name the tools, competitors or workarounds: their reviews and videos are the research.

Label the answers HYPOTHESIS. At the end, output them as a short `product-info.md` for the founder to save.

Each heading says how the technique works (chat · research · build · analyse · simulate) and, when it needs one, which building block: skill (it uses another skill), connector (it uses a connector) or schedule (runs on its own).

**Step by step.** If the founder asks to be taken through a technique, do one step at a time and stop at every hand-off. Each technique that needs the founder to act marks its steps: **Now** (what you do), **Your turn** (what the founder does; then stop and wait), **Resume** (the sentence that picks it up, in this chat or a new one), **Then** (what follows). At every stop, add one line to `product-info.md`: "Waiting for: [what], since [date]. To resume: Use review-mining to continue [the technique]." When you read a `product-info.md` that has a Waiting for line, start there: ask whether it has come in.

---

## Competitors’ bad reviews, via Apify · research · connector

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

**Step by step:**
1. **Now:** name the current solution, its two main competitors and where their reviews are. With a scraper, give the cost of the run for approval.
2. **Your turn:** approve the scraper run, or (no scraper) copy 50–100 of the 1–2 star reviews into one file, with the site each came from. **Stop.**
3. **Resume:** attach the file (with a scraper, nothing) and say: "continue the bad reviews".
4. **Then:** the analysis above, with the check.

---

## Output and hand-off

Write the Problem section of `pmf/product-info.md` in this format:

- **The what:** [who] has [problem], with numbers: how big, how often, how much it costs, what they resort to now.
- **The why:** why the problem exists: what current solutions offer and why that falls short; the structural gap.

Each line EVIDENCE (source) or HYPOTHESIS. Update `pmf/assumptions.md` and the Evidence table. If you can't write files, output the changed sections as a markdown block for the founder to save. Next: `workaround-mapper` (P3) for how people handle the problem today, then `interview-script` (P4) to turn the research into interview questions.

## Rules (from pmf)

Nothing is evidence until a real person did something. Every number has a source or says GUESS. Every quote is verbatim or says PARAPHRASE. Never send, publish, launch, charge or spend without approval of the exact action. Update product-info.md and assumptions.md after every step. Change one thing per cycle. Interview recordings are personal data: get consent, store them carefully, and don't upload them to tools the interviewee didn't agree to.

---
Part of *Fast-Tracking Product-Market Fit with AI* by Gilles De Clerck (gillesdc.com).
