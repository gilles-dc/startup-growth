---
name: workaround-mapper
description: Map how people handle a startup's problem today, from YouTube videos where they show their own routine, with AI. Use when looking for workarounds, spreadsheets, Excel, Notion or Google Sheets hacks, getting timed YouTube transcripts, listing the steps, tools and time of today's routine, or quoting every moment people complain, with timestamps. Works from transcripts copied by hand too. Workshop slide P3. Part of the pmf skills; reads pmf/product-info.md.
---

# Workaround mapper (P3) — how do people handle the problem today?

Goal: the steps, tools and complaints of people handling the problem today, from videos where they explain their own routine, every quote with its timestamp. This is the qualitative stage: research makes the hypotheses checkable, and interviews put them in front of real people.

## What you need

- **Chat only:** transcripts copied by hand from "Show transcript", pasted.
- **Free:** a YouTube transcript connector (e.g. the `youtube-transcript` MCP); Gemini, to watch what's on screen.
- **Blocked to a plain web fetch:** Capterra and G2 (anti-bot protection), Google Play and YouTube (pages built in JavaScript), most of Reddit. Use the connector named in each technique; pasting by hand is the last resort.

## Before you start

Read `pmf/product-info.md` and `pmf/assumptions.md` if they exist (also check the project root, or a file attached to the conversation). If they don't exist, run the `pmf` setup, or ask: product, customer, problem in their words, what they do today instead.

**If there is no product-info.md,** offer two routes and let the founder pick: run `pmf` first (seven questions, and every pmf skill reads the file it writes), or go straight on. Straight on: ask these in one message, and say short answers are fine:
1. What is the product or idea, in one sentence?
2. Who has the problem? Role, company type or life situation.
3. What is the problem, in the words your customer would use?
4. What do they do today about it? Name the tools, competitors or workarounds: their reviews and videos are the research.

Label the answers HYPOTHESIS. At the end, output them as a short `product-info.md` for the founder to save.

Each heading says how the technique works (chat · research · build · analyse · simulate) and, when it needs one, which building block: skill (it uses another skill), connector (it uses a connector) or schedule (runs on its own).

**Step by step.** If the founder asks to be taken through a technique, do one step at a time and stop at every hand-off. Each technique that needs the founder to act marks its steps: **Now** (what you do), **Your turn** (what the founder does; then stop and wait), **Resume** (the sentence that picks it up, in this chat or a new one), **Then** (what follows). At every stop, add one line to `product-info.md`: "Waiting for: [what], since [date]. To resume: Use workaround-mapper to continue [the technique]." When you read a `product-info.md` that has a Waiting for line, start there: ask whether it has come in.

---

## Watch their workarounds on YouTube · research · connector

People film their workaround and explain it out loud.
1. Search YouTube: "how I [task] in Excel / Notion / Google Sheets", or how they handle the problem today ("no-show policy salon"). Pick 5 where someone explains their own routine; skip vendor demos. YouTube's own search shows view counts; the connector doesn't.
2. Get the transcripts with a YouTube transcript connector (e.g. the `youtube-transcript` MCP), timed, so every quote has a timestamp. Claude reads them directly. No connector: copy "Show transcript" by hand; a plain web fetch gets empty transcripts. To analyse what's on screen as well, give the links to Gemini, which watches video; keep those under about 20 minutes: on a 45-minute video Gemini has invented details that weren't there (Caitlin Sullivan, Dec 2025).
> These are transcripts of people showing how they [task] today. For each video: the steps in order · the tools · how long it takes, if they say · every workaround · every moment they complain, sigh or apologise, quoted, with its timestamp.

Auto-captions mishear names ("Booksy" became "books e-books"): keep quotes word for word and flag the mishearing in brackets. In reaction videos, note whose voice each quote is.

The workaround is the competitor you have to beat. The complaints are your copy.

**Step by step:**
1. **Now:** give the search phrases and say what makes a video worth picking. With the transcript connector, pick the five, get the transcripts and go straight on.
2. **Your turn (no connector):** pick five videos, open "Show transcript" under each and copy it into one file, with the link. **Stop.**
3. **Resume:** attach the file and say: "continue the YouTube workarounds".
4. **Then:** the read above.

---

## Output and hand-off

Write the Problem section of `pmf/product-info.md` in this format:

- **The what:** [who] has [problem], with numbers: how big, how often, how much it costs, what they resort to now.
- **The why:** why the problem exists: what current solutions offer and why that falls short; the structural gap.

Each line EVIDENCE (source) or HYPOTHESIS. Update `pmf/assumptions.md` and the Evidence table. If you can't write files, output the changed sections as a markdown block for the founder to save. Next: `interview-script` (P4), to turn the research into interview questions.

## Rules (from pmf)

Nothing is evidence until a real person did something. Every number has a source or says GUESS. Every quote is verbatim or says PARAPHRASE. Never send, publish, launch, charge or spend without approval of the exact action. Update product-info.md and assumptions.md after every step. Change one thing per cycle. Interview recordings are personal data: get consent, store them carefully, and don't upload them to tools the interviewee didn't agree to.

---
Part of *Fast-Tracking Product-Market Fit with AI* by Gilles De Clerck (gillesdc.com).
