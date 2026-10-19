---
name: pivot-or-persevere
description: Lift a startup's head up from the work with AI. Lists everything the plan rests on that is still an assumption, sets each against the evidence so far, gives each a verdict (verified, open or pivot) and names the test that turns each open one into an answer, prioritised, as one table in a pivot-or-persevere memo with the decision under it. Also proposes five pivots that each change exactly one of customer, problem, value proposition, product or price, each tied to a quote. Also updates the assumption board from interviews and tests, change by change, for the founder to approve. Use after interviews or a market test, or for "should we pivot?", "what did we learn?", "update my assumption board". Workshop slide I2. Part of the pmf skills; reads pmf/product-info.md.
---

# Pivot or persevere (I2) — what changes?

Goal: know what you know, what you don't yet, and what to test next. Evidence in, one decision out, every cycle.

## What you need

- **Chat only:** Pivot-or-persevere memo; Five pivots, one change each; Update the assumption board.
- **Free, optional:** a pivot-decision skill, if one is installed (Pivot-or-persevere memo).

## Before you start

Read `pmf/product-info.md`, `pmf/assumptions.md`, `pmf/synthesis.md` and `pmf/tests/` if they exist (also check the project root, or a file attached to the conversation).

**If there is no product-info.md,** offer two routes and let the founder pick: run `pmf` first (seven questions, and every pmf skill reads the file it writes), or go straight on. Straight on: ask these in one message, and say short answers are fine:
1. What is the product, in one sentence, and who is it for?
2. What did you believe at the start, one line each: the customer, the problem, the value proposition, the product, the price?
3. What have you done since: how many interviews, which tests, which numbers? Attach the transcripts, notes or results you have.
4. What decision are you facing right now?

Label the answers HYPOTHESIS. Answer 2 is the starting assumption board for the memo and for Update the assumption board. At the end, output them as a short `product-info.md` for the founder to save.

Each heading says how the technique works (chat · research · build · analyse · simulate) and, when it needs one, which building block: skill (it uses another skill), connector (it uses a connector) or schedule (runs on its own).

---

## Pivot-or-persevere memo · chat · skill

Lift your head up from the work. Most of what a team builds on is still an assumption: something it believes but hasn't seen a real person confirm. The whole point of the pmf skills is to turn assumptions into answers; this memo checks where you stand and tells you what to test next.

1. **List everything the plan rests on.** From `assumptions.md`, `product-info.md` and this cycle's work, write each belief as a plain statement someone could prove wrong ("Sleep, blood and supplements in one place is the reason to buy"), never a slogan. Tag each with its **dimension**, so the founder sees what a pivot would change: **customer** (who, and who buys), **problem**, **value proposition**, **product**, **price** (and business model), **competition**.
2. **Set each against the evidence so far.** Name the source in words, with the skill code after it ("bad reviews, P2"; "the test page week, T3"). Use the strongest evidence for that dimension: a value proposition is answered by the market test (`value-proposition-test` (T3)) before reviews or posts. Mark anything resting on invented or role-played data as synthetic.
3. **Give each a verdict:**
   - **verified**: the evidence answers it. Keep it on the list: knowing what you know matters as much as knowing what you don't. Next step: nothing to test; build on it.
   - **open**: not settled yet. Next step: the test that turns it into an answer.
   - **pivot**: the evidence goes against it. Next step: change that one dimension, and what to change it to.
4. **For every open row, name the test** in plain words: the method (interviews, a test page week, the reply-rate test, doing it by hand for the first paying customers, a monthly competitor check), what you ask or measure, and the pass line, set before it runs ("Interviews: ask 10 customers how many private blood tests they paid for last year. Verified if 6 of 10 had two or more"). Never shorthand like "yes = 3".
5. **Prioritise.** Order the open rows by how much of the plan falls if the assumption is wrong, then by how cheap the test is. The top two or three are this cycle's work.
6. **Decide.** Persevere if nothing is pivot. If one or more rows are pivot, change one dimension this cycle and say which pivot comes next.

If a pivot-decision skill is installed (product-on-purpose/pm-skills `iterate-pivot-decision`, MaxKmet/idea-validation-agents `pivot-engine`), use it for the reasoning; keep this layout. Write the memo to `pmf/decisions/[date].md` as one table, one row per assumption: **dimension** · **the assumption** · **evidence so far** (with its source) · **verdict** (verified, open, pivot) · **next step**. Under the table, one line: the decision, what is verified, how many are open.

**Rule:** one change per cycle, on purpose. Book next week's conversations before building this week's version.

## More techniques

### Five pivots, one change each · chat

When a row comes back pivot and the founder wants options:
> Here's what we believed: customer [ ] · problem [ ] · value proposition [ ] · product [ ] · price [ ]. Here's what we learned: [top findings + verified quotes]. Propose 5 pivots. Each changes exactly one of customer, problem, value proposition, product or price, and is based on a specific quote. For each: the cheapest test we could run this week to check it.

A pivot that isn't tied to a quote is a new idea. Real pivots are often bigger than founders expect: Lattice kept the customer and changed problem, value and product; Plaid kept the product and changed everything else (First Round Capital, PMF Method).

### Update the assumption board · chat

> Here is my assumption table: [assumptions.md]. Here is this cycle's evidence: [synthesis, test results]. For each assumption, propose a verdict change (verified / open / pivot) only if the evidence supports it, with the exact quote or number. Don't change anything without one. List the assumptions nobody said anything about.

Show the proposed changes as a diff. **The founder approves each one.** Never update the board on your own. Flag any assumption open for two weeks without a test running: it isn't being tested.

---

## Output and hand-off

Updated `pmf/assumptions.md`, a decision memo in `pmf/decisions/`, updated `pmf/product-info.md`. If you can't write files, output the changed sections as a markdown block for the founder to save. Next: back to the stage the decision points to, with one change: usually `interview-script` (P4) for more conversations, or `landing-page-builder` (M1) or `prototype` (M2), then `ad-trigger-test` (T2) and `value-proposition-test` (T3), for the next market test.

## Rules (from pmf)

Nothing is evidence until a real person did something. Every number has a source or says GUESS. Every quote is verbatim or says PARAPHRASE. Never send, publish, launch, charge or spend without approval of the exact action. Update product-info.md and assumptions.md after every step. Change one thing per cycle.

---
Part of *Fast-Tracking Product-Market Fit with AI* by Gilles De Clerck (gillesdc.com).
