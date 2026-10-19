# social-listener: what are people saying about the problem?

Workshop slide P1 · stage: Problem

This skill finds what people said about your problem this month on Reddit, Hacker News, forums and social media, and counts every pain that recurs, with quotes word for word. It can also run deep research with a source table you can open line by line, compare two research tools, have the AI write a scraper for thousands of posts, sort every post by pain, and rate your idea on six dimensions, saying INSUFFICIENT DATA where nothing was found. It ends with the first lines of the problem in your customer's words, each marked evidence or hypothesis.

New to skills? Read [Start here](../start-here.md) first.

## When to use it

- You know who your customer is and want to know if their problem is worth solving.
- You want to hear how people describe the problem in their own words, before you talk to any of them.
- You want research with sources you can open, and every number marked as checked or guessed.
- You have thousands of posts or comments and no time to read them.

Before this, if you don't know who the customer is yet, use [icp](../customer/icp.md), or start at the front door, [pmf](../pmf.md). After it, go to [review-mining](review-mining.md), [workaround-mapper](workaround-mapper.md), then [interview-script](interview-script.md).

## How to start

**Claude.ai, ChatGPT or any chat.** Type one of these:

- "Use social-listener. What are people saying about the problem my startup solves?"
- "Use social-listener to find Reddit threads where people ask for a tool like mine."
- "Use social-listener to research the problem with a source table I can check."
- "Use social-listener and take me through the two research reports step by step."

Naming the skill makes sure it loads. Once it's installed, a question about pain points, Reddit threads or problem research usually loads it on its own.

**Claude Code.** Type `/pmf:social-listener`, or add what you want: `/pmf:social-listener what do people complain about when booking a plumber?`. If you installed it with `npx skills add`, it's `/social-listener`.

## What you need

Most techniques work in a plain chat. A connector saves you the copying and pasting.

| Technique | Chat only | Free | Paid, optional |
|---|---|---|---|
| What people said this month | fallback: the search strings, run with web search (no Reddit comments, X or TikTok) | last30days, installed with the workshop: the engine | |
| Research with sources you can check | | your AI's research mode | |
| Two research tools, side by side | | two research modes, e.g. Claude Research and ChatGPT deep research | |
| Have the AI write your scraper | | Claude Code | |
| Sort every post by pain | | Claude Code | |
| Rate your idea on six dimensions | | your AI's research mode | |

## Step by step

Ask to be taken through a technique and the skill stops at every point where you have to do something. To pick it up again, attach what it asked for and say the sentence in the last column. In a new chat, put the skill's name first, so the right skill loads: "Use social-listener to continue the two research reports".

| Technique | The skill does | You do | Then say |
|---|---|---|---|
| Two research tools | fills in the research brief | run it in two tools, save both reports | "continue the two research reports" |

At each stop, the skill notes in `product-info.md` what it's waiting for, so a new chat knows where you are.

## What you get

- **What people said this month:** every pain that recurs, with how many posts mention it and its strongest quote, word for word.
- **Research with sources you can check and Two research tools:** a source table you can open line by line, and the claims only one tool made.
- **Have the AI write your scraper and Sort every post by pain:** thousands of posts, each labelled by pain, segment and intensity, then clusters with counts and a quote per cluster.
- **Rate your idea on six dimensions:** HIGH, MED or LOW per dimension, or INSUFFICIENT DATA where nothing was found: that's where you go and talk to people.
- **Always:** the Problem section of `product-info.md`: who has the problem, with numbers, and why it exists.

Example: [TO ADD]

## Files it reads and writes

| File | What happens |
|---|---|
| `pmf/product-info.md` | Read first. The Problem section is written, each line marked evidence or hypothesis. |
| `pmf/assumptions.md` | Read, then updated with what the research proved or broke. |

**Without them:** the skill offers to run [pmf](../pmf.md) first, which writes `product-info.md` and `assumptions.md` in about seven questions. Or it asks you four short questions and carries on, then gives you a `product-info.md` to save. In a plain chat that can't save files, it prints the files for you to save or add to your Claude Project.

Next step after this skill: [review-mining](review-mining.md) for your competitors' bad reviews, [workaround-mapper](workaround-mapper.md) for how people handle the problem today, then [interview-script](interview-script.md) to turn the research into interview questions.
