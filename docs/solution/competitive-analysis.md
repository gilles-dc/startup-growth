# competitive-analysis: learn from the companies already solving your growth problem

Workshop slide S1 · stage: Solution

This skill picks the companies worth studying, maps what each one promises, to whom and for how much, and finds the corner nobody holds. It can study every competitor at once, one file each. Then it digs into how they grow: their A/B tests and hidden ad landing pages, their Meta and Google ads, their brand searches and traffic, their content and their onboarding emails. It reads their prices today and how those prices changed over the years, scores pricing pages, and can watch your competitors for changes. Every finding becomes a test idea, ranked, for your own page, ads or onboarding.

New to skills? Read [Start here](../start-here.md) first.

## When to use it

- You want to know who your competitors are and where they stand.
- You need a comparison table or a positioning map for a deck or a page.
- You want competitor prices, or what changed in their pricing.
- You want ideas for ads, landing pages or onboarding from companies that have grown for years.
- You have one growth problem (sign-ups, onboarding, trust, pricing) and want to see how others solved it.

The research from [review-mining](../problem/review-mining.md), [social-listener](../problem/social-listener.md) and [workaround-mapper](../problem/workaround-mapper.md) gives the map its complaints. To turn the gap into a promise, use [value-proposition-generator](../solution/value-proposition-generator.md). To test the ideas, go to [landing-page-builder](../mvp/landing-page-builder.md) and [ad-trigger-test](../test/ad-trigger-test.md). Not sure where to start? Use [pmf](../pmf.md).

## How to start

**Claude.ai, ChatGPT or any chat.** Type one of these:

- "Use competitive-analysis. Who should we study, and where do they stand?"
- "Use competitive-analysis to map our competitors' positioning and find the gap."
- "Use competitive-analysis and take me through competitor prices step by step."
- "Use competitive-analysis to turn these findings into a list of tests."

Naming the skill makes sure it loads. Once it's installed, a question about competitors, their ads, their prices or their positioning usually loads it on its own.

**Claude Code.** Type `/pmf:competitive-analysis`, or add what you want: `/pmf:competitive-analysis map the positioning of our five closest competitors`. If you installed it with `npx skills add`, it's `/competitive-analysis`.

## What you need

Every technique works without a connector. A browser tool or a connector saves you the screenshots.

| Technique | Chat only | Free | Paid, optional |
|---|---|---|---|
| Pick who to study | with web search | Crunchbase's free search | |
| Analyse every competitor at once | one competitor at a time | Claude Code subagents | |
| Map the positioning | pages saved as PDF or screenshots, reviews copied into one file | a browser tool (Claude in Chrome, Firecrawl) | |
| Find their A/B tests | screenshots from private windows, the saved sitemap | a browser tool (Claude in Chrome, Firecrawl) | Ahrefs, Semrush or DataForSEO for ad landing pages |
| Audit their ads | screenshots from the Meta Ad Library, Google Trends and Similarweb | Meta Ad Library, Google Trends, Similarweb's free tier | Ahrefs, Semrush or DataForSEO; Similarweb beyond its free tier; Sensor Tower |
| Audit their content | a sample checked by hand on Google | | Ahrefs, Semrush or DataForSEO; BuzzSumo |
| Audit their onboarding funnel | your own sign-ups, logged in a sheet | a BuiltWith lookup | |
| From findings to tests | yes | | |
| *More:* Competitors’ live prices, via a browser | pricing pages saved as PDF or screenshots | Claude in Chrome, or Firecrawl's free tier | |
| *More:* Competitors’ old prices, via Wayback | screenshots from web.archive.org | Wayback Machine connector | |
| *More:* Score a pricing page on ten points | saved pricing pages | Kyle Poyar's free pricing-teardown skill | |
| *More:* Competitor watch | copy the pages by hand on a fixed day | Claude Cowork scheduled tasks or Claude Code routines | Firecrawl monitor |

## Step by step

Ask to be taken through a technique and the skill stops at every point where you have to do something. To pick it up again, attach what it asked for and say the sentence in the last column. In a new chat, put the skill's name first, so the right skill loads: "Use competitive-analysis to continue the competitor map".

| Technique | The skill does | You do | Then say |
|---|---|---|---|
| Positioning | lists the pages and review sources per competitor | save the pages, copy the reviews (skip with a browser tool) | "continue the competitor map" |
| A/B tests | lists the key pages and sitemaps | load each page several times, screenshot every version (skip with a browser tool) | "continue the competitor A/B tests" |
| Ads | lists each company's Facebook Page, brand term and domain | take the screenshots (skip with connectors) | "continue the ad audit" |
| Onboarding | lists what to sign up for and gives you a log sheet | sign up, log every touchpoint until the emails slow down | "continue the onboarding audit" |
| Live prices | lists the competitors' pricing pages | save each as a PDF or a screenshot (skip with a browser tool) | "continue the live prices" |
| Old prices | gives the web.archive.org links and three dates | screenshot the snapshots (skip with the connector) | "continue the old prices" |
| Competitor watch | lists the pages to watch, writes the first snapshot and the watch | approve the schedule and switch it on, or copy the pages on the fixed day | "continue the competitor watch" |

At each stop, the skill notes in `product-info.md` what it's waiting for, so a new chat knows where you are.

## What you get

- **Who to study:** 3–5 companies plus what your customer does today, each with why it's on the list.
- **Every competitor at once:** one file per competitor (positioning, customer, pricing, features, reviews, recent changes) and a list you can rerun next month.
- **Positioning:** a positioning map on two or three axes taken from your customer's complaints, a comparison table with your product first, and the corner nobody holds.
- **A/B tests:** their page variants, the hypothesis behind each, and the landing pages they keep off the homepage.
- **Ads:** their longest-running ads, the objections in the comments, and the trend in brand searches and traffic.
- **Content:** the topics where their content ranks and gets shared.
- **Onboarding:** a timeline of every email, ad and message after sign-up, and the tools behind it.
- **Tests:** a ranked list of tests, each traced to a company and a finding, plus what every company in your space does.
- **Prices:** each competitor's plans, prices and limits today, what changed over the years, what each change suggests they learned, and a score for each pricing page, yours included.
- **Competitor watch:** only the material changes since the last snapshot, with links.

Example: [TO ADD]

## Files it reads and writes

| File | What happens |
|---|---|
| `pmf/product-info.md` | Read first, for your customer, your business model and your promise. The Alternatives section is updated. |
| `pmf/icp.md` | Read for what your customer does today and why they'd switch, if it exists. |
| `pmf/assumptions.md` | The price rows are updated. |
| `pmf/competitors.md` | Written: who to study, and why; the snapshots for the competitor watch. |
| `pmf/positioning.md` | Written: the map, the comparison table and the gap. |
| `pmf/competitors/[company].md` | Written: one per company, with its onboarding timeline. |
| `pmf/tests/backlog.md` | Written: the ranked list of tests. |

**Without them:** the skill offers to run [pmf](../pmf.md) first, which writes `product-info.md` and `assumptions.md` in about seven questions. Or it asks you four short questions, plus your growth problem and your promise, and carries on, then gives you a `product-info.md` to save. In a plain chat that can't save files, it prints the files for you to save or add to your Claude Project.

Next step after this skill: [value-proposition-generator](../solution/value-proposition-generator.md) to turn the gap into a promise, or [landing-page-builder](../mvp/landing-page-builder.md) and [ad-trigger-test](../test/ad-trigger-test.md) for the top test.
