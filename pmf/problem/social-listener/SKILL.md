---
name: social-listener
description: Find out what people say about a startup's problem online, with AI. Use when looking for pain points on Reddit, Hacker News, forums or social media, running last30days as its search engine, searching "I wish there was" or "[competitor] alternative" threads, counting how often each pain recurs, running deep research with a source table you can check, comparing two research tools, scraping thousands of posts, sorting posts by pain, or rating an idea on six dimensions. Workshop slide P1. Part of the pmf skills; reads pmf/product-info.md.
---

# Social listener (P1) — what are people saying about the problem?

Goal: the customer's world without the product, in their words, with numbers, starting from sources: what people said about the problem this month, ranked by engagement, with every pain that recurs counted. This is the qualitative stage: research makes the hypotheses checkable, and interviews put them in front of real people.

## What you need

- **Installed with the workshop:** the last30days skill (mvanhorn/last30days-skill), the engine for What people said this month. Reddit (with comments and upvotes), Hacker News and GitHub work without a key; its setup wizard adds X, YouTube and TikTok.
- **Fallback, any chat:** where last30days can't run (ChatGPT, or Claude.ai without the upload), What people said this month runs on web search with the search strings below. Narrower: no Reddit comments, X or TikTok.
- **Free:** your AI's research mode (Research with sources you can check, Two research tools, Rate your idea on six dimensions), Claude Code (Have the AI write your scraper, Sort every post by pain).
- **Blocked to a plain web fetch:** Capterra and G2 (anti-bot protection), Google Play and YouTube (pages built in JavaScript), most of Reddit. Use the connector named in each technique; pasting by hand is the last resort.

## Before you start

Read `pmf/product-info.md` and `pmf/assumptions.md` if they exist (also check the project root, or a file attached to the conversation). If they don't exist, run the `pmf` setup, or ask: product, customer, problem in their words, what they do today instead.

**If there is no product-info.md,** offer two routes and let the founder pick: run `pmf` first (seven questions, and every pmf skill reads the file it writes), or go straight on. Straight on: ask these in one message, and say short answers are fine:
1. What is the product or idea, in one sentence?
2. Who has the problem? Role, company type or life situation.
3. What is the problem, in the words your customer would use?
4. What do they do today about it? Name the tools, competitors or workarounds: their reviews and videos are the research.

Label the answers HYPOTHESIS. At the end, output them as a short `product-info.md` for the founder to save.

Recommend the techniques that fit the founder's situation. A typical first pass in the problem stage: Research with sources you can check + Two research tools + What people said this month (this skill) → Price the problem → Turn research into interview questions (`interview-script`, P4), then the Interview script → Interview invites → Patterns across interviews → Check every quote (`interview-synthesis`, P5).

Each heading says how the technique works (chat · research · build · analyse · simulate) and, when it needs one, which building block: skill (it uses another skill), connector (it uses a connector) or schedule (runs on its own).

**Step by step.** If the founder asks to be taken through a technique, do one step at a time and stop at every hand-off. Each technique that needs the founder to act marks its steps: **Now** (what you do), **Your turn** (what the founder does; then stop and wait), **Resume** (the sentence that picks it up, in this chat or a new one), **Then** (what follows). At every stop, add one line to `product-info.md`: "Waiting for: [what], since [date]. To resume: Use social-listener to continue [the technique]." When you read a `product-info.md` that has a Waiting for line, start there: ask whether it has come in.

---

## What people said this month · research · skill

What people said about the problem this month, ranked by engagement.
- **Engine: last30days.** It installs with the workshop skills. Run `/last30days [problem in plain words]` (in Claude Code: `/last30days:last30days`), once for the problem in the customer's words and once per main competitor ("[competitor] alternative"). It searches the last 30 days across Reddit, X, YouTube, TikTok, Hacker News and GitHub and scores what it finds by engagement. If it isn't installed, say so once and give the founder the install line (`/plugin install last30days@gilles-dc` in Claude Code; the `last30days.skill` file for Claude.ai), then carry on with the fallback.
- **Fallback, web search only:** search with these strings and analyse the threads:
```
site:reddit.com "I wish there was" [topic]
site:reddit.com "is there a tool that" [task]
site:reddit.com "how do you guys" [task]
"[competitor] alternative"
"[competitor]" "switched to"
```
> For each thread (from last30days or the fallback): each pain mentioned · the exact quote · the username · what they say they use today. Only from the text.

Then count the patterns: every pain that recurs, with how many items carry it ("12 of 60") and its strongest quote. Report every pattern you counted, all of them (usually 5–8), not a top few.

Note for the founder: Reddit is restricting API access from November 2026 (RSS ends 13 Nov 2026, broader public API access in 2027), so Reddit-based tools and monitors may stop working.

## More techniques

### Research with sources you can check · research · 10 min

Deep research you can check line by line. Use the research tool available (Claude Research, web search) and follow this brief exactly:

> Research [problem] for [ICP].
> First, show me your research plan. Wait for my OK.
> Source priority: 1. primary data, studies, filings · 2. industry reports · 3. news · 4. social posts (opinion only, never as fact).
> End with a source table: claim · number · source URL · the exact sentence it comes from. If you can't find a source, write UNKNOWN. Don't estimate. Separate what was measured from what is someone's opinion. List what you could not find.

If you could not open a source page yourself (only a search snippet), mark its row NOT VERIFIED.

**Check:** the founder opens three links and reads the sentence. If one isn't there, treat every number in the report as a guess until checked. (Deloitte refunded part of a $290k Australian government contract in 2025 over a report citing papers and a court quote that don't exist.)

Seen at: Torsten Walbaum, Growth Unhinged (Aug 2025): plan first, source priorities, source table.

### Two research tools, side by side · research

1. Run the brief from Research with sources you can check in two tools (e.g. Claude Research and ChatGPT deep research).
2. Paste both reports in and run:
> List every claim only one report makes, and every number the two reports disagree on, with both sources. Then list what both reports failed to find.
3. Disagreements and joint gaps go to Turn research into interview questions, in `interview-script` (P4).

**Step by step:**
1. **Now:** fill in the brief from Research with sources you can check, ready to paste into both tools.
2. **Your turn:** run it in each tool and save both reports. **Stop.**
3. **Resume:** attach the two reports and say: "continue the two research reports".
4. **Then:** the comparison above; disagreements and gaps go to `interview-script` (P4).

### Have the AI write your scraper · build (Claude Code)

When there's too much to read by hand: have Claude Code write a script that collects every post, comment or review about the problem from a source the founder is allowed to collect from. Respect terms of service and rate limits; avoid personal data. The result is thousands of rows to work with, ready for Sort every post by pain.

Seen at: Amir Klein (monday.com), How I AI, Oct 2025: a 34,000-row Reddit dataset, built with no coding background.

### Sort every post by pain · analyse

1. Label every item with a cheap, fast model: pain type · segment · intensity · current workaround.
2. Reason over the labelled table with a strong model: clusters, counts, the strongest quote per cluster with a link.

Brute-forcing everything through the strongest model is what makes this expensive. Seen at: Claire Vo, How I AI, Sept 2026: ~200,000 classifications for about $4 with a cheap classifier, then a frontier model for reasoning.

### Rate your idea on six dimensions · research · skill

A check that admits what it couldn't find. Rate: problem frequency · problem severity · current spend · competition · willingness to switch · reachability of the ICP. Each HIGH / MED / LOW or **INSUFFICIENT DATA**, with citations. INSUFFICIENT DATA is the useful answer: that's where the founder goes and talks to people.

Seen at: Eddie Larsen's `/validate` skill (Medium, May 2026).

---

## Output and hand-off

Write the Problem section of `pmf/product-info.md` in this format:

- **The what:** [who] has [problem], with numbers: how big, how often, how much it costs, what they resort to now.
- **The why:** why the problem exists: what current solutions offer and why that falls short; the structural gap.

Each line EVIDENCE (source) or HYPOTHESIS. Update `pmf/assumptions.md` and the Evidence table. If you can't write files, output the changed sections as a markdown block for the founder to save. Next: `review-mining` (P2) for competitors' bad reviews, `workaround-mapper` (P3) for how people handle it today, then `interview-script` (P4) to turn the research into interview questions.

## Rules (from pmf)

Nothing is evidence until a real person did something. Every number has a source or says GUESS. Every quote is verbatim or says PARAPHRASE. Never send, publish, launch, charge or spend without approval of the exact action. Update product-info.md and assumptions.md after every step. Change one thing per cycle. Interview recordings are personal data: get consent, store them carefully, and don't upload them to tools the interviewee didn't agree to.

---
Part of *Fast-Tracking Product-Market Fit with AI* by Gilles De Clerck (gillesdc.com).
