# pmf: start here

The front door · every stage

This is the first skill to run. It asks you seven questions about your product, your customer and your evidence, and writes two files from your answers: `product-info.md`, what you believe right now, each line marked as a guess or as evidence, and `assumptions.md`, everything you're assuming, ranked by how much it would hurt to be wrong. Then it names your riskiest assumption and sends you to the one skill that tests it. It also checks which tools you've connected and sets the rules every other skill follows, such as: nothing is evidence until a real person did something.

New to skills? Read [Start here](start-here.md) first.

## When to use it

- You have an idea or an early product and don't know where to start.
- You don't know which stage you're at, or what to test next.
- It's your first time using these skills: every other skill reads the two files this one writes.
- A lot has changed since you last updated your files, and you want to rank your assumptions again.

There is nothing to run before it. After it, go to the skill it names: the full list is in [Start here](start-here.md#4-the-skills).

## How to start

**Claude.ai, ChatGPT or any chat.** Type one of these:

- "Use the pmf skill. Help me find product-market fit for my startup."
- "Use the pmf skill. What is the riskiest assumption in my idea?"
- "Use the pmf skill. Here is my product-info.md from last month. What should I test next?"
- "Use the pmf skill. We have 20 paying customers. Which stage are we at?"

Naming the skill makes sure it loads. Once it's installed, a question about validating an idea or finding product-market fit usually loads it on its own.

**Claude Code.** Type `/pmf:pmf`, or add what you want: `/pmf:pmf help me validate my idea`. If you installed it with `npx skills add`, it's `/pmf`.

## What you need

Works in any chat. No connector needed.

| Technique | Chat only | Free | Paid, optional |
|---|---|---|---|
| 1. Load or create the product file | your answers to seven questions, or your saved file | | |
| 2. Build the assumption board | yes | | |
| 3. Route to one skill | yes | | |
| 4. Check what's connected | yes | | |

## What you get

- **1:** `product-info.md`: your product, customer, problem, value, alternatives, market size, price, evidence and biggest worry, each line marked HYPOTHESIS or EVIDENCE with its source. If you already have the file, a five-line summary and a question about what changed.
- **2:** `assumptions.md`: every assumption about persona, problem, promise, product, price and channel, ranked by how lethal it is and how little you know. The top row is your riskiest assumption.
- **3:** one skill to go to next, out of the 24, with one line on why.
- **4:** a short table of the tools you've connected and what each missing kind of tool would add.

Example: [TO ADD]

## Files it reads and writes

| File | What happens |
|---|---|
| `pmf/product-info.md` | Read and summarised if it exists (it also looks in your project root and in files you attach). Written from your seven answers if it doesn't. |
| `pmf/assumptions.md` | Written from the product file, riskiest first. |

**Without them:** this is the skill that writes them. In a plain chat that can't save files, it prints both for you to save or add to your Claude Project.

Next step after this skill: the skill it names, based on your riskiest assumption.
