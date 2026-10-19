# Worked examples

Two real runs. Copy the shape, never the numbers.

## 1. B2C: one dashboard for sleep, blood work and supplements (Europe, €144 a year)

**ICP (beachhead):** 34–46, knowledge worker or founder on €75K–150K in London, Amsterdam, Berlin, Stockholm; wears Oura or Whoop; pays privately for 2+ blood panels a year; takes 5–12 supplements; can't connect the three.

**Category:** "everyone who tracks their health with a wearable". Market type: resegmented (people already pay for wearable apps and for blood tests; the join is new).

**Criteria sorted:**
- Sharpeners: big city · 34–46 · knowledge worker on €75K+ (proxy: a degree) · male skew · the podcasts.
- Requirements: a wearable (the product's core input) · a recent blood result (the second input).
- Uncountable: pays privately · 5–12 supplements · has the problem · wears it at night.

**Rings (Europe, people, base, low–high):**

| Ring | Dropped | People | Spread | Product must add | Likely |
|---|---|---|---|---|---|
| R0 | — (35–44, degree, 33 metro areas of 2m+, wearable, blood test) | 2.7m (1.8–3.5m) | ×1.9 | — | probable |
| R1 | the city | 8.5m (5.6–11.3m) | ×2.0 | lab reports in every language | probable |
| R2 | the age band → 25–64 | 30m (20–39m) | ×1.9 | content per life stage | plausible |
| R3 | the degree | 66m (45–90m) | ×2.0 | a lower tier, plainer words | plausible |
| R4 | the blood test | 91m (88–95m) | ×1.1 | a blood test to sell | possible |
| R5 | the age limit → 16–74 | 119m (115–124m) | ×1.1 | insights from the wearable alone | possible |

**Answer (by spend):** TAM: 227m wearable users in Europe and the US × at least €27 a year on tracking, private blood tests and supplements = €6.2bn at least (up to €92bn). SAM: the 66m in the ring served as designed × the same spend = €1.8bn at least. SOM: 8.5m × €144 = €1.2bn; beachhead 2.7m × €144 = €383m. Verdict: big enough, but €144 is five times the documented floor spend per person, so the price must come out of the supplement and test budgets the product helps cut.

**Sources:** Eurostat wearable use 2024 by age and education (exact groups, per country); Labour Force Survey 2025 (degree share); European Health Interview Survey 2019 (blood cholesterol test in the last 12 months); Eurostat metro-area populations; HINTS 2024 for the US; Oura's S-1/A for the spend per member ($64 a year) and proven payers.

**What made the ranges tight:** only official shares for exact groups; one bounded overlap (wearable × blood test: independent to nested); the three guessed filters of the earlier run (night wear, private test, has the problem) moved to the uncounted list.

## 2. B2B: compliance automation for licensed fintechs (EU, €18,000 a year)

Three runs on 18 October 2026 (`fintech-test/`). The first priced every circle at €18,000 and found a €60m TAM, which Gilles rejected: fintech is a huge business, so the method was wrong. The third run sized the problem by spend.

**Category:** "every regulated financial firm that must run compliance": banks and licensed payment, e-money and crypto firms. Market type: existing.

**TAM and SAM by spend** (`spend.py`, sources in `raw/spend/SPEND-NOTES.md`):

| Who | Compliance staff | € a year |
|---|---|---|
| EU banks | 2.8% (Deutsche Bank's dedicated function) to 16.2% (Dutch banks, all financial-crime work) of 2.1m staff (ECB) | €6.4–37.3bn |
| UK banks | 20,009 FTE in financial-crime roles (FCA returns) | €2.2bn |
| Licensed fintechs | 2,081 firms × at least 2 people | €0.3bn |
| **TAM** | × €108k all-in per FTE (Dutch banks: €1.4bn ÷ 13,000) | **€8.8bn at least** (up to €40bn) |
| **SAM** | the 32–37% that goes to technology (LexisNexis UK 2023, EMEA 2019) | **€2.8bn at least** (up to €15bn) |

**SOM and beachhead by price:** all 228 licensed firms in Lithuania and Germany classified (`classify/`): beachhead 15 Series A–B firms (11 named) × €18,000 = €0.3m; SOM 802 independent firms in the EU and UK × €18,000 = €14.4m.

**Verdict:** big enough for a venture case: €100m a year is 3.5% of the SAM floor. The limit sits in the price: €18,000 is 12% of what the smallest licensed firm spends on compliance.

**What this example teaches:** the floor carries the verdict, so the wide range (narrow versus broad definition) doesn't change the decision; one all-in cost per FTE keeps the definition consistent; the beachhead's price says nothing about the size of the problem.
