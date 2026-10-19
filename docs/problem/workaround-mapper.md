# workaround-mapper: how do people handle the problem today?

Workshop slide P3 · stage: Problem

People film their workaround and explain it out loud. This skill finds five YouTube videos where someone shows their own routine for the problem, gets the timed transcripts, and lists the steps in order, the tools, how long it takes and every moment they complain, sigh or apologise, quoted with its timestamp. The workaround is the competitor you have to beat; the complaints are your copy. It ends with the problem written down in your customer's words, each line marked evidence or hypothesis.

New to skills? Read [Start here](../start-here.md) first.

## When to use it

- Your customers solve the problem today with a spreadsheet, Notion, paper or a patchwork of tools.
- You want to see the routine you have to replace, step by step.
- You want the words people use when the routine annoys them.

Before this, [social-listener](social-listener.md) and [review-mining](review-mining.md) find what people say and what they complain about. After it, go to [interview-script](interview-script.md). The front door is [pmf](../pmf.md).

## How to start

**Claude.ai, ChatGPT or any chat.** Type one of these:

- "Use workaround-mapper. How do people handle [task] today?"
- "Use workaround-mapper to find YouTube videos of people doing [task] in Excel."
- "Here are five transcripts. Use workaround-mapper to list the steps and every complaint."
- "Use workaround-mapper and take me through the YouTube workarounds step by step."

Naming the skill makes sure it loads. Once it's installed, a question about workarounds or how people do a task today usually loads it on its own.

**Claude Code.** Type `/pmf:workaround-mapper`, or add what you want: `/pmf:workaround-mapper how salons handle no-shows today`. If you installed it with `npx skills add`, it's `/workaround-mapper`.

## What you need

YouTube pages are built in JavaScript, so a plain web fetch gets empty transcripts. A transcript connector saves you the copying.

| Technique | Chat only | Free | Paid, optional |
|---|---|---|---|
| Watch their workarounds on YouTube | transcripts copied by hand | a YouTube transcript connector | |

## Step by step

Ask to be taken through a technique and the skill stops at every point where you have to do something. To pick it up again, attach what it asked for and say the sentence in the last column. In a new chat, put the skill's name first, so the right skill loads: "Use workaround-mapper to continue the YouTube workarounds".

| Technique | The skill does | You do | Then say |
|---|---|---|---|
| YouTube workarounds | gives the search phrases | pick five videos, copy their transcripts (skip with a connector) | "continue the YouTube workarounds" |

At each stop, the skill notes in `product-info.md` what it's waiting for, so a new chat knows where you are.

## What you get

- **Watch their workarounds on YouTube:** for each video, the steps in order, the tools, how long it takes, every workaround and every complaint, quoted with its timestamp.
- **Always:** the Problem section of `product-info.md`: who has the problem, with numbers, and why it exists.

Example: [TO ADD]

## Files it reads and writes

| File | What happens |
|---|---|
| `pmf/product-info.md` | Read first. The Problem section is written, each line marked evidence or hypothesis. |
| `pmf/assumptions.md` | Read, then updated with what the videos proved or broke. |

**Without them:** the skill offers to run [pmf](../pmf.md) first, which writes `product-info.md` and `assumptions.md` in about seven questions. Or it asks you four short questions and carries on, then gives you a `product-info.md` to save. In a plain chat that can't save files, it prints the files for you to save or add to your Claude Project.

Next step after this skill: [interview-script](interview-script.md), to turn the research into interview questions.
