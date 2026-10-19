---
name: icp
description: Define a startup's ideal customer persona with Gilles De Clerck's five-dimension method — WHO, WHAT, WHY, HOW, WHERE — for B2B or B2C, specific enough that a stranger could find the person. Drafts every sub-question of each dimension from a one-sentence product description, has the founder correct the draft, then compresses it into the one-slide ICP deliverable, and sharpens it with what customers published in reviews and job ads. Use when a founder wants to define, sharpen or check an ICP, write a customer profile, choose who to interview, or fill the Customer section of product-info.md. Workshop slide C1. Part of the pmf skills; reads pmf/product-info.md.
---

# ICP (C1) — who is this person?

Problems and solutions are always specific to a specific person. This skill turns "SMEs" or "young professionals" into one person a stranger could go and find.

Goal: one person a stranger could go and find, written as the Customer section of `pmf/product-info.md`.

**The ICP you start with is a hypothesis.** You build it by thinking hard about one person, the way a founder who knows the market would. Interviews prove or change it later (`icp-reply-rate-test` (C4), `interview-script` (P4)). This skill does not verify it. Its job is a picture so specific that the interviews have something sharp to test.

**The test for every answer:** if it fits five different people, it isn't specific enough.

## What you need

- **Chat only:** any chat, for the five dimensions. Sharpen the ICP with what customers published works with reviews and job ads pasted in.
- **Free:** web access helps for WHERE, to check that the names you give exist.
- **Optional:** a scraping connector (Apify, Bright Data) collects the reviews for Sharpen the ICP with what customers published.

## Before you start

Read `pmf/product-info.md` if it exists (also check the project root, or a file attached to the conversation). Work out whether the product is B2B or B2C, and ask only if you can't tell (some are both: then pick the one who pays first). If the founder is torn between several possible customers, run `icp-reply-rate-test` (C4) (Five first customers, picked by reply rate) first and let reply rates pick which one to describe here.

**If the founder gives a website (or a deck), read it first.** It is the founder's own input, not research: take the product, the price, the market, the languages it is written in, and what the careers page says about how they sell. Pre-fill the draft from it, and say in one line what it doesn't tell you (no price, no country, no customers named).

**If there is no product-info.md,** start drafting from what you have: the sentence and the website. Ask first only if the market (countries or region) is still unknown, in one line. A missing price or an unclear B2B or B2C is no reason to wait: make your best guess, mark it GUESS, and put it first in the answers you are least sure of. Mention once that `pmf` writes the product file every other skill reads, but don't make them run it first. Label everything you write HYPOTHESIS. At the end, output the ICP as the Customer section of a short `product-info.md` for the founder to save.

Each heading says how the technique works (chat · research · build · analyse · simulate) and, when it needs one, which building block: skill (it uses another skill), connector (it uses a connector) or schedule (runs on its own).

**Step by step.** If the founder asks to be taken through a technique, do one step at a time and stop at every hand-off. Each technique that needs the founder to act marks its steps: **Now** (what you do), **Your turn** (what the founder does; then stop and wait), **Resume** (the sentence that picks it up, in this chat or a new one), **Then** (what follows). At every stop, add one line to `product-info.md`: "Waiting for: [what], since [date]. To resume: Use icp to continue [the technique]." When you read a `product-info.md` that has a Waiting for line, start there: ask whether it has come in.

---

## The five dimensions · chat

### How to work

1. **Draft first, all five dimensions.** From the product sentence (and `product-info.md`, if there is one), answer every sub-question of WHO, WHAT, WHY, HOW and WHERE yourself, in that order. Don't interview the founder dimension by dimension: a founder facing a blank question writes generic answers, and a concrete draft is easier to correct. Anything the founder already told you goes into the draft. Never skip a sub-question.
2. **Show each dimension as a table** (sub-question → answer). This is the real exercise. See the worked tables in `references/examples.md`; read them before writing.
3. **Hand the draft to the founder to correct.** Show the five tables and the summary, mark the three to five answers you are least sure of, and ask: what is wrong, what is missing, what would you change?
4. **Hold every correction to the same standard.** The founder knows things you don't, so their correction replaces your guess, but write it to the rules below. If a correction makes a line vaguer ("all kinds of companies", "anyone who…"), say which check it fails (the five-people test, the stranger test) and offer a sharper version they can take or leave. The founder decides; you keep the bar.
5. **Then compress.** Each dimension's table becomes one line of the deliverable.

If the founder asks to go one dimension at a time, draft one dimension, let them correct it, then draft the next.

### How to write an answer

This is how Gilles writes them. Match it.

- **One or two sentences per sub-question, dense.** Fragments are fine. No preamble.
- **Commit to numbers.** Ranges you'd bet on: "35–42", "70/30", "€80K+", "€200–€500/month", "4–12 week cycle", "20+ hrs/week of a senior hire". A confident estimate is the hypothesis; a hedge tests nothing. Tag every number without a source (GUESS), in the tables and in the summary, so nobody mistakes a bet for a fact.
- **Name things.** Brands, tools, investors, publications, podcasts, people, events, law firms: "Seedcamp, Earlybird", "Oura/Whoop/Apple Watch", "Bird & Bird, Osborne Clarke", "Money20/20 Amsterdam".
- **Draw the edge.** Say what sets this person apart from the person next to them, including what they don't do or won't trust: "Not influencers." "Never a Google ad." "Price-insensitive if ROI is clear."
- **Show the inner world.** Identity, fear, ambition, what they refuse: "Not sick — refuses to become sick." "Sees peers aging and refuses."
- **Triggers are events** with a moment: a regulatory notice, a funding round closed with a condition, a bad blood result, a birthday, a new device.
- **Write from their world, at their stage.** A Series A fintech's anatomy, a 38-year-old's health stack. Nothing generic.
- **Keep the founder's market.** Geography is one attribute of WHO. Specificity comes from identity, stage, behaviour, stack and trigger. If the founder says Europe, the person lives across Europe: name the three or four cities or countries where they concentrate, and keep WHERE at that scale (the region's main podcasts, communities and events, plus the biggest local ones from more than one country). The same holds for rules: use the regulation that spans the market, with national regulators only as examples from several countries. Never shrink the ICP to one country, city or regulator unless the founder asks. If one market looks like the best place to start, say so in the hand-off. The cities you name describe the kind of place the person lives in (a large, international city); later steps use them as examples, never as a limit on the landing page or the ads, unless something physical ties the product to a place.

### The five dimensions and their sub-questions

#### 1. WHO

**B2B — who is this company, and who inside it do you need to reach?**
- **Vertical and stage:** what industry, what funding stage, what regulatory environment? A Series A fintech and a pre-seed healthtech are different worlds.
- **Company size:** headcount, revenue, investors, team structure. Who backed them? How big is the team?
- **Internal anatomy and hierarchy:** who was just hired? What tools do they use? What's missing? What does the org chart look like around your problem? Who does your ICP answer to? Who takes the buying decisions?
- **Target audience:** who does your ICP sell to? How does their customer base shape their needs and constraints?

**B2C — who is this person, and how do they see themselves in the world?**
- **Demographic profile:** age, gender, location, income, occupation. Specific enough to target an ad to this person.
- **Identity and psychographics:** how do they see themselves? What do they value? What's their relationship to the problem you solve?
- **Behavioural signals:** what do they do daily that signals they're your customer? What do they track, buy, follow, try?
- **Aspirational self:** who do they want to become? What future version of themselves are they working towards?

#### 2. WHAT — what their world looks like today

- **Current solutions and existing stack:** what tools and processes do they use right now? What's their duct-tape solution?
- **Status quo:** are you replacing a competitor, or is this a new category? Are they buying for the first time?
- **Discovery path:** how do they find out about solutions like yours? Peer intro, search, event, community?

#### 3. WHY — why they'd care enough to act

- **The core problem:** what specific problem keeps them up at night? What are they struggling with right now?
- **Cost of inaction:** what happens if they do nothing? Money lost, time wasted, risk exposure, opportunity missed?
- **The motivation:** what's driving them? Survival, growth, status, fear, ambition? What kind of value are they after?
- **Budget and ownership:** B2B: who holds the budget, who champions it internally? B2C: what do they already spend on this?
- **The buying trigger:** what specific event makes this a "now" problem? What just happened, or is about to?

#### 4. HOW — how they evaluate, decide and buy

- **Decision logic:** who decides? Who influences? Is there a champion who must sell it internally? Solo or committee?
- **Purchase process:** what does the buying journey look like from start to finish? How long? What are the steps?
- **Friction points:** what slows things down or kills deals? Legal, technical, trust, switching cost, inertia?

#### 5. WHERE — where to find them

- **Content they consume:** which newsletters, podcasts, publications, social accounts do they follow?
- **Communities:** which Slack groups, forums, associations, WhatsApp groups are they in?
- **Events:** which conferences, meetups or industry gatherings do they attend?
- **Who they trust:** who do they look up to? Whose recommendation would make them act?

### Research: only to fill in, never to grade

The draft and the founder's corrections lead. Use web tools, if you have them, for two things only:
- **WHERE:** check that the names exist and are alive (the podcast still publishes, the meetup still meets, the event has a date). Give a working link. Swap a dead name for a live one of the same kind; never invent a name to fill the line.
- **A number the founder asks for**, e.g. typical funding round size or what a blood panel costs.

Don't audit the ICP against what you find, and don't rewrite the person around search results. If research surprises you, say it in one line at the end, for the founder to weigh.

No web tools: mark every WHERE name UNCHECKED. The founder opens each one before the list is used, and swaps a dead one for a live one of the same kind.

If the ICP lives where search can't reach (Instagram DMs, WhatsApp groups, in person), say so plainly and list the reachable proxies: directories that list them (booking platforms, trade associations, the company register), trade fairs, and the suppliers or wholesalers they buy from.

### The deliverable

**Part 1: the five dimension tables**, every sub-question answered (see `references/examples.md`).

**Part 2: the ICP summary, one slide.** Five lines, one per dimension. Each line compresses its table into one dense paragraph: keep the numbers with their GUESS tags, the names, the trigger and the edge; drop the sub-question labels. End the summary with one line: "Numbers are GUESS unless a source is given." Example: the four WHO cells of the B2C longevity table become "35–42, male-skewing (70/30). Urban professional in tech/finance in London, Amsterdam, Berlin. €80K+ income. Data-driven, tracks HRV and glucose. Wears Oura/Whoop. Sees health as an engineering problem. Wants to perform at 60 like they do at 35."

Write both to the Customer section of `pmf/product-info.md` (WHO · WHAT · WHY · HOW · WHERE), marked as the starting hypothesis. If you can't write files, output the Customer section as a markdown block for the founder to save.

### Checks before you hand it over

1. **Every sub-question has an answer.** No blank cells, no "depends".
2. **The stranger test:** could someone who never met the founder find this person from the description alone?
3. **The five-people test:** read each line. Does it fit five different kinds of people? Then sharpen it.
4. **Numbers and names in every dimension.**
5. **The geography matches the founder's market**: no single country, city or regulator the founder didn't choose.
6. **The trigger is an event**, with a date or a moment, not a general feeling.
7. **B2B: the buyer and the champion are named** as roles, and they may be different people.
8. **WHERE has names**, not categories ("Money20/20 Amsterdam", not "fintech events").
9. **Every number without a source says GUESS**, in the summary as well as the tables.

### How many of these people exist

Add one line under the summary: roughly how many people (or companies) fit this ICP exactly, with the source. This is the size of your **beachhead**: the one group you focus on until you have product-market fit with them. It is not your market size. The market is bigger: once the product works for this group, you widen it to the customers next to them. Size the market separately, with looser criteria (`market-sizing` (S3)).

## More techniques

### Sharpen the ICP with what customers published · research

The ICP from the five dimensions above is the starting hypothesis. This technique fills it in with what customers already wrote about themselves: their job titles, tools, numbers and words. It adds detail to the person; it never replaces the founder's picture.

Sources, best first:
- **Reviews of the current solution** (G2, Capterra, App Store, Google Play, Amazon, Trustpilot): reviewers often state role and company size. Collect via a scraping connector (Apify, Bright Data) if available; otherwise ask the founder to paste 50–100 reviews.
- **Job ads (B2B):** a company hiring someone to do the painful work has the problem and a budget. Ask the founder to paste 20 job ads for the role that does the work.
- **Communities** (`icp-finder` (C2)).

Job-ad prompt:
> Below are 20 job ads for [role] at [type of company]. Make a table, one row per ad: company · tasks that sound manual or repetitive · tools named · team size · who the role reports to. Then: which tasks appear in more than half the ads? Quote the ad text for each.

Add what you found to the five dimensions in `pmf/product-info.md` (Customer section), with the source next to each detail you added. Where the sources contradict the ICP, list it under "To ask in interviews"; don't rewrite the ICP from it.

**Check:** if the ICP description fits five different kinds of people, it isn't specific enough. Could a stranger find this person from the description alone?

**Step by step:**
1. **Now:** name the current solution's review pages and, for B2B, the role to search job ads for. With a scraping connector, collect the reviews yourself.
2. **Your turn:** copy 20 job ads (B2B) and, without a scraping connector, 50–100 reviews into one file. **Stop.**
3. **Resume:** attach the file and say: "continue the ICP sharpening".
4. **Then:** the job-ad table, the details added to the Customer section with their sources, and the list under "To ask in interviews".

---

## Output and hand-off

- Write the five tables and the summary to the Customer section of `pmf/product-info.md`, marked as the starting hypothesis. Sharpen the ICP with what customers published adds its details there, with sources, and updates the persona rows in `pmf/assumptions.md`.
- If you can't write files, output the changed sections as a markdown block for the founder to save.
- Name the three to five answers you or the founder are least sure of, and that would change the most if they were wrong. That is the interview agenda: hand them to `interview-script` (P4) (Turn research into interview questions). Finding the places and the people to ask is `icp-finder` (C2) and `prospect-list-builder` (C3).
- Next: `icp-finder` (C2), then `prospect-list-builder` (C3). Torn between customers: `icp-reply-rate-test` (C4).

## Rules (from pmf)

Nothing is evidence until a real person did something. Every number has a source or says GUESS. Every quote is verbatim or says PARAPHRASE. Never send, publish, launch, charge or spend without approval of the exact action. Update product-info.md and assumptions.md after every step. Change one thing per cycle.

---
Method: Gilles De Clerck, *Customer, Problem, Value* workshop. Part of *Fast-Tracking Product-Market Fit with AI* by Gilles De Clerck (gillesdc.com).
