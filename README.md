# Startup Growth — skills by Gilles De Clerck

My library of skills for early-stage startup growth, built for Claude and usable in any AI that reads a SKILL.md. Eleven skills: eight that take a startup from idea to product-market fit along one path, and three standalone methods.

```
PRE-MARKET (qualitative)          MARKET (counted)
CUSTOMER → PROBLEM → SOLUTION  →  MVP → TEST → ITERATE → PMF → grow
```

**The path to product-market fit**

| Skill | Use it to |
|---|---|
| `pmf-loop` | start here: write your `product-info.md`, find your riskiest assumption, get sent to the right stage |
| `pmf-customer` | define and test your first customer, find where they are, build a list of real people, count the market |
| `pmf-problem` | first from sources: research with checkable sources, reviews, forums, your own scraper, watching people work; then from conversations: script, rehearsal, invites, synthetic vs real, AI interviewer, synthesis with every quote verified |
| `pmf-solution` | what buyers ask, competitors in parallel, live pricing and pricing history, market size, the promise in your customer's words |
| `pmf-mvp` | build the smallest thing that gets a market answer: kill criteria first, fake door with deposit or LOI, three versions, call to prototype, AI behind the curtain |
| `pmf-test` | put the test in front of the market: check the tracking, launch the traffic, read back against your kill criteria and decide |
| `pmf-iterate` | update your assumptions with evidence, pivot memo, and agents that keep the loop running |
| `pmf-retention` | the 40% survey, cohort retention, all feedback at once, churn reasons, and which level of fit you're at |

**Standalone methods**

| Skill | Use it to |
|---|---|
| `icp` | define your ideal customer in five dimensions (who, what, why, how, where), specific enough that a stranger could find them |
| `competitive-analysis` | learn how comparable companies grow: their A/B tests, ads, content and onboarding, turned into tests worth running |
| `landing-page` | build, audit or get feedback on a landing page with a proven conversion method |

Every technique is labelled with how it works (chat · research · build · analyse · simulate) and, where it needs one, the building block underneath: skill (it uses another skill), connector (it uses a connector) or schedule (runs on its own). Each skill starts with **What you need**: what works in a plain chat, which free tools help, which paid tools are optional.

The pmf skills read and update two files in a `pmf/` folder: `product-info.md` (your current hypothesis) and `assumptions.md` (what you believe, what proves it). Every skill applies the same rules: numbers need a source or say GUESS, quotes are verified or say PARAPHRASE, and nothing is sent, published, launched, charged or spent without your approval.

## Install

**Claude Code**
```
/plugin marketplace add gilles-dc/startup-growth
/plugin install startup-growth@gilles-dc
```
Then type `/pmf-loop` or just say "help me validate my startup idea".

**Claude.ai (web / desktop)**
Download the zips from `dist/`, then upload each one under Settings → Capabilities → Skills. Start with `pmf-loop.zip`. Skills are per user: everyone on the team uploads their own. Use them inside a Claude Project and keep `product-info.md` and `assumptions.md` as project files, so every chat starts from your latest hypothesis.

**ChatGPT and others**
A skill is a markdown file. Paste the contents of a `SKILL.md` into the chat or into a Project's instructions. For Codex, Cursor and other agents:
```
npx skills add gilles-dc/startup-growth
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

By Gilles De Clerck — [gillesdc.com](https://gillesdc.com). First presented at the workshop *Fast-Tracking Product-Market Fit with AI*.

Methods and examples credited inside each skill, including: Steve Blank (Lean LaunchPad, 2026), Todd Jackson / First Round Capital (PMF Method), Rahul Vohra / Superhuman, Sean Ellis, Rob Fitzpatrick (The Mom Test), Teresa Torres, Caitlin Sullivan, Kyle Poyar, Sachin Rekhi, Claire Vo (How I AI), Emily Kramer (MKT1), Nielsen Norman Group, Tohidi et al. (CHI 2006).
