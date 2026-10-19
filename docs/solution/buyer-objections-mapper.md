# buyer-objections-mapper: what do buyers ask before they buy?

Workshop slide S2 · stage: Solution

This skill reads your sales or interview calls, or your competitors' reviews when you have no calls yet, and pulls out what buyers were trying to find out before they bought. It groups the questions, counts them and quotes each one, then checks every theme against search demand and against what AI assistants answer about your category today. Where buyers ask and nobody answers well, you have a positioning opening.

New to skills? Read [Start here](../start-here.md) first.

## When to use it

- You want to know what buyers worry about before they buy.
- You need the objections your page or ads should answer.
- You have call transcripts or interview notes nobody has read for the buyer's questions.
- You want to find where the market leaves buyers without a good answer.

Calls come from [interview-script](../problem/interview-script.md) and [interview-synthesis](../problem/interview-synthesis.md); without calls, reviews from [review-mining](../problem/review-mining.md) work. After it, the questions feed the headers in [value-proposition-generator](../solution/value-proposition-generator.md) and the rows of the comparison table in [competitive-analysis](../solution/competitive-analysis.md). Not sure where to start? Use [pmf](../pmf.md).

## How to start

**Claude.ai, ChatGPT or any chat.** Type one of these:

- "Use buyer-objections-mapper. Here are our sales call transcripts. What do buyers ask before they buy?"
- "Use buyer-objections-mapper on these competitor reviews. We have no calls yet."
- "Use buyer-objections-mapper and take me through the buyer questions step by step."

Naming the skill makes sure it loads. Once it's installed, a question about buyer objections or what almost stopped people buying usually loads it on its own.

**Claude Code.** Type `/pmf:buyer-objections-mapper`, or add what you want: `/pmf:buyer-objections-mapper read the transcripts in calls/`. If you installed it with `npx skills add`, it's `/buyer-objections-mapper`.

## What you need

Works without a connector. A transcript connector saves you the export; an SEO connector adds the search-demand check.

| Technique | Chat only | Free | Paid, optional |
|---|---|---|---|
| Questions buyers ask before buying | call transcripts or reviews, attached | | DataForSEO, Ahrefs or Semrush for search demand |

## Step by step

Ask to be taken through it and the skill stops at the point where you have to do something. To pick it up again, attach what it asked for and say the sentence in the last column. In a new chat, put the skill's name first, so the right skill loads: "Use buyer-objections-mapper to continue the buyer questions".

| Technique | The skill does | You do | Then say |
|---|---|---|---|
| Buyer questions | asks whether you have sales or interview calls | export the transcripts or notes | "continue the buyer questions" |

At each stop, the skill notes in `product-info.md` what it's waiting for, so a new chat knows where you are.

## What you get

- The questions buyers ask, grouped and counted with quotes.
- For each theme, the search demand behind it and what AI assistants answer today, with their sources.
- Where buyers ask and nobody answers them well.

Example: [TO ADD]

## Files it reads and writes

| File | What happens |
|---|---|
| `pmf/product-info.md` | Read first, for your product, your customer and your quotes. Updated where the questions change a line. |
| `pmf/assumptions.md` | Read, then updated. |
| `pmf/buyer-questions.md` | Written: the grouped questions, counts, quotes and cross-check. |

**Without them:** the skill offers to run [pmf](../pmf.md) first, which writes both files in about seven questions. Or it asks you five short questions and carries on, then gives you a `product-info.md` to save. In a plain chat that can't save files, it prints the file for you to save or add to your Claude Project.

Next step after this skill: [value-proposition-generator](../solution/value-proposition-generator.md), to write headers that answer the main objection.
