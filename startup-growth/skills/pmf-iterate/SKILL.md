---
name: pmf-iterate
description: Turn evidence into decisions with AI — update the assumption board from interviews and tests, write a pivot-or-persevere memo, generate one-change pivot options, check whether the team really knows its customer, and set up recurring agents (discovery agent, Monday bets, competitor watch). Use after interviews or tests, when deciding what to change, or when setting up automation for the validation loop. Part of the pmf-* set.
---

# PMF · Iterate — what changes?

Goal: evidence in, one decision out, every cycle. Then make the loop run without the founder having to remember it.

## What you need

- **Chat only:** A, B, C.
- **Runs on its own:** Claude Cowork scheduled tasks or Claude Code routines (D, E, F); Slack for the digests.
- **Paid, optional:** Firecrawl monitor (F).

## Before you start

Read `pmf/product-info.md`, `pmf/assumptions.md`, `pmf/synthesis.md` and `pmf/tests/` if they exist.

Each heading says how the technique works (chat · research · build · analyse · simulate) and, when it needs one, which building block: teach (a skill), connect (a connector) or schedule (runs on its own).

---

## A. Update the assumption board · chat

> Here is my assumption table: [assumptions.md]. Here is this cycle's evidence: [synthesis, test results]. For each assumption, propose a status change (verified / invalidated / mixed / still untested) only if the evidence supports it, with the exact quote or number. Don't change anything without one. List the assumptions nobody said anything about.

Show the proposed changes as a diff. **The founder approves each one.** Never update the board on your own. Flag any assumption unchanged for two weeks: it isn't being tested.

## B. Quiz me · chat · 5 min

> You have my customer interviews: [transcripts / synthesis]. Quiz me: 10 questions about my customer: their day, their tools, what they pay for, the words they use, what they said word for word. Don't give hints. At the end, score me and show what I got wrong, with the quote.

Run it with every founder on the team. Under 7/10: reread the transcripts before the next call. If the AI knows the customer better than the team does, the team has learning debt (Steve Blank's term): any founder should be able to explain the customer, their workflow, the evidence, the economics and the contradictions without opening a laptop.

## C. Pivot memo · chat · teach

If a pivot-decision skill is installed (product-on-purpose/pm-skills `iterate-pivot-decision`, MaxKmet/idea-validation-agents `pivot-engine`), use it to write the memo. Otherwise write `pmf/decisions/[date].md`:
- what we believed · what we found (verified quotes, test numbers) · what that means
- options: persevere · iterate (one change) · pivot
- the recommendation and the evidence it rests on

**Five pivots, one change each:**
> Here's what we believed: persona [ ] · problem [ ] · promise [ ] · product [ ]. Here's what we learned: [top findings + verified quotes]. Propose 5 pivots. Each changes exactly one of persona, problem, promise or product, and is based on a specific quote. For each: the cheapest test we could run this week to check it.

A pivot that isn't tied to a quote is a new idea. Real pivots are often bigger than founders expect: Lattice kept the customer and changed problem, value and product; Plaid kept the product and changed everything else (First Round Capital, PMF Method).

**Rule:** one change per cycle, on purpose. Book next week's conversations before building this week's version.

## D. Discovery agent · analyse · schedule

For D, E and F: only automate a method that already works by hand; automating a bad process makes it fail faster. Set up with Claude Cowork scheduled tasks or Claude Code routines (the founder approves the schedule and the connectors). Agents write drafts and digests; they never send, launch or spend.

Every new transcript updates the evidence, without the founder opening anything. Trigger: a new transcript (Granola, a Drive folder) or a daily schedule.

> When a new transcript appears in [Granola / folder]: analyse it with the per-interview template from pmf-problem Q, verify every quote, append to pmf/interviews/, and propose assumption-board changes with quotes. Post a 5-line summary to [Slack / doc].
(Seen at: Caitlin Sullivan on Aakash Gupta's podcast: 1 survey + 5 transcripts in under 2 minutes.)

## E. Monday bets · analyse · schedule

Every Monday, the agent reads the week's data and proposes what to try next.

> Every Monday 8:00: read last week's product metrics [analytics connector], new interview notes, test results and [Slack channel]. Propose 3–5 specific bets, each with the evidence behind it and the test to run. Post before the team meeting.
(Seen at: Charles Cook, PostHog, Apr 2026 — he acts on about one in five; Jenny Wen, Anthropic, Mar 2026 — "3 vetted product ideas" every Monday.)

## F. Competitor watch · research · schedule

The agent checks competitors on a schedule and only reports what changed.

> Compare each competitor in pmf/competitors.md against its last snapshot: pricing, positioning, features, ads. Report only material changes, with links. Update the snapshots.
(Tools: Firecrawl monitor, changedetection.io, a scraping connector. Seen at: deanpeters/Product-Manager-Skills `competitive-intel-watch`.)

---

## Output and hand-off

Updated `pmf/assumptions.md`, a decision memo in `pmf/decisions/`, updated `pmf/product-info.md`. Next: back to the stage the decision points to, with one change: usually `pmf-problem` for more conversations, or `pmf-mvp` and `pmf-test` for the next market test.

## Rules (from pmf-loop)

Nothing is evidence until a real person did something. Every number has a source or says GUESS. Every quote is verbatim or says PARAPHRASE. Never send, publish, launch, charge or spend without approval of the exact action. Update product-info.md and assumptions.md after every step. Change one thing per cycle.

---
Part of *Fast-Tracking Product-Market Fit with AI* by Gilles De Clerck (gillesdc.com).
