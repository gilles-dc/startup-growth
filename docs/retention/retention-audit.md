# retention-audit: do they keep coming back?

Workshop slide PMF2 · stage: Retention

Once people use your product, this skill tells you whether they keep coming back. It draws your retention curve from your analytics or a spreadsheet, one line per segment, then splits the people who stay from the people who leave and shows what each group has in common. It also checks what each customer costs you to serve. It ends with the level of fit you're at and what to work on next.

New to skills? Read [Start here](../start-here.md) first.

## When to use it

- You have users or paying customers, even five.
- Sign-ups look fine but people drift away, and you don't know who or why.
- Your product runs on AI and you don't know what an active customer costs you.

Before you have users, start with [pmf](../pmf.md) instead. To ask users whether they'd miss it, use [pmf-survey](../retention/pmf-survey.md); to hear why they leave, [why-people-churn](../retention/why-people-churn.md).

## How to start

**Claude.ai, ChatGPT or any chat.** Type one of these:

- "Use retention-audit to draw our retention curve from this CSV."
- "Use retention-audit. We have PostHog connected. Are people coming back?"
- "Use retention-audit and take me through the retention curve step by step."
- "Use retention-audit to work out what each customer costs us to serve."

Naming the skill makes sure it loads. Once it's installed, a question about retention or cohorts usually loads it on its own.

**Claude Code.** Type `/pmf:retention-audit`, or add what you want: `/pmf:retention-audit draw our retention curve from users.csv`. If you installed it with `npx skills add`, it's `/retention-audit`.

## What you need

Every technique works without a connector. A connector saves you the export.

| Technique | Chat only | Free | Paid, optional |
|---|---|---|---|
| Ask your analytics about retention | a CSV export | PostHog, Mixpanel, Amplitude or GA4 connector | |
| The cost of keeping them | last month's invoices | | |

## Step by step

Ask to be taken through a technique and the skill stops at every point where you have to do something. To pick it up again, attach what it asked for and say the sentence in the last column. In a new chat, put the skill's name first, so the right skill loads: "Use retention-audit to continue the retention curve".

| Technique | The skill does | You do | Then say |
|---|---|---|---|
| Retention | agrees what counts as active, names the CSV columns | export the CSV (skip with a connector) | "continue the retention curve" |

At each stop, the skill notes in `product-info.md` what it's waiting for, so a new chat knows where you are.

## What you get

- **Retention:** the retention curve as a chart, one line per segment, then who stays and who leaves, what each group has in common, and three questions for your next interviews, on one page.
- **The cost of keeping them:** cost, price and margin per customer segment.
- **Always:** which level of fit you're at (from 3–5 customers up to 100+) and what to work on at that level.

Example: [TO ADD]

## Files it reads and writes

| File | What happens |
|---|---|
| `pmf/product-info.md` | Read first, for your customer types and what counts as value. Updated with the retention findings, the margin per segment and your level of fit. |
| `pmf/assumptions.md` | Read, then updated with what the results proved or broke. |

**Without them:** the skill offers to run [pmf](../pmf.md) first, which writes both files in about seven questions. Or it asks you five short questions and carries on, then gives you a `product-info.md` to save. In a plain chat that can't save files, it prints the file for you to save or add to your Claude Project.

Next step after this skill: [why-people-churn](../retention/why-people-churn.md), to hear from the people who leave; then [pivot-or-persevere](../iterate/pivot-or-persevere.md) and [weekly-product-bets](../iterate/weekly-product-bets.md), to decide what to change.
