# Where to count

Official statistics first, company filings second, analyst reports only as a cross-check. Save every file with its link; prefer an API query (rerunnable) over a page.

## People (B2C)

| What | Europe | UK | US |
|---|---|---|---|
| Population by age | Eurostat `demo_pjan` (single years), `demo_pjangroup` (five-year bands) | ONS mid-year estimates via Nomis (`NM_2002_1`) | Census Bureau national estimates by single year |
| Big cities | Eurostat `met_pjangrp3` (metro areas by age band) | in Eurostat to 2019 | Census metro-area estimates |
| Education, job, labour status | Eurostat Labour Force Survey `edat_lfs_9901`; metro areas `met_edat_lfse4` | Eurostat LFS to 2019; ONS Annual Population Survey | ACS (American Community Survey) |
| Digital behaviour (wearables, health apps, online purchases) | Eurostat ICT household survey `isoc_*` (e.g. `isoc_iiot_use`), by age, sex, education, income, city | Ofcom Technology Tracker (download by hand) | Pew Research; HINTS (health and devices) |
| Health behaviour (tests, medicines, screening) | European Health Interview Survey `hlth_ehis_*`, by age, education, income | Health Survey for England | NHIS, HINTS |
| Spending | Eurostat Household Budget Survey `hbs_*` | ONS Family Spending | BLS Consumer Expenditure Survey |

Eurostat's API: `https://ec.europa.eu/eurostat/api/dissemination/statistics/1.0/data/<dataset>?format=JSON&lang=EN&...`. The list of datasets: `https://ec.europa.eu/eurostat/api/dissemination/catalogue/toc/txt?lang=en` (search it for a word such as "cholesterol" or "wearable"). Each table's breakdowns (age band, education, income quartile, city) are the crosses you may use; a cross the table doesn't hold is an overlap to bound.

## Companies (B2B)

| What | Where |
|---|---|
| Companies by industry code and size | national business registers and statistics offices (Statbel, CBS, KVK, Companies House, INSEE Sirene, Destatis); Eurostat Structural Business Statistics `sbs_*` by NACE code and size class; US Census County Business Patterns by NAICS |
| Regulated firms | the regulator's own register (EBA payment and e-money institutions, ESMA MiCA register, FCA register, national health or professional registers) |
| Funding stage | Crunchbase, Dealroom, funding news; sample and classify when no filter exists |
| Named lists the founder can screenshot | Apollo, Sales Navigator, Crunchbase filter counts |
| Job titles (end users inside companies) | LinkedIn or Apollo title counts; national occupation statistics (ISCO codes in the LFS) |

## Company disclosures (floors and spend)

- **Filings:** S-1 and 10-K (SEC EDGAR), annual reports, Companies House accounts. Paying members, revenue per member, revenue by region, age and sex of members.
- **Company pages:** customer counts ("join 200,000+ people"). Usually cumulative and all ages: a floor for "ever bought", never an annual share.
- **Price pages:** the competitor's price, for rings without a founder price.

## Not inputs

- **Analyst market reports** (Statista, IDC, Grand View, Mordor and the like): unknown definitions, no rerun. Quote one only as a cross-check, with how far it sits from your count. A count an analyst made and a company quoted (IDC shipments in an S-1) is still a cross-check.
- **Search volume:** counts only the people already looking. A cross-check on the aware share at most.
- **Synthetic interviews:** never evidence for a share.
