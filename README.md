# Databricks, Decomposed

**A scroll-driven interactive essay on the Databricks business model.**

Best experienced on a desktop browser.

## The argument

Databricks is not a warehouse company, it is a data-gravity company. Storage was decoupled from compute on open table formats, and from that moment the marginal cost of pointing a new workload at data you already govern approaches zero. Every business line is a consequence of that one fact.

| Arm | Role in the model | Figures (June 2026) |
| --- | --- | --- |
| **01 Platform** | Land and govern. Get the single copy of the data under management, then sell against it forever. | ~$3.7B of the run rate, net revenue retention around 140% |
| **02 SQL** | The attack on Snowflake. Warehousing workloads run against data that is already landed. | ~$1.5B (Sacra estimate), up from a $600M run rate in Dec 2024 and $1B in Jan 2026 |
| **03 AI** | The wager on agents. Bought in, through MosaicML ($1.3B), Tabular, Neon and Tecton. | $1.7B, company-reported |

Total: roughly $6.9B annualized revenue as of June 2026, growing over 80% year on year, against company-reported run-rate milestones of $425M, $1.5B and $3B in prior years.

The piece closes on what the growth costs. Gross margin has slid from about 80% to about 74% as the AI buildout is funded. The company is still private on purpose: no S-1 filed, Ali Ghodsi called 2026 "a terrible year to go public" and pointed to 2027 at the earliest, and the February 2026 Series L (over $7B including roughly $2B of debt capacity) included employee tender liquidity, which removes the main internal pressure to list. Private capital is currently willing to underwrite margin compression at prices public markets have not had to. For scale, Snowflake's public market cap was about $83B when Databricks priced at $134B, with reported talks since at $165B to $175B.

## The build

A single self-contained `index.html`. No frameworks, no build step, no dependencies beyond Google Fonts.

- Full-viewport sections with scroll snap and a chapter rail across thesis, business model, the three arms, the flywheel and the numbers
- Count-up figures, a valuation timeline from $28B in Feb 2021 to the reported $165B to $175B talks, and a revenue-split breakdown, all driven by IntersectionObserver and CSS transitions
- Hand-composed vector diagrams: the lake / warehouse / lakehouse collapse into one copy of the data, and the compounding loop between the three arms
- DM Sans throughout, one accent color, light ground

## Sources

Figures as of 12 July 2026, with estimates labelled as estimates in the piece itself: Databricks newsroom, CNBC, Bloomberg, The Information, Reuters, PYMNTS, and Sacra for the warehousing estimate. Reported acquisition prices and the $165B to $175B talks are marked unconfirmed where they are unconfirmed.

## How it was built

Written with Claude Code as the implementation tool. The argument, the structure and the design calls are mine, and every figure was checked against a primary source before it went into the page, with estimates left labelled as estimates rather than rounded into facts. The model wrote code against decisions that were already made rather than deciding what the piece should say.
