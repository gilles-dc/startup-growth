# review-mining: what do people hate about what they use today?

Workshop slide P2 · stage: Problem

This skill collects the 1–2 star reviews of what your customers use today and of its two main competitors, from G2, Capterra, Trustpilot, the App Store, Google Play or Amazon. It groups the complaints into themes with counts and three quotes each, word for word, names the promise each complaint says was broken, and says who writes the angriest reviews. It ends with the problem written down in your customer's words, each line marked evidence or hypothesis.

New to skills? Read [Start here](../start-here.md) first.

## When to use it

- You know what your customers use today and want to know where it lets them down.
- You want complaints in the customer's own words, with how many people share each one.
- You want to know which kind of customer is angriest, so you know where to start.

Before this, [social-listener](social-listener.md) finds what people say about the problem in general. After it, go to [workaround-mapper](workaround-mapper.md), then [interview-script](interview-script.md). The front door is [pmf](../pmf.md).

## How to start

**Claude.ai, ChatGPT or any chat.** Type one of these:

- "Use review-mining. What do people complain about in my competitors' reviews?"
- "Use review-mining on the 1–2 star reviews of [competitor] on G2 and Capterra."
- "Here are 80 bad reviews of [competitor]. Use review-mining to group them into themes."
- "Use review-mining and take me through the bad reviews step by step."

Naming the skill makes sure it loads. Once it's installed, a question about competitors' reviews or complaints usually loads it on its own.

**Claude Code.** Type `/pmf:review-mining`, or add what you want: `/pmf:review-mining the bad reviews of Calendly and its two main competitors`. If you installed it with `npx skills add`, it's `/review-mining`.

## What you need

Capterra, G2 and Google Play block a plain web fetch, so you need a scraper or a paste.

| Technique | Chat only | Free | Paid, optional |
|---|---|---|---|
| Competitors' bad reviews | 50–100 reviews, pasted | Apify's free plan | Apify scraper runs |

## Step by step

Ask to be taken through a technique and the skill stops at every point where you have to do something. To pick it up again, attach what it asked for and say the sentence in the last column. In a new chat, put the skill's name first, so the right skill loads: "Use review-mining to continue the bad reviews".

| Technique | The skill does | You do | Then say |
|---|---|---|---|
| Bad reviews | names the competitors and where their reviews are | approve the scraper run, or copy 50–100 bad reviews into one file | "continue the bad reviews" |

At each stop, the skill notes in `product-info.md` what it's waiting for, so a new chat knows where you are.

## What you get

- **Competitors' bad reviews:** complaint themes with how many reviews mention each and three quotes word for word, the broken promise behind each theme, and who writes the angriest reviews, with three quotes checked against the source.
- **Always:** the Problem section of `product-info.md`: who has the problem, with numbers, and why it exists.

Example: [TO ADD]

## Files it reads and writes

| File | What happens |
|---|---|
| `pmf/product-info.md` | Read first. The Problem section is written, each line marked evidence or hypothesis. |
| `pmf/assumptions.md` | Read, then updated with what the reviews proved or broke. |

**Without them:** the skill offers to run [pmf](../pmf.md) first, which writes `product-info.md` and `assumptions.md` in about seven questions. Or it asks you four short questions and carries on, then gives you a `product-info.md` to save. In a plain chat that can't save files, it prints the files for you to save or add to your Claude Project.

Next step after this skill: [workaround-mapper](workaround-mapper.md) for how people handle the problem today, then [interview-script](interview-script.md) to turn the research into interview questions.
