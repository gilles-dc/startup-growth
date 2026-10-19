# icp: who is this person?

Workshop slide C1 · stage: Customer

This skill turns "SMEs" or "young professionals" into one person a stranger could go and find. Give it your product in one sentence and it drafts all of Gilles De Clerck's five dimensions, WHO, WHAT, WHY, HOW and WHERE, for B2B or B2C: every sub-question answered in a table. Then you correct the draft; it holds your corrections to the same standard and pushes back when one makes the person vaguer. Then it compresses the tables into a one-slide ICP. It ends with how many of these people exist and the answers you're least sure of, which become your interview agenda. The ICP is your starting hypothesis: interviews prove or change it later. Once it's written, it can fill the ICP in with what customers published about themselves in reviews and job ads.

New to skills? Read [Start here](../start-here.md) first.

## When to use it

- Your customer is still a category: "SMEs", "young professionals", "anyone with a phone".
- You're about to run interviews and need to know who to talk to.
- You have an ICP and want to check whether it's specific enough.
- You want to fill the Customer section of your `product-info.md`.

No product file yet? Start with [pmf](../pmf.md). Torn between several possible customers? Run [icp-reply-rate-test](../customer/icp-reply-rate-test.md) first and let reply rates pick one. After this, find the places with [icp-finder](../customer/icp-finder.md) and the people with [prospect-list-builder](../customer/prospect-list-builder.md), and turn your least-sure answers into interview questions with [interview-script](../problem/interview-script.md).

## How to start

**Claude.ai, ChatGPT or any chat.** Type one of these:

- "Use icp. Help me define my ideal customer."
- "Use icp. My product, in one sentence: … Draft it, then I'll correct you."
- "Use icp and take me through the five dimensions, one at a time."
- "Use icp to check my ICP: is it specific enough?"

Naming the skill makes sure it loads. Once it's installed, a question about your ideal customer or customer profile usually loads it on its own.

**Claude Code.** Type `/pmf:icp`, or add what you want: `/pmf:icp define the ideal customer for my B2B tool`. If you installed it with `npx skills add`, it's `/icp`.

## What you need

Works in any chat. Web access helps for WHERE, to check that the names exist.

| Technique | Chat only | Free | Paid, optional |
|---|---|---|---|
| 1. WHO | yes | | |
| 2. WHAT | yes | | |
| 3. WHY | yes | | |
| 4. HOW | yes | | |
| 5. WHERE | names marked UNCHECKED, for you to open | web search, to check every name exists | |
| How many of these people exist | a number you give, with its source | web search, for a number with a source | |
| Sharpen the ICP with what customers published | 50–100 reviews and 20 job ads, pasted | | a scraping connector (Apify, Bright Data) to collect the reviews |

## Step by step

Ask to be taken through a technique and the skill stops at every point where you have to do something. To pick it up again, attach what it asked for and say the sentence in the last column. In a new chat, put the skill's name first, so the right skill loads: "Use icp to continue the ICP sharpening".

| Technique | The skill does | You do | Then say |
|---|---|---|---|
| Sharpen the ICP | says which reviews and job ads to collect | copy them into one file | "continue the ICP sharpening" |

At each stop, the skill notes in `product-info.md` what it's waiting for, so a new chat knows where you are.

## What you get

- **The five tables:** every sub-question of WHO, WHAT, WHY, HOW and WHERE answered in one or two dense sentences, with numbers and names.
- **The one-slide ICP:** five lines, one per dimension, keeping the numbers, the names, the trigger and what sets this person apart.
- **The beachhead:** roughly how many people or companies fit exactly, with the source. This is the group to focus on until you have product-market fit with them.
- **The interview agenda:** the three to five answers you're least sure of, and that would change the most if they were wrong.
- **Sharpen the ICP:** a table of what the job ads have in common, new detail in your ICP with the source next to each, and what contradicts it listed as questions for your interviews.

Example: [TO ADD]

## Files it reads and writes

| File | What happens |
|---|---|
| `pmf/product-info.md` | Read first if it exists. The Customer section (WHO · WHAT · WHY · HOW · WHERE) is written with the tables and the summary, marked as the starting hypothesis. Sharpening adds detail there, with sources. |
| `pmf/assumptions.md` | The persona rows are updated with what the sharpening found. |

**Without them:** the skill offers to run [pmf](../pmf.md) first, which writes the file in about seven questions. Or it asks for three lines (the product, B2B or B2C, the market), drafts the rest, then gives you a `product-info.md` with your ICP in it to save. In a plain chat that can't save files, it prints the Customer section for you to save or add to your Claude Project.

Next step after this skill: [icp-finder](../customer/icp-finder.md) and [prospect-list-builder](../customer/prospect-list-builder.md), to find the places and the people to ask; [interview-script](../problem/interview-script.md), to turn your least-sure answers into interview questions.
