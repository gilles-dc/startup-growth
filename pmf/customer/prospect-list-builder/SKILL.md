---
name: prospect-list-builder
description: Build a list of 50 real named people who match a startup's ICP, with a profile link, why they match and one recent thing they posted or did — from Apollo, Clay or search filters run by hand; for local businesses, Google Maps (via Apify) plus the company register; for consumers, the people who posted about the problem in public. Then count the companies that fit, bottom-up, and once some people said yes, find ten new lookalikes every Monday. Use when a founder needs people to interview, a prospect or lead list, lookalike prospects, or a market count from companies they can name. Workshop slide C3. Part of the pmf skills; reads pmf/product-info.md.
---

# Prospect list builder (C3) — who, by name, do I talk to this week?

Goal: the real people who have the problem. Output is a list of named people to talk to this week, and a count of the companies that fit.

## What you need

- **Chat only:** the list, the count and the Monday prospects done by hand (search filters and a sheet, a pasted count, a weekly chat).
- **Free:** Apollo free plan (the list, the count), a free CRM tier such as Attio or HubSpot (the list), Apify free credit (local businesses from Google Maps).
- **Runs on its own:** Claude Cowork scheduled tasks or Claude Code routines (Ten new matching prospects every Monday).
- **Paid, optional:** Clay, LinkedIn Sales Navigator.

## Before you start

Read `pmf/product-info.md` and `pmf/assumptions.md` (also check the project root, or a file attached to the conversation).

**If there is no product-info.md,** offer two routes and let the founder pick: run `pmf` first (seven questions, and every pmf skill reads the file it writes), or go straight on. Straight on: ask these in one message, and say short answers are fine:
1. What is the product, in one sentence?
2. Who is it for? B2B: the role, the type and size of company, the countries. B2C: the person, their situation, where they live.
3. What problem does it solve, in their words, and what do they do today instead?
4. What event makes the problem urgent for them right now?
5. What evidence do you have so far: conversations, sign-ups, people who said yes?

Label the answers HYPOTHESIS. At the end, output them as a short `product-info.md` for the founder to save.

Ask which technique the founder wants, or recommend one based on their evidence.

Each heading says how the technique works (chat · research · build · analyse · simulate) and, when it needs one, which building block: skill (it uses another skill), connector (it uses a connector) or schedule (runs on its own).

**Step by step.** If the founder asks to be taken through a technique, do one step at a time and stop at every hand-off. Each technique that needs the founder to act marks its steps: **Now** (what you do), **Your turn** (what the founder does; then stop and wait), **Resume** (the sentence that picks it up, in this chat or a new one), **Then** (what follows). At every stop, add one line to `product-info.md`: "Waiting for: [what], since [date]. To resume: Use prospect-list-builder to continue [the technique]." When you read a `product-info.md` that has a Waiting for line, start there: ask whether it has come in.

---

## 50 named prospects from Apollo · research · connector

Named people who match the ICP, with a reason to talk now. **Pick the route from the ICP, and say which one you picked and why:**
- **B2B with a LinkedIn footprint** (people with job titles at companies that list their staff): Apollo or Clay (below).
- **Local businesses** (shops, salons, clinics, restaurants, trades: they sit on Google Maps, rarely on LinkedIn, and seldom post about their problems): Google Maps plus the company register (after B2B).
- **B2C:** the people who posted about the problem in public (end of this section).

If the first route finds fewer than 20 matches, say so and try the next one that fits.

**If a prospecting connector is available (Apollo, Clay):**
> Using [Apollo], find 50 people who match: role: [ ] · company: [industry], [size], [country] · signal: [hired for X / raised in last 12 months / uses tool Y]. For each: name, role, company, LinkedIn URL, one line on why they match. Don't include anyone who doesn't match all three criteria; list the rejected ones and why.

If a CRM connector is available (Attio, HubSpot), offer to add them, tagged with the ICP letter. **Ask before writing to the CRM.**

**Name and profile, always.** The list is people to talk to, so every row carries the person's name and, for B2B, their LinkedIn profile URL. Take the URL from a public page that links it (team page, speaker page, press release, podcast notes) or from a web search result that shows the same name and company. Never build a URL from a name, never open or scrape LinkedIn pages. Where none is found, write "not found yet": the founder searches those names in their own LinkedIn, by hand.

**Research column** (per person, if web tools are available):
> For [name], [role] at [company]: find one thing they posted, said, hired for or launched in the last 90 days that relates to [problem area]. Return one sentence and the link. If you find nothing, return "none". Don't guess.

**Without connectors:** give the founder the exact LinkedIn / Sales Navigator search filters to use by hand, and a sheet template: name · role · company · URL · why they match · research line · ICP · status.

**Step by step:**
1. **Now:** with Apollo or Clay, pull the 50 and go to step 4. Without, write the search filters and the sheet template.
2. **Your turn (no connector):** run the search by hand and fill the first four columns for 50 people. **Stop.**
3. **Resume:** attach the sheet and say: "continue the prospect list".
4. **Then:** the research column, how the list was built, the shortlist. Adding them to the CRM waits for the founder's yes.

**Check:** the founder opens five profiles. Are these really people they'd sell to? Click five research links: an invented post quoted back to a real person ends the conversation.

**Local businesses: Google Maps plus the company register.** Apollo misses most of them; Google Maps lists nearly all of them. With a scraping connector (Apify's Google Maps scraper), run:
> Using Google Maps (via Apify), find 50 [type of business] in [cities from the ICP] that match: · [rating and review count, e.g. 4.2+, 50+ reviews] · [a visible signal, e.g. has an online booking link]. Add size from the company register: staff count or revenue from filed accounts (e.g. Belgium: KBO + National Bank; UK: Companies House). Drop anyone outside [size range]; write UNKNOWN where the register has nothing. For each: name, address, website, Instagram, one line on why they match, one recent Google review. Tag each with its ICP. Put them in a sheet. List the ones you rejected and why.

The owner is the person to talk to: take the name from the website, the register or the reviews' owner replies; where none is found, write "owner, name not found". Contact them the way they take customers (phone, booking page, Instagram, a visit), one by one.

**Without a scraping connector:** give the founder the Maps searches to run by hand (one per city) and the same sheet template, with a size column filled from the register.

**Check:** open five Maps listings. Is this really the business you'd sell to?

**B2C: people who posted about the problem.** Consumers aren't in Apollo, but many of them describe the problem in public. Go through the places from `icp-finder` (C2) (subreddits, forums, YouTube, podcasts that take listener questions, Facebook groups you can see) and list the people who wrote or showed something about it:
> In [places from `icp-finder`], find 50 people who posted, commented or made a video about [problem] in the last 90 days and who match the ICP as far as the post shows. For each: public handle or channel name · platform · link to the post · date · one line of what they said, quoted · why they match. Only public posts; no emails, no real names unless they publish under them. Skip brands and sellers. List the rejected ones and why.

The founder contacts them through the platform itself (a reply or a direct message), one by one. Keep the list to what was posted publicly, and delete it once the interviews are done.

**Show how the list was built (every route).** Report every filter as a step, with how many are left and the share of the starting number ("502, 27% of 1,879"); the first row carries no percentage. In the shortlist, what makes the person worth talking to comes first (B2C: their situation, from the post; B2B: why now), and where they were found comes last.

**Never** automate LinkedIn messaging or scraping (it violates LinkedIn's terms and risks the account). Never enrol people in email sequences. Outreach is drafted; the founder sends. EU contacts: GDPR applies to cold outreach.

### Next step: count the companies that fit, in Apollo · analyse · connector

A market size built from companies you can name.

1. Population: the result count of the ICP filter in Sales Navigator, Apollo or Crunchbase. A number the founder can screenshot.
2. If Claude Code and web tools are available: merge lists from 2–3 sources, then qualify each company from its own website against the founder's rules, including exclusion rules. Keep 5–10 data points per company.
3. Count the qualified companies.
4. Multiply by the share with the problem (from interviews, not an industry average) and what they spend today (from interviews, reviews, job ads).

Write it to the Market size section of `product-info.md`, every input with its source or GUESS. Do not use top-down industry figures.

**Check:** if the population came from a report rather than a filter the founder can show, start again.

No connector: write the ICP filter for the founder to run by hand in Apollo, Sales Navigator or Crunchbase. They paste the result count with a screenshot, and attach the company list as a CSV or paste it.

**Step by step:**
1. **Now:** write the filter and the qualifying rules, including the exclusions. With Apollo, run it and go straight on.
2. **Your turn (no connector):** run the filter, screenshot the count, export or copy the company list. **Stop.**
3. **Resume:** attach the screenshot and the list and say: "continue the company count".
4. **Then:** qualify, count, multiply. Until interviews give the share with the problem and the current spend, mark both GUESS.

Seen at: Dan Rosenthal (Workflows.io), Growth Unhinged, May 2026: bottom-up account mapping with AI qualification from company websites.

## More techniques

### Ten new matching prospects every Monday · research · schedule

Once some people have taken a call, signed up or paid: every week, find ten more like them.

Set up as a scheduled task (Claude Cowork scheduled tasks, or a Claude Code routine):
> Every Monday 8:00: read companies tagged "said yes" in [CRM]. Find 10 lookalike companies via [Apollo/Clay] and the right person at each. Research one recent post or news item per person. Draft a three-line message for each. Post the drafts to [Slack channel / a doc] for review. Do not send anything.

Seen at: Elaine Zelby, via MKT1 (2026), on Closed-Won deals.

No schedule or connectors: every Monday the founder opens a chat, attaches the "said yes" list (a CRM export, or the sheet from 50 named prospects from Apollo) and asks for ten lookalikes. Claude finds them with web search, writes the research line and drafts the messages; the founder sends.

**Step by step:**
1. **Now:** write the scheduled task (or the Monday routine by hand) and the message template, for approval.
2. **Your turn:** approve it and switch it on, or put the Monday chat in your calendar. Each week, review the drafts and send the ones you like yourself. **Stop.**
3. **Resume:** each Monday by hand, attach the "said yes" list and say: "continue the Monday prospects".
4. **Then:** ten new people, their research lines and the drafts.

---

## Output and hand-off

- Update `pmf/product-info.md` (Customer section, and Market size from the company count) and `pmf/assumptions.md` (persona rows).
- Save lists to `pmf/lists/`.
- If you can't write files, output the changed sections as a markdown block for the founder to save, and each list as a table to paste into a sheet.
- Next: usually the problem stage: is the problem real for these people? Research it with `social-listener` (P1), then book the conversations with this list using `interview-script` (P4). Torn between customers: `icp-reply-rate-test` (C4) uses ten people per variant from this list. The company count feeds `market-sizing` (S3).

## Rules (from pmf)

Nothing is evidence until a real person did something. Every number has a source or says GUESS. Every quote is verbatim or says PARAPHRASE. Never send, publish, launch, charge or spend without approval of the exact action. Update product-info.md and assumptions.md after every step. Change one thing per cycle.

---
Part of *Fast-Tracking Product-Market Fit with AI* by Gilles De Clerck (gillesdc.com).
