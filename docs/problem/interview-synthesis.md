# interview-synthesis: what did the interviews tell us?

Workshop slide P5 · stage: Problem

This skill reads your interview transcripts or notes one interview at a time with a fixed template, then builds a table of pains across all of them, sorted by whether people spent money or time on it, with the surprises and what contradicts your assumptions. Then it checks every quote against the transcripts and keeps only the ones it found word for word. It can also send the four Van Westendorp price questions to the people you interviewed and read the price range they find acceptable. It ends with the problem written down in your customer's words, with numbers.

New to skills? Read [Start here](../start-here.md) first.

## When to use it

- You have interview transcripts or notes and want the patterns, with quotes you can trust.
- You want to know what people said that you didn't ask about, and what breaks your assumptions.
- The people you interviewed described the problem and you want to know what they'd pay.

Before this, use [interview-script](interview-script.md) for the questions and the invites. After it, go to the solution stage, from [competitive-analysis](../solution/competitive-analysis.md) to [value-proposition-generator](../solution/value-proposition-generator.md), or [pivot-or-persevere](../iterate/pivot-or-persevere.md) if the interviews changed what you believe. The front door is [pmf](../pmf.md).

## How to start

**Claude.ai, ChatGPT or any chat.** Type one of these:

- "Use interview-synthesis. Here are my interview transcripts: find the patterns."
- "Use interview-synthesis to check every quote in this summary against the transcripts."
- "Use interview-synthesis and take me through the interview patterns step by step."
- "Use interview-synthesis to ask the people I interviewed the price question."

Naming the skill makes sure it loads. Once it's installed, a question about interview transcripts, synthesis or quotes usually loads it on its own.

**Claude Code.** Type `/pmf:interview-synthesis`, or add what you want: `/pmf:interview-synthesis read the transcripts in pmf/interviews`. If you installed it with `npx skills add`, it's `/interview-synthesis`.

## What you need

Every technique works without a connector. A connector saves you the export.

| Technique | Chat only | Free | Paid, optional |
|---|---|---|---|
| Patterns across interviews | transcripts or notes, attached | Granola, Fireflies or Otter free tiers | |
| Check every quote | in the chat | | |
| The price question | the four questions, pasted into Google Forms or any form tool | Tally connector | |

## Step by step

Ask to be taken through a technique and the skill stops at every point where you have to do something. To pick it up again, attach what it asked for and say the sentence in the last column. In a new chat, put the skill's name first, so the right skill loads: "Use interview-synthesis to continue the interview patterns".

| Technique | The skill does | You do | Then say |
|---|---|---|---|
| Patterns | says how to get the transcripts out | put them in one folder (skip with a connector) | "continue the interview patterns" |
| Price question | writes the four questions and the message | send them, wait for answers | "continue the price question" |

At each stop, the skill notes in `product-info.md` what it's waiting for, so a new chat knows where you are.

## What you get

- **Patterns across interviews and Check every quote:** one summary per interview, then a table of pains across all of them, using only quotes checked against the transcripts, and the count of quotes it could not find.
- **The price question:** the price range people find acceptable, the four curves, and the answers that don't add up.
- **Always:** the Problem section of `product-info.md`: who has the problem, with numbers, and why it exists.

Example: [TO ADD]

## Files it reads and writes

| File | What happens |
|---|---|
| `pmf/product-info.md` | Read first. The Problem section is written, each line marked evidence or hypothesis. |
| `pmf/assumptions.md` | Read, then updated with what the interviews proved or broke. |
| `pmf/interviews/` | One note per interview. |
| `pmf/synthesis.md` | The patterns across interviews, verified quotes only. |

**Without them:** the skill offers to run [pmf](../pmf.md) first, which writes `product-info.md` and `assumptions.md` in about seven questions. Or it asks you five short questions and carries on, then gives you a `product-info.md` to save. In a plain chat that can't save files, it prints the files for you to save or add to your Claude Project.

Next step after this skill: the solution stage, from [competitive-analysis](../solution/competitive-analysis.md) to [value-proposition-generator](../solution/value-proposition-generator.md), to shape the promise, or [pivot-or-persevere](../iterate/pivot-or-persevere.md) if the interviews changed what you believe.
