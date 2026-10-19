# icp-reply-rate-test: which customer do I start with?

Workshop slide C4 · stage: Customer

This skill lets reply rates pick your first customer. It writes five variants of your customer, each a different role, life stage, company type or trigger, with ten people per variant and one three-line message per variant, all with the same ask so the reply rates compare. You send the messages yourself and log the replies; the variant with the highest reply rate is where you start.

New to skills? Read [Start here](../start-here.md) first.

## When to use it

- You're torn between several possible customers.
- You have an ICP and want to know which version of it is readiest to talk.
- You want the first customer picked by what people did.

No product file yet? Start with [pmf](../pmf.md). The ten people per variant come from [prospect-list-builder](../customer/prospect-list-builder.md). After this, describe the winner with [icp](../customer/icp.md) and check the problem is real for them with [social-listener](../problem/social-listener.md).

## How to start

**Claude.ai, ChatGPT or any chat.** Type one of these:

- "Use icp-reply-rate-test. I'm torn between three possible customers."
- "Use icp-reply-rate-test and take me through the five first customers step by step."
- "Use icp-reply-rate-test. Here are my reply counts per variant: which one do I start with?"

Naming the skill makes sure it loads. Once it's installed, a question about picking your first customer usually loads it on its own.

**Claude Code.** Type `/pmf:icp-reply-rate-test`, or add what you want: `/pmf:icp-reply-rate-test write five variants of my customer`. If you installed it with `npx skills add`, it's `/icp-reply-rate-test`.

## What you need

| Technique | Chat only | Free | Paid, optional |
|---|---|---|---|
| Five first customers, picked by reply rate | yes; you send the messages | | |

## Step by step

Ask to be taken through it and the skill stops at every point where you have to do something. To pick it up again, attach what it asked for and say the sentence in the last column. In a new chat, put the skill's name first, so the right skill loads: "Use icp-reply-rate-test to continue the first-customer test".

| Technique | The skill does | You do | Then say |
|---|---|---|---|
| First customers | writes five variants, ten people each, five messages and a reply tracker | send the messages yourself, wait a week, log the replies | "continue the first-customer test" |

At each stop, the skill notes in `product-info.md` what it's waiting for, so a new chat knows where you are.

## What you get

- Five variants of your customer, each with a trigger and an angle on the problem.
- One message per variant, with the same ask in all five.
- A reply tracker, one row per variant.
- The variant to start with, picked by reply rate, or ten more messages each if the top two are close.

Example: [TO ADD]

## Files it reads and writes

| File | What happens |
|---|---|
| `pmf/product-info.md` | Read first, for your customer and the problem. The Customer section gets the variant to start with. |
| `pmf/assumptions.md` | Read, then the persona rows are updated with what you found. |
| `pmf/icp-test.md` | The reply tracker, one row per variant. |

**Without them:** the skill offers to run [pmf](../pmf.md) first, which writes both files in about seven questions. Or it asks you five short questions and carries on, then gives you a `product-info.md` to save. In a plain chat that can't save files, it prints the changes for you to save and the tracker as a table you can paste into a sheet.

Next step after this skill: [icp](../customer/icp.md), to describe the winning variant in five dimensions; then [social-listener](../problem/social-listener.md), to check the problem is real for these people.
