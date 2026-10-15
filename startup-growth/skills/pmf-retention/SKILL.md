---
name: pmf-retention
description: Measure whether a startup has product-market fit with AI — run and analyse the Sean Ellis 40% survey with Superhuman-style segmentation, build cohort retention from analytics or a CSV, read all open feedback at once, cluster churn reasons, and know which level of fit you're at and what to optimise. Use once a product has users. Part of the pmf-* set.
---

# PMF · Retention — do they stay?

Goal: know whether people use it regularly and keep paying, and what to do next at the level of fit the startup is actually at.

## What you need

- **Chat only:** A (paste the answers), F.
- **Free:** PostHog, Mixpanel or Amplitude free tiers (C), Tally (B), Stripe (E), n8n's self-hosted template (E), an email connector (D).
- **Paid, optional:** Zapier or Make instead of n8n (E).

## Before you start

Read `pmf/product-info.md` and `pmf/assumptions.md`. Ask: how many active users or customers, how long they've had access, what data is available (analytics connector, Stripe, exports).

## Where are you?

| Level | Customers | Optimise | Ignore for now |
|---|---|---|---|
| L1 nascent | 3–5 | satisfaction | efficiency |
| L2 developing | 5–25 | demand | efficiency |
| L3 strong | 25–100 | efficiency | — |
| L4 extreme | 100+ | the next market | — |

Source: Todd Jackson, First Round Capital, PMF Method. Most early teams think they're L2 and are L1. Satisfaction first: five customers who'd be upset if the product disappeared.

A customer who paid for three subscription cycles is product-market fit with that one customer. A second one is fit with two.

Each heading says how the technique works (chat · research · build · analyse · simulate) and, when it needs one, which building block: skill (it uses another skill), connector (it uses a connector) or schedule (runs on its own).

---

## A. Read all the feedback · analyse

Every open-ended answer at once: survey comments, NPS, support tickets, app reviews, sales notes.
> Read all of it. Themes · counts · 2 verbatim quotes per theme · what differs by segment · what changed over time. Then: what are people trying to do when they write to us?

Use a deep research run or code for large files, not a quick chat; a shallow pass returns keyword counts. Check the counts against the file and verify five quotes. (Seen at: Zach Leach, Gamma, How I AI, Jun 2025: 550 responses in 12+ languages, about 19 minutes.)

## B. The 40% survey · analyse · connector

Survey only people who used the product at least twice in the last two weeks.
1. How would you feel if you could no longer use [product]? — very disappointed · somewhat disappointed · not disappointed
2. What type of people do you think would most benefit from [product]?
3. What is the main benefit you receive from [product]?
4. How can we improve [product] for you?

Create it with a forms connector (Tally, Typeform) or as an in-app survey (PostHog), **as a draft for the founder to publish**. Benchmark: 40% "very disappointed" (Sean Ellis, from nearly 100 startups).

**Analysis (Superhuman's method):**
> 1. Filter to "very disappointed". Describe who they are (role, company, use case) and the top 3 main benefits they name, with quotes. That group is the real ICP; that benefit is the positioning.
> 2. Filter "somewhat disappointed" to those who name the same top benefit. What do they say holds them back? Group and quote. That's the roadmap.
> 3. Ignore "not disappointed".

Superhuman went from 22% to 58% very disappointed by building for the first group and the second (Rahul Vohra). Small samples are directional; say how many responses the percentage rests on.

**Check:** if the "very disappointed" respondents are all different kinds of people, there is no ICP yet.

## C. Retention by asking · analyse · connector

With an analytics connector (PostHog, Mixpanel, Amplitude, GA4):
> Weekly retention by sign-up cohort, where active means [the event that means they got value, e.g. "created a report"]. Logging in doesn't count. Does any cohort's curve flatten, and after which week? Are newer cohorts retaining better than older ones?

Without one: ask for a CSV of sign-ups and events, compute the cohort table and chart with code.

A curve that flattens above zero is the signal. A curve that keeps falling to zero is a leaky bucket, whatever the sign-up numbers say: Clubhouse had 9.6M downloads in February 2021 and 922k in April.

## D. Customer archetypes · analyse · connector

With access to the support inbox and community forum (email connector, exported files):
> Read everything. Group customers into archetypes; mark promoters and detractors; for each archetype, what were they trying to do when they wrote?

The archetype that loves the product is the ICP to sell to. (Seen at: Dan Shipper, Every, Jul 2025: 1,500 support emails and 500 forum posts for Cora.) Customer emails are personal data: keep the analysis inside tools the founder controls.

## E. Churn agent · analyse · schedule

On every cancellation (Stripe) or 30 days of inactivity, one question:
"What were you hoping it would do that it didn't?"

Set up as an automation (n8n has a ready template for Stripe cancellation → exit question → Claude classification → sheet; or a Zapier/Make flow; or a scheduled task reading replies). Emails are drafted or sent from the founder's own tool with their approval of the template.

Monthly:
> Group these replies into themes. For each: count, 2 quotes, and whether it's something we could fix or a sign they were the wrong customer.

A "wrong customer" answer updates the ICP in `product-info.md`. A fixable one goes on the roadmap.

## F. The cost of keeping them · analyse

AI products have a variable cost per use. For each customer segment: what does one customer cost per month to serve (model and infrastructure), what do they pay, what's the margin? Fit that loses money on every active user isn't fit yet.

---

## Output and hand-off

Write the PMF score, retention findings and level to `pmf/product-info.md` (Evidence), update the ICP if the "very disappointed" group says so, update `pmf/assumptions.md`. Next: `pmf-iterate` to decide what to optimise at this level.

## Rules (from pmf-loop)

Nothing is evidence until a real person did something. Every number has a source or says GUESS. Every quote is verbatim or says PARAPHRASE. Never send, publish, launch, charge or spend without approval of the exact action. Update product-info.md and assumptions.md after every step. Change one thing per cycle.

---
Part of *Fast-Tracking Product-Market Fit with AI* by Gilles De Clerck (gillesdc.com).
