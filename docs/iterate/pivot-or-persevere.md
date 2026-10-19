# pivot-or-persevere: what changes?

Workshop slide I2 · stage: Iterate

This skill makes you lift your head up from the work. It lists everything your plan rests on that is still an assumption, sets each against the evidence so far and gives it a verdict: verified (you know it), open (you don't yet) or pivot (the evidence goes against it). For every open one it names the test that turns it into an answer, with the pass line set before it runs, and puts the riskiest first. The decision, pivot or persevere, sits under the table. It can also propose five pivots that each change one thing, and update your assumption board, change by change, for you to approve.

New to skills? Read [Start here](../start-here.md) first.

## When to use it

- You finished interviews or a test and want to know what they changed.
- You're deciding whether to pivot, and to what.
- Your assumption board needs updating with this cycle's evidence.

No evidence yet? Get some first with [interview-script](../problem/interview-script.md) (conversations) or with [ad-trigger-test](../test/ad-trigger-test.md) and [value-proposition-test](../test/value-proposition-test.md) (a market test). After this skill, go back to the stage the decision points to. Not sure where you are? Start at the front door, [pmf](../pmf.md).

## How to start

**Claude.ai, ChatGPT or any chat.** Type one of these:

- "Use pivot-or-persevere: what are we still assuming, and how do we test it?"
- "Use pivot-or-persevere to write a memo from our test results."
- "Use pivot-or-persevere. Here are this week's interview notes. Should we pivot?"
- "Use pivot-or-persevere to update my assumption board with this cycle's evidence."
- "Use pivot-or-persevere and give me five pivots that each change one thing."

Naming the skill makes sure it loads.

**Claude Code.** Type `/pmf:pivot-or-persevere`, or add what you want: `/pmf:pivot-or-persevere write a pivot-or-persevere memo`. If you installed it with `npx skills add`, it's `/pivot-or-persevere`.

## What you need

All three techniques work in any chat.

| Technique | Chat only | Free | Paid, optional |
|---|---|---|---|
| Pivot-or-persevere memo | your evidence, attached | a pivot-decision skill, if installed | |
| Five pivots, one change each | your evidence, attached | | |
| Update the assumption board | your notes, transcripts or test results, attached | | |

## What you get

- **Pivot-or-persevere memo:** one table, one row per assumption: its dimension, the evidence so far with its source, the verdict (verified, open or pivot) and the next step, which for every open row is the test that turns it into an answer. Open rows are ordered riskiest first, and the decision sits under the table.
- **Five pivots, one change each:** five options that each change one of customer, problem, value proposition, product or price, each tied to a quote, with the cheapest test for each.
- **Update the assumption board:** proposed changes to your assumption board, shown as a diff, each with its quote or number, for you to approve one by one; plus the assumptions nobody said anything about.

Example: [TO ADD]

## Files it reads and writes

| File | What happens |
|---|---|
| `pmf/product-info.md` | Read first, for the product and the customer. Updated with the decision. |
| `pmf/assumptions.md` | Read, then updated, each change approved by you. |
| `pmf/synthesis.md` and `pmf/tests/` | Read if they exist: the evidence from interviews and tests. |
| `pmf/decisions/[date].md` | Written: the pivot-or-persevere memo. |

**Without them:** the skill offers to run [pmf](../pmf.md) first, which writes both files in about seven questions. Or it asks you four short questions, including what you believed at the start, and uses that as your assumption board, then gives you a `product-info.md` to save. In a plain chat that can't save files, it prints the files for you to save or add to your Claude Project.

Next step after this skill: back to the stage the decision points to, with one change: usually [interview-script](../problem/interview-script.md) for more conversations, or [landing-page-builder](../mvp/landing-page-builder.md) or [prototype](../mvp/prototype.md), then [ad-trigger-test](../test/ad-trigger-test.md) and [value-proposition-test](../test/value-proposition-test.md), for the next market test.
