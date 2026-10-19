# landing-page-builder: build, audit or test a page

Workshop slide M1 · stage: MVP

This skill writes, checks and tests a landing page with the method from Gilles De Clerck's landing page workshop. BUILD writes your value propositions, five headers to choose from and the copy for every section, then the page itself as one HTML file. AUDIT scores an existing page section by section and rewrites the three things that cost you the most sign-ups. FEEDBACK gives you the questions to send to two groups of people and turns their answers into a list of changes. As a market test, it writes the rules for kill, iterate or scale before any result comes in, then builds a one-page site with a refundable deposit or a waitlist, plus the form, the payment link and the tracking.

New to skills? Read [Start here](../start-here.md) first.

## When to use it

- You need a new landing page, homepage or product page.
- You want a better headline, subheader or button text.
- You have a page and want to know why visitors don't sign up.
- You have a draft and want people's reactions before it goes live.
- You want a test page with a deposit, a waitlist, a pre-order or a fake door, live this week.
- You know your riskiest assumption and want the quickest way to test it.

Not sure what to promise yet? Start with [value-proposition-generator](../solution/value-proposition-generator.md): this skill takes its headers from it. Not sure which assumption is riskiest? Start with [pmf](../pmf.md). Testing a workflow with prototype screens, or selling the outcome by hand? Use [prototype](prototype.md).

## How to start

**Claude.ai, ChatGPT or any chat.** Type one of these:

- "Use landing-page-builder to build a page for my product."
- "Use landing-page-builder to audit my homepage at [link]. What are the three fixes that matter most?"
- "Use landing-page-builder and take me through the test page step by step."
- "Use landing-page-builder to write the kill criteria for our deposit test."

Naming the skill makes sure it loads. Once it's installed, a request to write, review or rewrite a landing page, or to build a test page or a fake door, usually loads it on its own.

**Claude Code.** Type `/pmf:landing-page-builder`, or add what you want: `/pmf:landing-page-builder build a test page with a refundable deposit`. If you installed it with `npx skills add`, it's `/landing-page-builder`.

## What you need

All three modes work in a plain chat. A connector puts the page live, or creates the form, the payment link and the tracking for you, as drafts you approve.

| Technique | Chat only | Free | Paid, optional |
|---|---|---|---|
| BUILD | the page as one HTML file, to put live yourself (Lovable, v0, Framer, Netlify drop) | Vercel or Netlify, Tally, Stripe (test mode first) connectors | |
| AUDIT | a screenshot, the copy or the file; a link if the chat can open web pages | | |
| FEEDBACK | the questions, to paste into a form or a message | | |
| A test page with deposits in 15 minutes (kill criteria first) | a single HTML file; you make the payment link and the form by hand | Vercel or Netlify, Tally, Stripe in test mode, PostHog | a domain name |
| Pick the right test | yes | | |

## Step by step

Ask to be taken through a technique and the skill stops at every point where you have to do something. To pick it up again, attach what it asked for and say the sentence in the last column. In a new chat, put the skill's name first, so the right skill loads: "Use landing-page-builder to continue the test page".

| Technique | The skill does | You do | Then say |
|---|---|---|---|
| BUILD | writes the value propositions, five headers and the copy for every section | pick the header, check every claim is true, gather real screenshots and quotes | "continue the landing page" |
| FEEDBACK | writes the questions and a note for each reviewer group | send them to both groups, collect the answers | "continue the page feedback" |
| Test page | writes the kill criteria and the page; drafts the form, the payment link and the tracking | approve them, or make the link and form by hand; publish the page | "continue the test page" |

At each stop, the skill notes in `product-info.md` what it's waiting for, so a new chat knows where you are.

## What you get

- **BUILD:** the value-proposition table, five headers with one recommended, copy for every section in the template order, and a working one-file page, audited by the skill before you see it.
- **AUDIT:** a one-line verdict, a score per section with quotes from your page, the three fixes that matter most with rewritten copy, three rewritten heroes, and what's missing from the template.
- **FEEDBACK:** seven questions for two groups of reviewers, then their answers grouped and quoted, turned into a list of changes, and a fresh audit of the revised page.
- **Test page:** a test file with the hypothesis, the kill, iterate and scale thresholds, and what you'll do in each case, written before launch; then a one-page test site with one button (a refundable deposit or a waitlist), plus the form, a test-mode payment link and tracking; or an HTML file and a list of what to make by hand.
- **Pick the right test:** the kind of test that fits your riskiest assumption.

Example: [TO ADD]

## Files it reads and writes

| File | What happens |
|---|---|
| `pmf/value-props.md` | Read first if it exists: the headers, hooks, subheaders and positionings from [value-proposition-generator](../solution/value-proposition-generator.md). |
| `pmf/product-info.md` | Read for the product, the customer, the problem, the alternatives, your proof and the promise. |
| `pmf/assumptions.md` | Read for the riskiest assumption, then updated. |
| `pmf/tests/[test-name].md` | Written before launch: the kill criteria, then the live address of the test. |
| The page | Written by BUILD as one HTML file. |

**Without them:** the skill offers to run [pmf](../pmf.md) first, which writes `product-info.md` and `assumptions.md` in about seven questions. Or it asks you six short questions in one message (what it does and costs, who it's for, what they do today and why that falls short, the main objection, your proof, what visitors should do), three more for a test page (the riskiest assumption, what the test promises, the budget and days), and carries on, then gives you a `product-info.md` to save. In a plain chat that can't save files, it prints the files for you to save or add to your Claude Project.

Next step after this skill: if the page is a market test, [tracking-audit](../test/tracking-audit.md) checks the tracking, [ad-trigger-test](../test/ad-trigger-test.md) puts traffic on it and [value-proposition-test](../test/value-proposition-test.md) reads the result.
