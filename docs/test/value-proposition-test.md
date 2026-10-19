# value-proposition-test: kill, iterate or scale?

Workshop slide T3 · stage: Test

When the results of your test are in, this skill reads spend, clicks, sign-ups and deposits per variant against the rules you wrote before launch, and recommends kill, iterate or scale. You decide. Each variant is named by its header, word for word, and judged on its own, on what people did on the page.

New to skills? Read [Start here](../start-here.md) first.

## When to use it

- The results are in and you need a decision.
- You ran ads or sent the page to your own list, and want to know which promise worked.

Traffic not running yet? Start it with [ad-trigger-test](../test/ad-trigger-test.md). After this skill, talk to the people who signed up with [interview-script](../problem/interview-script.md), and take the decision to [pivot-or-persevere](../iterate/pivot-or-persevere.md). Not sure where you are? Start at [pmf](../pmf.md).

## How to start

**Claude.ai, ChatGPT or any chat.** Type one of these:

- "Here are my ads, analytics and Stripe exports. Read the results with value-proposition-test: kill, iterate or scale?"
- "Use value-proposition-test and take me through the results step by step."
- "Use value-proposition-test. I sent my page to my list last week. Which variant won?"

Naming the skill makes sure it loads. Once it's installed, a question about reading test results usually loads it on its own.

**Claude Code.** Type `/pmf:value-proposition-test`, or add what you want: `/pmf:value-proposition-test read my test results`. If you installed it with `npx skills add`, it's `/value-proposition-test`.

## What you need

Every technique works without a connector. A connector saves you the export.

| Technique | Chat only | Free | Paid, optional |
|---|---|---|---|
| Read the results, decide | an export from each tool, attached | ads, analytics, forms and Stripe connectors | |

## Step by step

Ask to be taken through a technique and the skill stops at every point where you have to do something. To pick it up again, attach what it asked for and say the sentence in the last column. In a new chat, put the skill's name first, so the right skill loads: "Use value-proposition-test to continue the test results".

| Technique | The skill does | You do | Then say |
|---|---|---|---|
| Results | names the exports it needs, for the same dates | export them (skip with connectors) | "continue the test results" |

At each stop, the skill notes in `product-info.md` what it's waiting for, so a new chat knows where you are.

## What you get

- One row per variant, named by its header: spend, clicks, page views, button clicks, sign-ups, deposits and cost per deposit. Each variant judged against your own numbers, then a recommendation: kill, iterate or scale, with the reason.

Example: [TO ADD]

## Files it reads and writes

| File | What happens |
|---|---|
| `pmf/tests/[test-name].md` | Read first, for the variants, the main button and your kill, iterate and scale numbers. The results and the decision are logged here. |
| `pmf/product-info.md` | Read for context. The Evidence table is updated: sign-ups count as interest, deposits and letters of intent as commitment. |
| `pmf/assumptions.md` | Read, then updated with what the test proved or broke. |

**Without them:** the skill offers to run [pmf](../pmf.md) first, which writes both files in about seven questions. Or it asks you six short questions and carries on, then gives you a `product-info.md` to save. With no test file, it writes the kill, iterate and scale numbers with you before it reads a single result. In a plain chat that can't save files, it prints the files for you to save or add to your Claude Project.

Next step after this skill: invite the people who signed up to a conversation ([interview-script](../problem/interview-script.md)), and take the decision to [pivot-or-persevere](../iterate/pivot-or-persevere.md).
