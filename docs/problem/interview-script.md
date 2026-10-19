# interview-script: what do I ask, and whom?

Workshop slide P4 · stage: Problem

This skill turns every open question from your research into a question about the last time it happened, then writes or fixes your interview script with the rules of The Mom Test: numbered, each question marked must ask or optional, with nothing leading, hypothetical or about your idea. It can also put a price on the problem, argue against your problem statement, draft the invites for you to send yourself, prepare an AI interviewer, and write the ask and the one-page pilot agreement for the end of a good call.

New to skills? Read [Start here](../start-here.md) first.

## When to use it

- You're about to talk to customers and need the questions, the script or the invites.
- You have a script and want to know which questions will only get you "yes, probably".
- You want to know what the problem costs your customer, and which numbers are still guesses.
- Your calls go well and you want to ask for something at the end.

Before this, [social-listener](social-listener.md), [review-mining](review-mining.md) and [workaround-mapper](workaround-mapper.md) give the research the questions come from, and [prospect-list-builder](../customer/prospect-list-builder.md) gives the people to invite. After the interviews, go to [interview-synthesis](interview-synthesis.md). The front door is [pmf](../pmf.md).

## How to start

**Claude.ai, ChatGPT or any chat.** Type one of these:

- "Use interview-script. Write my customer interview script."
- "Use interview-script to fix this script: [paste]."
- "Use interview-script to price the problem my startup solves."
- "Use interview-script and take me through the interview invites step by step."

Naming the skill makes sure it loads. Once it's installed, a question about customer interviews, interview questions or The Mom Test usually loads it on its own.

**Claude Code.** Type `/pmf:interview-script`, or add what you want: `/pmf:interview-script turn my research into interview questions`. If you installed it with `npx skills add`, it's `/interview-script`.

## What you need

Most techniques work in a plain chat. A connector saves you the copying and pasting.

| Technique | Chat only | Free | Paid, optional |
|---|---|---|---|
| Interview script (with Turn research into interview questions) | in the chat | | |
| Price the problem | in the chat | | |
| Argue against yourself | in the chat | | |
| Interview invites in your Gmail drafts | invites as text, sent by hand | Gmail drafts and Calendly | |
| AI interviewer | | | AI interviewer tools, e.g. UserCall |
| Ask for a commitment | in the chat | | |

## Step by step

Ask to be taken through a technique and the skill stops at every point where you have to do something. To pick it up again, attach what it asked for and say the sentence in the last column. In a new chat, put the skill's name first, so the right skill loads: "Use interview-script to continue the interviews".

| Technique | The skill does | You do | Then say |
|---|---|---|---|
| Interview invites | writes one invite per person | send them yourself, book the calls, run the interviews | "continue the interviews" |
| AI interviewer | prepares the script and the list for the tool | set up the tool, send the invites, wait | "continue the AI interviews" |
| Commitment | writes the ask and the pilot agreement | make the ask, send the agreement | "continue the commitments" |

At each stop, the skill notes in `product-info.md` what it's waiting for, so a new chat knows where you are.

## What you get

- **Interview script:** interview questions about the last time it happened, saved to `interview-questions.md`, then a numbered interview script, each question marked must ask or optional.
- **Price the problem:** what the problem costs per customer per year, every assumption a row. The guessed rows are your interview agenda.
- **Argue against yourself:** the seven strongest reasons your problem isn't worth paying to solve, each with what would prove it wrong, added to `interview-questions.md`.
- **Interview invites and AI interviewer:** invites for you to send, as Gmail drafts or text, and everything an AI interviewer tool needs.
- **Ask for a commitment:** the ask for the end of the call and a one-page pilot agreement; every commitment logged with its strength.

Example: [TO ADD]

## Files it reads and writes

| File | What happens |
|---|---|
| `pmf/product-info.md` | Read first. Updated with what the research changed; commitments go in the Evidence table. |
| `pmf/assumptions.md` | Read, then updated. |
| `pmf/interview-questions.md` | Read if it exists. Turn research into interview questions and Argue against yourself add to it; the script uses it. |
| `pmf/lists/` | The people to invite, from [prospect-list-builder](../customer/prospect-list-builder.md). |
| `pmf/problem-cost.csv` | Written by Price the problem, with working formulas. |

**Without them:** the skill offers to run [pmf](../pmf.md) first, which writes `product-info.md` and `assumptions.md` in about seven questions. Or it asks you five short questions and carries on, then gives you a `product-info.md` to save. In a plain chat that can't save files, it prints the files for you to save or add to your Claude Project.

Next step after this skill: run the interviews, then [interview-synthesis](interview-synthesis.md) for the patterns, with every quote checked.
