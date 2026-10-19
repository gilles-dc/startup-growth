# icp-finder: where do they hang out?

Workshop slide C2 · stage: Customer

This skill finds every place, online and offline, where your customers talk shop: subreddits and forums, Discord, Slack and Telegram communities, Facebook and LinkedIn groups, Instagram, TikTok and YouTube accounts, podcasts, newsletters, events and meetups. It searches each type on its own, keeps only places with a working link, and ranks a top ten with the best place of each type first, each with a line on why it's there. People complaining about the problem in those places are your first interview candidates.

New to skills? Read [Start here](../start-here.md) first.

## When to use it

- You don't know where your customers gather, online or in person.
- You want to complete the WHERE line of your ICP.
- You need places to find people to interview, or communities to join and read.

Before this, define the person with [icp](../customer/icp.md). No product file yet? Start with [pmf](../pmf.md). After this, find named people in these places with [prospect-list-builder](../customer/prospect-list-builder.md).

## How to start

**Claude.ai, ChatGPT or any chat.** Type one of these:

- "Use icp-finder to find where my customers hang out online."
- "Use icp-finder. Here's my ICP: which communities, podcasts and events should I join?"
- "Use icp-finder to check every link in my WHERE line and add what's missing."

Naming the skill makes sure it loads. Once it's installed, a question about where your customers gather usually loads it on its own.

**Claude Code.** Type `/pmf:icp-finder`, or add what you want: `/pmf:icp-finder find the communities where independent hairdressers talk shop`. If you installed it with `npx skills add`, it's `/icp-finder`.

## What you need

| Technique | Chat only | Free | Paid, optional |
|---|---|---|---|
| Where your customers hang out online | web search | web access to open and check every link | |

A scraping connector lets it check Reddit, which most AI web tools can't open. If the `where-your-customer-lives` skill (Varnan-Tech/opendirectory) is installed, it runs that first.

## What you get

- 20 to 40 places with working links, grouped by type, each with its country or language, its size where stated publicly, and one recent thread, post or episode about the problem.
- A top ten with the best place of each type first, each with its type and a line on why it's there.
- What could not be searched, per type, and reachable proxies where your customers gather out of search's reach.

Example: [TO ADD]

## Files it reads and writes

| File | What happens |
|---|---|
| `pmf/product-info.md` | Read first, for your customer and the problem. The WHERE line of the Customer section gets the new places. |
| `pmf/assumptions.md` | Read, then the persona rows are updated with what you found. |
| `pmf/lists/` | The places, saved here. |

**Without them:** the skill offers to run [pmf](../pmf.md) first, which writes both files in about seven questions. Or it asks you five short questions and carries on, then gives you a `product-info.md` to save. In a plain chat that can't save files, it prints the changes for you to save and the places as a table you can paste into a sheet.

Next step after this skill: [prospect-list-builder](../customer/prospect-list-builder.md), for named people in these places; then [social-listener](../problem/social-listener.md), to check the problem is real for them.
