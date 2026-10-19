# why-people-churn: why do they leave?

Workshop slide PMF3 · stage: Retention

Once people pay for your product, this skill asks everyone who cancels, or goes quiet for 30 days, one question: what were you hoping it would do that it didn't? It sets that up as an automation or a sheet you fill by hand, then groups the replies every month, each labelled fixable for your customer, fixable for another segment, wrong customer, or neither. It ends with the level of fit you're at and what to work on next.

New to skills? Read [Start here](../start-here.md) first.

## When to use it

- You have paying customers, and some of them cancel.
- People drift away, and you don't know why.
- You have cancel reasons nobody has read in one go.

Before you have users, start with [pmf](../pmf.md) instead. To see who stays and who leaves on a retention curve, use [retention-audit](../retention/retention-audit.md).

## How to start

**Claude.ai, ChatGPT or any chat.** Type one of these:

- "Use why-people-churn to set up a cancel question for our Stripe customers."
- "Use why-people-churn and take me through the cancel reasons step by step."
- "Use why-people-churn to group this month's cancel replies."

Naming the skill makes sure it loads. Once it's installed, a question about churn or why customers cancel usually loads it on its own.

**Claude Code.** Type `/pmf:why-people-churn`, or add what you want: `/pmf:why-people-churn group the replies in cancels.csv`. If you installed it with `npx skills add`, it's `/why-people-churn`.

## What you need

Every technique works without a connector. A connector saves you the export.

| Technique | Chat only | Free | Paid, optional |
|---|---|---|---|
| Ask everyone who cancels why | the question in your cancel screen; without an app, by hand by email | PostHog surveys, Tally, Stripe customer portal; n8n for the email fallback | Typeform, Chargebee, Paddle; Zapier or Make |

## Step by step

Ask to be taken through a technique and the skill stops at every point where you have to do something. To pick it up again, attach what it asked for and say the sentence in the last column. In a new chat, put the skill's name first, so the right skill loads: "Use why-people-churn to continue the cancel reasons".

| Technique | The skill does | You do | Then say |
|---|---|---|---|
| Cancel reasons | writes the question and the cancel-flow setup (or the email, without an app) | add it to the cancel flow, switch it on, wait a month | "continue the cancel reasons" |

At each stop, the skill notes in `product-info.md` what it's waiting for, so a new chat knows where you are.

## What you get

- **Cancel reasons:** grouped each month, each labelled fixable for your customer, fixable for another segment, wrong customer, or neither.
- **Always:** which level of fit you're at (from 3–5 customers up to 100+) and what to work on at that level.

Example: [TO ADD]

## Files it reads and writes

| File | What happens |
|---|---|
| `pmf/product-info.md` | Read first, for your customer types and what counts as value. Updated with the grouped cancel reasons and your level of fit, and with a sharper customer when a "wrong customer" answer says so. |
| `pmf/assumptions.md` | Read, then updated with what the results proved or broke. |

**Without them:** the skill offers to run [pmf](../pmf.md) first, which writes both files in about seven questions. Or it asks you five short questions and carries on, then gives you a `product-info.md` to save. In a plain chat that can't save files, it prints the file for you to save or add to your Claude Project.

Next step after this skill: [retention-audit](../retention/retention-audit.md), to join the cancel reasons to the people who left; then [pivot-or-persevere](../iterate/pivot-or-persevere.md) and [weekly-product-bets](../iterate/weekly-product-bets.md), to decide what to change.
