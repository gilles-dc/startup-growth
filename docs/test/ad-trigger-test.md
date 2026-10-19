# ad-trigger-test: put the promises in front of people

Workshop slide T2 · stage: Test

Once your test page is built and the tracking holds, this skill puts it in front of people. It builds one ad per promise in Meta, paused, for you to switch on, each to the same audience with the same budget, or writes the ads as blocks to paste into Ads Manager. No ad budget? It drafts messages to your own list and communities. The next morning, [value-proposition-test](../test/value-proposition-test.md) makes the first read: whether every variant is spending and every click lands on its own page.

New to skills? Read [Start here](../start-here.md) first.

## When to use it

- Your test page is live and the tracking is checked.
- You want small paid traffic on two or three promises, or to send the page to your own list.

No test page yet? Build it with [landing-page-builder](../mvp/landing-page-builder.md) first, which also writes the numbers that decide the test. Check the tracking with [tracking-audit](../test/tracking-audit.md) before you spend. After this skill, read the results with [value-proposition-test](../test/value-proposition-test.md). Not sure where you are? Start at [pmf](../pmf.md).

## How to start

**Claude.ai, ChatGPT or any chat.** Type one of these:

- "Use ad-trigger-test and take me through the Meta ads step by step."
- "Use ad-trigger-test to send my page to my own list. I have no ad budget."
- "Use ad-trigger-test to write the ads for my three variants as blocks I can paste into Ads Manager."

Naming the skill makes sure it loads. Once it's installed, a question about putting traffic on a test page usually loads it on its own.

**Claude Code.** Type `/pmf:ad-trigger-test`, or add what you want: `/pmf:ad-trigger-test build the Meta ads for my test page, paused`. If you installed it with `npx skills add`, it's `/ad-trigger-test`.

## What you need

Every technique works without a connector. A connector saves you the copy and paste. Paid traffic needs a Meta ad account and a Facebook Page; a paused campaign costs nothing, and switching it on costs the budget you set.

| Technique | Chat only | Free | Paid, optional |
|---|---|---|---|
| Build the ads in Meta, paused | the ads as blocks to paste into Ads Manager, or messages to your own list | Meta Ads, TikTok Ads or LinkedIn Ads connector (community server, drafts) | the ad budget you switch on |

## Step by step

Ask to be taken through a technique and the skill stops at every point where you have to do something. To pick it up again, attach what it asked for and say the sentence in the last column. In a new chat, put the skill's name first, so the right skill loads: "Use ad-trigger-test to continue the ad test".

| Technique | The skill does | You do | Then say |
|---|---|---|---|
| Ads | writes each ad and the campaign, paused (or the paste-ready blocks, or drafts for your list) | review every line, switch it on (or send), wait until the next morning | "continue the ad test" |

At each stop, the skill notes in `product-info.md` what it's waiting for, so a new chat knows where you are.

## What you get

- One ad per promise, each to the same audience with the same budget, created paused; or the messages for your own list.

Example: [TO ADD]

## Files it reads and writes

| File | What happens |
|---|---|
| `pmf/tests/[test-name].md` | Read first, for the variants and your kill, iterate and scale numbers. The campaign is logged here. |
| `pmf/product-info.md` | Read for context. |
| `pmf/assumptions.md` | Read. |

**Without them:** the skill offers to run [pmf](../pmf.md) first, which writes both files in about seven questions. Or it asks you five short questions and carries on, then gives you a `product-info.md` to save. With no test file, it writes the kill, iterate and scale numbers with you before it builds a single ad. In a plain chat that can't save files, it prints the files for you to save or add to your Claude Project.

Next step after this skill: read the results with [value-proposition-test](../test/value-proposition-test.md), the next morning and again after the agreed duration.
