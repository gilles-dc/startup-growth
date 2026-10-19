---
name: market-sizing
description: Size a startup's market as TAM, SAM and SOM with Gilles De Clerck's method — the ICP is the beachhead and the market is bigger, so define the broader category and count it top-down from official statistics and company filings, then loosen the ICP one criterion at a time into rings of adjacent customers and count each ring bottom-up, every number with a source, a confidence and a range tight enough to mean something. Use when a founder asks how big the market is, for TAM/SAM/SOM, a market-size slide for investors, whether the market is big enough, or which customers come after the first ones. Workshop slide S3. Part of the pmf skills; reads pmf/product-info.md and feeds the pitch and the expansion plan.
---

# Market sizing (S3) — count the category, then the rings around your beachhead

**The ICP is a beachhead.** It is deliberately narrow: the one group you focus on until you have product-market fit with them. The market is bigger, because after product-market fit you widen the product to the customers next to them. So a market is never sized from the ICP. The ICP sets where you start (the SOM). The category sets how far you can go (the TAM).

**Two questions, two methods.**
- **How big is the problem?** (TAM, SAM) Count everyone in the category and multiply by **what they already spend on the problem** a year: the staff who do the work, the tools, the outside help, the substitutes. Never by your own price.
- **How much can we capture?** (SOM, beachhead) Count the customers you can reach and multiply by **your price**.

Sizing the whole market at your own price measures the market for one product at one price, which is almost always small. Sizing it by spend measures the problem.

The counting itself has two routes:
- **Top-down:** name the category the product belongs to, and count everyone in it with official statistics and company filings.
- **Bottom-up:** take the ICP's criteria and loosen them one at a time. Each loosening is a ring of adjacent customers. Count every ring.
- **TAM / SAM / SOM:** the category is the TAM; the widest ring the product serves as designed is the SAM; what you can reach within three years (the beachhead and its nearest rings) is the SOM.
- **A verdict:** is it big enough for what the founder wants to build, and if not, which moves make it bigger.

## Where it sits in the chain

**IN:** the ICP (`icp`, C1) · the product in one sentence and its price (`pmf/product-info.md`, `value-proposition-generator`, S4) · the competitors (`competitive-analysis`, S1), whose filings are sources.
**OUT:** `pmf/market-size.md`: one slide and the full file (format below).
**FEEDS:** the pitch, the expansion plan (which ring comes next and what the product must add; see `references/adjacent-customers.md`), the screener survey (the criteria no source could count).

## What you need

- **Any chat with web search:** the whole method. Official statistics, registers and filings are public.
- **Code execution** (Claude.ai with code execution on, Claude Code): for the arithmetic script. Without it, show every calculation step by step instead.
- **Optional:** a company count from `prospect-list-builder` (C3) or a filter you ran in Apollo or Sales Navigator, as a cross-check on the beachhead.

## Before you start

**If there is no product-info.md,** offer two routes and let the founder pick: run `pmf` first (seven questions, and every pmf skill reads the file it writes), or go straight on. Straight on: ask in one message for the product in one sentence, its price, the ICP (or run `icp` first), and the goal (venture-backed or bootstrapped). Label the answers HYPOTHESIS.

**Step by step.** If the founder asks to be taken through it, do one step at a time and stop at every hand-off: the category sentence (step 1) and the rings (step 3) are worth a check by the founder before you count. At every stop, add one line to `product-info.md`: "Waiting for: [what], since [date]. To resume: Use market-sizing to continue the market size."

Read `pmf/product-info.md` (the ICP is in its Customer section). You need three things: the ICP's criteria, what the product needs to work, and a price. If there is no price, use what the nearest competitor charges and say so. Read `references/examples.md` before writing; `references/sources.md` lists where to count.

Use code for the arithmetic (a script that reads only saved source files and prints every ring at low, base and high). Save every source file with its link. Never type a number into the answer that the script didn't print.

## 1. Name the category

Write one sentence: **"everyone who ___"**, at the level a competitor in the same category would count as its own customers. It must hold the product's minimum input, and nothing narrower.
- Longevity app: "everyone who tracks their health with a wearable" (the product needs wearable data).
- Compliance tool for fintechs: "every licensed payments, e-money or crypto firm" (the licence creates the obligation).
- Salon booking: "every hair and beauty business that takes appointments".

Test it two ways. Upward: would a wider sentence still need this product's core input? If yes, widen. Downward: does any ICP criterion sneak in (an age, a city, a job)? If yes, take it out.

Then say which kind of market it is, because that decides how much the top-down count can carry:
- **Existing:** people already buy this kind of product. The category count and its spend are solid.
- **Resegmented:** an existing category, sold to a slice of it in a new way. Count the category; the slice comes from the rings.
- **New:** nobody buys this yet. Count the people with the job to be done and what they spend on substitutes today (a consultant, a spreadsheet, a doctor's visit). Say that the market may grow past today's spend once the product exists.

## 2. Top-down: count the category

Count the category in people (B2C) or companies (B2B), country by country.
- **Official statistics first**: national statistics offices, Eurostat, the US Census Bureau, business registers by industry code and size class, licence registers. They can be rerun, and they say exactly who was counted.
- **Company filings second**: S-1s, annual reports, investor letters, member counts on the company's own site. A competitor's paying members are a floor for the people who already pay for this kind of product.
- **Analyst reports** (Statista, IDC, Grand View and the like) are cross-checks only, never inputs. Their definitions are unknown and nobody can rerun them. Quote one only to show how far it sits from your count.

Then count **what the category already spends on the problem**, per customer and in total. This is the TAM's money, so it is never skipped; if no competitor files accounts, build it from the work:
- **Spend = the people doing the work × their all-in cost a year**, plus tools and outside help. People: headcount disclosures in annual reports, regulators' returns, official employee counts × the share doing the work (from those disclosures). Cost: official wage statistics, a published all-in cost (total spend ÷ staff), job ads.
- **Or spend on substitutes:** what customers pay today for the workaround (a consultant, a membership, a test, a spreadsheet plus a person).
- **Industry cost studies** (survey-based) are cross-checks, like analyst reports.
- **Use one definition of the work throughout** (for example "a dedicated compliance function" or "all financial-crime work"); different sources count different things, and mixing them is what makes ranges explode.
- **Spend differs by customer size.** A large customer can spend a thousand times what a small one does; give the spend per size band, never one figure for all.

## 3. Bottom-up: the rings

Write the ICP's criteria as a list and sort them into two kinds:
- **Sharpeners** make the beachhead easy to find and talk to: city, age, sex, income, job, company stage, the podcasts they hear. The product works without them.
- **Requirements** are what the product needs to work: a device, a data source, a system, a licence, a team size.

Loosen **one criterion per ring**, in the order you would expand after product-market fit: sharpeners first, then requirements. Rings go **wider** (more customers like these) and **upward** (bigger customers who spend more on the problem); include at least one upward ring. Never loosen a customer criterion and a product requirement in the same ring. Dropping a sharpener changes the marketing. Dropping a requirement changes the product: write what it must add. Within each kind, put first the ring where most of the product and the references carry over. The last ring is the category from step 2. Five to seven rings is usual.

Tag each ring by how likely the product is to reach it: **probable** (the beachhead and the same person elsewhere), **plausible** (the rest of the SAM: same product, wider people), **possible** (every ring after a requirement drops). Possible rings are upside; they never go in the SAM.

| Ring | Who is in it (written as who it adds) | What the product must add |
|---|---|---|
| **Beachhead** | the ICP, on its countable criteria | — |
| + the rest of the country list | the same person anywhere you sell | nothing; channels and languages |
| + one more sharpener dropped, each | wider ages, incomes, jobs, company stages | messaging, content, maybe a price tier |
| + one requirement dropped, each | people or firms without the input the product needs | the missing input |
| **Category** | everyone in step 1 | — |

**Name every ring in plain words, by who it adds** ("+ people aged 25–64", "+ people with or without a recent blood test"), never by a code (R0, R1) or by what is dropped ("no blood test" reads as "people without one"). Inside the work you may number them; on the slide and in the file they carry their names.

Expansion branches. Side branches (a second persona the ICP flagged, buyers of a neighbouring product, the professionals who advise your customer) go in the adjacent-customers plan (`references/adjacent-customers.md`); the rings hold one line of loosening.

## 4. Count each ring on criteria a source can count

Each ring = population × the share with each criterion, country by country, every share from a source for that exact group where one exists (age band, education, country).

**Criteria no source counts are never multiplied in as guesses.** "Has the problem", "pays privately", "takes 5–12 supplements", "sees health as an engineering problem": these are what make the true beachhead a fraction of the counted one. List them under the SOM as **uncounted criteria**, each with the cheapest way to count it (a screener survey, interviews, a provider's disclosed count). Multiplying three guessed shares is what turns a market size into a range nobody can use.

Proxies are fine when named: tertiary education for "knowledge worker on €75K+", a blood test by a health professional for "has blood results". Say what the proxy includes that the criterion doesn't.

## 5. Ranges that mean something

Every input has a low, base and high, each from a source: another year, another survey wording, a neighbouring country as stand-in, the two ends of a published range.

When two criteria must hold together and no source crosses them, bound the overlap instead of guessing it:
- **low:** independent (share A × share B)
- **high:** one group inside the other (the smaller share)
- **base:** the midpoint, labelled as such.

Report each ring's spread (high ÷ low), and act on it:
- **Up to 3×:** fine. Say which input sets it.
- **Above 3×:** narrow it in this run when the narrowing is desk work: classify the whole list instead of a sample, pull the missing statistic, count the named firms. A market size that leaves the founder a to-do where an afternoon of research would do is unfinished.
- **Still above 3× after that:** give the base number and the money anyway, write the range as "between X and Y" next to it, and name the input that causes it and the cheapest way to measure it. Never leave a circle without a number or a € value.

## 6. TAM, SAM, SOM

- **TAM** = the category × what it spends on the problem a year, in named regions (for example "the EU and the UK"). Choose regions because the product could sell there, never because a statistic happens to exist for a country. Say which regions are left out; the TAM is then a floor.
- **SAM** = the part of that spend this kind of product competes for (for software: the share of the spend that goes to technology, from a cost study or filings), for the widest ring the product serves **as designed** (every sharpener dropped, no requirement dropped), in the countries it can sell to today.
- **SOM** = what the startup can reach **within three years** × its own price: the beachhead and the rings next to it that need no product change, in the SAM's countries. Say which rings it holds. Under it, the uncounted criteria.
- **Beachhead** = the ICP's countable firms or people × the price.

**Money on every circle:** spend for the TAM and SAM, people (or companies) × the price for the SOM and the beachhead. If a ring would pay a different price (a lower tier, a larger company), use that ring's price and say so.

**When a range stays wide** because of a definition (narrow versus broad), give the floor as the headline ("€8.8bn a year, at least") and the ceiling in small type, and check whether the verdict changes between them. If it holds at the floor, the range doesn't matter for the decision; say so.

## 7. Judge the size, and say what to do about it

A market size is an exercise: the number is feedback on the inputs. Every run ends with a verdict and its lessons.

1. **What the founder needs.** A venture-backed company needs a path to about €100m a year (investors look for roughly a $5bn+ TAM, [Lenny Rachitsky](https://www.lennysnewsletter.com/p/your-startup-idea-probably-isnt-venture)); a bootstrapped one may need €1–5m. Ask if it isn't written down.
2. **The reality check, in one sentence each:** how many customers €1m and €10m a year take, and what share of the beachhead, the SOM and the SAM that is. For scale: tech companies at IPO typically hold 0.1% to 2% of their addressable market ([Pear VC](https://pear.vc/market-sizing-guide/)).
3. **The verdict:** big enough, borderline, or too small for that goal, and why.
4. **If too small, the moves**, each sized where the data allows: a higher price or bigger customers (up-market), more products to the same customers, adjacent customer types (the next rings or side branches), more countries or rulebooks. Say which you would test first.
5. **If large**, check the price against what one customer already spends on the problem. A price far below that spend (the fintech test: €18,000 against at least €150,000 per firm) says the limit is the price, and the next run tests a higher one. Also check the beachhead is narrow enough to win.
6. **What to change in the next run:** the input, assumption or definition that the result shows is wrong.

## 8. Check it against itself

- Every ring holds the ring inside it; none exceeds the category.
- The TAM is spend, the SOM is price × reachable customers. If the SOM is more than about a tenth of the SAM, either the spend was undercounted or the price is above what customers spend: find out which.
- The top-down count and the outer ring describe the same group. Within 20%: say they agree. Up to 3×: name the definition difference that explains it. Above 3×: stop and find out why. Never narrow the category to make them agree.
- Add up what the named competitors earn (filings) and set it next to the TAM at full price. If the competitors already earn more than your TAM, the TAM is too narrow.
- Every company floor (members, customers) is below the ring it belongs to. If a competitor alone has more members than your ring, the ring is wrong.
- Search volume is not an input: it counts only the people who already know they have the problem and are looking. Use it, if at all, as a cross-check on how many are searching now.

## The deliverable

`pmf/market-size.md` (or a markdown block if you can't write files).

**The slide** (one slide, for the deck or the pitch). Someone who has never heard of the method must read it in thirty seconds.
- Title: "Market size: [product in five words]".
- Left: four nested circles, Beachhead inside SOM inside SAM inside TAM.
- Right, level with each circle: its name, who is in it in plain words, the number of people or firms, and the market a year (number × price). The range in small type underneath ("between 45m and 90m"), only where it matters.
- Under it, two plain sentences: the verdict (big enough or not, and the reality check in customers), and what is not counted yet.
- No codes, no "×" spreads, no unexplained terms. Footer: the price used and the three main sources.

**The full file:**
1. **The answer:** the slide's four circles and its two sentences.
2. **The verdict:** step 7 in full, with the moves sized and the lessons for the next run.
3. **The category:** the sentence, the top-down count, what the category already spends.
4. **The rings,** by name: who it adds · people low / base / high · € a year · what the product must add.
5. **Inputs, one row each:** # · input · value (low · base · high) · source (link) · confidence (high: official count of the exact group, rerunnable · medium: official, but a proxy group, another year or another country · stand-in: a neighbour's figure · guess: no source).
6. **Uncounted criteria** of the beachhead, each with the cheapest way to count it.
7. **Cross-checks:** company floors, the analyst figure (if quoted) and how far it sits from the count.
8. **What would narrow it**, cheapest first.
9. **Where the ICP and the count differ** (a sex skew a filing contradicts, a proxy that includes more people).

## Checks before you hand it over

1. No circle is built from the ICP alone. The ICP's cities, ages and incomes appear only in the beachhead and the SOM.
2. Every number has a source and a confidence, or says GUESS. No analyst figure is an input.
3. No ring multiplies a guessed share. Uncounted criteria are listed, never multiplied.
4. The TAM and SAM are sized by spend on the problem, the SOM and beachhead by the price; the slide says which is which.
5. Every circle has a number and a € value. Any spread above 3× was narrowed in the run, or says why it couldn't be.
6. Every requirement dropped names what the product must add.
7. The verdict says whether the market is big enough for the founder's goal, with the customers €1m and €10m take, and the moves if it is too small.
8. The slide uses plain names (Beachhead, SOM, SAM, TAM) and no codes.

## Rules (from pmf)

Every number has a source or says GUESS. Every quote is verbatim, with its link. Nothing is evidence until a real person did something: the market size tells you how far the product can go, and the interviews and the test page tell you whether anyone in the beachhead will pay.

---
Method: Gilles De Clerck, with the beachhead and follow-on markets from Bill Aulet's *Disciplined Entrepreneurship* (steps 4 and 14) and the nested market definitions from Aswath Damodaran's Uber valuations (2014–2015). Part of *Fast-Tracking Product-Market Fit with AI* (gillesdc.com).
