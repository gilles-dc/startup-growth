# prototype: which version would they have used?

Workshop slide M2 · stage: MVP

This skill builds prototypes to test whether your workflow makes sense to the people you sell to. It builds three versions of one key screen to show at the end of an interview, so people compare them and get critical. It can also turn a customer call into a clickable prototype within the hour, or set you up to deliver the outcome by hand first, charge for it, and log every step until the steps that repeat become your product spec.

New to skills? Read [Start here](../start-here.md) first.

## When to use it

- You want prototypes to show in customer interviews.
- You just had a call and want to send the customer a prototype the same day.
- You want to sell the outcome by hand before you build the product.

Not sure which assumption is riskiest? Start with [pmf](../pmf.md). Testing whether people want the outcome enough to pay a deposit? Use [landing-page-builder](landing-page-builder.md).

## How to start

**Claude.ai, ChatGPT or any chat.** Type one of these:

- "Use prototype to build three prototype screens for my next interviews."
- "Use prototype and take me through the prototype interviews step by step."
- "Use prototype to turn this call transcript into a clickable prototype."
- "Use prototype to set up a test where I deliver the outcome by hand first."

Naming the skill makes sure it loads. Once it's installed, a request for prototypes, mockups for interviews or a concierge test usually loads it on its own.

**Claude Code.** Type `/pmf:prototype`, or add what you want: `/pmf:prototype build three versions of our onboarding screen`. If you installed it with `npx skills add`, it's `/prototype`.

## What you need

Every technique works without a connector. With a builder connected, you get links to click.

| Technique | Chat only | Free | Paid, optional |
|---|---|---|---|
| Test three prototypes side by side | HTML files, or a prompt to paste into a builder | Lovable, v0 or Magic Patterns free tiers | |
| From a call to a prototype in an hour | an HTML file, or a prompt to paste into a builder | Lovable, v0 or Magic Patterns free tiers | |
| Deliver it by hand first | a log sheet | | |

## Step by step

Ask to be taken through a technique and the skill stops at every point where you have to do something. To pick it up again, attach what it asked for and say the sentence in the last column. In a new chat, put the skill's name first, so the right skill loads: "Use prototype to continue the prototype interviews".

| Technique | The skill does | You do | Then say |
|---|---|---|---|
| Three prototypes | builds three versions and a short interview guide | show them in your next interviews, note which one each person picks | "continue the prototype interviews" |
| Call to prototype | builds the prototype from your call transcript | send it to the customer the same day, wait for the reply | "continue the call prototype" |
| By hand | writes the offer, the prompts and a log sheet | sell it to 3–5 customers, deliver it, log every step | "continue the hand delivery" |

At each stop, the skill notes in `product-info.md` what it's waiting for, so a new chat knows where you are.

## What you get

- **Three prototypes:** three versions of one key screen and an interview guide; then which one people picked, and why.
- **Call to prototype:** a clickable prototype from one call, and the strongest case for skipping the feature.
- **By hand:** an offer to sell by hand, a log of every step, and the steps that repeat, as your product spec.

Example: [TO ADD]

## Files it reads and writes

| File | What happens |
|---|---|
| `pmf/product-info.md` | Read first, for the product, the customer and the promise. |
| `pmf/assumptions.md` | Read for the riskiest assumption, then updated with what people picked and what they paid. |

**Without them:** the skill offers to run [pmf](../pmf.md) first, which writes both files in about seven questions. Or it asks you five short questions and carries on, then gives you a `product-info.md` to save. In a plain chat that can't save files, it prints the files for you to save or add to your Claude Project.

Next step after this skill: [landing-page-builder](landing-page-builder.md) when the next test is a page with a deposit or a waitlist; [tracking-audit](../test/tracking-audit.md), [ad-trigger-test](../test/ad-trigger-test.md) and [value-proposition-test](../test/value-proposition-test.md) to put traffic on it and read the numbers back.
