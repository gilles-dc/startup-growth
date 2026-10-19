# know-your-customer: does the team know the customer?

Workshop slide I1 · stage: Iterate

After a round of interviews, this skill checks whether you know your customer as well as your transcripts do. It quizzes you with ten questions on your customer's day, tools, spending and exact words, then scores you and shows what you got wrong, with the quote. It can also set up an agent that analyses every new interview as it comes in, checks every quote and proposes changes to your assumption board. The agent also works by hand.

New to skills? Read [Start here](../start-here.md) first.

## When to use it

- You finished interviews and want to check the team knows the customer without opening the transcripts.
- You're about to start the next round of calls.
- You want every new interview analysed without anyone having to remember it.

No interviews yet? Run them first with [interview-script](../problem/interview-script.md) and read them with [interview-synthesis](../problem/interview-synthesis.md). After this skill, take what changed to [pivot-or-persevere](pivot-or-persevere.md). Not sure where you are? Start at the front door, [pmf](../pmf.md).

## How to start

**Claude.ai, ChatGPT or any chat.** Type one of these:

- "Use know-your-customer and quiz me on my customer. Here are our interview transcripts."
- "Use know-your-customer to quiz each of us on the customer before the next calls."
- "Use know-your-customer to analyse this new interview and propose changes to my assumption board."
- "Use know-your-customer and take me through the interview analysis step by step."

Naming the skill makes sure it loads.

**Claude Code.** Type `/pmf:know-your-customer`, or add what you want: `/pmf:know-your-customer quiz me on my customer`. If you installed it with `npx skills add`, it's `/know-your-customer`.

## What you need

The quiz works in any chat. The interview analysis runs on its own as a Claude Cowork scheduled task or a Claude Code routine; without one, you run the same prompt by hand.

| Technique | Chat only | Free | Paid, optional |
|---|---|---|---|
| Quiz yourself on your customer | your transcripts or synthesis, attached | | |
| Every new interview, analysed | attach each transcript after the call | Granola or a Drive folder; Slack for the summary | |

## Step by step

Ask to be taken through a technique and the skill stops at every point where you have to do something. To pick it up again, attach what it asked for and say the sentence in the last column. In a new chat, put the skill's name first, so the right skill loads: "Use know-your-customer to continue the interview analysis".

| Technique | The skill does | You do | Then say |
|---|---|---|---|
| Every new interview, analysed | writes the agent's prompt, trigger and connectors (or the prompt to run by hand) | switch it on, or hold the next interview | "continue the interview analysis" |

At each stop, the skill notes in `product-info.md` what it's waiting for, so a new chat knows where you are.

## What you get

- **Quiz yourself on your customer:** ten questions on your customer, a score, and what you got wrong, with the quote.
- **Every new interview, analysed:** every new interview analysed, every quote checked, board changes proposed, and a five-line summary.

Example: [TO ADD]

## Files it reads and writes

| File | What happens |
|---|---|
| `pmf/product-info.md` | Read first, for the product and the customer. Updated after each step. |
| `pmf/assumptions.md` | Read; changes are proposed for you to approve. |
| `pmf/synthesis.md` and `pmf/tests/` | Read if they exist: the evidence from interviews and tests. |
| `pmf/interviews/` | Each analysed interview is added. |

**Without them:** the skill offers to run [pmf](../pmf.md) first, which writes both files in about seven questions. Or it asks you three short questions, including what you believed at the start, and uses that as your assumption board, then gives you a `product-info.md` to save. In a plain chat that can't save files, it prints the files for you to save or add to your Claude Project.

Next step after this skill: [pivot-or-persevere](pivot-or-persevere.md), to approve the board changes and decide what changes, or [interview-script](../problem/interview-script.md) for more conversations.
