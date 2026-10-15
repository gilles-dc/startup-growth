---
name: competitive-analysis
description: Learn how comparable companies grow, with AI doing the legwork — pick the right companies to study, uncover their A/B tests and hidden ad landing pages, audit their Meta and Google ads, branded search, traffic and app-store keywords, audit their content and onboarding funnel, and turn what you find into a prioritised list of tests. Use when a founder wants competitor research for growth, ad or landing-page ideas, or to understand what works in their market. Part of the pmf-* set.
---

# Competitive analysis — learn from the companies already solving your growth problem

Goal: a short list of tests worth running, sourced from companies that face the same growth challenge and have kept growing for a long time. The output is ideas to test. Never implement another company's tactic without testing it.

## What you need

- **Free:** a browser (B, E), Meta Ad Library (public, C), Google Trends (C), a BuiltWith lookup (E), Crunchbase's free search (A).
- **Paid, optional:** Ahrefs or Semrush, or DataForSEO pay as you go (B, C, D); Similarweb beyond its free tier (C); Sensor Tower (C); BuzzSumo (D).

## Before you start

Read `pmf/product-info.md`. Ask: which growth problem are we trying to solve (onboarding, conversion, acquisition, trust, pricing)? The analysis is aimed at that one problem.

Each heading says how the technique works (chat · research · build · analyse · simulate) and, when it needs one, which building block: skill (it uses another skill), connector (it uses a connector) or schedule (runs on its own).

---

## A. Pick who to study · research

1. Define the founder's own **audience** and **business model** in one line each (e.g. "tech-savvy adult consumers" · "freemium SaaS").
2. Find companies that match both and have **grown for a long time**. Use Crunchbase or similar databases, and search.
3. Skip very early companies: their growth may come from network effects or other things you can't see or copy.

Output: 3–5 companies in `pmf/competitors.md`, each with one line on why it's comparable.

## B. Find their A/B tests · research · connector

With a browser tool (Claude in Chrome, Firecrawl, or the founder's own browser):
1. Open the key pages (homepage, pricing, sign-up) in fresh private windows several times. When the page changes, you've been placed in another variant. Screenshot every variant.
2. Look for test parameters in the URL.
3. For each pair of variants, state the hypothesis they're testing: value proposition, imagery, social proof, pricing display.

**Hidden ad landing pages:** read the site's `sitemap.xml` for pages that aren't linked from the homepage. Pages that receive ad traffic are usually the most heavily tested. An SEO connector (Ahrefs, Semrush, DataForSEO) can also show which landing pages their search ads point to.

## C. Audit their ads · research · connector

- **Meta (Facebook, Instagram):** search the company's Page in the Meta Ad Library. Ads that have run for a long time are probably working. Ads with many comments and reactions likely run at high frequency. Note the copy, the creative hook, and the **objections in the comments**: those are the objections your own ads should answer. The founder can also get retargeted on purpose (visit their site without an ad blocker) to see which ads come back.
- **Google Ads:** with an SEO connector, list their paid keywords, cost per click and volume, and how long each keyword has been funded. Keywords funded consistently for a long time probably work; keywords tried briefly and dropped are ones to avoid.
- **Branded search:** Google Trends for their brand name. A steady decline can mean their growth is struggling, which makes them a cautionary example rather than a model.
- **Traffic:** Similarweb for the trend. It isn't always accurate, and a drop can simply mean they stopped an experiment that didn't pay off.
- **Mobile-first companies:** web traffic misleads, because users go straight to the app store. Use an app-intelligence tool (Sensor Tower or similar) for top keywords and estimated installs.

## D. Audit their content · analyse · connector

1. With an SEO connector: their highest-volume organic keywords and the blog posts that rank for them.
2. With a social-share tool (BuzzSumo or similar): which of their posts people shared most.
3. Topics that score high on both lists are the sweet spot worth considering for the founder's own content.

## E. Audit their onboarding funnel · research

1. Sign up for their newsletter, free trial or paid plan. Click through the tutorial links in their drip emails.
2. Log every touchpoint in order: emails, ads, sales contact, in-app messages, with dates.
3. Identify the tools behind their funnel with BuiltWith or a similar technology lookup.

Write it as a timeline in `pmf/competitors/[company].md`.

## F. From findings to tests · chat

For every finding, one test idea, aimed at the growth problem from "Before you start":
1. **Source** the idea (which company, which finding, with the screenshot or link).
2. **Prioritise** it: expected impact × confidence ÷ effort.
3. **A/B test** it on the founder's own page, ads or onboarding (`pmf-mvp`, `pmf-test`).
4. **Measure** whether the winner beat the baseline significantly, and whether the gain is worth implementing.
5. Only then **implement** it.

Also note the **norms**: what every company in the space does on its ads and landing pages. Knowing the norm lets the founder break it on purpose to stand out.

---

## Output and hand-off

`pmf/competitors.md` (who and why), one file per company in `pmf/competitors/`, and a prioritised test list in `pmf/tests/backlog.md`. Next: `pmf-mvp` and `pmf-test` for the top test, or `pmf-solution` D (Competitors’ old prices, via Wayback) and C (Competitors’ live prices, via a browser) for the pricing side.

## Rules (from pmf-loop)

Every number has a source or says GUESS. Never implement a competitor's tactic without testing it. Never send, publish, launch, charge or spend without approval of the exact action. Signing up for a competitor's product is fine; don't misrepresent who you are to their sales team.

---
Method: Gilles De Clerck. Part of *Fast-Tracking Product-Market Fit with AI* (gillesdc.com).
