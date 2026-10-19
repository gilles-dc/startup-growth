# pmf-survey: would they miss it?

Workshop slide PMF1 · stage: Retention

Once people use your product, this skill finds who would miss it most and why. It runs Sean Ellis's product-market fit survey and reads it the way Superhuman did: split by segment, the group that would be very disappointed, the benefit they name and what holds the near-fans back. Then, per segment, 40% very disappointed is the gate to grow: under it, keep iterating; over it, that segment is ready for acquisition. With fewer than about 40 active users it sends you to interviews instead. It can also read every piece of open feedback at once and group your customers into types from their support emails. It ends with the level of fit you're at and what to work on next.

New to skills? Read [Start here](../start-here.md) first.

## When to use it

- You have users or paying customers, even five.
- You want to know if you have product-market fit, or which customers you have it with.
- You have a pile of feedback or support emails nobody has read in one go.

Before you have users, start with [pmf](../pmf.md) instead. To see whether people keep coming back, use [retention-audit](../retention/retention-audit.md); to hear why they leave, [why-people-churn](../retention/why-people-churn.md).

## How to start

**Claude.ai, ChatGPT or any chat.** Type one of these:

- "Use pmf-survey. We have about 60 active users. Do we have product-market fit?"
- "Use pmf-survey and take me through the PMF survey step by step."
- "Use pmf-survey to analyse this survey export."
- "Use pmf-survey to read all our feedback in one go."

Naming the skill makes sure it loads. Once it's installed, a question about product-market fit or the PMF survey usually loads it on its own.

**Claude Code.** Type `/pmf:pmf-survey`, or add what you want: `/pmf:pmf-survey take me through the PMF survey`. If you installed it with `npx skills add`, it's `/pmf-survey`.

## What you need

Every technique works without a connector. A connector saves you the export.

| Technique | Chat only | Free | Paid, optional |
|---|---|---|---|
| The PMF survey | the survey as text, pasted into Google Forms or any form tool | Tally connector | Typeform |
| Read all the feedback | your exports, attached | | |
| Customer types from their emails | an inbox or help-desk export | an email connector | |

## Step by step

Ask to be taken through a technique and the skill stops at every point where you have to do something. To pick it up again, attach what it asked for and say the sentence in the last column. In a new chat, put the skill's name first, so the right skill loads: "Use pmf-survey to continue the PMF survey".

| Technique | The skill does | You do | Then say |
|---|---|---|---|
| PMF survey | writes the survey and the invitation | publish it, send it to active users, wait for about 40 answers | "continue the PMF survey" |
| Feedback | lists your sources and how to export each | export them into one folder | "continue the feedback read" |
| Customer types | says what to export and from where | export, take out anything private | "continue the customer types" |

At each stop, the skill notes in `product-info.md` what it's waiting for, so a new chat knows where you are.

## What you get

- **The PMF survey:** the answers split by segment with counts, the group that would be very disappointed (your real customer), the benefit they name (your promise), what holds back the near-fans (your roadmap), and per segment whether it passes the 40% gate to grow.
- **Feedback and customer types:** themes with counts and quotes; for customer types, promoters and detractors marked.
- **Always:** which level of fit you're at (from 3–5 customers up to 100+) and what to work on at that level.

Example: [TO ADD]

## Files it reads and writes

| File | What happens |
|---|---|
| `pmf/product-info.md` | Read first, for your customer types. Updated with the score and your level of fit, and with a sharper customer if the very disappointed group says so. |
| `pmf/assumptions.md` | Read, then updated with what the results proved or broke. |

**Without them:** the skill offers to run [pmf](../pmf.md) first, which writes both files in about seven questions. Or it asks you four short questions and carries on, then gives you a `product-info.md` to save. In a plain chat that can't save files, it prints the file for you to save or add to your Claude Project.

Next step after this skill: [retention-audit](../retention/retention-audit.md), to see whether they keep coming back; then [pivot-or-persevere](../iterate/pivot-or-persevere.md) and [weekly-product-bets](../iterate/weekly-product-bets.md), to decide what to change.
