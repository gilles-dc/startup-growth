---
name: pmf-survey
description: Run and analyse Sean Ellis's product-market fit survey with AI, read the way Superhuman did — split by segment, find who would be very disappointed (the real ICP), what they'd miss (the positioning) and what holds the near-fans back (the roadmap), then use 40% very disappointed per segment as the gate to grow. Under about 40 active users it sends the founder to interviews instead. Also reads all open feedback at once and groups customers into types from their support emails. Use once a product has users, for "do we have product-market fit", "PMF survey", "very disappointed", "Sean Ellis test", "Superhuman PMF engine". Workshop slide PMF1. Part of the pmf skills; reads pmf/product-info.md.
---

# The PMF survey (PMF1) — who would miss it, and why?

Goal: know who would miss the product most, what they'd miss, and what to build so the almost-fans become fans. Then, per segment, whether it's ready to grow.

## What you need

- **Chat only:** Read all the feedback (paste the answers); The PMF survey and Customer types from their emails from a file export or done by hand.
- **Free:** Tally (The PMF survey), an email connector (Customer types from their emails).

## Before you start

Read `pmf/product-info.md` and `pmf/assumptions.md` (also check the project root, or a file attached to the conversation). If they're there, ask: how many active users or customers, how long they've had access, what data is available (survey answers, analytics connector, exports).

**If there is no product-info.md,** offer two routes and let the founder pick: run `pmf` first (seven questions, and every pmf skill reads the file it writes), or go straight on. Straight on: ask these in one message, and say short answers are fine:
1. What is the product, in one sentence, and what does it cost?
2. Which kinds of customer use it? (Type, size, use case: the lines to split every result by.)
3. How many active users or customers, and since when?
4. What data do you have: an analytics tool, Stripe, survey answers, a spreadsheet export?

Label the answers HYPOTHESIS. At the end, output them as a short `product-info.md` for the founder to save.

Each heading says how the technique works (chat · research · build · analyse · simulate) and, when it needs one, which building block: skill (it uses another skill), connector (it uses a connector) or schedule (runs on its own).

**Step by step.** If the founder asks to be taken through a technique, do one step at a time and stop at every hand-off. Each technique that needs the founder to act marks its steps: **Now** (what you do), **Your turn** (what the founder does; then stop and wait), **Resume** (the sentence that picks it up, in this chat or a new one), **Then** (what follows). At every stop, add one line to `product-info.md`: "Waiting for: [what], since [date]. To resume: Use pmf-survey to continue [the technique]." When you read a `product-info.md` that has a Waiting for line, start there: ask whether it has come in.

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

## The PMF survey · analyse · connector

Sean Ellis's question, read the way Superhuman did. The point isn't a score. It's to learn who your best users are, what they love, and what to build so the almost-fans become fans. The 40% comes last, as the gate to grow.

**First: are there enough users?** A share only means something from about 40 answers by active users ("you start to get directionally correct results around 40 respondents", Rahul Vohra). With fewer than about 40 active users, don't run the survey read: talk to them. Use `interview-script` (P4) with the people who use it most: walk through the last time they used it, what they'd do without it, what they'd miss, and what almost stopped them. Same goal, by conversation, and no percentages.

Survey only people who used the product at least twice in the last two weeks.
1. How would you feel if you could no longer use [product]? — very disappointed · somewhat disappointed · not disappointed
2. What type of people do you think would most benefit from [product]?
3. What is the main benefit you receive from [product]?
4. How can we improve [product] for you?

Create it with a forms connector (Tally, Typeform) or as an in-app survey (PostHog), **as a draft for the founder to publish**.

No forms connector: output the survey ready to paste into any form tool (Google Forms, Tally, Typeform, Microsoft Forms): question 1 as multiple choice with the three answers in that order, questions 2–4 as open text. Only if the founder's own data can't say who is active or which segment someone is in, add two multiple-choice questions at the top: "How many times have you used [product] in the last two weeks?" (0 · 1 · 2–5 · more than 5) and one for the segment (customer type, size or use case). Filter and split on them in the analysis.

**Step by step:**
1. **Now:** agree who counts as active and how to reach them. Under about 40 active users: say so and switch to interviews. Otherwise write the survey (a draft in the forms tool, or the paste-ready text) and the invitation email, for approval.
2. **Your turn:** publish the survey and send it to the active users. Wait for about 40 answers. **Stop.**
3. **Resume:** attach the export (CSV or spreadsheet) and say: "continue the PMF survey". With the forms connector, read the answers directly. Fewer than about 40 answers came back: don't compute shares; read the answers as interview notes and suggest calls with the very disappointed.
4. **Then:** the analysis and the report below.

**Analysis: the engine (Superhuman's method):**
> 1. Split by segment first: customer type, size, use case, whatever the ICP lines in product-info.md vary on. Give each segment its count. Never read one blended number: it hides the segment that loves the product.
> 2. The very disappointed: who they are (role, company, use case) and the top 3 main benefits they name, with quotes. That group is the real ICP; that benefit is the positioning. Double down on it.
> 3. The somewhat disappointed who name the same top benefit: what holds them back? Group and quote. That's the roadmap: build it to turn them into fans.
> 4. Set aside the not disappointed, and the somewhat disappointed who name another benefit: they wouldn't become fans.
> 5. If the group in step 3 is mostly a different segment from step 2, its roadmap serves another customer. Flag it as a choice about who the customer is; don't put it on the roadmap.
> 6. The gate, per segment: the share who'd be very disappointed. **Under 40%: keep iterating** on steps 2 and 3, and don't scale acquisition for that segment yet; the product isn't ready for it. **Over 40%: that segment is ready to grow.** (Sean Ellis, from nearly 100 startups: above 40%, growth tended to work; below it, they struggled.) Never apply the gate to everyone together.

Re-run it every quarter and track each segment's share: Superhuman went from 22% to 58% by building for the groups in steps 2 and 3 (Rahul Vohra). Say how many answers each share rests on.

**Report it as a walk-through, step by step, so the numbers explain each other:** (1) who was sent the survey and how many answered; (2) who counts as active, why (someone who barely used it can't judge losing it), and how many answers that leaves: the base for every share; (3) question 1 across the base, stated plainly, without a verdict; (4) the split of the base by segment, with counts that add up to it, and one line on what doesn't separate them; (5) question 3 to the very disappointed: what they love, the promise; (6) question 4 to the somewhat disappointed in that segment: what to build next; (7) the gate: which segment is over 40% and ready to grow, which keep iterating. End with one "so" line. Every count names what it is a count of.

**Check:** if the "very disappointed" respondents are all different kinds of people, there is no ICP yet: interview them before building anything.

## More techniques

### Read all the feedback · analyse

Every open-ended answer at once: survey comments, NPS, support tickets, app reviews, sales notes.
> Read all of it. Themes · counts · 2 verbatim quotes per theme · what differs by segment · what changed over time. Then: what are people trying to do when they write to us?

Use a deep research run or code for large files, not a quick chat; a shallow pass returns keyword counts. Check the counts against the file and verify five quotes. (Seen at: Zach Leach, Gamma, How I AI, Jun 2025: 550 responses in 12+ languages, about 19 minutes.)

**Step by step:**
1. **Now:** ask which sources exist and say how to export each (survey tool: CSV; help desk: CSV; app reviews: copy or a scraper; sales notes: the CRM's export).
2. **Your turn:** export them into one folder. **Stop.**
3. **Resume:** attach the files and say: "continue the feedback read".
4. **Then:** the read above, with the checks.

### Customer types from their emails · analyse · connector

With access to the support inbox and community forum (email connector, exported files):
> Read everything. Group customers into archetypes; mark promoters and detractors; for each archetype, what were they trying to do when they wrote?

The archetype that loves the product is the ICP to sell to. (Seen at: Dan Shipper, Every, Jul 2025: 1,500 support emails and 500 forum posts for Cora.) Customer emails are personal data: keep the analysis inside tools the founder controls.

No email connector: export the inbox (help desks such as Intercom, Zendesk and Help Scout export to CSV; Gmail through Google Takeout) and copy the forum posts into one file. A few hundred messages pasted into the chat also work.

**Step by step:**
1. **Now:** say what to export and from where.
2. **Your turn:** export it, and take out anything that shouldn't leave the founder's tools. **Stop.**
3. **Resume:** attach the files and say: "continue the customer types".
4. **Then:** the archetypes above.

---

## Output and hand-off

Write each segment's share, which segment passed the gate, and the level to `pmf/product-info.md` (Evidence), update the ICP if the "very disappointed" group says so, update `pmf/assumptions.md`. If you can't write files, output the changed sections as a markdown block for the founder to save. Next: `retention-audit` (PMF2) to see whether they keep coming back, `why-people-churn` (PMF3) to hear from the ones who leave, then `pivot-or-persevere` (I2) and `weekly-product-bets` (I3) to decide what to optimise at this level.

## Rules (from pmf)

Nothing is evidence until a real person did something. Every number has a source or says GUESS. Every quote is verbatim or says PARAPHRASE. Never send, publish, launch, charge or spend without approval of the exact action. Update product-info.md and assumptions.md after every step. Change one thing per cycle.

---
Part of *Fast-Tracking Product-Market Fit with AI* by Gilles De Clerck (gillesdc.com).
