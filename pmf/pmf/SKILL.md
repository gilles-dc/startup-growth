---
name: pmf
description: Start here. Entry point for taking a startup from idea to product-market fit with AI. Use when a founder wants to validate an idea, find product-market fit, work out what to test next, or doesn't know which stage or skill they need. Sets up product-info.md and assumptions.md, which every other pmf skill reads, and sends the founder to the one skill that tests their riskiest assumption.
---

# PMF — where do you start?

The path from idea to a product people pay for and keep using:

```
PRE-MARKET                     MARKET
CUSTOMER → PROBLEM → SOLUTION → MVP → TEST → ITERATE → PMF → grow
```

Pre-market work (customer, problem, solution) is **qualitative**: research and conversations that turn guesses into sharper hypotheses. Market work (MVP, test, iterate, PMF) is **counted**: sign-ups, deposits, payments, retention. AI compresses both, in different ways. This skill sets up the founder's working files and sends them to the stage, and the skill, that matters most right now. Each skill carries the code of its workshop slide (C1, P2, …).

Every technique in the pmf skills is labelled with how it works (**chat · research · build · analyse · simulate**) and, when it needs one, the building block underneath: **skill** (it uses another skill), **connector** (it uses a connector) or **schedule** (it runs on its own). All of them run on **context**: the two files this skill writes.

## What you need

Works in any chat. With file access (Claude Code, Cowork, or a Claude Project) it saves the two files; otherwise it outputs them for you to save.

## 1. Load or create the product file

Look for `pmf/product-info.md` (also check `product-info.md` in the project root, or a file attached to the conversation).

**If it exists:** read it, summarise it back in five lines, and ask what changed since it was last updated. If it has a "Waiting for" line, start there: say what the founder was going to bring back, and the sentence that resumes it.

**If it doesn't:** ask the founder these questions in one message, and tell them short answers are fine:

1. What is the product, in one sentence?
2. Who is it for? As specific as you can: role, company type or life situation.
3. What problem does it solve, in the words your customer would use?
4. What do they do today instead? (Another tool, a spreadsheet, a person, nothing.)
5. How will you make money, and roughly at what price?
6. What evidence do you have so far? Numbers: conversations, sign-ups, pilots, revenue.
7. What worries you most about this idea?

Then write `pmf/product-info.md` using `references/product-info-template.md`. Label every statement **HYPOTHESIS** or **EVIDENCE (source)**. If the founder has no evidence for something, it is a hypothesis, however confident they are. If you can't write files (for example in a plain chat), output the file as a markdown block and ask them to save it, or to add it to their Claude Project.

## 2. Build the assumption board

From the product file, list every assumption under these headings: persona, problem, promise (value), product, price, channel. Rank them by:

- **Lethality:** if this is wrong, does the company die, or just adjust?
- **Evidence:** how little do we actually know?

Write `pmf/assumptions.md` using `references/assumptions-template.md`. The top row is the **riskiest assumption**: lethal and untested.

## 3. Route to one skill

Recommend one skill, based on the riskiest assumption. One line of reasoning, then ask to proceed.

| The riskiest assumption is about… | Stage | Go to |
|---|---|---|
| who the first customer is, specific enough to find | Customer | `icp` (C1) |
| where those people gather online | Customer | `icp-finder` (C2) |
| needing a list of real, named people to contact, or how many companies fit | Customer | `prospect-list-builder` (C3) |
| which of several possible customers to start with | Customer | `icp-reply-rate-test` (C4) |
| whether the problem is real: what people say about it now | Problem | `social-listener` (P1) |
| what customers of today's solutions complain about | Problem | `review-mining` (P2) |
| what people do today to get around the problem | Problem | `workaround-mapper` (P3) |
| needing to talk to customers: questions, script, invites | Problem | `interview-script` (P4) |
| having interviews and needing the patterns, with checked quotes | Problem | `interview-synthesis` (P5) |
| how competitors sell, price and grow | Solution | `competitive-analysis` (S1) |
| what buyers ask and worry about before buying | Solution | `buyer-objections-mapper` (S2) |
| whether the market is big enough | Solution | `market-sizing` (S3) |
| what to promise, against which alternatives | Solution | `value-proposition-generator` (S4) |
| needing the smallest thing that gets a market answer: a page, a fake door, a deposit | MVP | `landing-page-builder` (M1) |
| whether a workflow or design makes sense to people | MVP | `prototype` (M2) |
| having a test page and needing to know the tracking works | Test | `tracking-audit` (T1) |
| needing traffic on the test | Test | `ad-trigger-test` (T2) |
| having results and needing a kill / iterate / scale decision | Test | `value-proposition-test` (T3) |
| whether the team knows the customer without opening a laptop | Iterate | `know-your-customer` (I1) |
| having evidence but needing a decision: update, pivot, persevere | Iterate | `pivot-or-persevere` (I2) |
| what to try next, every week | Iterate | `weekly-product-bets` (I3) |
| having users and needing to know whether they'd miss it | Retention | `pmf-survey` (PMF1) |
| whether users keep coming back | Retention | `retention-audit` (PMF2) |
| why people leave | Retention | `why-people-churn` (PMF3) |

## 4. Check what's connected

Look at the tools available in this session and tell the founder, in a short table, what is connected and what each missing category would unlock. Never block on a missing connector: every pmf skill has a fallback that works with research and chat alone.

| Category | Examples | Unlocks |
|---|---|---|
| Web research / scraping | Firecrawl, Apify, Bright Data, Exa | reviews at scale, live competitor pages, community threads |
| Prospecting / CRM | Apollo, Clay, Attio, HubSpot | lists of real people, interview pipeline |
| Meeting transcripts | Granola, Fireflies, Otter | interview synthesis without copy-paste |
| Forms / surveys | Tally, Typeform | waitlists, PMF survey, price survey |
| Payments | Stripe | deposit links, who paid |
| Product analytics | PostHog, Mixpanel, Amplitude, GA4 | funnels, experiments, retention |
| Ads | Meta Ads, TikTok Ads (Google Ads is read-only) | smoke-test traffic |
| Hosting | Vercel, Netlify | deploying test pages |
| Scheduling / chat | Calendly, Slack | booking links, agent digests |

## Rules every pmf skill follows

These are the part no tool does for the founder. Apply them everywhere, and say so when you apply one.

1. **Nothing is evidence until a real person did something.** Answered a question about their past, gave time, data, an introduction or money. Research output, AI summaries and synthetic personas are hypotheses.
2. **Every number has a source the founder can open**, or it is labelled **GUESS**.
3. **Every quote is verbatim and traceable**, or it is labelled **PARAPHRASE**.
4. **Never send, publish, launch, charge or spend without explicit approval of the exact action.** Outreach is drafted, ads are created paused, payment links start in test mode.
5. **Update `product-info.md` and `assumptions.md` after every step.** Research that changes nothing in those files was reading.
6. **Change one thing per cycle**, so you know which change mattered.

## Credits

Part of *Fast-Tracking Product-Market Fit with AI*, a workshop by Gilles De Clerck (gillesdc.com).
