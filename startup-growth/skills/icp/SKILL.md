---
name: icp
description: Define a startup's ideal customer persona with Gilles De Clerck's five-dimension method — WHO, WHAT, WHY, HOW, WHERE — for B2B or B2C, specific enough that a stranger could find the person. Use when a founder wants to define, sharpen or check an ICP, write a customer profile, choose who to interview, or fill the Customer section of product-info.md. Part of the pmf-* set.
---

# ICP — who is this person?

Problems and solutions are always specific to a specific person. This skill turns "SMEs" or "young professionals" into one person a stranger could go and find.

**The test for every answer:** if it fits five different people, it isn't specific enough.

## What you need

Any chat. Web access helps for WHERE (real names and working links).

## Before you start

Read `pmf/product-info.md` if it exists. Ask whether the product is B2B or B2C (some are both: then pick the one who pays first). If the founder is torn between several possible customers, run `pmf-customer` A (Five first customers, picked by reply rate) first and let reply rates pick which one to describe here.

## The five dimensions

Work through them in order. For each, ask the founder the questions, fill in what they know, and mark every line **EVIDENCE (source)** or **HYPOTHESIS**.

### 1. WHO

**B2B — who is this company, and who inside it do you need to reach?**
- **Vertical and stage:** industry, funding stage, regulatory environment. A Series A fintech and a pre-seed healthtech are different worlds.
- **Company size:** headcount, revenue, investors, team structure.
- **Internal anatomy:** who was just hired, what tools they use, what's missing, what the org chart looks like around the problem, who the ICP answers to, who takes the buying decision.
- **Their customers:** who does the ICP sell to, and how does that shape their needs and constraints?

**B2C — who is this person, and how do they see themselves?**
- **Demographic profile:** age, gender, location, income, occupation. Specific enough to target an ad.
- **Identity and psychographics:** how they see themselves, what they value, their relationship to the problem.
- **Behavioural signals:** what they do daily that signals they're the customer: what they track, buy, follow, try.
- **Aspirational self:** who they want to become.

### 2. WHAT — their world today

- **Current solutions and stack:** the tools and processes they use now; the duct-tape solution.
- **Status quo:** replacing a competitor, or a new category? Are they buying for the first time?
- **Discovery path:** how they find solutions like this: peer intro, search, event, community.

### 3. WHY — why they'd care enough to act

- **The core problem:** what keeps them up at night, right now.
- **Cost of inaction:** money lost, time wasted, risk, missed opportunity.
- **Motivation:** survival, growth, status, fear, ambition. What kind of value they're after.
- **Budget and ownership:** B2B: who holds the budget, who champions it internally. B2C: what they already spend on this.
- **Buying trigger:** the specific event that makes it a "now" problem.

### 4. HOW — how they evaluate, decide and buy

- **Decision logic:** who decides, who influences, whether a champion has to sell it internally, solo or committee.
- **Purchase process:** the buying journey from start to finish, how long, which steps.
- **Friction points:** what slows deals down or kills them: legal, technical, trust, switching cost, inertia.

### 5. WHERE — where to find them

- **Content they consume:** newsletters, podcasts, publications, social accounts.
- **Communities:** Slack groups, forums, associations, WhatsApp groups.
- **Events:** conferences, meetups, industry gatherings.
- **Who they trust:** whose recommendation would make them act.

If web tools are available, research WHERE for real: names and working links, not categories. Open every link; drop dead ones.

## The deliverable

Five lines, one per dimension, each a dense paragraph with numbers and names. Format and two full examples (a B2B fintech compliance tool and a B2C longevity app) are in `references/examples.md`. Read it before writing.

Write it to the Customer section of `pmf/product-info.md` (WHO · WHAT · WHY · HOW · WHERE), each line tagged EVIDENCE or HYPOTHESIS.

## Checks before you hand it over

1. **The stranger test:** could someone who never met the founder find this person from the description alone?
2. **The five-people test:** read each line. Does it fit five different kinds of people? Then sharpen it.
3. **The trigger is an event**, with a date or a moment, not a general feeling.
4. **B2B: the buyer and the champion are named** as roles, and they may be different people.
5. **WHERE has names**, not categories ("Money20/20 Amsterdam", not "fintech events").
6. **Count the HYPOTHESIS lines.** That's the interview agenda: hand them to `pmf-problem` K (Turn research into interview questions).

## Rules (from pmf-loop)

Nothing is evidence until a real person did something. Every number has a source or says GUESS. Every quote is verbatim or says PARAPHRASE. Update product-info.md and assumptions.md after every step.

---
Method: Gilles De Clerck, *Customer, Problem, Value* workshop. Part of *Fast-Tracking Product-Market Fit with AI* (gillesdc.com).
