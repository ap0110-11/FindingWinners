# Source Playbook

Concrete instructions for where to look and how. Organized by research **lane** — each lane maps to a parallel task in `skills/catalyst-scan.md`.

Two rules govern everything here:

1. **Every factual claim carries an as-of date and a source tier.** A number without a date is not a number.
2. **Never claim to have checked a source you couldn't reach.** Write "Reddit not accessible in this run" and move on. Fabricated or implied access is the single worst failure mode in this system.

---

## Source Tiers

Tier determines what a source is allowed to support.

| Tier | What | May support |
|---|---|---|
| **T1** | SEC filings, earnings call transcripts, official company releases, audited financials | Any factual claim |
| **T2** | Government/regulatory data (FERC, FCC, USPTO, USAspending, ISO queues), exchange data, official foreign-exchange filings (TWSE, KRX, TSE) | Any factual claim |
| **T3** | Specialist trade press with named sourcing (SemiAnalysis, The Information, DigiTimes, TrendForce, Blocks & Files, Data Center Dynamics, Light Reading) | Factual claim if corroborated by a second T1–T3 source; otherwise a hypothesis |
| **T4** | Sell-side notes, mainstream financial media, data aggregators, Seeking Alpha | Consensus/expectations claims. **Not** standalone facts. |
| **T5** | Reddit, X, StockTwits, Discord, YouTube, anonymous forums, Glassdoor/Blind | Sentiment and hypothesis-generation **only**. Never a fact. |

**Hard rule:** a T4 or T5 source can never be the sole basis for a factual claim in a report. It can tell you what people *believe*, which is exactly what we need for the expectations side — just don't confuse the two.

---

## Lane A — Primary Filings (SEC / EDGAR)

The highest-yield, lowest-competition lane. Most research stops at the press release; the filing says more.

### Endpoints

If your platform can issue raw HTTP requests, SEC endpoints require a `User-Agent` header identifying you (e.g. `FindingWinners research contact@example.com`) and rate-limit at 10 req/sec. If it can only browse rendered pages, use the human-facing UI in the last column — same data, more steps.

| Purpose | JSON endpoint | Browse-only fallback |
|---|---|---|
| Ticker → CIK map | `https://www.sec.gov/files/company_tickers.json` | search the company on `sec.gov/edgar/search/` |
| All filings for a company | `https://data.sec.gov/submissions/CIK{10-digit-padded}.json` | `sec.gov/cgi-bin/browse-edgar?action=getcompany&CIK={ticker}&type={form}` |
| Every XBRL fact a company reported | `https://data.sec.gov/api/xbrl/companyfacts/CIK{padded}.json` | the "Financial Report" / R-file exhibits on the filing index page |
| One metric's full history | `https://data.sec.gov/api/xbrl/companyconcept/CIK{padded}/us-gaap/{Tag}.json` | read it out of successive filings |
| Same metric across all filers in a period | `https://data.sec.gov/api/xbrl/frames/us-gaap/{Tag}/USD/CY2026Q2I.json` | no good fallback; skip and note it |
| Full-text search (2001→present) | `https://efts.sec.gov/LATEST/search-index?q=%22phrase%22&forms=8-K&startdt=&enddt=&ciks=` | `https://www.sec.gov/edgar/search/` — same index, rendered |

Full-text search notes: `/LATEST/` must be uppercase, page size is 10 via the `from` offset, `forms=` matches the root form so `10-K` includes `10-K/A`, and the `items` field filters 8-K item codes.

The filings themselves are always plain HTML or text on `sec.gov/Archives/`, so **Lane A works on every platform with web access** even when the structured APIs don't. That matters, because this is the highest-value lane and it should never be the one that gets skipped.

### What to actually extract

**Forms and what they're good for:**

| Form | Signal |
|---|---|
| 10-K / 10-Q | The real numbers, segment detail, customer concentration, and the language diff (below) |
| 8-K Item 2.02 | Earnings release + the exhibit tables the press release summarizes |
| 8-K Item 1.01 | Material definitive agreement — the actual contract terms behind a "partnership" headline |
| 8-K Item 5.02 | Executive departure. An unexplained CFO exit before an earnings date is a live red flag |
| 8-K Item 4.02 | Non-reliance on prior financials. Hard disqualifier |
| DEF 14A (proxy) | What management is actually paid to maximize. If comp flipped from revenue growth to FCF/ROIC, strategy changed before the strategy was announced |
| S-1 / S-3 / 424B | Dilution incoming; S-3 shelf activity is a financing tell |
| SC 13D / 13G | Ownership stakes above 5%; 13D means activist intent |
| Form 4 | Insider transactions, filed within 2 business days |
| NT 10-K / NT 10-Q | Late filing notification. Almost never benign |
| 20-F / 6-K | Foreign private issuers — thinner coverage, more inefficiency |

**The highest-value technique: the language diff.** Pull the current 10-Q/10-K and the prior one, and diff:

- Risk factors — a newly added risk factor is management telling you what's changed, in writing, under legal liability. Year-over-year risk factor changes are systematically under-read.
- MD&A phrasing — "we expect continued strength" → "we expect demand to remain stable" is a downgrade.
- Customer concentration — did "one customer represented 22%" become 31%?
- Backlog / RPO / deferred revenue — check the *composition* and duration, not just the total. RPO growing while short-term deferred revenue shrinks means the backlog is lengthening, which is worse than it looks.
- Segment reporting changes — a re-segmentation almost always hides or highlights something deliberately.
- Share count — actual dilution vs. what the adjusted EPS implies.

**Cash flow reconciliation:** compare net income to operating cash flow to free cash flow. Widening gaps mean receivables, inventory, or capitalization games. In AI infrastructure specifically, check whether capex is being financed off-balance-sheet or via customer prepayments, and whether GPU depreciation schedules were extended (an easy, quiet margin boost).

### Deliverable
Evidence cards for: reported vs. consensus deltas, three material language diffs, cash conversion trend, share count trend, any red-flag form filed.

---

## Lane B — Institutional Positioning (13F / 13D-G / Form 4 / Short Interest)

This lane answers "who owns it and who's leaning which way" — the other half of the expectations question.

### 13F

- Filed by institutions managing >$100M, **due 45 days after quarter end**: ~Feb 14, May 15, Aug 14, Nov 14.
- Access: EDGAR `forms=13F-HR` full-text search by CIK, or aggregators like `13f.info` and WhaleWisdom for the pre-joined quarter-over-quarter deltas.
- Two useful directions:
  - **Ticker-centric:** who initiated, added, trimmed, or exited a position last quarter, and what happened to the holder count.
  - **Manager-centric:** track a short list of managers whose process resembles ours (concentrated, research-driven, long-horizon) and read their new positions as idea generation.

**Limitations you must state, not ignore:**
- Up to 45 days stale, and it's a snapshot of one day. A manager can have fully exited before you read it.
- Long US equity positions only. No shorts, no bonds, no non-US listings, no swaps. A "new position" can be a hedge leg.
- Confidential treatment requests let managers delay disclosure of accumulations.
- Index and quant funds dominate the holder list and their changes are mechanical, not opinions. Filter for discretionary managers.

**How to use it correctly:** as an *expectations* input, not a *validation* input. Institutional under-ownership plus improving fundamentals is a setup. Institutional crowding plus a consensus-long narrative is a warning. Never buy something because a famous manager did.

### 13D / 13G
- 13D (>5% with intent to influence) is due within 5 business days and is a genuine event. 13G is the passive version.
- A 13D on a watchlist name changes the catalyst calendar immediately.

### Form 4 — Insider Activity
- Filed within 2 business days. `openinsider.com` is the fastest screen.
- **Signal ranking:** clustered open-market buys by multiple officers/directors > a single large CEO open-market buy > buys at a premium to market. All of these are meaningfully informative.
- **Noise:** sales under a 10b5-1 plan, option exercises, tax withholding. Most insider selling is noise; almost no insider buying is.
- Check for *new or amended* 10b5-1 plans right before a catalyst — that's a tell worth noting.

### Short Interest & Borrow
- Exchange short interest is published twice monthly (settlement mid-month and month-end, published ~8 business days later).
- Track days-to-cover and the trend, plus borrow cost/availability if reachable.
- High short interest is not bullish by itself. High short interest *plus* an improving fundamental trend *plus* a near-dated catalyst is a distinct, higher-variance setup — flag it as such and size accordingly.

### Options-implied expectations
- Earnings-implied move from the front-dated straddle tells you what the market has already priced for the event. This is the single most direct read on "what's priced in" for a catalyst.
- Skew and term structure show where the fear is. Compare the implied move to the last 4–8 actual post-earnings moves.

### Deliverable
Holder concentration and direction, notable discretionary initiations/exits with as-of quarter, insider cluster activity, short interest trend, implied move vs. realized history.

---

## Lane C — Expectations Baseline

You cannot detect a mismatch without knowing the baseline. Do this **before** forming any view.

Capture:
- Consensus revenue/EPS for the next 2–4 quarters and the **revision trend** over 30/90 days. The direction of revisions matters far more than the level.
- Price vs. 52-week range, and performance vs. sector and vs. the S&P over 1/3/6/12 months.
- Forward multiple vs. its own 3–5 year history and vs. named peers. Use the multiple that fits the business (EV/EBITDA, EV/S with a margin bridge, P/E only for stable earners).
- Sell-side price target *dispersion* — the spread between high and low is more informative than the mean. Wide dispersion means the street disagrees, which is where variant perception lives.
- **Reverse-engineer the price:** roughly what revenue growth and margin does the current price imply over the next 3–5 years? Then state whether the actual trajectory beats or misses that implied path. This one step converts a vague "it's cheap" into a testable claim, and it is the core of the whole framework.
- Recent multiple compression/expansion decomposition: how much of the stock's move was estimates vs. multiple?

---

## Lane D — Social & Retail Sentiment

Used for **perception and crowding**, never for facts. The goal is to locate the crowd relative to us.

### Reddit
If accessible directly or through search: cover `r/stocks`, `r/investing`, `r/wallstreetbets`, `r/ValueInvesting`, ticker-specific subs, and domain subs where practitioners actually work (`r/hardware`, `r/networking`, `r/datacenter`, `r/sysadmin`, `r/MachineLearning`, `r/energy`).

The domain subs are more valuable than the stock subs. A network engineer complaining about optics lead times is a supply-chain data point; a WSB options post is not.

For each ticker with real signal, capture:
- **Sources checked** — subreddit names and representative threads
- **Attention level** — ignored / low / medium / high / crowded / mania
- **Crowd stance** — bullish / bearish / mixed / polarized / confused
- **Repeated narrative** — the story the crowd keeps retelling
- **Strongest bear objection** — the best recurring skepticism, stated fairly
- **Signal quality** — meme chatter / low-effort hype / informed debate / practitioner insight / domain expertise
- **Variant opportunity** — what the crowd is missing, overweighting, or getting wrong
- **Trend** — is this warmer or cooler than the last scan?

If Reddit is inaccessible, use aggregators (mention counts, sentiment scores, trending/cooling) and label the result as weaker second-hand data.

### X / Twitter
Only if authenticated or publicly reachable. Practitioner accounts (semiconductor analysts, data center operators, infra engineers) are worth far more than finance accounts. If access is unavailable, say so plainly rather than inferring an X-native scan from generic web snippets.

### Other sentiment surfaces
- **StockTwits** — retail message volume and bull/bear ratio; useful purely as a crowding gauge
- **Seeking Alpha** — often the earliest written variant perception; read the *comments* on bullish articles for the best bear cases
- **Substack / independent research** — increasingly where the differentiated work lives
- **Glassdoor / Blind** — employee sentiment, reorg and attrition signals, unadvertised layoffs
- **YouTube / podcast transcripts** — management often says more, and more loosely, in long-form interviews than on earnings calls

### The interpretation rule
Sentiment is only actionable in combination with something else. Write the conclusion as a **two-factor statement**:

> "Retail is euphoric while insiders are selling and estimates are flat" (warning)
> "Retail is ignoring it while institutions are quietly accumulating and estimates are rising" (setup)

Sentiment alone — "Reddit likes it" — is worthless and should not appear in a report.

---

## Lane E — Under-Appreciated News

The lane most likely to produce the differentiated insight, because it requires effort nobody expends. Work outward from the company.

### Hiring and org signals
- Company careers page and LinkedIn: headcount trend by function, and specifically **what** they're hiring for. Twenty new field-application engineers in Taiwan is a capacity signal. A new "VP, Sovereign AI" is a market-entry signal.
- Job postings frequently describe unannounced products in the requirements section.
- Sudden hiring freezes or pulled postings lead layoff announcements by weeks.

### Government and regulatory records
- **USAspending.gov / SAM.gov / DoD daily contract announcements** — awarded contracts appear here before they appear in press releases
- **FERC filings and ISO/RTO interconnection queues** (PJM, ERCOT, MISO, CAISO) — for power, cooling, and data center names this is the ground truth on what's actually getting built and when
- **State/county permits, utility commission dockets, local news** — data center construction shows up in a county zoning board agenda long before an investor deck
- **FCC filings** — spectrum, device authorizations, satellite licenses
- **USPTO / Google Patents** — filing velocity by area, and continuation filings that reveal where R&D actually went; note patents publish 18 months after filing
- **Customs/import-export data** where accessible — physical goods movement is hard to spin

### Supply chain
- **Monthly revenue disclosures from Asian suppliers** — TSMC, Foxconn, Quanta, Wistron, Delta, and other TWSE filers publish *monthly* revenue. This is the fastest legitimate read on hardware demand available anywhere, and it's public.
- Korean and Japanese filings and press (Samsung, SK Hynix, Advantest, Tokyo Electron, Nikkei) for memory and equipment
- Read the **customers' and competitors'** earnings calls for what they say about your company. Suppliers describe demand; customers describe pricing power.
- Lead times, spot pricing, and channel inventory commentary from distributors

### Non-English and regional press
Systematically underweighted by the market. DigiTimes and the Taiwanese/Korean tech press regularly break supply chain news 1–2 weeks ahead of US coverage. Search in the local language and translate.

### Second-order chains
When a large capex or contract announcement lands, immediately ask: **who supplies the supplier?** The obvious beneficiary is priced within hours. The component vendor two layers down often takes a quarter to be discovered. This is where the Slow Pivot and Orphan setups get found.

### Credit and financing
- Bond spreads, new issuance terms, and CDS where available. Credit markets often reprice risk before equity does.
- Convertible issuance, warrant overhangs, and lockup expiry dates for recent listings

### Conference and event calendar
Build the forward calendar: earnings dates, investor days, industry conferences (GTC, Computex, OFC, Hot Chips, SC, CES, and the sector-specific ones), and index rebalance dates. Half of catalyst research is just knowing what's on the calendar before others plan around it.

---

## Lane F — Macro & Regime

Not a thesis input. A **sizing and correlation** input.

- Rates: 10Y level and direction, real yields, Fed expectations. This is the discount-rate channel that hits long-duration names.
- Sector rotation, factor performance (growth vs. value, momentum), and credit spreads as a risk appetite gauge
- Commodity and energy shocks relevant to holdings
- Regulatory or geopolitical developments with direct sector impact

Write the regime as one sentence, then state which watchlist buckets it helps, hurts, and leaves alone. Explicitly separate **discount-rate-driven** moves from **demand-driven** moves, because conflating them is how sentiment overshoots get misread as fundamental deterioration.

---

## Cross-Source Triangulation

The most valuable output isn't any single lane — it's the contradictions between them. Actively hunt for these:

| Pattern | Reading |
|---|---|
| Filings improving + sentiment negative | Candidate Sentiment Overshoot |
| Press release glowing + 10-Q language hedged | Trust the filing |
| Retail euphoric + insiders selling + estimates flat | Distribution risk |
| Retail absent + institutions accumulating + estimates rising | Best available setup |
| Company guides down + suppliers guide up | One of them is wrong; find out which |
| Backlog growing + cash conversion deteriorating | Revenue quality problem |
| Narrative says glut + supply chain data says sold out | Narrative is wrong (this was the July 2026 memory call) |
| Bullish thesis rests entirely on T4/T5 sources | Not a thesis yet |

---

## Access Honesty Checklist

Every report must include a short source-availability note stating which of these were reachable this run: EDGAR, XBRL/financial data, transcripts, 13F, Form 4, short interest, options data, Reddit, X, trade press, foreign-language sources.

An honest "not reachable" is a useful data point for improving the framework. A fabricated check corrupts the ledger and destroys the entire feedback loop.
