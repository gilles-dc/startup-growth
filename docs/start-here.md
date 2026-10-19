# Start here

A skill is a set of instructions your AI follows for one kind of job. Install these once, and when you ask for help with your startup, the AI follows a tested method: it asks the questions that matter, uses the tools you've connected, checks its own numbers, and stops for your approval before anything is sent, published or paid.

You don't need to code. You need a Claude account (or ChatGPT, or a coding agent) and ten minutes.

## 1. Install

### Claude.ai (web and desktop app)

Works on every plan, Free included.

1. Turn on **Code execution and file creation**: Settings → Capabilities. Skills don't run without it. On a Team or Enterprise plan, an owner first allows skills in the organisation settings.
2. Download the zip for each skill you want from the [`dist/`](../dist) folder: one zip per skill, named after it (`pmf.zip`, `icp.zip`, `pmf-survey.zip`…). Start with `pmf.zip`, then add the skills for the stage you're at. Using `social-listener`? Also download `last30days.skill` from [its latest release](https://github.com/mvanhorn/last30days-skill/releases/latest) and upload it the same way.
3. Upload each zip: Customize → Skills → **+** → Create skill → Upload a skill.

**Safari catch:** Safari unzips downloads by default, so you end up with a folder and Claude.ai won't take it. Either turn it off (Safari → Settings → General → untick "Open 'safe' files after downloading") and download again, or right-click the folder in Finder → Compress, and upload the new zip.

Skills are per person: everyone on your team uploads their own, or a Team or Enterprise owner shares them with the whole organisation.

### Claude Code

```
/plugin marketplace add gilles-dc/startup-growth
/plugin install pmf@gilles-dc
/plugin install last30days@gilles-dc
```

This installs all 25 skills, plus [last30days](https://github.com/mvanhorn/last30days-skill) (by Matt Van Horn, MIT), the search engine `social-listener` runs on. Its setup wizard adds X, YouTube and TikTok the first time you run it. Type `/pmf:pmf` to start, or just ask for help with your startup idea and the right skill loads on its own. Every skill is `/pmf:<skill name>`, for example `/pmf:pmf-survey`.

### ChatGPT

Uploading skills to ChatGPT is limited to Business, Enterprise and Edu plans (and a workspace owner has to switch skills on). On any plan, open a skill's `SKILL.md` on GitHub, copy all of it, and paste it into the chat or into a ChatGPT Project's instructions. One skill per chat or Project works best.

### Codex, Cursor and other coding agents

```
npx skills add gilles-dc/startup-growth
```

One skill only: add `--skill pmf` (or any other skill's name). For `social-listener`'s search engine, also run:

```
npx skills add mvanhorn/last30days-skill
```

## 2. Your first conversation

Start with `pmf`, the front door. Type:

> Use the pmf skill. Help me find product-market fit for my startup.

It asks you seven questions about your product, your customer and your evidence so far. Short answers are fine. From those it writes two files:

- `product-info.md`: what you believe about your product and customer right now, each line marked as a guess or as evidence.
- `assumptions.md`: everything you're assuming, ranked by how much it would hurt to be wrong.

Then it names your riskiest assumption and sends you to the one skill that tests it. Every other skill reads these two files and updates them when you learn something.

Skipped `pmf`? Any skill still works: it asks the few questions it needs, or offers to run `pmf` first.

**Going step by step.** Say "take me through it step by step" and the skill stops every time you need to do something: send a survey, export a file, publish a page. It tells you what to bring back and the sentence to say when you return, so you can pick it up days later. In a new chat, put the skill's name first: "Use pmf-survey to continue the PMF survey".

## 3. Use a Claude Project

Create a Project for your startup (Projects in the Claude.ai sidebar) and add `product-info.md` and `assumptions.md` as project files. Every chat in that Project then starts from your latest version, so you never paste your context again, and one chat per job stays short and focused.

After a skill updates the files, replace the project files with the new versions. In Claude Code, the files live in a `pmf/` folder in your project and are updated in place.

## 4. The skills

One skill per technique, grouped by the stage it belongs to. The code is the slide it comes from in the workshop.

| Stage | Skill | Slide | Use it to |
|---|---|---|---|
| Start | [pmf](pmf.md) | | write your files, find your riskiest assumption, get sent to the right skill |
| Customer | [icp](customer/icp.md) | C1 | define your ideal customer, specific enough that a stranger could find them |
| | [icp-finder](customer/icp-finder.md) | C2 | find where your customers gather online |
| | [prospect-list-builder](customer/prospect-list-builder.md) | C3 | build a list of named people to contact, and count how many companies fit |
| | [icp-reply-rate-test](customer/icp-reply-rate-test.md) | C4 | pick your first customer by who replies |
| Problem | [social-listener](problem/social-listener.md) | P1 | what people said about the problem this month, plus research with sources you can check |
| | [review-mining](problem/review-mining.md) | P2 | what customers of today's solutions complain about |
| | [workaround-mapper](problem/workaround-mapper.md) | P3 | watch people show their workarounds on YouTube |
| | [interview-script](problem/interview-script.md) | P4 | interview questions about the past, the script and the invites |
| | [interview-synthesis](problem/interview-synthesis.md) | P5 | patterns across interviews, with every quote checked |
| Solution | [competitive-analysis](solution/competitive-analysis.md) | S1 | how competitors sell, price and grow, turned into tests |
| | [buyer-objections-mapper](solution/buyer-objections-mapper.md) | S2 | the questions buyers ask before buying |
| | [market-sizing](solution/market-sizing.md) | S3 | whether the market is big enough |
| | [value-proposition-generator](solution/value-proposition-generator.md) | S4 | what you promise, against which alternatives, and the headers worth testing |
| MVP | [landing-page-builder](mvp/landing-page-builder.md) | M1 | decide what counts as a yes, then build, audit or test a landing page |
| | [prototype](mvp/prototype.md) | M2 | three prototypes side by side, for interviews |
| Test | [tracking-audit](test/tracking-audit.md) | T1 | check every click is counted before you spend a euro |
| | [ad-trigger-test](test/ad-trigger-test.md) | T2 | build the test ads, paused, for your approval |
| | [value-proposition-test](test/value-proposition-test.md) | T3 | read the results and decide: kill, iterate or scale |
| Iterate | [know-your-customer](iterate/know-your-customer.md) | I1 | quiz yourself on your customer |
| | [pivot-or-persevere](iterate/pivot-or-persevere.md) | I2 | update what you believe and decide |
| | [weekly-product-bets](iterate/weekly-product-bets.md) | I3 | five ranked bets to test, every Monday |
| Retention | [pmf-survey](retention/pmf-survey.md) | PMF1 | the PMF survey, read the way Superhuman did, 40% per segment as the gate to grow |
| | [retention-audit](retention/retention-audit.md) | PMF2 | your retention curve, and who stays and who leaves |
| | [why-people-churn](retention/why-people-churn.md) | PMF3 | ask everyone who cancels why, and group the answers |

## 5. Connect your tools (optional)

Every skill works with chat and web research alone. Connecting a tool (Settings → Connectors in Claude.ai) lets the skill read your data or create drafts directly. Without one, you export a file and attach it. Each skill's page lists what it can use, per technique. The full list is in the [main README](../README.md#connect-your-tools-optional).
