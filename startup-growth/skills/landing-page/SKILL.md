---
name: landing-page
description: Write, build, audit and get feedback on a startup landing page or homepage with a proven conversion method. Use when someone wants a new landing page, homepage, persona or product page; wants headline, subheader, value proposition or CTA copy; wants an existing page reviewed, scored or rewritten; or wants a page for a waitlist, pre-order or fake-door test. Reads pmf/product-info.md if it exists.
---

# Landing page

Conversion = **desire − (labor + confusion)**.
Increase desire with specific value. Decrease labor: every word, visual and element must add meaning. Decrease confusion: be specific and consistent at every step, and make the next action obvious.

**Messaging > design.** Hone the message first, then combine copy and media to convey it, then design to make that clearer. Never start from layout.

The full method, with examples, is in `references/method.md`. Read it before writing or auditing anything.

## What you need

Any chat that can open a web page (Claude, ChatGPT) for AUDIT. Nothing else. BUILD can deploy with Vercel or Netlify if connected; otherwise it outputs the page as a file.

## Choose a mode

Ask which one, or infer it from the request:

| Mode | When | Output |
|---|---|---|
| **BUILD** | new page, or a rewrite from scratch | value-prop table → copy for every section → a working page |
| **AUDIT** | an existing page (URL, screenshot, pasted copy or file) | section-by-section scores, the three fixes that matter most, rewritten copy |
| **FEEDBACK** | a draft is ready to show people | questions for two reviewer groups, then a synthesis of their answers |

## Inputs

1. Look for `pmf/product-info.md`. If it exists, take the customer, problem (world without), value (world with), alternatives and evidence from it. Prefer the customer's own words from quotes.
2. If it doesn't exist, ask in one message: what the product does · who it's for (one persona or several?) · what they do today without it · why that falls short · the main objection that stops people buying · proof you have (customers, logos, numbers, testimonials) · what you want visitors to do (sign up, waitlist, pre-order, book a demo).
3. Decide the page type: **product page** (1 product, several personas) · **audience page** (several products, 1 persona) · **homepage** (several of each). If several personas: one tailored page per persona, or a "choose your own adventure" selector at the top.

## BUILD

**Step 1 — Value propositions.** Fill the table, one row per bad alternative:

| Bad alternative (what they do without you) | How you're better | Value prop (action statement, the customer's benefit) |
|---|---|---|

Write benefits, not capabilities: "here's what you can do with our product", never "here's what our product can do".

**Step 2 — Objections.** List what stops this persona from buying. Pick the **one** biggest objection for the header; the rest go to the features section.

**Step 3 — Header options.** Write 5 hero headers, each on a different strategy:
- value prop + bold specific claim (a number, a time, a result)
- value prop + the main objection handled ("Build your own website in 20 minutes. No code.")
- value prop spoken to the persona ("Get your favourite local meals right to your office.")
- value prop in the customer's own words, from a quote
- the plainest possible description of what you sell

**Litmus test for each:** if a visitor reads only this line, do they know exactly what you sell and why they'd want it? No slogans ("Supercharge your workflow!"), no corporate speak, no self-congratulation, no "AI-powered". Recommend one, with a reason.

**Step 4 — The rest of the copy**, in the proven template order:
1. **Navbar:** logo · links to key sections · CTA.
2. **Hero:** header · subheader (one or two sentences: introduce the product and how it creates the value prop: which feature makes the claim believable) · image direction (the product itself, in action; no abstract eye candy).
3. **Social proof:** logos and/or testimonials vouching for the hero's value prop. If there is none yet, say so and use the early-stage options in the method (never invent customers, logos, numbers or testimonials).
4. **CTA:** a button that continues the header's promise in a specific verb ("Find food", "Start recording", "Show my heatmap"), plus a short incentive. Not "Submit", not "Learn more".
5. **Features & objections:** 3–6 features. Each: a short, blunt header stating the value prop · 1–3 sentences (or bullets) on how the status quo falls short and how you make it better, handling the objection that belongs to it · image direction showing the feature in action. Every feature ties back to the hero's main value prop.
6. **CTA repeated.**
7. **Footer:** logo · links · CTA.

Above the fold you earn the attention; below the fold you earn the sale. Check the above-the-fold sequence: 1. your magic (header) · 2. how you create it (subheader) · 3. visualize it (image) · 4. they say it's magic (social proof) · 5. click here for magic (CTA).

**Step 5 — Build the page.** Write a single, self-contained HTML file (inline CSS, responsive, fast, no external frameworks unless the founder uses one), following the template order and the design checklist in the method. Use real product screenshots if the founder provides them; otherwise clearly labelled placeholders that say what the image must show. Wire the CTA to what the founder specifies: a form (Tally/Typeform connector if available), a payment link (Stripe, test mode first), or a booking link. Add analytics event names for page view, CTA click and form submit if the founder uses analytics.

If hosting, form or payment connectors are available, offer to deploy or wire them. **Ask before every write action.** Never publish without the founder's approval of the final page.

**Step 6 — Self-audit.** Run AUDIT on your own output before showing it. Fix anything that scores below 4.

## AUDIT

Get the page: fetch the URL if a web tool is available; otherwise ask for a screenshot, the copy, or the file. Read `references/audit-rubric.md` and score every section 1–5 with a one-line reason quoting the page.

Report:
1. **The verdict in one line:** would a first-time visitor know what's sold, why it's better, and what to do next, within five seconds?
2. **Scores** per section, in a table.
3. **The three fixes with the biggest effect**, most important first. For each: what's wrong (quote it), why it costs conversion (desire, labor or confusion), and the rewritten copy.
4. **Rewritten hero:** 3 header + subheader options, following BUILD step 3.
5. **What's missing** from the template (e.g. no social proof, CTA only once, features without objections).

Be direct and specific. Quote the page. Never praise generally.

## FEEDBACK

Before a page goes live, show it to two groups:
- **People outside the target market:** is the copy enticing and understandable without context? (The common mistake is assuming too much baseline knowledge.)
- **People in the target market:** is the message unique and convincing enough to choose this over the alternatives?

Give the founder these questions to send, as a form or a message (drafts only; the founder sends):
1. Would you take out your credit card and sign up right now? If not, what would it take?
2. On a scale of 1–10, how well did the page hold your interest?
3. What would you rewrite or redesign so it holds your interest better?
4. What questions are you left with?
5. What did you want more detail on?
6. If you had to delete half the page's copy and imagery, which half?
7. What triggered your "bulls*t" reflex?

When answers come back: group them by question and by reviewer group, quote them verbatim, and turn them into a list of changes, most frequent and most severe first. Then run AUDIT again on the revised page.

## Rules

- Never invent customers, logos, testimonials, numbers or claims. Every claim on the page must be true and supportable. A specific claim is only allowed if the founder can back it.
- Copy describes; it doesn't decorate. No slogans, no buzzwords, no "revolutionize", "empower", "supercharge", "AI-powered" as a value prop.
- One page, one primary action.
- If the page is for a validation test (waitlist, deposit, fake door), say so in the brief and keep the claims honest about what exists today.

---
Method: Gilles De Clerck's landing page workshop (gillesdc.com), used by hundreds of startups.
