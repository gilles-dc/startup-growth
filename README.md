# Startup Growth — skills by Gilles De Clerck

My library of skills for finding product-market fit, built for Claude and usable in any AI that reads a SKILL.md. 25 skills: one front door, and one skill per technique, grouped by stage. Each skill carries the code of its slide in the workshop *Fast-Tracking Product-Market Fit with AI* (C1, P2, …).

New to skills? Read **[Start here](docs/start-here.md)**.

```
PRE-MARKET (qualitative)          MARKET (counted)
CUSTOMER → PROBLEM → SOLUTION  →  MVP → TEST → ITERATE → PMF → grow
```

| Stage | Skill | Slide | Use it to |
|---|---|---|---|
| Start | [`pmf`](docs/pmf.md) | | write your `product-info.md`, find your riskiest assumption, get sent to the right skill |
| Customer | [`icp`](docs/customer/icp.md) | C1 | define your ideal customer in five dimensions (who, what, why, how, where), specific enough that a stranger could find them |
| | [`icp-finder`](docs/customer/icp-finder.md) | C2 | find where your customers gather online |
| | [`prospect-list-builder`](docs/customer/prospect-list-builder.md) | C3 | 50 named prospects, and a count of the companies that fit |
| | [`icp-reply-rate-test`](docs/customer/icp-reply-rate-test.md) | C4 | five first customers, picked by reply rate |
| Problem | [`social-listener`](docs/problem/social-listener.md) | P1 | what people said about the problem this month; research with sources you can check |
| | [`review-mining`](docs/problem/review-mining.md) | P2 | competitors' bad reviews, themed and counted |
| | [`workaround-mapper`](docs/problem/workaround-mapper.md) | P3 | the workarounds people show on YouTube |
| | [`interview-script`](docs/problem/interview-script.md) | P4 | interview questions about the past, the script, the invites |
| | [`interview-synthesis`](docs/problem/interview-synthesis.md) | P5 | patterns across interviews, with every quote verified |
| Solution | [`competitive-analysis`](docs/solution/competitive-analysis.md) | S1 | how comparable companies grow and price: their A/B tests, ads, content and onboarding, turned into tests worth running |
| | [`buyer-objections-mapper`](docs/solution/buyer-objections-mapper.md) | S2 | the questions buyers ask before buying |
| | [`market-sizing`](docs/solution/market-sizing.md) | S3 | TAM, SAM, SOM, from sources you can open |
| | [`value-proposition-generator`](docs/solution/value-proposition-generator.md) | S4 | every bad alternative, how you do each better, headers with a hook, the positionings worth testing |
| MVP | [`landing-page-builder`](docs/mvp/landing-page-builder.md) | M1 | write what counts as a yes, then build, audit or get feedback on a test page with deposits |
| | [`prototype`](docs/mvp/prototype.md) | M2 | three prototypes side by side; from a call to a prototype; deliver it by hand first |
| Test | [`tracking-audit`](docs/test/tracking-audit.md) | T1 | check the tracking end to end before any traffic |
| | [`ad-trigger-test`](docs/test/ad-trigger-test.md) | T2 | build the ads in Meta, paused |
| | [`value-proposition-test`](docs/test/value-proposition-test.md) | T3 | read the results against your kill criteria and decide |
| Iterate | [`know-your-customer`](docs/iterate/know-your-customer.md) | I1 | quiz yourself on your customer |
| | [`pivot-or-persevere`](docs/iterate/pivot-or-persevere.md) | I2 | update the assumption board, write the pivot-or-persevere memo |
| | [`weekly-product-bets`](docs/iterate/weekly-product-bets.md) | I3 | five ranked ideas to test, every Monday |
| Retention | [`pmf-survey`](docs/retention/pmf-survey.md) | PMF1 | the PMF survey, read the Superhuman way; 40% per segment is the gate to grow |
| | [`retention-audit`](docs/retention/retention-audit.md) | PMF2 | cohort retention, who stays and who leaves, and which level of fit you're at |
| | [`why-people-churn`](docs/retention/why-people-churn.md) | PMF3 | ask everyone who cancels why, and group the answers each month |

Techniques that don't have a slide of their own sit in the closest skill under **More techniques**.

Every technique is labelled with how it works (chat · research · build · analyse · simulate) and, where it needs one, the building block underneath: skill (it uses another skill), connector (it uses a connector) or schedule (runs on its own). Each skill starts with **What you need**: what works in a plain chat, which free tools help, which paid tools are optional.

The skills read and update two files in a `pmf/` folder: `product-info.md` (your current hypothesis) and `assumptions.md` (what you believe, what proves it). Every skill applies the same rules: numbers need a source or say GUESS, quotes are verified or say PARAPHRASE, and nothing is sent, published, launched, charged or spent without your approval.

## Install

Step-by-step instructions per platform, with the catches: **[Start here](docs/start-here.md)**.

**Claude Code**
```
/plugin marketplace add gilles-dc/startup-growth
/plugin install pmf@gilles-dc
/plugin install last30days@gilles-dc
```
The second line installs [last30days](https://github.com/mvanhorn/last30days-skill) by Matt Van Horn (MIT), the search engine `social-listener` runs on. Then type `/pmf:pmf` or just say "help me validate my startup idea". Every skill is `/pmf:<skill>`.

**Claude.ai (web / desktop)**
Turn on Code execution and file creation (Settings → Capabilities). Download the zips from `dist/`, one per skill, and upload each one under Customize → Skills. Start with `pmf.zip`. For `social-listener`, also upload `last30days.skill` from [its latest release](https://github.com/mvanhorn/last30days-skill/releases/latest). Skills are per user: everyone on the team uploads their own. Use them inside a Claude Project and keep `product-info.md` and `assumptions.md` as project files, so every chat starts from your latest hypothesis.

**ChatGPT and others**
A skill is a markdown file. Paste the contents of a `SKILL.md` into the chat or into a Project's instructions. For Codex, Cursor and other agents:
```
npx skills add gilles-dc/startup-growth
```
Add `--skill <name>` to install one skill. For `social-listener`'s search engine, also run `npx skills add mvanhorn/last30days-skill`.

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
| Ads | Meta Ads, TikTok Ads, LinkedIn Ads (community server; Google Ads is read-only) | test traffic, created paused or as drafts |
| Hosting | Vercel, Netlify | deploying test pages |
| Scheduling / chat | Calendly, Slack | booking links, agent digests |

Recurring agents (every new interview analysed, five ideas to test every Monday, competitor watch, ask everyone who cancels why) run as Claude Cowork scheduled tasks or Claude Code routines. `know-your-customer`, `weekly-product-bets`, `competitive-analysis` and `why-people-churn` contain the instructions.

## License

MIT. See `LICENSE`.

## Credits

By Gilles De Clerck — [gillesdc.com](https://gillesdc.com). First presented at the workshop *Fast-Tracking Product-Market Fit with AI*.

Methods and examples credited inside each skill, including: Steve Blank (Lean LaunchPad, 2026), Todd Jackson / First Round Capital (PMF Method), Rahul Vohra / Superhuman, Sean Ellis, Rob Fitzpatrick (The Mom Test), Teresa Torres, Caitlin Sullivan, Kyle Poyar, Sachin Rekhi, Claire Vo (How I AI), Emily Kramer (MKT1), Nielsen Norman Group, Tohidi et al. (CHI 2006).
