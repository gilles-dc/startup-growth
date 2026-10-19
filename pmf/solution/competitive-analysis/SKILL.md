---
name: competitive-analysis
description: Map the competitive landscape and learn how comparable companies grow, with AI doing the legwork — pick who to study, analyse every competitor at once, map their positioning and find the gap, build the comparison table, uncover their A/B tests and hidden ad landing pages, audit their ads, branded search, traffic, content and onboarding, read their live and old prices, watch them for changes, and turn findings into a ranked list of tests. Use when a founder wants competitor research, a competitor table, a positioning map, competitor pricing, or ad and landing-page ideas. Workshop slide S1. Part of the pmf skills; reads pmf/product-info.md.
---

# Competitive analysis (S1) — who else plays here, and how do they grow?

Goal: learn from the companies already solving your growth problem. A short list of tests worth running, sourced from companies that face the same growth challenge and have kept growing for a long time. The output is ideas to test. Never implement another company's tactic without testing it.

## What you need

- **Chat only:** From findings to tests, and Pick who to study with web search; Map the positioning, Find their A/B tests, Audit their ads, Audit their content and Audit their onboarding funnel from pages, screenshots, exports and sign-ups the founder saves and attaches. Analyse every competitor at once one competitor at a time. The live prices, the old prices and the pricing-page score from saved pages and screenshots the founder attaches. Competitor watch by hand, with the same prompt run on a fixed day.
- **Free:** a browser (Map the positioning: homepages and pricing pages; Find their A/B tests; Audit their onboarding funnel), Meta Ad Library (public, Audit their ads), Google Trends (Audit their ads), a BuiltWith lookup (Audit their onboarding funnel), Crunchbase's free search (Pick who to study), Claude Code subagents (Analyse every competitor at once), a browser tool such as Claude in Chrome, or Firecrawl's free tier (live prices), the Wayback Machine connector (old prices), Kyle Poyar's free pricing-teardown skill (Score a pricing page).
- **Runs on its own:** Claude Cowork scheduled tasks or Claude Code routines (Competitor watch); Slack for the digests.
- **For an agent, use a connector:** a plain web fetch is blocked by the Meta Ad Library and Google Trends. Meta's Ad Library API covers every ad shown in the EU (needs a verified developer account, a few days); an Apify Ad Library scraper or an ad-intelligence tool such as Foreplay does the same. Google Trends: DataForSEO's Google Trends endpoint. A/B variants (Find their A/B tests) and the onboarding funnel (Audit their onboarding funnel) need a browser tool (Claude in Chrome, Firecrawl), because pages have to be loaded several times or signed up for; the sign-up stays with the founder.
- **Paid, optional:** Ahrefs or Semrush, or DataForSEO pay as you go (Find their A/B tests, Audit their ads, Audit their content); Similarweb beyond its free tier (Audit their ads); Sensor Tower (Audit their ads); BuzzSumo (Audit their content); Firecrawl monitor (Competitor watch).

## Before you start

Read `pmf/product-info.md` (also check the project root, or a file attached to the conversation). Ask: which growth problem are we trying to solve (onboarding, conversion, acquisition, trust, pricing)? The analysis is aimed at that one problem. Also ask for the founder's promise in one sentence: Map the positioning tests it against every competitor.

**If there is no product-info.md,** offer two routes and let the founder pick: run `pmf` first (seven questions, and every pmf skill reads the file it writes), or go straight on. Straight on: ask these in one message, together with the growth problem and the promise, and say short answers are fine:
1. What is the product, in one sentence, and what does it cost?
2. Who is it for, and how do you make money? One line each, e.g. "small accounting firms" · "monthly subscription".
3. What do your customers use today? Name every competitor, tool or workaround you know.
4. Where do you sell: which countries, which languages?

Label the answers HYPOTHESIS. At the end, output them as a short `product-info.md` for the founder to save.

Each heading says how the technique works (chat · research · build · analyse · simulate) and, when it needs one, which building block: skill (it uses another skill), connector (it uses a connector) or schedule (runs on its own).

**Step by step.** If the founder asks to be taken through a technique, do one step at a time and stop at every hand-off. Each technique that needs the founder to act marks its steps: **Now** (what you do), **Your turn** (what the founder does; then stop and wait), **Resume** (the sentence that picks it up, in this chat or a new one), **Then** (what follows). At every stop, add one line to `product-info.md`: "Waiting for: [what], since [date]. To resume: Use competitive-analysis to continue [the technique]." When you read a `product-info.md` that has a Waiting for line, start there: ask whether it has come in.

---

## Pick who to study · research

1. Define the founder's own **audience** and **business model** in one line each (e.g. "tech-savvy adult consumers" · "freemium SaaS").
2. Find companies that match both and have **grown for a long time**. Use Crunchbase or similar databases, and search.
3. Skip very early companies: their growth may come from network effects or other things you can't see or copy.

4. Add the **status quo** (what the customer does today instead) and the companies named in the complaints (`review-mining` (P2)). For a new category, mix direct rivals with the tools the customer already owns.

Output: 3–5 companies plus the status quo in `pmf/competitors.md`, each with one line on why it's on the list.

## Analyse every competitor at once · research · skill

1. Do one competitor analysis by hand with the founder, reading `product-info.md` first: positioning, ICP, pricing, features, reviews, recent changes.
2. Turn the method into a reusable instruction and save the list in `pmf/competitors.md`.
3. Run each competitor as a parallel subagent, writing one file per competitor to `pmf/competitors/`.
4. Next month: rerun everything from `competitors.md`.

Seen at: Teresa Torres, Product Talk (Oct 2025): 1–2 minutes per competitor, 15 in parallel. The same work in browser chat took about an hour and came back shallow.

No Claude Code: run the saved instruction for one competitor at a time, in this chat or in one chat each, and save each result as its own file.

## Map the positioning · research · analyse

What each competitor promises, to whom, for how much, and the corner nobody holds. Do this before studying their tactics: a tactic only makes sense once you know which position it defends.

**Inputs:** the companies from Pick who to study, plus the **status quo** (what the customer does today instead: a spreadsheet, a DIY Notion + Claude set-up, a consultant) from `pmf/icp.md` · the complaints from every research source, counted per company: the bad reviews (`review-mining` (P2)), the posts (`social-listener` (P1)), the people who posted about the problem (`prospect-list-builder` (C3)) and the workaround videos (`workaround-mapper` (P3)) · the ICP's WHY (core problem, cost, motivation, budget) · the founder's own promise in one sentence, from `pmf/product-info.md`.

1. **One row per competitor, status quo included.** For each, open the homepage (read the whole page, below the hero too: the closest rival claim can sit halfway down), the pricing page and one solution page aimed at the founder's customer. Save every page.
2. **Collect the complaints from every source,** per competitor and for the status quo. The reviews are one source; the posts, the people list and the workaround videos often carry the sharper complaint ("I double-log my supplements in the WHOOP journal every day", "the blood feature isn't offered in Europe"). Count each theme per source. If a competitor has no reviews in `review-mining` (P2), collect them now with the same method; never leave a competitor without complaints because the earlier step skipped it.
3. **Sort each complaint: built in or fixable.** *Built in*: it comes from what the company sells and how (what you must buy, the price model, what it hands back, which data or rules it covers, where it's sold); the company can't fix it without changing its model. *Fixable*: bugs, sync, support, a clunky screen; a patch fixes it. Position against the built-in ones. A fixable complaint, however often raised, is no gap: the competitor ships a fix and it's gone. On the slide, call them what they are for the founder: **our opening** (a complaint built into how they sell) and **no opening** (a complaint they can patch), with plain counts ("24 complaints") and the complaint in plain words ("the app crashes, data won't sync"), never theme codes or source codes.
4. **Find the price.** If the pricing page is blocked or renders in the browser only, try the product page, the store page, the App Store listing (its in-app purchases list shows subscription prices) or a browser. A price another company quotes for this competitor is that company's claim: label it as such. No price found = UNVERIFIED.
5. **Pick two or three axes from the customer's side.** Name both ends of each axis in the customer's words, concretely ("self-service: you do the work in a tool" ↔ "done for you: experts do the work"), and name the opening plainly ("the consultant's work, done by software at a software price"), so nobody has to infer it. Each axis comes from a complaint theme or a line of the ICP's WHY (what they must buy first, who does the work, which rules it covers, what it hands back). Never from a feature list.
6. **Place each competitor on the axes by its own claim,** and mark where the complaints contradict the claim.
7. **Name the gap**: the corner nobody holds, in one line under the map.

> Below are the saved homepages and pricing pages of [competitors], the complaints counted per competitor, and the ICP's WHY.
> 1. One row per competitor, the status quo included: the promise in their own words (quoted, with the page link) · who it's for · price and model (subscription, device, one-off, quote only; with the page it came from) · what they stress most · what they don't offer · the built-in complaint raised about them most, with its count per source ("P2 14, P1 6"), and the most-raised fixable one apart.
> 2. Two or three axes that matter to this customer, each taken from a complaint theme or the ICP's WHY. For each axis, say which complaint or line it comes from.
> 3. Place every competitor on the axes: a 2×2 for the first two, a ranked list for the third. Place by their claim; note where the complaints say otherwise.
> 4. The comparison table (the workshop's "Who else plays here?"), built the way founders' comparison tables are (`references/comparison-tables.md`): the founder's product as the first column, highlighted, marked planned where it doesn't exist yet; five to eight alternatives after it, the status quo included. Fact rows: founded, funding, where sold, who it's for, price. Then six to ten capability rows, each one concrete thing a buyer checks for, and each traced to a buyer question, a built-in complaint or a value proposition (say which, with its count, in the file). Cells: ✓, ~ (partly, with a few words why), – (not offered), ? (not checked). Every mark has a source in the file.
> 5. The gap: the corner nobody holds, and whether [the founder's promise] can take it. One paragraph; its first sentence goes under the map. The wording of the promise itself is the next step's job (`value-proposition-generator` (S4)).
> Only use what is on the saved pages and in the complaints. A price or claim you couldn't read is UNVERIFIED. Write "not checked" where you didn't look.

**Output:** `pmf/positioning.md`: the competitor table, the axes with their source, the map, the comparison table, the gap paragraph. Lead with the map and the gap: a reader should see in ten seconds where each competitor sits and which corner is free. It feeds `landing-page-builder` (M1) (the test page's headline and objections) and the three versions in `prototype` (M2).

**Check:**
- Ctrl-F three promises and three prices in the saved pages. If one isn't there, redo it.
- Every axis names the complaint theme or ICP line it came from. An axis without one is a feature: replace it.
- The status quo has a row and a place on the map, with complaints from the posts or videos if it has no reviews.
- Every competitor in the table has complaints counted, from at least one source. No "not in the sample".
- Read the founder's promise next to every competitor's: if one says almost the same words, that competitor is the main rival, whatever the founder thought.

No browser or web fetch, or a page that won't load: the founder saves each page as a PDF (print, then save as PDF) or screenshots the whole page, and attaches the files. Reviews the same way: copy them from the store or review site into one file.

**Step by step:**
1. **Now:** list the pages to save per competitor (homepage, pricing page, one solution page) and the review sources. With a browser tool, open them and go straight on.
2. **Your turn (no browser tool):** save the pages and copy the reviews. **Stop.**
3. **Resume:** attach the files and say: "continue the competitor map".
4. **Then:** steps 1–7 and the prompt above, with the checks.

## Find their A/B tests · research · connector

With a browser tool (Claude in Chrome, Firecrawl, or the founder's own browser):
1. Open the key pages (homepage, pricing, sign-up) in fresh private windows several times. When the page changes, you've been placed in another variant. Screenshot every variant.
2. Look for test parameters in the URL.
3. For each pair of variants, state the hypothesis they're testing: value proposition, imagery, social proof, pricing display.

**Hidden ad landing pages:** read the site's `sitemap.xml` for pages that aren't linked from the homepage. Pages that receive ad traffic are usually the most heavily tested. An SEO connector (Ahrefs, Semrush, DataForSEO) can also show which landing pages their search ads point to.

No browser tool: the founder does the loading. Each key page in a fresh private window, several times; a screenshot of every version that differs, with its full address. For the sitemap, open the site's address followed by /sitemap.xml and save the page.

**Step by step:**
1. **Now:** list the key pages per competitor and their sitemap addresses. With a browser tool, load them and go straight on.
2. **Your turn (no browser tool):** load each page several times, screenshot every version, save each sitemap. **Stop.**
3. **Resume:** attach the screenshots and sitemaps and say: "continue the competitor A/B tests".
4. **Then:** the hypothesis behind each pair of variants, and the pages missing from the homepage.

## Audit their ads · research · connector

- **Meta (Facebook, Instagram):** search the company's Page in the Meta Ad Library. Ads that have run for a long time are probably working. Ads with many comments and reactions likely run at high frequency. Note the copy, the creative hook, and the **objections in the comments**: those are the objections your own ads should answer. The founder can also get retargeted on purpose (visit their site without an ad blocker) to see which ads come back.
- **Google Ads:** with an SEO connector, list their paid keywords, cost per click and volume, and how long each keyword has been funded. Keywords funded consistently for a long time probably work; keywords tried briefly and dropped are ones to avoid.
- **Branded search:** Google Trends for their brand name. A steady decline can mean their growth is struggling, which makes them a cautionary example rather than a model.
- **Traffic:** Similarweb for the trend. It isn't always accurate, and a drop can simply mean they stopped an experiment that didn't pay off.
- **Mobile-first companies:** web traffic misleads, because users go straight to the app store. Use an app-intelligence tool (Sensor Tower or similar) for top keywords and estimated installs.

No connector: the founder searches each company's Page in the Meta Ad Library and screenshots the ads that have run longest, with their start dates; looks up each brand name in Google Trends and screenshots the line; and screenshots Similarweb's free page for each domain. Without an SEO connector or Sensor Tower, mark the Google Ads keywords and the app-store keywords "not checked".

**Step by step:**
1. **Now:** list each company's Facebook Page name, brand search term and domain. With connectors, pull them and go straight on.
2. **Your turn (no connector):** take the screenshots. **Stop.**
3. **Resume:** attach the screenshots and say: "continue the ad audit".
4. **Then:** the read above: what has run longest, the objections, the brand trend, the traffic.

## Audit their content · analyse · connector

1. With an SEO connector: their highest-volume organic keywords and the blog posts that rank for them.
2. With a social-share tool (BuzzSumo or similar): which of their posts people shared most.
3. Topics that score high on both lists are the sweet spot worth considering for the founder's own content.

No SEO connector or social-share tool: list their posts from the blog archive or the sitemap, search the topics of ten of them on Google, and note which of their posts show on the first page. It's a sample; say so.

## Audit their onboarding funnel · research

1. Sign up for their newsletter, free trial or paid plan. Click through the tutorial links in their drip emails.
2. Log every touchpoint in order: emails, ads, sales contact, in-app messages, with dates.
3. Identify the tools behind their funnel with BuiltWith or a similar technology lookup.

Write it as a timeline in `pmf/competitors/[company].md`.

No browser tool for the lookup: the founder enters each domain on builtwith.com and pastes the result.

**Step by step:**
1. **Now:** list what to sign up for per company, and a log sheet: date, channel, what it said, screenshot or link.
2. **Your turn:** sign up, click through the tutorial links, and log every touchpoint as it arrives, until the emails slow down. **Stop.**
3. **Resume:** attach the log and the screenshots and say: "continue the onboarding audit".
4. **Then:** the timeline per company and the tools behind it.

## From findings to tests · chat

For every finding, one test idea, aimed at the growth problem from "Before you start":
1. **Source** the idea (which company, which finding, with the screenshot or link).
2. **Prioritise** it: expected impact × confidence ÷ effort.
3. **A/B test** it on the founder's own page, ads or onboarding (`landing-page-builder` (M1), `ad-trigger-test` (T2), `value-proposition-test` (T3)).
4. **Measure** whether the winner beat the baseline significantly, and whether the gain is worth implementing.
5. Only then **implement** it.

Also note the **norms**: what every company in the space does on its ads and landing pages. Knowing the norm lets the founder break it on purpose to stand out.

## More techniques

### Competitors’ live prices, via a browser · research · connector

Research tools often return cached or outdated pricing pages. If a browser or scraping tool is available (Claude in Chrome, Firecrawl, Bright Data), open each competitor's live pricing page and extract: plans · prices · billing · limits · who each plan is for · free tier. Tell the founder to spot-check two by hand.

Seen at: Sachin Rekhi (2025): deep research returned stale prices; only live browsing was right.

No browser tool: the founder opens each pricing page and saves it as a PDF (print, then save as PDF) or screenshots the whole page, and attaches the files. Extract from those.

**Step by step:**
1. **Now:** list the competitors' pricing page links. With a browser tool, open them and go straight on.
2. **Your turn (no browser tool):** save each pricing page as a PDF or a screenshot. **Stop.**
3. **Resume:** attach the files and say: "continue the live prices".
4. **Then:** the extraction above, and the two pages to spot-check.

### Competitors’ old prices, via Wayback · research · connector

A competitor's pricing history is their customer research, published.
- With a Wayback Machine connector: compare the competitor's /pricing page three years ago, one year ago, today.
- Without: the founder screenshots web.archive.org snapshots and you compare the images.
> What changed in prices · plan names · what each plan includes · limits · wording · who each plan is for? For each change: what does it suggest they learned about their customers?

Prices that went up and stayed up were accepted. Plans that vanished didn't sell. Offer to schedule a monthly page check (Firecrawl monitor, changedetection.io, or a scheduled task).

No schedule: the founder puts a monthly reminder in their calendar to save each competitor's pricing page and attach it here, with the same sentence as below.

**Step by step:**
1. **Now:** for each competitor, give the snapshot list link (web.archive.org/web/*/ followed by their pricing page address) and the three dates to pick. With the connector, go straight on.
2. **Your turn (no connector):** open the snapshot closest to each date and screenshot the whole page. **Stop.**
3. **Resume:** attach the screenshots and say: "continue the old prices".
4. **Then:** the comparison above, change by change.

### Score a pricing page on ten points · analyse · skill

Score each competitor's pricing page, and the founder's draft pricing, on: clarity · value metric · packaging · anchoring · free-to-paid path · enterprise path · how readable it is to AI agents. Kyle Poyar publishes a free pricing-teardown skill that does this (Growth Unhinged, Apr 2026); if it's installed, use it.

Seen at: Kyle Poyar, Growth Unhinged (Apr 2026): all 50 Forbes AI 50 pricing pages in minutes.

### Competitor watch · research · schedule

Only automate a method that already works by hand; automating a bad process makes it fail faster. Set up with Claude Cowork scheduled tasks or Claude Code routines (the founder approves the schedule and the connectors). Agents write drafts and digests; they never send, launch or spend.

The agent checks competitors on a schedule and only reports what changed.

> Compare each competitor in pmf/competitors.md against its last snapshot: pricing, positioning, features, ads. Report only material changes, with links. Update the snapshots.
(Tools: Firecrawl monitor, changedetection.io, a scraping connector. Seen at: deanpeters/Product-Manager-Skills `competitive-intel-watch`.)

By hand (no schedule, no scraper): on a fixed day, the founder copies each competitor's home page and pricing page into one file (the text, or a screenshot), with the date. Compare it with the last copy in `pmf/competitors.md` and report only what changed. No `competitors.md` yet: the first copy is the first snapshot.

**Step by step:**
1. **Now:** list the competitors and the pages to watch, and write the first snapshot of each in `pmf/competitors.md`. Then the watch, for approval.
2. **Your turn:** approve the schedule and switch it on. By hand: on the fixed day, copy the pages. **Stop.**
3. **Resume:** attach the copies (on a schedule, nothing) and say: "continue the competitor watch". Every time after, the same sentence.
4. **Then:** only the material changes, with links, and the snapshots updated.

---

## Output and hand-off

`pmf/competitors.md` (who and why, and the snapshots for Competitor watch), `pmf/positioning.md` (the map, the comparison table and the gap; it feeds the test page's headline in `landing-page-builder` (M1) and the three versions in `prototype` (M2)), one file per company in `pmf/competitors/`, and a prioritised test list in `pmf/tests/backlog.md`. Update the Alternatives section of `pmf/product-info.md` and the price rows of `pmf/assumptions.md`. If you can't write files, output the changed sections as a markdown block for the founder to save. Next: `landing-page-builder` (M1) and `ad-trigger-test` (T2) for the top test, `value-proposition-generator` (S4) to turn the gap into a promise, or Competitors’ old prices, via Wayback and Competitors’ live prices, via a browser (under More techniques) for the pricing side.

## Rules (from pmf)

Nothing is evidence until a real person did something. Every number has a source or says GUESS. Every quote is verbatim or says PARAPHRASE. Never implement a competitor's tactic without testing it. Never send, publish, launch, charge or spend without approval of the exact action. Signing up for a competitor's product is fine; don't misrepresent who you are to their sales team. Update product-info.md and assumptions.md after every step. Change one thing per cycle.

---
Part of *Fast-Tracking Product-Market Fit with AI* by Gilles De Clerck (gillesdc.com).
