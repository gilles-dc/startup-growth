# tracking-audit: is every sign-up counted?

Workshop slide T1 · stage: Test

Once your test page is built, this skill checks your tracking from ad click to deposit, so every sign-up and payment is counted before you spend a euro. It follows the chain across your analytics, session recording, ads and payments tools, has you click through as a visitor on a phone and a laptop, with cookies accepted and declined, and lists the gaps tool by tool, with the fixes.

New to skills? Read [Start here](../start-here.md) first.

## When to use it

- Your test page is live, or nearly, and you want people on it.
- You want to know your tracking counts every sign-up and deposit before you pay for traffic.

No test page yet? Build it with [landing-page-builder](../mvp/landing-page-builder.md) first, which also writes the numbers that decide the test. After this skill, put traffic on the page with [ad-trigger-test](../test/ad-trigger-test.md). Not sure where you are? Start at [pmf](../pmf.md).

## How to start

**Claude.ai, ChatGPT or any chat.** Type one of these:

- "Use tracking-audit. My test page is live. Check the tracking before I spend anything."
- "Use tracking-audit and take me through the tracking check step by step."
- "Use tracking-audit on my page. I have PostHog, Clarity and Stripe connected."
- "Use tracking-audit. Here are my notes and screenshots from clicking through the page."

Naming the skill makes sure it loads. Once it's installed, a question about checking the tracking on a test page usually loads it on its own.

**Claude Code.** Type `/pmf:tracking-audit`, or add what you want: `/pmf:tracking-audit check the tracking on my test page`. If you installed it with `npx skills add`, it's `/tracking-audit`.

## What you need

Every technique works without a connector. A connector saves you the export.

| Technique | Chat only | Free | Paid, optional |
|---|---|---|---|
| Conversion tracking audit | a checklist you click through, with notes or screenshots | PostHog or GA4, Microsoft Clarity, Stripe connectors | |

## Step by step

Ask to be taken through a technique and the skill stops at every point where you have to do something. To pick it up again, attach what it asked for and say the sentence in the last column. In a new chat, put the skill's name first, so the right skill loads: "Use tracking-audit to continue the tracking check".

| Technique | The skill does | You do | Then say |
|---|---|---|---|
| Tracking | writes the chain for your page and the checklist of what breaks | click through as a visitor, on phone and laptop, with cookies accepted and declined; note what each tool recorded | "continue the tracking check" |

At each stop, the skill notes in `product-info.md` what it's waiting for, so a new chat knows where you are.

## What you get

- The gaps in your tracking, tool by tool, with the fixes, before any traffic.

Example: [TO ADD]

## Files it reads and writes

| File | What happens |
|---|---|
| `pmf/tests/[test-name].md` | Read first, for the variants, the main button and your kill, iterate and scale numbers. The gaps and fixes are logged here. |
| `pmf/product-info.md` | Read for context. |
| `pmf/assumptions.md` | Read, then updated. |

**Without them:** the skill offers to run [pmf](../pmf.md) first, which writes both files in about seven questions. Or it asks you five short questions and carries on, then gives you a `product-info.md` to save. With no test file, it writes the kill, iterate and scale numbers with you first. In a plain chat that can't save files, it prints the files for you to save or add to your Claude Project.

Next step after this skill: put traffic on the page with [ad-trigger-test](../test/ad-trigger-test.md).
