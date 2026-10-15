---
name: pmf-customer
description: Find and define a startup's first customer with AI. Use when building or sharpening an ICP, choosing between candidate segments, finding where target customers hang out, building a list of real named people to interview, or counting a market bottom-up from real companies. Part of the pmf-* set; reads pmf/product-info.md.
---

# PMF · Customer — who has the problem?

Goal: the real people who have the problem. Output is an ICP the founder can test, and a list of named people to talk to this week.

## What you need

- **Chat only:** A, B (paste reviews or job ads), C.
- **Free:** Apollo free plan (D, E), a free CRM tier such as Attio or HubSpot (D), web access to check links (C).
- **Runs on its own:** Claude Cowork scheduled tasks or Claude Code routines (F).
- **Paid, optional:** Clay, LinkedIn Sales Navigator.

## Before you start

Read `pmf/product-info.md` and `pmf/assumptions.md`. If they don't exist, run the setup from the `pmf-loop` skill, or ask: product in one sentence, who it's for, the problem in their words, what they do today instead, evidence so far.

Ask which technique the founder wants, or recommend one based on their evidence.

Each heading says how the technique works (chat · research · build · analyse · simulate) and, when it needs one, which building block: skill (it uses another skill), connect (a connector) or schedule (runs on its own).

---

## A. Five ICPs that disagree · chat · 10 min

Let reply rates pick the first customer instead of the founder's gut.

Prompt (run it yourself with the founder's product):

> My product: [one sentence]. Write 5 ideal customer profiles that could each be the right first customer. Make them as different as possible: different role, company type, and trigger event. For each: who, specifically · the moment that makes the problem urgent · where I'd find 10 of them this week.

Then:
1. Build a list of 10 people per ICP (technique D).
2. Draft the same three-line message for all 50: 20 minutes to learn how they handle [task]. No pitch.
3. The founder sends them (never you). Track replies per ICP in `pmf/icp-test.md`.
4. Highest reply rate becomes ICP hypothesis #1.

**Check:** the decision is made on reply rate per ICP, not on which one sounds best.

## B. Where your customer lives · research · skill

Find where the ICP talks shop, with links that work.

> Find where [ICP, one sentence] talk shop, online and offline. For each place: name · link · type (subreddit, Slack, Discord, newsletter, podcast, event, LinkedIn group) · approximate size · one recent thread or episode where they discussed [problem], with its link. Only include places you found a working link for. Maximum 20.

If a web-fetch or scraping tool is available, open every link yourself and drop dead ones. If the `where-your-customer-lives` skill (Varnan-Tech/opendirectory) is installed, use it first: it searches Reddit, HN, GitHub issues, G2 and Google Trends and returns an ICP and positioning doc plus the channels ranked by where the ICP actually is.

**Check:** the founder opens every link and joins three. Read before posting. People complaining about the problem in those places are the first interview candidates.

## C. The ICP from evidence · research

Build the five dimensions from what customers already published, not from imagination.

Sources, best first:
- **Reviews of the current solution** (G2, Capterra, App Store, Google Play, Amazon, Trustpilot): reviewers often state role and company size. Collect via a scraping connector (Apify, Bright Data) if available; otherwise ask the founder to paste 50–100 reviews.
- **Job ads (B2B):** a company hiring someone to do the painful work has the problem and a budget. Ask the founder to paste 20 job ads for the role that does the work.
- **Communities** (technique B).

Job-ad prompt:
> Below are 20 job ads for [role] at [type of company]. Make a table, one row per ad: company · tasks that sound manual or repetitive · tools named · team size · who the role reports to. Then: which tasks appear in more than half the ads? Quote the ad text for each.

Write the result as five dimensions in `pmf/product-info.md` (Customer section):
**WHO · WHAT · WHY · HOW · WHERE.** Each line tagged EVIDENCE (source) or HYPOTHESIS.

**Check:** if the ICP description fits five different kinds of people, it isn't specific enough. Could a stranger find this person from the description alone?

## D. The list of 50 · research · connect

Named people who match the ICP, with a reason to talk now.

**If a prospecting connector is available (Apollo, Clay):**
> Using [Apollo], find 50 people who match: role: [ ] · company: [industry], [size], [country] · signal: [hired for X / raised in last 12 months / uses tool Y]. For each: name, role, company, LinkedIn URL, one line on why they match. Don't include anyone who doesn't match all three criteria; list the rejected ones and why.

If a CRM connector is available (Attio, HubSpot), offer to add them, tagged with the ICP letter. **Ask before writing to the CRM.**

**Research column** (per person, if web tools are available):
> For [name], [role] at [company]: find one thing they posted, said, hired for or launched in the last 90 days that relates to [problem area]. Return one sentence and the link. If you find nothing, return "none". Don't guess.

**Without connectors:** give the founder the exact LinkedIn / Sales Navigator search filters to use by hand, and a sheet template: name · role · company · URL · why they match · research line · ICP · status.

**Check:** the founder opens five profiles. Are these really people they'd sell to? Click five research links: an invented post quoted back to a real person ends the conversation.

**Never** automate LinkedIn messaging or scraping (it violates LinkedIn's terms and risks the account). Never enrol people in email sequences. Outreach is drafted; the founder sends. EU contacts: GDPR applies to cold outreach.

## E. Count your market · analyse · connect

A market size built from companies you can name.

1. Population: the result count of the ICP filter in Sales Navigator, Apollo or Crunchbase. A number the founder can screenshot.
2. If Claude Code and web tools are available: merge lists from 2–3 sources, then qualify each company from its own website against the founder's rules, including exclusion rules. Keep 5–10 data points per company.
3. Count the qualified companies.
4. Multiply by the share with the problem (from interviews, not an industry average) and what they spend today (from interviews, reviews, job ads).

Write it to the Market size section of `product-info.md`, every input with its source or GUESS. Do not use top-down industry figures.

**Check:** if the population came from a report rather than a filter the founder can show, start again.

Seen at: Dan Rosenthal (Workflows.io), Growth Unhinged, May 2026: bottom-up account mapping with AI qualification from company websites.

## F. Weekly lookalikes · research · schedule

Once some people have taken a call, signed up or paid: every week, find ten more like them.

Set up as a scheduled task (Claude Cowork scheduled tasks, or a Claude Code routine):
> Every Monday 8:00: read companies tagged "said yes" in [CRM]. Find 10 lookalike companies via [Apollo/Clay] and the right person at each. Research one recent post or news item per person. Draft a three-line message for each. Post the drafts to [Slack channel / a doc] for review. Do not send anything.

Seen at: Elaine Zelby, via MKT1 (2026), on Closed-Won deals.

---

## Output and hand-off

- Update `pmf/product-info.md` (Customer section) and `pmf/assumptions.md` (persona rows).
- Save lists to `pmf/lists/`.
- Next: usually `pmf-problem`: is the problem real for these people? Research it, then book the conversations with this list.

## Rules (from pmf-loop)

Nothing is evidence until a real person did something. Every number has a source or says GUESS. Every quote is verbatim or says PARAPHRASE. Never send, publish, launch, charge or spend without approval of the exact action. Update product-info.md and assumptions.md after every step. Change one thing per cycle.

---
Part of *Fast-Tracking Product-Market Fit with AI* by Gilles De Clerck (gillesdc.com).
