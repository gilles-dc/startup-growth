---
name: buyer-objections-mapper
description: Find the questions and objections buyers have before they buy, with AI — read sales or interview call transcripts (or competitor reviews when there are no calls yet), group and count what buyers were trying to find out, cross-check each theme with search demand and with what AI assistants answer about the category, and show where buyers ask and nobody answers well. Use when a founder asks what buyers worry about, what almost stopped people buying, which objections a page or ad should answer, or where the positioning opening is. Workshop slide S2. Part of the pmf skills; reads pmf/product-info.md.
---

# Buyer objections (S2) — what do buyers ask before they buy?

Goal: the questions buyers ask when they evaluate options, grouped and counted with quotes, and where nobody answers them well.

## What you need

- **Chat only:** call transcripts or notes the founder attaches, or competitor reviews if there are no calls yet.
- **Paid, optional:** search data from DataForSEO (pay as you go), Ahrefs or Semrush.

## Before you start

Read `pmf/product-info.md` and `pmf/assumptions.md` (also check the project root, or a file attached to the conversation).

**If there is no product-info.md,** offer two routes and let the founder pick: run `pmf` first (seven questions, and every pmf skill reads the file it writes), or go straight on. Straight on: ask these in one message, and say short answers are fine:
1. What is the product, in one sentence, and what will it cost?
2. Who is it for? Role, company type or life situation, and the countries and languages you sell in.
3. What problem does it solve, in your customer's words?
4. What do they use today? Name every competitor, tool or workaround you know.
5. Do you have customer quotes: interview notes, call transcripts, reviews? Attach them.

Label the answers HYPOTHESIS. At the end, output them as a short `product-info.md` for the founder to save.

Each heading says how the technique works (chat · research · build · analyse · simulate) and, when it needs one, which building block: skill (it uses another skill), connector (it uses a connector) or schedule (runs on its own).

**Step by step.** If the founder asks to be taken through a technique, do one step at a time and stop at every hand-off. Each technique that needs the founder to act marks its steps: **Now** (what you do), **Your turn** (what the founder does; then stop and wait), **Resume** (the sentence that picks it up, in this chat or a new one), **Then** (what follows). At every stop, add one line to `product-info.md`: "Waiting for: [what], since [date]. To resume: Use buyer-objections-mapper to continue [the technique]." When you read a `product-info.md` that has a Waiting for line, start there: ask whether it has come in.

---

## Questions buyers ask before buying · research

1. Load call transcripts (or competitor reviews if there are no calls yet).
> What were buyers trying to find out when they evaluated options? Group the questions, count them, quote each.
2. Cross-check each theme with search demand (an SEO connector: DataForSEO, Semrush, Ahrefs) and with what AI assistants currently answer about the category (ask the question yourself and report the answer and its sources).
3. Where buyers ask and nobody answers well is positioning.

Seen at: Docebo, via Kyle Poyar, Growth Unhinged (Oct 2025).

No transcript connector: the founder exports the transcripts from their call recorder (Granola, Fireflies, Otter) or pastes the call notes. No SEO connector: skip the search-demand check and say so, or the founder pastes volumes from any keyword tool they use.

**Step by step:**
1. **Now:** ask whether there are sales or interview calls. If there are none, use competitor reviews and go straight on.
2. **Your turn:** export the transcripts or notes into one folder. **Stop.**
3. **Resume:** attach the files and say: "continue the buyer questions".
4. **Then:** the grouping, the cross-check and the positioning above.

---

## Output and hand-off

Write the grouped questions, with counts, quotes and the search-demand and AI-answer cross-check, to `pmf/buyer-questions.md`; update `pmf/product-info.md` and `pmf/assumptions.md` where the questions change a line. If you can't write files, output the changed sections as a markdown block for the founder to save. Next: `value-proposition-generator` (S4), whose headers answer the main objection, and `competitive-analysis` (S1), whose comparison table traces its rows to the buyer questions.

## Rules (from pmf)

Nothing is evidence until a real person did something. Every number has a source or says GUESS. Every quote is verbatim or says PARAPHRASE. Never send, publish, launch, charge or spend without approval of the exact action. Update product-info.md and assumptions.md after every step. Change one thing per cycle.

---
Part of *Fast-Tracking Product-Market Fit with AI* by Gilles De Clerck (gillesdc.com).
