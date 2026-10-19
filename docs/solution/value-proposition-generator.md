# value-proposition-generator: the world without your product, and how you make it better

Workshop slide S4 · stage: Solution

This skill writes down everything your customer does today without your product, and for each one, what your product does better and what that lets the customer do. Together that's the vault: every value proposition you have, each traced to the world your customer lives in now. From the vault it picks the one that matters most, writes your problem statement and value proposition statement, turns the best rows into headers that answer the main objection, and chooses three positionings to test on a page or in ads. For a quick start, it also writes a from–to table in your customer's own words, the comparison table your customer would draw, and ten headlines to test.

New to skills? Read [Start here](../start-here.md) first.

## When to use it

- You need the headline and subheadline for a landing page.
- You want to know what to promise, and against which alternatives.
- You're about to run a test page or ads and need three different promises to compare.
- You have research or interview notes and want to turn them into value propositions.

Before this, the research from [social-listener](../problem/social-listener.md), [review-mining](../problem/review-mining.md), [workaround-mapper](../problem/workaround-mapper.md), [interview-synthesis](../problem/interview-synthesis.md), [icp](../customer/icp.md), [competitive-analysis](../solution/competitive-analysis.md) and [buyer-objections-mapper](../solution/buyer-objections-mapper.md) makes the vault sharper. After it, the vault goes into [landing-page-builder](../mvp/landing-page-builder.md) and [ad-trigger-test](../test/ad-trigger-test.md). Not sure where to start? Use [pmf](../pmf.md).

## How to start

**Claude.ai, ChatGPT or any chat.** Type one of these:

- "Use value-proposition-generator. Build the value propositions for my product."
- "Use value-proposition-generator to write the headline for my landing page."
- "Here's my research. Turn it into a value proposition vault with value-proposition-generator."
- "Use value-proposition-generator to pick three positionings to test in ads."

Naming the skill makes sure it loads. Once it's installed, a question about value propositions, positioning or headlines usually loads it on its own.

**Claude Code.** Type `/pmf:value-proposition-generator`, or add what you want: `/pmf:value-proposition-generator write my landing-page headers`. If you installed it with `npx skills add`, it's `/value-proposition-generator`.

## What you need

Everything works in a plain chat. Research files from the other skills make each row stronger; without them, every row is marked HYPOTHESIS.

| Technique | Chat only | Free | Paid, optional |
|---|---|---|---|
| The vault: from every bad alternative to three positionings | your research files, or your own list | | |
| *More:* Write it in their words | your quotes, pasted | | |
| *More:* The table the customer would draw | your complaint themes, pasted | | |
| *More:* Ten headlines | your quotes, pasted | | |

## What you get

- **The vault:** 8–15 rows or more: each bad alternative with its source and count, how the product does it better with a number where there is one, the value proposition as something the customer can do, and whether it relieves a pain or creates a gain.
- **Focus:** the one row that matters most and why, your problem statement and your value proposition statement.
- **Headers:** for at least the top ten rows, the main objection and a header that answers it; subheaders for the three to test.
- **Positionings:** three different promises to test, each with a header, subheader, the objection it answers, the gap it bets on and an image idea.
- **Write it in their words:** a from–to table in your customer's words, a problem statement and a value proposition statement.
- **The table the customer would draw:** a comparison table on the three complaints that matter most, with your guesses marked.
- **Ten headlines:** each promising a different outcome, with a subheading under each.

Example: [TO ADD]

## Files it reads and writes

| File | What happens |
|---|---|
| `pmf/product-info.md` | Read first, for the product, the customer and the problem. The Value and Alternatives sections are updated. |
| `pmf/assumptions.md` | Read, then the promise rows are updated. |
| `pmf/icp.md` | Read, for who the customer is. |
| Research files | Read if they exist: what people say, the bad reviews, the workarounds and the interview findings from the problem stage, the positioning map from [competitive-analysis](../solution/competitive-analysis.md), the buyer questions from [buyer-objections-mapper](../solution/buyer-objections-mapper.md). |
| `pmf/value-props.md` | Written: the vault, the two statements, the headers and the three positionings. |

**Without them:** the skill offers to run [pmf](../pmf.md) first, which writes `product-info.md` and `assumptions.md` in about seven questions. Or it asks you six short questions and carries on, then gives you a `product-info.md` to save. In a plain chat that can't save files, it prints the files for you to save or add to your Claude Project.

Next step after this skill: [landing-page-builder](../mvp/landing-page-builder.md), to build the page from the vault, then [ad-trigger-test](../test/ad-trigger-test.md) to test the three positionings.
