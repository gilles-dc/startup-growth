---
name: value-proposition-generator
description: Build a startup's value propositions with Gilles De Clerck's method — every bad alternative the customer resorts to today, how the product does each one better, the value proposition as an action statement, the problem and value proposition statements, headers with a hook that answer the main objection, and the three positionings worth testing. Use when a founder wants value propositions, a from–to table, landing-page headlines, positioning variants for a test page or ads, or the step before writing a landing page. Workshop slide S4. Part of the pmf skills; reads pmf/product-info.md.
---

# Value propositions (S4) — what do you promise, and against whom?

Goal: a value proposition built from the customer's words, and a comparison with what they use today: the world without your product, and how you make it better.

A value proposition matches what the product does to what the customer gets.
- Product quality: "Here's what our product can do."
- Value proposition: "Here's what **you** can do with our product."

This skill builds the **vault**: every value proposition the product has, each one sourced from the world the customer lives in today. The landing page, the ads and the test variants all draw from it.

## Where it sits in the chain

**IN:** the ICP (`icp` (C1)) · what people say (`social-listener` (P1)), the complaints (`review-mining` (P2)), the workarounds (`workaround-mapper` (P3)) · the positioning map (`competitive-analysis` (S1)) · the buyer questions (`buyer-objections-mapper` (S2)) · interview findings (`interview-synthesis` (P5)), once there are real interviews.
**OUT:** `pmf/value-props.md`: the vault, the value proposition statement, headers and subheaders, and the three positionings worth testing.
**FEEDS:** `landing-page-builder` (M1): BUILD (the hero, the features and objections) and the kill criteria (what counts as a yes per variant); `ad-trigger-test` (T2) (one ad per positioning).

## What you need

- **Chat only:** everything in this skill. Research files from the other skills make each row stronger; without them, every row is marked HYPOTHESIS.

## Before you start

Read `pmf/product-info.md`, `pmf/assumptions.md`, `pmf/icp.md` and the research files that exist (also check the project root, or a file attached to the conversation). Ask for the product in one sentence and what it does, if it isn't written down. Without research, ask the founder for the alternatives and mark every row HYPOTHESIS; the vault is still worth building.

This skill works best with customer quotes already collected (`social-listener` (P1), `review-mining` (P2), `interview-synthesis` (P5)). If there are none, say so: Write it in their words, The table the customer would draw and Ten headlines will then be hypotheses in the founder's words. Start with the market (`competitive-analysis` (S1), `buyer-objections-mapper` (S2), `market-sizing` (S3)), then write the promise here.

**If there is no product-info.md,** offer two routes and let the founder pick: run `pmf` first (seven questions, and every pmf skill reads the file it writes), or go straight on. Straight on: ask these in one message, and say short answers are fine:
1. What is the product, in one sentence, and what does it do?
2. Who is it for? Role, company type or life situation.
3. What problem does it solve, in the words your customer would use?
4. What do they do today without it? Everything: nothing at all, a workaround, an old solution, a substitute, competitors by name.
5. What almost stopped your customers from buying, or what do you think would?
6. Any research or customer words to use: reviews, interview notes, survey answers? Attach them.

Label the answers HYPOTHESIS. At the end, output them as a short `product-info.md` for the founder to save.

Read `references/examples.md` before writing: the method is easiest to copy from the worked examples.

Each heading says how the technique works (chat · research · build · analyse · simulate) and, when it needs one, which building block: skill (it uses another skill), connector (it uses a connector) or schedule (runs on its own).

---

## The vault: from every bad alternative to three positionings · chat

### 1. Every bad alternative (column 1)

What does the customer resort to, today, without the product? List all of it:
- **doing nothing** and living with the problem
- **the workaround**: the manual, DIY or duct-tape way (a spreadsheet, a WhatsApp thread, a Notion set-up, an assistant doing it by hand)
- **the old solution** they grew up with (the bank branch, the hotel, the agency)
- **a substitute** that does a different job instead (a consultant, a doctor's appointment, a course)
- **each competitor**, from the positioning map

Write each as the customer experiences it: the cost, the delay, the risk, the frustration. Use their words from the research, and give the count where the research has one ("money: 105 of 226 bad reviews"). One alternative can hurt in several ways: give each its own row.

### 2. How the product does it better (column 2)

Per row, the specific thing the product does differently. Name the mechanism, not a feeling. **Quantify** whenever you can, and say which kind of number it is:

| Kind | Example |
|---|---|
| absolute | Onboard in 1 day instead of 2 weeks. |
| multiplier | Reach 10x more prospects. |
| percentage | Automate 90% of compliance reviews. |
| range | €400–€600 a month saved on exchange fees. |
| rate | 87% of users keep their plants alive past 6 months. |
| ratio | €3.99 per station per month vs €20K+ setup. |
| average + % | 13 sick days a year → 10.4 (−20%). |

A number the founder can't back yet is written as a GUESS and goes to the interviews to check.

### 3. The value proposition (column 3)

Turn column 2 into an action statement: what the customer can now do. "Learn a new language for free." "Trade stocks for free." "Experience new cities like a local."
- A benefit, never a feature. One product quality gives several benefits (fast → "get work done faster", "get more done", "save yourself time"): write each as its own row if the research supports it.
- Tag each row: **relieves a pain** (removes a cost, risk, frustration, wasted effort) or **creates a gain** (more revenue, time, control, confidence, status).

Columns 1–3 together are the **vault**. Aim for 8–15 rows. More is fine; the next step chooses.

### 4. Focus

At this stage the biggest mistake is promising everything. Pick the one row that matters most to the ICP: the pain mentioned most often and most angrily in the research, where the positioning map shows a gap nobody holds. If you pick two or three, they must serve the same person. Everything else becomes a feature or an objection block on the page.

Then write the two statements:
- **Problem statement:** the what (who has which problem, with numbers: how big, how often, what it costs, what they resort to) + the why (what current solutions offer, and the structural gap that keeps the problem alive). *The what earns recognition. The why earns belief.*
- **Value proposition statement:** the value (what gets better, quantified) + the mechanism (how the product does it). *The value earns attention. The mechanism earns belief.* No marketing poetry, no feature list.

### 5. Headers: the value proposition plus a hook

For every row you'd consider for the page (at least the top ten of the vault):
1. Start from the value proposition as written.
2. Find the **main objection** a customer would raise on reading it. Take it from the research: the complaints about competitors, the buyer questions (`buyer-objections-mapper` (S2)), what almost stopped people buying. "Build your own website" → "but I can't code", "it'll take too long", "it'll be limited".
3. Answer it inside the header, before they think it: "Build your own website in 20 minutes. No code."
4. If the page speaks to one persona, speak to them: "Reimburse your employees instantly. No fees."

The header is **descriptive, never clever**. Test: if a visitor reads only the header, do they know what you sell and why they'd want it? No vague promises ("Improve your workflow!"). No geography unless something physical limits where the product works.

**Subheader:** one or two sentences that introduce the product and say **how** it creates the value in the header: "Webflow is a website building platform that uses plug-and-play tech to help you launch quickly."

### 6. The positionings worth testing

Choose **three different value propositions** from the vault for the test page and the ads: three different promises to the same person, never three wordings of one promise. Map each to the positioning map (which axis or gap it bets on). For each: header, subheader, the objection it answers, and the image that would show it.

These become the variants in the kill criteria of `landing-page-builder` (M1) (what counts as a yes for each), the hero variants in `landing-page-builder` BUILD and the three ads in `ad-trigger-test` (T2), all to the same audience.

### The deliverable

`pmf/value-props.md` (or a markdown block if you can't write files):
1. **The vault:** bad alternative (with source and count) · how we're better (with the number and its kind) · value proposition · pain or gain.
2. **Focus:** the chosen row, and why (count, gap).
3. **Problem statement** and **value proposition statement**.
4. **Headers:** for at least the top ten rows: bad alternative · value proposition · main objection (with source) · header with hook; subheaders for the three to test.
5. **Three positionings to test:** header, subheader, objection answered, axis or gap, image idea.

### Checks before you hand it over

1. Every bad alternative has a source in the research, or says HYPOTHESIS. The status quo (doing nothing, the workaround) has at least one row.
2. Column 3 is something the customer **does**, never something the product **is**.
3. Every number has a source or says GUESS.
4. Each header passes the read-only-this test, and answers an objection someone in the research raised.
5. The three test positionings promise three different things. If two would win or lose for the same reason, replace one.
6. No city or country in a header unless the product only works there.

## More techniques

### Write it in their words · chat · 10 min

The short version. For the full method (every bad alternative, the vault, headers with a hook, the positionings to test), use The vault above.

The from–to table: the world without the product → the world with it.

> Here are customer quotes about [problem]: [paste]. Make a from–to table. Left column: the problem in the customer's exact words, quoted, with the source. Right column: what changes with [product], quantified where the quotes give a number. Don't put a word in the left column that isn't in a quote.

Then synthesise:
- **Problem statement:** the what (quantified) + the why (underlying mechanics).
- **Value proposition statement:** the value (the quantified outcome) + the mechanism (how the product achieves it). No marketing poetry, no feature lists.

**Check:** pick any left-hand cell and find the original quote. If you can't, delete the row.

### The table the customer would draw · chat

> From these complaint themes: [paste], pick the 3 that matter most to [ICP]: mentioned most often and most angrily. Use them as the rows of a comparison table. Columns: [alternative 1] · [alternative 2] · doing nothing · [my product]. Rate each cell honestly with one line of reasoning. Where the evidence for my product is a guess, write GUESS.

**Check:** if the product wins every row, the rows came from the feature list. Rebuild them from the problem column.

### Ten headlines · chat · 5 min

For headers that answer the main objection, built from the vault, use step 5 of The vault (Headers: the value proposition plus a hook).

> Write 10 landing-page headlines for [product] for [ICP], using the language in these quotes: [paste]. Each must promise a different outcome: save time, save money, reduce risk, look good to their boss, avoid a specific mistake, and so on. Maximum 8 words each. Under each: one subheading with a number in it.

**Check:** if two headlines promise the same thing in different words, replace one. These feed the page in `landing-page-builder` (M1) and the ad test in `ad-trigger-test` (T2).

---

## Output and hand-off

`pmf/value-props.md` (The deliverable above). Update the Value section of `pmf/product-info.md` (the from–to rows and the value + mechanism line) and its Alternatives section (from The table the customer would draw); update `pmf/assumptions.md` (promise rows). If you can't write files, output the changed sections as a markdown block for the founder to save. Next: `landing-page-builder` (M1) to build the smallest test of the strongest promise, then `ad-trigger-test` (T2) to test the three positionings.

## Rules (from pmf)

Nothing is evidence until a real person did something: the vault is the founder's best bet, and the test page and the interviews check it. Every number has a source or says GUESS. Every quote is verbatim or says PARAPHRASE. Never send, publish, launch, charge or spend without approval of the exact action. Update product-info.md and assumptions.md after every step. Change one thing per cycle.

---
Method: Gilles De Clerck, *Customer, Problem, Value* and *Landing Pages* workshops.
Part of *Fast-Tracking Product-Market Fit with AI* by Gilles De Clerck (gillesdc.com).
