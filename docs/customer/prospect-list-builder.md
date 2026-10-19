# prospect-list-builder: who, by name, do I talk to this week?

Workshop slide C3 · stage: Customer

This skill builds a list of 50 named people who match your ICP, each with a profile link, why they match and one recent thing they posted or did, and shows how the list was built, filter by filter. It picks the route from your ICP: Apollo or Clay for B2B, Google Maps (via Apify) plus the company register for local businesses such as salons or clinics, and for consumers the people who posted about the problem in public. Then it counts the companies that fit, a market size built from companies you can name. Once some people have said yes, it can find ten more like them every Monday, with a drafted message each for you to send.

New to skills? Read [Start here](../start-here.md) first.

## When to use it

- You have a picture of your customer and need real people to talk to.
- You want a market count built from companies you can name.
- Some people have taken a call, signed up or paid, and you want more like them.

Before this, define the person with [icp](../customer/icp.md) and find the places with [icp-finder](../customer/icp-finder.md). No product file yet? Start with [pmf](../pmf.md). After this, check the problem is real for these people with [social-listener](../problem/social-listener.md).

## How to start

**Claude.ai, ChatGPT or any chat.** Type one of these:

- "Use prospect-list-builder to build a list of 50 people I could interview."
- "Use prospect-list-builder and take me through the prospect list step by step."
- "Use prospect-list-builder to count the companies that fit my ICP."
- "Use prospect-list-builder to find ten new people like the ones who said yes."

Naming the skill makes sure it loads. Once it's installed, a question about building a prospect list usually loads it on its own.

**Claude Code.** Type `/pmf:prospect-list-builder`, or add what you want: `/pmf:prospect-list-builder find 50 heads of compliance at Series A fintechs`. If you installed it with `npx skills add`, it's `/prospect-list-builder`.

## What you need

Every technique works without a connector. A connector saves you the searching and the copying.

| Technique | Chat only | Free | Paid, optional |
|---|---|---|---|
| 50 named prospects | search filters (or Maps searches) to run by hand, and a sheet | Apollo free plan, Apify free credit for Google Maps, a free CRM tier such as Attio or HubSpot | Clay, LinkedIn Sales Navigator |
| Count the companies that fit, in Apollo | the filter run by hand, the count pasted with a screenshot | Apollo free plan | LinkedIn Sales Navigator |
| Ten new matching prospects every Monday | a chat each Monday with your "said yes" list | Apollo free plan, a free CRM tier | a scheduled task in Claude Cowork or a Claude Code routine; Clay |

## Step by step

Ask to be taken through a technique and the skill stops at every point where you have to do something. To pick it up again, attach what it asked for and say the sentence in the last column. In a new chat, put the skill's name first, so the right skill loads: "Use prospect-list-builder to continue the prospect list".

| Technique | The skill does | You do | Then say |
|---|---|---|---|
| Prospects | pulls 50 from Apollo, or writes the search filters and a sheet | run the search and fill the sheet (skip with Apollo) | "continue the prospect list" |
| Company count | writes the filter and the rules for who qualifies | run the filter, screenshot the count, export the list (skip with Apollo) | "continue the company count" |
| Monday prospects | writes the weekly task, or the Monday routine, and the message template | switch it on or put the Monday chat in your calendar; send the drafts you like | "continue the Monday prospects" |

At each stop, the skill notes in `product-info.md` what it's waiting for, so a new chat knows where you are.

## What you get

- **Prospects:** 50 named people with a profile link, why they match and one recent thing they posted or did, and how the list was built, step by step. Local businesses: the business, its owner and its size from the register. For consumers: people who posted about the problem in public.
- **Company count:** a market size from companies you can name: the count, the share with the problem and what they spend today, each with its source or marked GUESS.
- **Monday prospects:** ten new people every Monday, with a research line and a drafted message each, for you to send.

Example: [TO ADD]

## Files it reads and writes

| File | What happens |
|---|---|
| `pmf/product-info.md` | Read first, for your customer and the problem. The Customer section gets the new detail, and Market size gets the company count. |
| `pmf/assumptions.md` | Read, then the persona rows are updated with what you found. |
| `pmf/lists/` | Your prospect lists, saved here. |

**Without them:** the skill offers to run [pmf](../pmf.md) first, which writes both files in about seven questions. Or it asks you five short questions and carries on, then gives you a `product-info.md` to save. In a plain chat that can't save files, it prints the changes for you to save and the lists as tables you can paste into a sheet.

Next step after this skill: [social-listener](../problem/social-listener.md), to check the problem is real for these people, then [interview-script](../problem/interview-script.md), to book the conversations with this list. Torn between customers? [icp-reply-rate-test](../customer/icp-reply-rate-test.md) uses ten people per variant from this list. The company count feeds [market-sizing](../solution/market-sizing.md).
