---
name: icp-finder
description: Find every place where a startup's ideal customers talk shop, online and offline — subreddits and forums, Discord, Slack and Telegram communities, Facebook and LinkedIn groups, Instagram, TikTok and YouTube accounts, podcasts, newsletters, events and meetups — with working links, ranked by how close the talk is to the problem. Use when a founder asks where their customers hang out, which communities to join, where to find people to interview, or wants to complete the WHERE line of their ICP. Workshop slide C2. Part of the pmf skills; reads pmf/product-info.md.
---

# ICP finder (C2) — where do they hang out?

Goal: every place where the ICP talks shop, online and offline, with links that work, and a top ten the founder can join this week.

## What you need

- **Chat only:** a chat with web search.
- **Free:** web access to open and check every link.
- **Optional:** a scraping connector, for Reddit; the `where-your-customer-lives` skill (Varnan-Tech/opendirectory).

## Before you start

Read `pmf/product-info.md` and `pmf/assumptions.md` (also check the project root, or a file attached to the conversation).

**If there is no product-info.md,** offer two routes and let the founder pick: run `pmf` first (seven questions, and every pmf skill reads the file it writes), or go straight on. Straight on: ask these in one message, and say short answers are fine:
1. What is the product, in one sentence?
2. Who is it for? B2B: the role, the type and size of company, the countries. B2C: the person, their situation, where they live.
3. What problem does it solve, in their words, and what do they do today instead?
4. What event makes the problem urgent for them right now?
5. What evidence do you have so far: conversations, sign-ups, people who said yes?

Label the answers HYPOTHESIS. At the end, output them as a short `product-info.md` for the founder to save.

Each heading says how the technique works (chat · research · build · analyse · simulate) and, when it needs one, which building block: skill (it uses another skill), connector (it uses a connector) or schedule (runs on its own).

---

## Where your customers hang out online · research · skill

Find every place where the ICP talks shop, with links that work. The ICP's WHERE line is the starting point; this technique makes it complete.

**Cover every type, and search each one on its own:**
- Forums: subreddits, Hacker News, niche forums, Stack Exchange sites.
- Chat communities: Discord servers, Slack groups, Telegram and WhatsApp groups. Search the public directories, not only the web: for Discord disboard.org, discord.me, top.gg and discadia.com; for Slack slofile.com and web searches for "join our Slack" pages; for Telegram tgstat.com. Many are only reachable through an invite page or the organisation that runs them.
- Social: Facebook groups, LinkedIn groups, Instagram, TikTok and YouTube accounts the ICP follows.
- Audio and email: podcasts, newsletters, Substacks.
- In person: events, conferences, meetups, trade fairs.

> Find where [ICP, one sentence] talk shop, online and offline. Search each of these types separately: subreddits and forums · Discord, Slack, Telegram and WhatsApp communities · Facebook and LinkedIn groups · Instagram, TikTok and YouTube accounts · podcasts · newsletters · events and meetups. For each place: name · link · type · country or language · approximate size (only if stated publicly, else UNKNOWN) · one thread, post or episode from the last 90 days where they discussed [problem], with its link, or "none". Only include places you found a working link for. Aim for 20–40; list every one you found, grouped by type.

Then rank the top ten by how close the talk is to the problem and how reachable the place is, with **the best place of each type first** (the strongest forum, chat community, social account, podcast, newsletter, event), then the rest by rank, so the ten don't collapse into one platform. Say per type what you could not search (for example private Facebook groups). Give each ranked place its **type** (subreddit, trade association, podcast, Slack community, event…) and a **relevance** line: why it is on the list, in one phrase the founder can check ("People describe the exact problem, every week").

If a web-fetch or scraping tool is available, open every link yourself and drop dead ones. Most AI web tools can't open Reddit: use a scraping connector, or say Reddit wasn't checked. If the ICP gathers where search can't reach (DMs, WhatsApp groups, in person), say so, and list reachable proxies: directories and booking platforms that list them, trade associations, trade fairs, suppliers. Never invent a group name. If the `where-your-customer-lives` skill (Varnan-Tech/opendirectory) is installed, use it first: it searches Reddit, HN, GitHub issues, G2 and Google Trends and returns an ICP and positioning doc plus the channels ranked by where the ICP actually is.

**Check:** the founder opens every link and joins three. Read before posting. People complaining about the problem in those places are the first interview candidates.

---

## Output and hand-off

- Update `pmf/product-info.md` (Customer section, WHERE) and `pmf/assumptions.md` (persona rows).
- Save the places to `pmf/lists/`.
- If you can't write files, output the changed sections as a markdown block for the founder to save, and the places as a table to paste into a sheet.
- Next: `prospect-list-builder` (C3), for named people in these places. Then the problem stage: is the problem real for these people? Research it with `social-listener` (P1).

## Rules (from pmf)

Nothing is evidence until a real person did something. Every number has a source or says GUESS. Every quote is verbatim or says PARAPHRASE. Never send, publish, launch, charge or spend without approval of the exact action. Update product-info.md and assumptions.md after every step. Change one thing per cycle.

---
Part of *Fast-Tracking Product-Market Fit with AI* by Gilles De Clerck (gillesdc.com).
