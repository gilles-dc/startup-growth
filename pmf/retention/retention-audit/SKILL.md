---
name: retention-audit
description: Measure retention with AI — build cohort retention curves from PostHog, Mixpanel, Amplitude, GA4 or a CSV, check whether the curve flattens or leaks to zero, split by segment, then split the people who stay from the people who leave, find what each group has in common and why, on a one-page dashboard. Also works out what each customer segment costs to serve against what it pays, and which level of fit you're at. Use once a product has users, for "retention curve", "cohort analysis", "do people come back", "leaky bucket", "are we retaining". Workshop slide PMF2. Part of the pmf skills; reads pmf/product-info.md.
---

# Retention audit (PMF2) — do they keep coming back?

Goal: know whether people use it regularly and keep paying, and what to do next at the level of fit the startup is at.

## What you need

- **Chat only:** The cost of keeping them; Ask your analytics about retention from a file export or done by hand.
- **Free:** PostHog, Mixpanel or Amplitude free tiers (Ask your analytics about retention).

## Before you start

Read `pmf/product-info.md` and `pmf/assumptions.md` (also check the project root, or a file attached to the conversation). If they're there, ask: how many active users or customers, how long they've had access, what data is available (analytics connector, Stripe, exports).

**If there is no product-info.md,** offer two routes and let the founder pick: run `pmf` first (seven questions, and every pmf skill reads the file it writes), or go straight on. Straight on: ask these in one message, and say short answers are fine:
1. What is the product, in one sentence, and what does it cost?
2. Which kinds of customer use it? (Type, size, use case: the lines to split every result by.)
3. What does a customer do that means they got value? A login doesn't count.
4. How many active users or customers, and since when?
5. What data do you have: an analytics tool, Stripe, survey answers, a spreadsheet export?

Label the answers HYPOTHESIS. At the end, output them as a short `product-info.md` for the founder to save.

Each heading says how the technique works (chat · research · build · analyse · simulate) and, when it needs one, which building block: skill (it uses another skill), connector (it uses a connector) or schedule (runs on its own).

**Step by step.** If the founder asks to be taken through a technique, do one step at a time and stop at every hand-off. Each technique that needs the founder to act marks its steps: **Now** (what you do), **Your turn** (what the founder does; then stop and wait), **Resume** (the sentence that picks it up, in this chat or a new one), **Then** (what follows). At every stop, add one line to `product-info.md`: "Waiting for: [what], since [date]. To resume: Use retention-audit to continue [the technique]." When you read a `product-info.md` that has a Waiting for line, start there: ask whether it has come in.

## Where are you?

| Level | Customers | Optimise | Ignore for now |
|---|---|---|---|
| L1 nascent | 3–5 | satisfaction | efficiency |
| L2 developing | 5–25 | demand | efficiency |
| L3 strong | 25–100 | efficiency | — |
| L4 extreme | 100+ | the next market | — |

Source: Todd Jackson, First Round Capital, PMF Method. Most early teams think they're L2 and are L1. Satisfaction first: five customers who'd be upset if the product disappeared.

A customer who paid for three subscription cycles is product-market fit with that one customer. A second one is fit with two.

---

## Ask your analytics about retention · analyse · connector

With an analytics connector (PostHog, Mixpanel, Amplitude, GA4):
> Weekly retention by sign-up cohort, where active means [the event that means they got value, e.g. "created a report"]. Logging in doesn't count. Does any cohort's curve flatten, and after which week? Are newer cohorts retaining better than older ones? Then split the same curves by segment (customer type, size, plan): a blended curve can hide one segment that stays and another that leaves.

Without one: ask for a CSV of sign-ups and events, compute the cohort table and chart with code. Name the columns: one row per user (user id, sign-up date, segment) and one row per value action (user id, date). The analytics tool's export gives it, or one database query by whoever built the product.

**Step by step:**
1. **Now:** agree the value action and the window (below). With a connector, pull the data and go straight on.
2. **Your turn (no connector):** export the CSV with those columns. **Stop.**
3. **Resume:** attach the CSV and say: "continue the retention curve".
4. **Then:** the curve, the stayers and leavers, the dashboard.

Pick the window to match how often the value happens: weekly for a weekly report, 4-week blocks for something done every month or so (a haircut, an invoice run). "Flattens" means the share active stays within a few points for three windows or more. Cohorts younger than that can't show it yet; say so instead of guessing.

A curve that flattens above zero is the signal. A curve that keeps falling to zero is a leaky bucket, whatever the sign-up numbers say: Clubhouse had 9.6M downloads in February 2021 and 922k in April.

**Always draw the curve.** The first thing to show is the retention curve itself, as a chart: weeks (or months) since sign-up across, the share still doing the value action up, one line overall and one per segment, with the moments that cut it marked (the trial ending, the pilot ending). A table of segment shares is no substitute.

**The chart and the table must match.** Plot the same segments the table lists, with the same measure, and give the table the chart's own points (week 0, the week the trial ends, the last week). Use segments that add up to all users, name them the same way everywhere, and if you show everyone together, call it "All users (the four together)", dashed. Never mix a weekly share on the chart with a monthly or block share in the table.

**Then split the people who stay from the people who leave, and find out why.** This is what the curve is for:
1. **Define both groups from the curve:** stayers did the value action in most windows late on (e.g. 2+ of weeks 8–11); leavers did it early and then stopped. Only count people observed long enough to be either.
2. **What each group has in common:** compare them on everything the data holds (segment, device, plan, source, country, what they set up in the first week). Show each trait as stayers % against leavers %. The traits with the biggest gap describe who the product is for; the ones with none (often city, age, gender) are worth saying too.
3. **Join what they said:** the survey answers (`pmf-survey`, PMF1) of stayers and leavers, and the cancel reasons (`why-people-churn`, PMF3) of the leavers, with counts and labels.
4. **Ask next:** three questions for the interviews, one per group that matters (stayers: what made it worth it; leavers who match the ICP: what happened; the nearest segment: what would bring them in).

Put it on one page as a dashboard: who they are, what the stayers say, why the leavers left, what to ask next. Every number is a count of people; small groups are directions, and say so.

## More techniques

### The cost of keeping them · analyse

AI products have a variable cost per use. For each customer segment: what does one customer cost per month to serve (model and infrastructure), what do they pay, what's the margin? Fit that loses money on every active user isn't fit yet.

No numbers to hand: ask for last month's model and hosting invoices and the number of active customers that month, and divide.

---

## Output and hand-off

Write the retention findings, the cost and margin per segment, and the level to `pmf/product-info.md` (Evidence), update the ICP if the stayers say so, update `pmf/assumptions.md`. If you can't write files, output the changed sections as a markdown block for the founder to save. Next: `pmf-survey` (PMF1) if the stayers have not been surveyed yet, `why-people-churn` (PMF3) to hear from the leavers, then `pivot-or-persevere` (I2) and `weekly-product-bets` (I3) to decide what to optimise at this level.

## Rules (from pmf)

Nothing is evidence until a real person did something. Every number has a source or says GUESS. Every quote is verbatim or says PARAPHRASE. Never send, publish, launch, charge or spend without approval of the exact action. Update product-info.md and assumptions.md after every step. Change one thing per cycle.

---
Part of *Fast-Tracking Product-Market Fit with AI* by Gilles De Clerck (gillesdc.com).
