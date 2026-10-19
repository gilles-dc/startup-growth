# market-sizing: is the market big enough?

Workshop slide S3 · stage: Solution

This skill sizes your market as TAM, SAM and SOM. Your ICP is the beachhead, and the market is bigger: it names the broader category and counts it from official statistics and company filings, then loosens your ICP one criterion at a time into rings of adjacent customers and counts each ring. The big circles are sized by what customers already spend on the problem, the small ones by your price. Every number has a source, a confidence and a range, and it ends with a verdict: big enough for your goal, or which moves make it bigger.

New to skills? Read [Start here](../start-here.md) first.

## When to use it

- Someone asked how big your market is, and you want a number with names behind it.
- You need TAM, SAM and SOM for a deck.
- You want to check whether the market is big enough before you build.

The company count comes from [prospect-list-builder](../customer/prospect-list-builder.md); the cost of the problem from [interview-script](../problem/interview-script.md) (Price the problem). After it, write the promise with [value-proposition-generator](../solution/value-proposition-generator.md). Not sure where to start? Use [pmf](../pmf.md).

## How to start

**Claude.ai, ChatGPT or any chat.** Type one of these:

- "Use market-sizing. How big is our market?"
- "Use market-sizing to build TAM, SAM and SOM from this filter count."
- "Use market-sizing and take me through the market size step by step."

Naming the skill makes sure it loads. Once it's installed, a question about market size or TAM usually loads it on its own.

**Claude Code.** Type `/pmf:market-sizing`, or add what you want: `/pmf:market-sizing size our market in Europe`. If you installed it with `npx skills add`, it's `/market-sizing`.

## What you need

Works in any chat with web search. Code execution helps with the arithmetic.

| Technique | Chat only | Free | Paid, optional |
|---|---|---|---|
| Market size: TAM, SAM, SOM | web search: official statistics, registers, filings | code execution (Claude.ai, Claude Code) | |

## Step by step

Ask to be taken through it and the skill stops at the point where you have to do something. To pick it up again, attach what it asked for and say the sentence in the last column. In a new chat, put the skill's name first, so the right skill loads: "Use market-sizing to continue the market size".

| Technique | The skill does | You do | Then say |
|---|---|---|---|
| Market size | names the category and the rings | check the category sentence and the rings before it counts | "continue the market size" |

At each stop, the skill notes in `product-info.md` what it's waiting for, so a new chat knows where you are.

## What you get

- One slide: Beachhead, SOM, SAM and TAM as nested circles, each with who is in it, how many, and € a year.
- The verdict: big enough for your goal or not, how many customers €1m and €10m a year take, and the moves if it's too small.
- The full file: the category, the rings, every input with its source and confidence, and what would narrow the ranges.

Example: [TO ADD]

## Files it reads and writes

| File | What happens |
|---|---|
| `pmf/product-info.md` | Read first, for your customer and the problem. The Market size section is updated. |
| `pmf/assumptions.md` | Read, then updated. |

**Without them:** the skill offers to run [pmf](../pmf.md) first, which writes both files in about seven questions. Or it asks you four short questions and carries on, then gives you a `product-info.md` to save. In a plain chat that can't save files, it prints the file for you to save or add to your Claude Project.

Next step after this skill: [value-proposition-generator](../solution/value-proposition-generator.md), to write the promise.
