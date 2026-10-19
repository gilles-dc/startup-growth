---
name: why-people-churn
description: Find out why customers leave — ask everyone who cancels one question in the app's cancel flow (by email only when there is no app, set up as an n8n, Zapier or Make automation or sent by hand), then group the replies every month into themes with counts and quotes, each labelled fixable for the ICP, fixable for another segment, wrong customer, or neither, and know which level of fit you're at. Use for "churn", "why do people cancel", "exit survey", "cancellation reasons", "customers leaving". Workshop slide PMF3. Part of the pmf skills; reads pmf/product-info.md.
---

# Why people churn (PMF3) — why do they leave?

Goal: know why people stop paying or stop using it, which of those reasons belong on the roadmap and which say something about who the customer is, and what to do next at the level of fit the startup is at.

## What you need

- **Chat only:** Ask everyone who cancels why from a file export of the answers.
- **Free:** the product's in-app survey (PostHog surveys, Tally) or the billing tool's cancel flow (Stripe customer portal); without an app, n8n's self-hosted template for email.
- **Paid, optional:** Typeform, Chargebee or Paddle cancel surveys; Zapier or Make instead of n8n.

## Before you start

Read `pmf/product-info.md` and `pmf/assumptions.md` (also check the project root, or a file attached to the conversation). If they're there, ask: how many active users or customers, how long they've had access, what data is available (Stripe, an in-app survey tool, exports).

**If there is no product-info.md,** offer two routes and let the founder pick: run `pmf` first (seven questions, and every pmf skill reads the file it writes), or go straight on. Straight on: ask these in one message, and say short answers are fine:
1. What is the product, in one sentence, and what does it cost?
2. Which kinds of customer use it? (Type, size, use case: the lines to split every result by.)
3. What does a customer do that means they got value? A login doesn't count.
4. How many active users or customers, and since when?
5. What data do you have: an analytics tool, Stripe, survey answers, a spreadsheet export?

Label the answers HYPOTHESIS. At the end, output them as a short `product-info.md` for the founder to save.

Each heading says how the technique works (chat · research · build · analyse · simulate) and, when it needs one, which building block: skill (it uses another skill), connector (it uses a connector) or schedule (runs on its own).

**Step by step.** If the founder asks to be taken through a technique, do one step at a time and stop at every hand-off. Each technique that needs the founder to act marks its steps: **Now** (what you do), **Your turn** (what the founder does; then stop and wait), **Resume** (the sentence that picks it up, in this chat or a new one), **Then** (what follows). At every stop, add one line to `product-info.md`: "Waiting for: [what], since [date]. To resume: Use why-people-churn to continue [the technique]." When you read a `product-info.md` that has a Waiting for line, start there: ask whether it has come in.

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

## Ask everyone who cancels why · analyse · schedule

One question, asked **in the app, in the cancel flow**, right after the person clicks cancel and before it's confirmed:
"What were you hoping it would do that it didn't?"

One open-text box, optional, with cancelling still one click away. Asked at that moment, most people answer; an email afterwards mostly goes unanswered. Build it with the in-app survey tool the product already has (PostHog surveys, Tally or Typeform embedded, or a plain form in the cancel screen), or in the billing tool's own cancel flow (Stripe's customer portal can ask for a cancellation reason; Chargebee and Paddle have cancel surveys). For B2B accounts that cancel through a contract, ask it in the app when an admin cancels or turns off renewal. Store each answer with the customer, their segment and months active.

**Only if there is no app or cancel screen** (a service, an invoice-based contract): send the same question by email within a day of each cancellation, from the founder's own address. Set up as an automation (n8n has a ready template for Stripe cancellation → exit question → Claude classification → sheet; or a Zapier/Make flow), or by hand, keeping the replies in one sheet (date, customer, segment, months active, reply). Emails are drafted or sent from the founder's own tool with their approval of the template. Expect far fewer answers.

People who never paid (a free trial that simply ended) aren't asked in the cancel flow; to hear from them, use `retention-audit` (PMF2) on their behaviour, or interview a few.

**Step by step:**
1. **Now:** write the question and the cancel-flow setup for the founder's survey or billing tool (or, without an app, the email and the automation), for approval.
2. **Your turn:** add it to the cancel flow and switch it on. Wait a month. **Stop.**
3. **Resume:** attach the export of the answers (with a connector, nothing) and say: "continue the cancel reasons". Every month after, the same sentence.
4. **Then:** the monthly grouping below. Report how many answered out of how many cancelled, and make the theme counts add up to the answers (an "other" row if needed).

Monthly:
> Group these replies into themes. For each: count, 2 quotes, the customer's segment and months active, and one of four labels: **fixable for our ICP** · **fixable, but for another segment** · **wrong customer** · **neither** (closing down, budget cut).

A "wrong customer" answer updates the ICP in `product-info.md`. A fixable one for the ICP goes on the roadmap. "Fixable, but for another segment" is a question about who the customer is, not a roadmap item: count how many cancellations it covers before building it.

---

## Output and hand-off

Write the grouped cancel reasons, with their labels and counts, and the level to `pmf/product-info.md` (Evidence), update the ICP when a "wrong customer" answer says so, update `pmf/assumptions.md`. If you can't write files, output the changed sections as a markdown block for the founder to save. Next: `retention-audit` (PMF2) to join the cancel reasons to the leavers on the retention curve, then `pivot-or-persevere` (I2) and `weekly-product-bets` (I3) to decide what to optimise at this level.

## Rules (from pmf)

Nothing is evidence until a real person did something. Every number has a source or says GUESS. Every quote is verbatim or says PARAPHRASE. Never send, publish, launch, charge or spend without approval of the exact action. Update product-info.md and assumptions.md after every step. Change one thing per cycle.

---
Part of *Fast-Tracking Product-Market Fit with AI* by Gilles De Clerck (gillesdc.com).
