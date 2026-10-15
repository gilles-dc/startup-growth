---
name: pmf-solution
description: Shape what a startup promises, against which alternatives, and whether the market is big enough, with AI. Use when writing a value proposition or from–to table, building a competitor or alternatives table, analysing competitor pricing and pricing history, finding what buyers ask before they buy, generating headline variants to test, or sizing a market bottom-up. Part of the pmf-* set; reads pmf/product-info.md.
---

# PMF · Solution — what do you promise, and against whom?

Goal: a value proposition built from the customer's words, an honest comparison with what they use today, and a market size with names behind it.

## Before you start

Read `pmf/product-info.md` and `pmf/assumptions.md`. This stage works best with customer quotes already collected (`pmf-problem`). If there are none, say so: G, H and I will then be hypotheses in the founder's words.

Start with the market (A–F), then write the promise (G–I).

Each heading says how the technique works (chat · research · build · analyse · simulate) and, when it needs one, which building block: teach (a skill), connect (a connector) or schedule (runs on its own).

---

## A. What buyers ask · research

1. Load call transcripts (or competitor reviews if there are no calls yet).
> What were buyers trying to find out when they evaluated options? Group the questions, count them, quote each.
2. Cross-check each theme with search demand (an SEO connector: DataForSEO, Semrush, Ahrefs) and with what AI assistants currently answer about the category (ask the question yourself and report the answer and its sources).
3. Where buyers ask and nobody answers well is positioning.

Seen at: Docebo, via Kyle Poyar, Growth Unhinged (Oct 2025).

## B. Competitors in parallel · research · teach

1. Do one competitor analysis by hand with the founder, reading `product-info.md` first: positioning, ICP, pricing, features, reviews, recent changes.
2. Turn the method into a reusable instruction and save the list in `pmf/competitors.md`.
3. Run each competitor as a parallel subagent, writing one file per competitor to `pmf/competitors/`.
4. Next month: rerun everything from `competitors.md`.

Seen at: Teresa Torres, Product Talk (Oct 2025): 1–2 minutes per competitor, 15 in parallel. The same work in browser chat took about an hour and came back shallow.

## C. Live pricing · research · connect

Research tools often return cached or outdated pricing pages. If a browser or scraping tool is available (Claude in Chrome, Firecrawl, Bright Data), open each competitor's live pricing page and extract: plans · prices · billing · limits · who each plan is for · free tier. Tell the founder to spot-check two by hand.

Seen at: Sachin Rekhi (2025): deep research returned stale prices; only live browsing was right.

## D. Pricing history · research · connect

A competitor's pricing history is their customer research, published.
- With a Wayback Machine connector: compare the competitor's /pricing page three years ago, one year ago, today.
- Without: the founder screenshots web.archive.org snapshots and you compare the images.
> What changed in prices · plan names · what each plan includes · limits · wording · who each plan is for? For each change: what does it suggest they learned about their customers?

Prices that went up and stayed up were accepted. Plans that vanished didn't sell. Offer to schedule a monthly page check (Firecrawl monitor, changedetection.io, or a scheduled task).

## E. Pricing teardown · analyse · teach

Score each competitor's pricing page, and the founder's draft pricing, on: clarity · value metric · packaging · anchoring · free-to-paid path · enterprise path · how readable it is to AI agents. Kyle Poyar publishes a free pricing-teardown skill that does this (Growth Unhinged, Apr 2026); if it's installed, use it.

Seen at: Kyle Poyar, Growth Unhinged (Apr 2026): all 50 Forbes AI 50 pricing pages in minutes.

## F. Size from search demand · analyse · connect

Market size = customers × what they spend on this problem, with real search volume and named companies as inputs and every assumption labelled.

1. With an SEO connector (DataForSEO pay as you go, or Semrush / Ahrefs / Similarweb): pull search volume for the problem, using the words people use to describe the pain.
2. Combine with the bottom-up company count from `pmf-customer` E.
3. If a TAM/SAM/SOM skill is installed (deanpeters `tam-sam-som-calculator`, phuryn `market-sizing`), run it so every assumption becomes a row with its source.

| Input | Where it comes from |
|---|---|
| ICP population | the result count of a Sales Navigator / Apollo / Crunchbase filter (`pmf-customer` E) |
| geography | which markets they can serve today |
| problem prevalence | the share of interviewees with the problem, not an industry average |
| current spend / cost of problem | interviews, reviews, job ads, the cost model from `pmf-problem` I |
| search demand | keyword volume for how people describe the pain (SEO connector) |

> Build a bottom-up market size as a table: row · value · source · confidence (high / medium / guess). Do not use any top-down industry figure.

**Check:** if the population came from a report rather than a filter the founder can show, start again. If the sizing segment doesn't match the ICP in `product-info.md`, say so.

## G. Write it in their words · chat · 10 min

The from–to table: the world without the product → the world with it.

> Here are customer quotes about [problem]: [paste]. Make a from–to table. Left column: the problem in the customer's exact words, quoted, with the source. Right column: what changes with [product], quantified where the quotes give a number. Don't put a word in the left column that isn't in a quote.

Then synthesise:
- **Problem statement:** the what (quantified) + the why (underlying mechanics).
- **Value proposition statement:** the value (the quantified outcome) + the mechanism (how the product achieves it). No marketing poetry, no feature lists.

**Check:** pick any left-hand cell and find the original quote. If you can't, delete the row.

## H. The table the customer would draw · chat

> From these complaint themes: [paste], pick the 3 that matter most to [ICP]: mentioned most often and most angrily. Use them as the rows of a comparison table. Columns: [alternative 1] · [alternative 2] · doing nothing · [my product]. Rate each cell honestly with one line of reasoning. Where the evidence for my product is a guess, write GUESS.

**Check:** if the product wins every row, the rows came from the feature list. Rebuild them from the problem column.

## I. Ten promises · chat · 5 min

> Write 10 landing-page headlines for [product] for [ICP], using the language in these quotes: [paste]. Each must promise a different outcome: save time, save money, reduce risk, look good to their boss, avoid a specific mistake, and so on. Maximum 8 words each. Under each: one subheading with a number in it.

**Check:** if two headlines promise the same thing in different words, replace one. These feed the page in `pmf-mvp` and the ad test in `pmf-test`.

---

## Output and hand-off

Update the Value, Alternatives and Market size sections of `pmf/product-info.md`; update `pmf/assumptions.md` (promise, price rows). Next: `pmf-mvp` to build the smallest test of the strongest promise.

## Rules (from pmf-loop)

Nothing is evidence until a real person did something. Every number has a source or says GUESS. Every quote is verbatim or says PARAPHRASE. Never send, publish, launch, charge or spend without approval of the exact action. Update product-info.md and assumptions.md after every step. Change one thing per cycle.

---
Part of *Fast-Tracking Product-Market Fit with AI* by Gilles De Clerck (gillesdc.com).
