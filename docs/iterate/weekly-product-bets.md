# weekly-product-bets: what do we try next?

Workshop slide I3 · stage: Iterate

Every Monday, this skill reads last week's product numbers, new interview notes, test results and the team channel, and proposes five ideas to test, ranked. Each comes with the evidence behind it, the test to run and the result that would change the plan. It starts from the biggest drop in your funnel, weighs what people did above what they asked for, and lists requests from customers you don't serve apart. It runs on its own as a scheduled agent, or by hand from your exports.

New to skills? Read [Start here](../start-here.md) first.

## When to use it

- You want the loop to run every week without anyone having to remember it.
- You have numbers, notes and messages each week and need to pick what to try next.

Have the decision from this cycle first with [pivot-or-persevere](pivot-or-persevere.md). After this skill, run the first bet's test and take what it shows back to [pivot-or-persevere](pivot-or-persevere.md). Not sure where you are? Start at the front door, [pmf](../pmf.md).

## How to start

**Claude.ai, ChatGPT or any chat.** Type one of these:

- "Use weekly-product-bets. Here are last week's numbers, notes and messages. What should we test next?"
- "Use weekly-product-bets and take me through the Monday ideas step by step."
- "Use weekly-product-bets to set up an agent that proposes five bets every Monday."

Naming the skill makes sure it loads.

**Claude Code.** Type `/pmf:weekly-product-bets`, or add what you want: `/pmf:weekly-product-bets set up the Monday agent`. If you installed it with `npx skills add`, it's `/weekly-product-bets`.

## What you need

It runs on its own as a Claude Cowork scheduled task or a Claude Code routine; without one, you run the same prompt by hand.

| Technique | Chat only | Free | Paid, optional |
|---|---|---|---|
| Monday: five ideas to test | attach last week's numbers, notes and messages each Monday | an analytics connector; Slack | |

## Step by step

Ask to be taken through a technique and the skill stops at every point where you have to do something. To pick it up again, attach what it asked for and say the sentence in the last column. In a new chat, put the skill's name first, so the right skill loads: "Use weekly-product-bets to continue the Monday bets".

| Technique | The skill does | You do | Then say |
|---|---|---|---|
| Monday: five ideas to test | writes the Monday prompt and what it reads (or the exports to bring) | switch it on, or gather the exports on Monday | "continue the Monday bets" |

At each stop, the skill notes in `product-info.md` what it's waiting for, so a new chat knows where you are.

## What you get

- **Monday: five ideas to test:** five ranked ideas to test every Monday, each with its evidence, the test to run and the result that would change the plan; which one to run first, and which can run alongside it; requests from outside your ICP listed apart.

Example: [TO ADD]

## Files it reads and writes

| File | What happens |
|---|---|
| `pmf/product-info.md` | Read first, for the product and the customer. Updated after each step. |
| `pmf/assumptions.md` | Read if it exists. |
| `pmf/synthesis.md` and `pmf/tests/` | Read if they exist: the evidence from interviews and tests. |

**Without them:** the skill offers to run [pmf](../pmf.md) first, which writes both files in about seven questions. Or it asks you three short questions and carries on, then gives you a `product-info.md` to save. In a plain chat that can't save files, it prints the file for you to save or add to your Claude Project.

Next step after this skill: run the first bet's test, then take what it shows to [pivot-or-persevere](pivot-or-persevere.md). Requests from outside your ICP go to [icp](../customer/icp.md).
