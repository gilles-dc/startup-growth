# Fast-Track PMF — skills for Claude

Nine skills that take a startup from idea to product-market fit with AI. They follow one path:

```
PRE-MARKET                     MARKET
CUSTOMER → PROBLEM → SOLUTION → MVP → TEST → ITERATE → PMF → grow
```

| Skill | Use it to |
|---|---|
| `pmf-loop` | start here: write your `product-info.md`, find your riskiest assumption, get sent to the right stage |
| `pmf-customer` | define and test your first customer, find where they are, build a list of real people, count the market |
| `pmf-problem` | first from sources: research with checkable sources, reviews, forums, your own scraper, watching people work; then from conversations: script, rehearsal, invites, synthetic vs real, AI interviewer, synthesis with every quote verified |
| `pmf-solution` | write the promise in your customer's words, compare honestly with alternatives, read competitor pricing, size the market bottom-up |
| `pmf-mvp` | build the smallest thing that gets a market answer: kill criteria first, fake door with deposit or LOI, three versions, call to prototype, AI behind the curtain |
| `pmf-test` | put the test in front of the market: check the tracking, launch the traffic, read back against your kill criteria and decide |
| `pmf-iterate` | update your assumptions with evidence, pivot or persevere, and set up agents that keep the loop running |
| `pmf-retention` | the 40% survey, cohort retention, all feedback at once, churn reasons, and which level of fit you're at |
| `landing-page` | build, audit or get feedback on a landing page with a proven conversion method (Gilles De Clerck's landing page workshop) |

Every technique is labelled with how it works (chat · research · build · analyse · simulate) and, where it needs one, the building block underneath: teach (a skill), connect (a connector) or schedule (runs on its own). The names match the workshop slides.

Every skill reads and updates two files in a `pmf/` folder: `product-info.md` (your current hypothesis) and `assumptions.md` (what you believe, what proves it). Every skill applies the same rules: numbers need a source or say GUESS, quotes are verified or say PARAPHRASE, and nothing is sent, published, launched, charged or spent without your approval.

## Install

**Claude Code**
```
/plugin marketplace add gilles-dc/pmf-fast-track
/plugin install pmf-fast-track@gilles-dc
```
Then type `/pmf-loop` or just say "help me validate my startup idea".

**Claude.ai (web / desktop)**
Download the zips from `dist/`, then upload each one under Settings → Capabilities → Skills. Start with `pmf-loop.zip`. Skills are per user: everyone on the team uploads their own. Use them inside a Claude Project and keep `product-info.md` and `assumptions.md` as project files, so every chat starts from your latest hypothesis.

**Other agents (Codex, Cursor and others)**
```
npx skills add gilles-dc/pmf-fast-track
```

## Connect your tools (optional)

The skills work with research and chat alone. Each connected tool unlocks more; add them as custom connectors in Claude (Settings → Connectors) or in Claude Code. Turn on only what a task needs.

| Category | Examples (official remote servers) | Unlocks |
|---|---|---|
| Web research / scraping | Firecrawl, Apify, Bright Data | reviews at scale, live competitor pages, community threads |
| Prospecting / CRM | Apollo, Clay, Attio, HubSpot | lists of real people, interview pipeline |
| Meeting transcripts | Granola, Fireflies, Otter | interview synthesis without copy-paste |
| Forms | Tally, Typeform | waitlists, PMF survey, price survey |
| Payments | Stripe | deposit links, who paid |
| Product analytics | PostHog, Mixpanel, Amplitude, GA4 | funnels, experiments, retention |
| Ads | Meta Ads, TikTok Ads (Google Ads is read-only) | test traffic, created paused |
| Hosting | Vercel, Netlify | deploying test pages |
| Scheduling / chat | Calendly, Slack | booking links, agent digests |

Recurring agents (discovery agent, Monday bets, competitor watch, churn reasons) run as Claude Cowork scheduled tasks or Claude Code routines. `pmf-iterate` and `pmf-retention` contain the instructions.

## License

MIT. See `LICENSE`.

## Credits

Built for the workshop *Fast-Tracking Product-Market Fit with AI* by Gilles De Clerck — [gillesdc.com](https://gillesdc.com).

Methods and examples credited inside each skill, including: Steve Blank (Lean LaunchPad, 2026), Todd Jackson / First Round Capital (PMF Method), Rahul Vohra / Superhuman, Sean Ellis, Rob Fitzpatrick (The Mom Test), Teresa Torres, Caitlin Sullivan, Kyle Poyar, Sachin Rekhi, Claire Vo (How I AI), Emily Kramer (MKT1), Nielsen Norman Group, Tohidi et al. (CHI 2006).
