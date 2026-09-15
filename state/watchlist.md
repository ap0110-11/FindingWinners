# Watchlist

Candidates for research and investment. **Restructured 2026-09-09** after the July entries carried stale prices and wrong earnings dates into the September scan. The old format was free-text notes with no as-of dates; four wrong dates propagated from it into lane briefs, and one produced a false finding. This schema exists to stop that.

**Last full scan:** [2026-09-09](../reports/catalyst-scans/2026-09-09-all.md) · **Previous:** 2026-07-13
**Names added 2026-09-11:** AVGO, SKHY (SK hynix), SNOW, NET — all in *New — Baseline Required*, none scored.

🛑 **Retraction, 2026-09-11.** The **CRWD** entry's "15 estimate cuts and 0 raises" was **false** — there were 17 raises and 0 cuts. CRWD's score is **void pending re-score**, and the *Security software* theme split, which cited that number as its justification, is **provisional and unjustified**. Cause: a vendor revision-counter that never restated its stored priors across CRWD's 2026-07-02 four-for-one split. Details in the CRWD entry.

## How to read this file

Tiers set effort per `skills/catalyst-scan.md` Phase 0:


| Tier              | Treatment                                                                                              |
| ----------------- | ------------------------------------------------------------------------------------------------------ |
| **T1 — Deep**     | All six lanes, full dossier, council                                                                   |
| **T2 — Delta**    | Lanes A/C/E only; changes since last scan                                                              |
| **T3 — Tripwire** | Automated check only — earnings date, >15% move, 8-K, analyst action. Promote only if a tripwire fires |

Names added between scans sit in **New — Baseline Required** until one pass has run. They carry no score and no numbers by design, and they may not be used in a theme's sizing math until they do.


**Two rules for writing in this file.**

1. **Every number carries an as-of date.** A price or multiple without one is not usable in a brief.
2. **Never copy a date from memory.** Earnings dates are marked either *(confirmed)* — verified against the company's own IR page — or *(est.)* — inferred from reporting cadence. **An *(est.)* date may not be stated as fact in a lane brief.** Write "date unverified — confirm at IR" instead.

---



# Tier 1 — Deep

Four names. All six lanes, dossier, council.

## CRDO — Credo Technology

**Theme:** High-speed connectivity · AECs · optical DSPs and silicon photonics
**Score:** 19/25 (**+3** — a 35-point de-rating with rising estimates is the largest gap-opening event in the window) · **Confidence:** Med-High · **P(bull):** 65%
**Conviction:** **Core** · **Setup:** Sentiment Overshoot · **Divergence:** Positive


| Fact                         | Value                                                                                         | As of           |
| ---------------------------- | --------------------------------------------------------------------------------------------- | --------------- |
| Price                        | $167.92 (−29.1% since Jul 13)                                                                 | 2026-09-09      |
| Forward P/E                  | 23.0x vs own FY22–26 range 38.7–112.7x                                                        | 2026-09-09      |
| FY Apr-27 consensus EPS      | **+3.7% over 30 days**, 5 raises / 1 cut                                                      | 2026-09-09      |
| Mean target                  | $281 (n=19), 68% above spot, range $185–$350                                                  | 2026-09-09      |
| Top-3 customer concentration | **74%** end-customer basis (top two 61%, **top four 84%**) — and **down from 88% a year earlier, 84% at FY-end 2026-05-02**, so it is *improving* | quarter ended 2026-08-01 (T1) |
| Receivables concentration    | **85% in two customers** (57% + 28%), worse than its revenue concentration. AVGO discloses no equivalent figure at all — only qualitative language | quarter ended 2026-08-01 (T1) |
| GAAP gross margin            | 64.5%, from 68.2%                                                                             | 2026-09-01 (T1) |
| Short interest               | 3.26% of shares out, 1.43 days to cover, **flat through the drawdown**                        | 2026-08-14      |
| Institutional ownership      | 80.2% — least owned of the connectivity group; ~8.7 days of volume in non-institutional hands | ~2026-06-30     |
| Next earnings                | FQ2 FY27, ~Dec 2026 **(est. — confirm at IR)**                                                | —               |


**Thesis:** Fell 29% (−20% the day after a beat-and-raise) while forward estimates *rose* 3.7% and short interest stayed flat at 6.01M→6.13M shares — long liquidation, not a fundamental break. Optical guided above $600M carries the H2 FY27 inflection.
**Crux:** Is 64.5% gross margin (from 68.2%) price commoditization at the top-two customers, or deliberate mix into lower-rate, higher-dollar-content optics?

**Exit conditions (all four, per** `framework/scoring.md`**):**

1. *Invalidation* — FQ2 FY27 10-Q shows top-two concentration above 65%, or FY27 growth guidance cut below 60%
2. *Time stop* — FQ3 FY27 print, late March 2027. If optical is not a disclosed line by then, re-underwrite from zero
3. *Gap closure* — forward multiple back above 40x, or the mean-target gap closing below 20%
4. *Drift check* — is the reason still "estimates rose while price fell," or has it become "it bounced"?

**Open predictions:** P-009 (top-three concentration below 74%, 50%, resolves 2027-01-15)

⚠ **Calibration note added 2026-09-11, deliberately *not* an amendment.** P-009 was set at 50% without the trend in hand. On the end-customer measure concentration has run **88% → 84% → 74%** across the last four quarters — a clear three-quarter downtrend that makes 50% look too low, and the ledger already grades this framework as *underconfident*. **P-009 stays at 50% and is not being revised.** Revising a stated probability as the answer emerges destroys the Brier score it exists to produce; the honest move is to log the miscalibration and decide at Phase 6 whether a *separate* prediction is warranted. Filed for the retro as a calibration data point, not a correction.

## MU — Micron Technology

**Theme:** HBM · DRAM · NAND · AI memory
**Score:** 18/25 (unchanged) · **Confidence:** **High** (best evidence quality in the scan) · **P(bull):** 65%
**Conviction:** **Starter** · **Setup:** Structural Break · **Divergence:** Positive


| Fact                        | Value                                                                                      | As of             |
| --------------------------- | ------------------------------------------------------------------------------------------ | ----------------- |
| Price                       | $1,027.77 (+9.7% since Jul 13)                                                             | 2026-09-09        |
| Forward P/E                 | 7.2x; **6.5x** on FY Aug-27 consensus $158.01; own FY21–25 range 7.1–12.8x                 | 2026-09-09        |
| FY Aug-26 consensus         | EPS $60.14→$73.40 (**+22.0%**), revenue $112.04B→$129.74B (+15.8%) over 84 days            | 2026-09-09        |
| Implied durable EPS @12x    | $85.65 = **117% of FY26 consensus**, 54% of FY27 — the market pays for ~FY26 in perpetuity | 2026-09-09        |
| Consensus shape             | Peaks FY28 at $165.94, **falls to $139.33 in FY29**                                        | 2026-09-09        |
| **Audited ASC 606 backlog** | **$5B** — ~1/10th the cited "$100bn," which is a minimum-volume construct                  | FY26 filings (T1) |
| FQ3 actual                  | Revenue $41.46B (+346%), non-GAAP EPS $25.11                                               | 2026-06-24 (T1)   |
| FQ4 guide                   | $50B ± $1B, ~86% gross margin, EPS ~$31                                                    | 2026-06-24 (T1)   |
| Short interest              | 2.66% of shares out, **1.0 days to cover** — squeeze mechanically impossible               | 2026-08-14        |
| Institutional ownership     | ~88.0%; long-only sold ~20.6M shares, fast money bought                                    | ~2026-06-30       |
| Options                     | ~7.5% implied earnings move vs 8.1% realized four-quarter mean                             | 2026-09-09        |
| **Next earnings**           | **FQ4, 2026-09-30, after market close (confirmed)**                                        | —                 |


**Thesis:** HBM consumes ~3x the wafer area per bit of standard DRAM and sells on qualification-gated multi-year agreements, so the marginal wafer is absorbed into a contracted channel rather than dumped into spot. The mechanism that historically ended memory cycles has no channel to operate through while HBM is sold out.
**Crux:** **Are the HBM long-term agreements price-committed or volume-only?** If volume-only at prevailing market prices, 86% gross margins are a spot spike wearing a contract's clothing.

**Struck from all reasoning:** the "$100bn backlog" figure. Only the $5B audited number and the qualitative booking language may be cited.
**Open flag:** the chief business officer who architected the Strategic Customer Agreement program moved to senior advisor with no successor named (T1, in-window).

**Exit conditions:**

1. *Invalidation* — Sept 30 FQ4 guides FQ1 revenue below $52.0B or gross margin below 82%; or management drops "fully booked through CY2027"
2. *Time stop* — FQ1 print, mid-December 2026
3. *Gap closure* — forward multiple above 10x on FY Aug-27 (mid-range of its own history)
4. *Drift check* — is the thesis still the contract structure, or has it become "memory is going up"? The first is testable

**Open predictions:** P-001 (FQ4 revenue ≥$50.0B with GM ≥84%, 65%, resolves 2026-09-30) · P-010 (FQ4 guides FQ1 revenue ≥$52.0B, 65%, resolves 2026-10-07)

## CRM — Salesforce

**Theme:** CRM · enterprise AI · Agentforce
**Score:** 17/25 · **Confidence:** Medium · **P(bull):** 50%
**Conviction:** **Starter** (promoted to T1 from T2) · **Setup:** Misclassified · **Divergence:** Contested


| Fact                       | Value                                                                                                     | As of           |
| -------------------------- | --------------------------------------------------------------------------------------------------------- | --------------- |
| Price                      | $244.16 (+42.6% since Jul 13, essentially all on one +22.6% session Aug 27)                               | 2026-09-09      |
| Forward P/E — headline     | 14.7x on FY Jan-27 non-GAAP EPS $16.65; below its entire FY22–26 range of 16.8–56.0x                      | 2026-09-09      |
| **Forward P/E — ex-gain**  | **~19x.** Strip $3,171M of H1 strategic-investment gains (~$3.86/sh) from the $16.67–16.71 guide → ~$12.8 | 2026-09-09      |
| Q2 FY27 non-GAAP EPS       | $5.90 (+103%) — but **$2.53 of it is gains on strategic investments**; ex-gain ~$3.37                     | 2026-08-26 (T1) |
| **Income from operations** | **$2,331M vs $2,332M** — flat in absolute dollars on 11% revenue growth                                   | 2026-08-26 (T1) |
| Anthropic stake            | ~45% of the $11,324M strategic portfolio (from ~22%); implied carrying value ~$5.1B from ~$1.7B           | 2026-08-26 (T1) |
| cRPO                       | $33.5B, +14% — three points ahead of revenue growth                                                       | 2026-08-26 (T1) |
| FY27 cash guidance         | OCF and FCF growth **maintained at ~4–5%**; GAAP operating margin guidance **cut** to 20.1%               | 2026-08-26 (T1) |
| Diluted shares             | 821M vs 962M (−14.7%) on a $25.0B ASR at $198.34; final settlement Oct 2026                               | 2026-08-26 (T1) |
| Revision breadth           | FY **15 raises / 0 cuts** (+23.2% in 30 days) — but the **Jan-27 quarter took 10 cuts / 0 raises**        | 2026-09-09      |
| Short interest             | **−43.0%** to 3.22% of shares out, 2.12 days to cover — ~20M shares of covering already spent             | 2026-08-14      |
| Institutional ownership    | ~96.5%; **390 exits vs 171 initiations** (worst ratio in the watchlist), growth→value handoff             | ~2026-06-30     |
| Retail                     | Lowest attention of any name (0.011 msg/hr per 1,000 watchers); soured to 58.6% bullish while up 49%      | 2026-09-09      |
| Next earnings              | Q3 FY27, ~Dec 2026 **(est. — confirm at IR)**                                                             | —               |


**Metric caution (T1):** the Agentforce ARR definition was **widened** effective Q2 FY27 to include Slackbot and Headless 360, in the same quarter it was reported at +240%, and the company says it may update it again. The core Agentforce Apps bucket (Sales, Service, Marketing, Commerce, Slack) grew only **8%** to $7,193M.
**Crux:** Does operating income resume growing in absolute dollars, or is flat operating profit on 11% revenue growth the new structural state? **Live risk:** OpenAI's GPT-6 Astra launched Sept 4; CRM fell ~4% on Sept 8 with no company news. A February 2026 version of this trade erased ~$1T of software market cap in a week. **Repriceable by something that isn't a number**, which caps Catalyst Path at 3 under the Transmission Check.

**Exit conditions:**

1. *Invalidation* — Q3 FY27 shows GAAP operating income flat or down YoY in absolute dollars for a second consecutive quarter
2. *Time stop* — Q4 FY27 and initial FY28 guidance, late Feb / early Mar 2027
3. *Gap closure* — forward multiple above 22x **on the ex-gain number**, not the headline
4. *Drift check* — the thesis is **not** "Agentforce works." If it becomes that, we have drifted onto a claim we cannot verify

**Open predictions:** P-011 (Q3 FY27 GAAP operating income exceeds the year-ago quarter in absolute dollars, 50%, resolves 2026-12-31)

## SNDK — Sandisk

**Theme:** NAND flash · enterprise SSDs · AI data-center storage
**Score:** 14/25 · **Confidence:** Medium · **P(bull):** 50%
**Conviction:** **Watch** · **Setup:** Structural Break · **Divergence:** Contested


| Fact                       | Value                                                                                                                                 | As of              |
| -------------------------- | ------------------------------------------------------------------------------------------------------------------------------------- | ------------------ |
| Price                      | $1,764.17 (+5.4% since Jul 13; YTD **+643%**); fell to $1,212 Aug 7 then rallied 45.5%                                                | 2026-09-09         |
| Forward P/E                | 8.2x vs 9.9–14.4x since the Feb-2025 spin                                                                                             | 2026-09-09         |
| **Backlog**                | **$31.3bn of new contracts** (10-K subsequent-events footnote) **on top of $59.8bn RPO** = ~$91bn vs $20.2bn revenue                  | FY26 10-K (T1)     |
| Counter in the same filing | A **brand-new risk factor** warning those agreements carry significant execution and market risk                                      | FY26 10-K (T1)     |
| FY Jun-27 consensus        | $37.51B/$137.07 → $48.96B/$214.10 in 127 days (+30.5%/+56.2%) — largest revision in the group                                         | 2026-09-09         |
| Growth composition         | FQ4's 372% growth was roughly **two-thirds price, one-third volume**                                                                  | 2026-09-09 (T3/T4) |
| Implied net margin in base | **51.2%** — no precedent in a pure-play NAND business; at 35% the required revenue is $99B                                            | 2026-09-09         |
| Short interest             | **+12.5%** to 5.26% of shares out, but **1.0 days to cover** — the squeeze narrative is unsupported                                   | 2026-08-14         |
| Institutional              | FMR **−41.3%** (confirmed past quarter-end by 13G/A Aug 6); discretionary −11.1%; only ~2.2 days of volume in non-institutional hands | 2026-08-06         |
| Retail                     | **Mania** — 4.46 msg/hr per 1,000 watchers, ~400x the quietest name; 82.4% bullish                                                    | 2026-09-09         |
| Sector                     | TrendForce: NAND supply **loosening in 2H27** while DRAM stays tight                                                                  | 2026-07-30 (T3)    |
| Next earnings              | FQ1 FY2027, ~Nov 2026 **(est. — confirm at IR)**                                                                                      | —                  |


**Crux:** Is the $91bn stack fixed-price or take-or-pay, or volume-only at prevailing market prices? If volume-only, 4.5 years of backlog provides no protection against the ASP reversion that two-thirds-price growth invites.
**Promotion trigger (specific, required for Watch):** the FQ1 FY2027 10-Q discloses fixed-price or take-or-pay terms on a material portion of the $31.3bn stack, **or** ASC 606 RPO above $70bn. Absent that, this is a commodity at a cyclical peak with mania-level retail attention.

**Open predictions:** P-014 (FQ1 FY2027 ASC 606 RPO below $70bn, 50%, resolves 2026-12-15)

---



# Tier 2 — Delta

Lanes A/C/E only. Changes since last scan.

## DELL — Dell Technologies *(demoted from T1)*

**Score:** 13/25 (**−2**, entirely Expectations Gap 3→1) · **Confidence:** High · **P(bull):** 35% · **Conviction:** **Pass**
Right about the business, wrong about the opportunity — and that is the point. Q2 FY27 (2026-09-01, T1): revenue $46,971M +58%, above every estimate; AI server revenue a record $16,401M +100%; FY27 AI guidance raised **$60B→$74B**; **gross margin expanded to 20.9% from 18.3%** and ISG operating margin to 15.0% from 8.8%, which refutes the standard margin-dilution bear case; $95B AI backlog, ~$132B RPO.
And yet: price $535.25 (+25.3%; YTD +325%) at 19.0x forward against its own FY22–26 range of 7.0–12.8x. **Implied durable EPS at a 12x exit is $44.60 = 137% of the FY Jan-2029 consensus peak of $32.49** — the only name of eight where the visible trajectory misses the implied path. Required EPS CAGR 22.7%/yr vs consensus 13.7%. Mean target $564 (n=28) is 5.5% above spot, lowest on the list, at a 1.58x dispersion.
Cash-quality flags (T1, 2026-09-01): **true FCF $986M, −47%**, while the headline $8,149M "adjusted FCF" adds back $6,667M of financing receivables; receivables $14.3B→$20.4B with the charge-off rate **0.1%→0.5%**; inventory doubled to $21,290M funded by payables at $49,723M; equity negative $(1,427)M. Governance: Texas redomestication (2026-07-01) **bars derivative suits by holders under 3%**, permanent, no separate shareholder vote.
**Do not re-underwrite monthly. Returns to the book only if** price falls below ~$400 without ISG margin deterioration, **or** consensus FY Jan-2029 EPS rises above $40.
**Open predictions:** P-016 (Q3 FY27 true FCF below $2.0B, 65%, resolves 2026-12-15)
*Framework case study (Fade the Pop) — see* `framework/goal.md` *§5. As of this scan it is also the first recorded **successful** exit: right, and priced.*

## CEG — Constellation Energy *(demoted from T1)*

**Score:** 15/25 (**−2** — the de-rating that made it July's top pick has substantially unwound) · **Conviction:** **Hold, do not add**
Worked: +14.1% over the window against XLU −6.1%, best revision breadth in power (4 raises / 0 cuts), +12.3 points vs the S&P. The **ECP ControlCo overhang is two-thirds discharged** — 22.04M→14,443,227 shares, now below the 5% reporting threshold, which also means further ECP selling becomes invisible. A director bought 1,500 shares at $278.62 on 2026-08-11 ($417,931). Short interest −9.8% at **3.34 days to cover**, the thickest short base relative to liquidity in the watchlist.
But 16.1x EV/EBITDA is the upper half of its range with only 18.5% upside to target and the tightest dispersion in the group. And the filings lane found what the income statement hid: **H1 free cash flow ≈ −$968M with operating cash flow *falling* YoY** despite Calpine nearly doubling revenue, alongside $2.28bn of debt-funded buybacks and a guidance raise; cash $3.64bn→$697m while short-term borrowings tripled.
**Open predictions:** P-004 (65%, resolves 2026-10-13 — earnings leg HIT on the income statement, **contested on cash**; price leg tracking hit)

## VST — Vistra

**Score:** 12/25 · **Confidence:** Medium · **P(bull):** 50% · **Conviction:** **Watch** · **Divergence:** Contested
The only one of eight core names to fall: $151.10, −4.4% since Jul 13, YTD −6%. EV/EBITDA 10.7x vs its own 5.7–40.1x range; mean target $217 (n=20), 43.9% above spot.
**The strongest insider signal in the watchlist** (T1): CEO James Burke bought in the open market on **three separate days** — 2,000 @ $135.00 (Aug 24), 2,200 @ $135.99 (Aug 31), 4,465 @ $135.25 (Sep 1) — 8,665 shares for $1,173,069, no offsetting sales. Short interest −23.5% to 2.87% of shares out.
**Against that, three structural problems.** PJM capacity cleared **down a second consecutive auction** ($325/MW-day for 2028/29 vs $333), every Vistra zone at an identical price with no locational premium — the capacity leg now contributes ~zero to growth. The **only power name with negative revision breadth** (0 raises / 2 cuts; mean target cut $225.29→$217.42). And **institutional ownership 97.8%, the most crowded name in the watchlist**, with 16 buy / 0 hold / 0 sell ratings — no upgrade left to publish — and only ~1.6 days of volume in non-institutional hands. **A correct thesis with no marginal buyer does not pay.** The CEO's purchase is an information event, not a flow event: 8,665 shares is under 0.2% of one day's volume.
Filed an **S-3ASR on 2026-09-09** (a capacity filing, not a priced deal — retail identified it same-day from primary sources and is misreading it) plus two Form 144s Sept 8.
**Promotion trigger (both required, not either):** revision breadth turns positive — at least 2 raises with zero cuts on FY Dec-2026 — **and** the S-3ASR remains unused at 2026-12-31.
**Drift check failed:** the original reason to own this was the merchant power tailwind. The current reason has quietly become "the CEO is buying and it is cheaper than CEG." That is a different thesis.
**Open predictions:** P-005 (50%, resolves 2026-10-13 — **currently failing**, price leg −6.2pts behind) · P-015 (no equity priced off the S-3ASR, 80%, resolves 2026-12-31)
**Next earnings:** Q3, ~Nov 2026 **(est. — confirm at IR)**

## IREN — IREN Limited

**Score:** 11/25 (**−2**) · **Confidence:** Medium · **P(bull):** 35% · **Conviction:** **Watch** · ⚠ **governance flag**
Materially worse than the narrative. FY26 reported **2026-08-27** (fiscal year ends June 30 — *not* September, which was a propagated error in the July notes). Revenue $707.0M vs a Street figure of ~$740M; net loss $(702.6)M; **Q4 revenue fell sequentially** to $137.2M from $144.8M; adjusted EBITDA margin **41%→14%**; FY26 impairments $638.8M.
The two facts that matter most (T1, 2026-08-27): **88% of FY26 operating cash flow was the increase in deferred revenue** — customer prepayments, 95% in Q4 alone — and $1,623.5M of the $1,842.5M balance is deferred *lease* revenue on which **no lease revenue was recognized in any period presented**. FY27 capex guided **$25–30B against ~$22B identified — a $3–8B gap** to be met from "corporate sources." Only **$0.9B of the $5.1B ASC 606 RPO** converts in FY27, against a ">$4B ARR by December" headline. The Microsoft agreement contains **grace periods** allowing delivery to slip to the start of Q2 CY2027 without breach. Debt grew ~8x to $7,976.0M; 146.1M anti-dilutive shares ≈ 37% of the count.
Genuinely positive (T1): Horizon 1 **delivered to and accepted by Microsoft 2026-08-13**, starting the contractual service term; NVIDIA Exemplar Cloud on GB300 NVL72; $3.6B of **investment-grade** GPU financing at 6.0% funding ~96% of associated GPU capex; contracts above $20M revenue/MW with ~2-year paybacks against capex inflation of only 15–20%.
Positioning: **23.92% short interest, ~5x the next-highest**, but composition unknown — with 71.8M convertible-linked shares and broker-dealer 13Gs from Goldman (9.4%) and BofA (5.8%), much may be convert-arb. **Borrow cost unobtainable — the most valuable missing input in the scan.** The only genuinely under-owned name at 56.7% institutional. **Zero Form 4s in the window** — management did not buy to defend the stock through either drawdown. Fallen after four consecutive prints with worsening magnitude: −4.64%, −7.44%, −9.89%, −12.53%. Retail 96.2% bullish and content-free; price sits within $1 of JPMorgan's $46 underweight target.
⚠ **Governance — closest disqualifier call in the scan.** 9,099,328 RSUs to **each** co-CEO (~4.6% of the company), purely time-based, granted **after** the independent Chair disclosed that earlier awards with share-price hurdles "failed to vest" and were restructured to time-based in 2025. A performance hurdle that was missed was replaced with a time hurdle that cannot be. The special shareholder meeting remains **undated**.
**Promotion trigger (both required):** the Q1 FY27 10-Q recognizes operating-lease revenue above zero **and** the special meeting receives a date.
**Open predictions:** P-012 (Q1 FY27 recognizes operating-lease revenue >$0, 65%, resolves 2026-12-15)
**Next earnings:** Q1 FY27, ~Nov 2026 **(est. — confirm at IR)**

## MRVL — Marvell Technology

**Score:** 13/25 · **Conviction:** **Pass** · **Divergence:** Negative
**Fidelity cut 56.6% — 74.3M shares, the largest discretionary reduction anywhere in the scan** — confirmed at T1 by 13G/A, in the same quarter Jensen Huang publicly called it "the next trillion-dollar company" and the stock spiked 32.5%. The most sophisticated large holder sold the narrative spike. Estimates show a classic push-out: 7 cuts / 2 raises on the near year, 9 raises / 0 cuts on the next. That is tolerable at a low multiple; MRVL trades at 43.1x forward, the top of its own range. *(Note: reported institutional ownership of 116% is filer-entity contamination — see §Data integrity.)*

## NVDA — NVIDIA

**Score:** 14/25 · **Conviction:** **Watch** · **Divergence:** Confirmation
Genuinely interesting on multiple — 18.6x forward, below its entire FY22–26 range. But short interest is 1.19%, the lowest in the watchlist, Q2 institutional flow was perfectly balanced, and **there is no identifiable marginal buyer**: upside requires new capital entering equities rather than rotation within them. Employee sentiment strong (Blind 4.3 on 1,171 reviews; no attrition or layoff signal). **Promotion trigger:** short interest above 2.0% or a quarter of net institutional accumulation.

## ALAB — Astera Labs

**Score:** 13/25 · **Conviction:** **Watch**
Flat on both axes: −17.0% with estimates unchanged and retail stance genuinely unmoved at 62.7%. 53.6x forward. The one live signal is negative and unusual: the **CEO and COO made matched non-plan sales on the same day at $344.99** (stock now $300.54) — the only insider event in the scan reading as discretionary rather than mechanical. Near-term support leans on a possible Sept 21 index addition, which is mechanical and transient. *Framework case study (Muted Reaction).* *(Reported 122% institutional ownership is filer contamination.)*

## CRWD — CrowdStrike

**Score:** ~~10/25~~ **VOID — must be re-scored** · **Conviction:** ~~Pass~~ pending · **Divergence:** ~~Negative~~ **retracted**

🛑 **Corrected 2026-09-11. The 2026-09-09 entry stated a false number as fact, and the score was built on it.** It read: *"The worst combination on the list: **15 estimate cuts and 0 raises** on the current year, 14 cuts on FY28, yet the stock rose 10.6%."* **There were no cuts.** CRWD ran **17 raises / 0 cuts** on FY Jan-2027 and **14 raises / 0 cuts** on FY Jan-2028 (Zacks, company non-GAAP, 2026-09-11), with consensus moving **$1.18 → $1.26, or +6.78%**, over 30 days.

Settled at T1 rather than by choosing between panels. The 8-K of **2026-08-26** shows a beat and a full-year guidance **raise on every line** — revenue midpoint $5,936.7M → $6,001.1M, ARR $6,543.6M → $6,607.4M, non-GAAP operating income +2.49%, non-GAAP EPS $1.23 → $1.255 split-adjusted — on record net new ARR of $332.8M, +51% YoY. The stock then closed **+20.50% on 2026-08-27 on 2.93x average volume**. A consensus mean cannot rise 6.78% while 15 of its constituents are cut and none are raised.

**Root cause, and it is still a live trap.** The false counts are reproducible *today* on Nasdaq's panel, which returns exactly 15 down / 0 up on FY Jan-2027 and 14 down / 0 up on FY Jan-2028 — the old numbers verbatim, on today's date. That panel's up-counter reads **zero on all eight CRWD rows** while working normally for PANW on the same day (12 up / 4 down). CRWD executed a **4-for-1 split effective 2026-07-02**; the panel restated current levels but appears not to have restated stored priors, so every analyst re-basing their model registered as a large cut. → **new Lane C rule at Phase 6.**

**What survives:** the +10.6% move, verified exactly ($187.91 → $207.80, 2026-07-13 to 2026-09-09, T2). But it decomposes into 9.85 points of IGV and roughly 0.7 points of CRWD — the software index, not an idiosyncratic security-software move — and CRWD was *behind* IGV on 09-11 intraday. Essentially the whole window return is the single print: CRWD gained 0.68% from 07-13 to 08-26. **The EV/Sales-above-its-own-five-year-peak claim is untested and must not be carried forward as fact without verification.**

**Corrected read: estimates up and price up is confirmation, not negative divergence.** Different setup, and probably a materially different score.

## BE — Bloom Energy

**Score:** 11/25 · **Conviction:** **Pass** — gap closed
Mean target $275.08 against a $269.28 price is **2.2% upside**, with estimates completely flat (0 raises / 0 cuts) after a 210% YTD move and EV/Sales at 25.5x against a 3.2–10.6x history. Joins the S&P 500 on Sept 21 — a mechanical bid, not a thesis. Structurally still the cleanest beneficiary of states mandating bring-your-own-generation.

## NOW — ServiceNow

**Score:** not scored (insufficient work this run) · **Conviction:** **Watch**
Pure multiple compression: 28.9x forward against a 39.5–96.2x five-year range, estimates completely static, 3.4x target dispersion alongside two outright sell ratings. Fell ~5% on Sept 8 with CRM on the Astra launch. **Worth a dossier next scan** — the most under-researched name relative to its setup quality.

## AMD · VRT · PANW · RBRK · DOCN · NBIS

Delta-tracked, no material change this window. Two data-quality flags rather than theses:

- **NBIS** — analyst count dropped 14 → 4 in a month. Almost certainly a vendor coverage-mapping change, not ten firms dropping the stock. Treat all NBIS consensus as suspect until re-verified.
- **PANW** — ~~the positive-revision counterexample to CRWD~~ **no longer a counterexample, because both names have rising estimates** (corrected 2026-09-11). PANW is now the only *genuine* divergence in the pair, and it is unexamined: **13 raises / 4 cuts on FY Jul-2027, and the stock fell 9.28% on 2026-09-02 on 2.36x average volume**, with consensus pinned at $4.16 against guidance of $4.16–$4.19 — the *floor* of the range. Raised, and sold anyway. Flagged for Phase 5; warrants a dossier.

---



# Tier 3 — Tripwire

Automated check only: earnings date, >15% price move, 8-K filed, analyst action.

## AVAV — AeroVironment *(demoted from T1)*

**Score:** 10/25 (**−3**) · **Conviction:** **Pass** — **thesis falsified**
**Exit condition triggered, not a drawdown.** The July upgrade rested on conflict-driven demand and is now falsified from three independent directions:

1. **Appropriations (macro lane).** The FY27 defense budget is stalled — the House resolution carries $60B for defense against a ~$1.5T ask, both chambers are on continuing resolutions at FY26 levels into early December, the Senate NDAA is blocked. Despite six months of conflict the primes de-rated: Northrop −30%, L3Harris −20%, Lockheed −13%. Trump said on 2026-09-09 that the war ends after the November midterms, which removes the premium *without* delivering the budget.
2. **Segment contraction (filings lane, T1, 2026-09-09).** BlueHalo-heavy SCDE revenue **−21%** to $134.5M; adjusted EBITDA **fell** to $53.4M from $56.6M on +6% revenue; guidance **not raised** despite the beat; the 26% gross margin is an **amortization roll-off** the company itself attributes, not operating improvement. FQ1 EBITDA is 17.5% of the guidance floor against a one-third/two-thirds plan. And the decisive detail: the Titan MS initial task order is **$80M against a $500M headline — a 16% obligation rate**. Applied to $1.0B of announced ceilings, that is ~$160M of money.
3. **Estimate breadth (expectations lane).** 2 cuts / 0 raises on FY Apr-27; current-quarter consensus **−35%** ($0.34→$0.22) in 30 days; FY27 revenue growth consensus only +10.8% after a +140.9% FY26 that was the acquisition, not organic. Closed **−5.4% on the print** with retail collapsing 36 points overnight.

Genuinely on the other side: funded backlog is a record $1.5B (+37% YoY, +23% sequentially) and it is a real ASC 606 measure of obligated dollars that grew *during* the CR; the **best discretionary institutional accumulation in the scan** (+12.9%, the only name where the aggregate rose) at 68.2% ownership; and the **only mechanically live squeeze** on the list (7.19% short at 2.93 days on a thin float).
**Returns to the book only if:** obligated (not ceiling) DoD dollars above $400M with FY27 action dates appear in USAspending.gov, **or** SCDE returns to YoY growth.
**Open predictions:** P-013 (obligated DoD dollars >$150M with post-2026-07-13 action dates appear in USAspending, 50%, resolves 2026-12-31)

---

## Data center land and power — NEW, added 2026-09-15

**GLXY (Galaxy Digital) · HUT (Hut 8) · CIFR (Cipher Mining) · APLD (Applied Digital)**

**Score: none. Conviction: none. These are unresearched placeholders.**

⚠ **No figure appears below because none has been pulled.** Every price, megawatt, lease term, tenant name, and enterprise value I could write for these four from prior knowledge would be stale and unsourced, which is the failure mode `AGENTS.md` names explicitly — confident fiction written into state. They are entered here so the next scan picks them up, and nothing more.

**Why they belong on the list, and why they are not neoclouds.** These are companies converting into **lessors of energized land** — powered shell, substation, and grid interconnection — rather than sellers of compute. Three arrive from bitcoin mining; APLD arrives from hosting other people's miners, which is a different lineage but the same destination. The distinction from a neocloud is not cosmetic. A landlord's revenue lands under **ASC 842** as operating lease income against a 20–40 year asset with no technological obsolescence, on 10–20 year contracts, with the *tenant* buying the GPUs. A neocloud's revenue lands under **ASC 606** against a 3–6 year depreciating fleet it bought itself. Revenue per MW is far lower for the landlord and so is capex per MW, and the obsolescence risk sits with someone else. Applying a neocloud multiple to a landlord — or the reverse — is wrong by multiples, not by percentages.

**How to value them: `framework/valuing-powered-capacity.md`** (written 2026-09-15). Four-part sum of the parts — cap rate on energized leased NOI, replacement cost on energized-unleased, an explicitly probability-weighted option on the interconnection queue, and the legacy mining or hosting fleet valued separately and possibly at a negative on opportunity cost. Screen on **EV per MW computed three ways**; the ratio between EV/leased-MW and EV/pipeline-MW is the finding. The playbook's §3 also now covers the **legal wrapper** — a cap rate drawn from REIT comps applied to a C-corp's pre-tax NOI overvalues by the whole corporate tax wedge, so establish C-corp versus REIT-elected versus REIT-intended before capitalizing anything.

**GLXY is probably misclassified, and that is the reason to look.** Galaxy carries a crypto financial-services business — trading, asset management, staking — alongside the data center asset. A blended multiple on a company that is part broker, part asset manager and part landlord cannot be right, which makes it a **Misclassified** candidate in the `framework/goal.md` §3 sense. It is also the name where a sum-of-the-parts is mandatory rather than preferable. **Whether the data center segment is material to the whole is itself an open question** and must be established from the segment footnote before any thesis is written.

**APLD is the cohort's test case, and it is the one that runs both business models at once.** Applied Digital appears to report a build-to-suit leasing business and a GPU-cloud business *in separate segments of the same company* — **structural expectation from prior knowledge, not yet read off a segment footnote, and it may have been reclassified or divested** — which would mean the ASC 842 versus ASC 606 split this framework is built around is, for this one name, an internal segment boundary rather than a classification question. That makes it the cleanest available read on what each model actually earns per megawatt, and it makes any single blended EV/EBITDA on the consolidated entity meaningless by construction.

Two things set it apart from the other three, and both must be resolved before a score:

- **It has publicly pursued REIT treatment.** If an election is actually made, cap-rate-on-NOI stops being our analytical choice and becomes the legally correct frame — but it also imposes income and asset tests that a GPU-cloud segment may not pass, which is a live structural tension rather than a technicality. The question is not "is REIT conversion good"; it is whether the services revenue has to be quarantined in a taxable REIT subsidiary, what that costs, and whether the distribution requirement collides with a balance sheet that is mid-build. **Status is unverified here and must come from the filings.**
- **Its capacity is not in ERCOT.** Applied Digital's build has historically centred on **North Dakota**, which is MISO/SPP territory, not Texas. The ERCOT large-load approval amendment and the Texas queue audit — the two regulatory events driving the scarcity hypothesis below — may simply not apply to it. That could be a genuine advantage or it could mean a thinner power market and a different interconnection bottleneck. **Either way it breaks the assumption that this cohort shares one regulatory exposure**, and it is the reason the four cannot be sized as a single position.

Also unlike the others, APLD's tenant roster may be concentrated in **one or two non-investment-grade AI-infrastructure counterparties**. Single-tenant concentration against an unrated lessee is the dominant risk in a landlord model and dwarfs everything else in the valuation; a 15-year lease is worth what the tenant's balance sheet says it is worth.

**Blocking questions, in priority order.** Each must be answered from T1/T2 before a score:
1. Revenue split by ASC 606 versus ASC 842 — which business is this actually?
2. MW normalized to **critical IT load** with the conversion factor stated, split energized / leased / queued. Assume the headline number is gross and inflated; IREN's own guidance changed units by 1.6x inside five weeks.
3. Tenant identity and **credit standing**. A hyperscaler and a venture-funded AI startup are the same megawatt at completely different cap rates, and this single input moves the valuation more than any other.
4. Interconnection stage per site, and the governing **state statute** — three states legislated in three months and Virginia segregates data-center power markets on 2027-01-01.
5. Power procurement: fixed, merchant, hedged, or owned generation. A fixed-price lease funded by merchant power purchases is a written energy option, and Brent is up ~25% since July 13.
6. Full dilution — convertibles, resale shelves, anti-dilutive shares. Serial issuance is near-universal in this vertical, so the test is whether $/MW energized added exceeds dilution per share.
7. Related-party footnote. Common in miner conversions.
8. **Legal and tax structure** — C-corp, REIT elected, REIT intended, or partnership. This determines which valuation method is *correct* rather than merely defensible, and it constrains what non-qualifying revenue the entity can carry. Applies to all four, not just APLD.
9. **Recourse versus non-recourse debt, and joint-venture economics.** Project-level non-recourse debt and a JV interest both mean the company owns less of the megawatt than the headline implies. Consolidated EV can materially overstate economic EV where there is a large non-controlling interest, so compute EV both ways and say which one the thesis uses.

**Why this theme may be genuinely under-priced, stated as a hypothesis rather than a finding.** Capex per MW is inflating (IREN disclosed data center and GPU capex requirements up ~15–20%, T1 2026-08-27), which raises the replacement-cost floor under already-energized capacity. Meanwhile interconnection queues are getting *harder* to enter — ERCOT amended its large-load approval process and the Texas Governor ordered an audit of the entire queue. An asset whose replacement cost is rising while its replicability is falling is the structural setup, and screens do not capture it because these names still screen as bitcoin miners or crypto hosts. **That is a hypothesis. It has not been tested against a single filing.** Note the scope limit the APLD notes above expose: the queue-scarcity leg of this argument is ERCOT-specific, so it does not automatically transfer to a non-Texas footprint.

**Tripwire conditions until researched:** a signed lease announcement with a named tenant, an 8-K on an interconnection milestone, a REIT election or a change in stated intent to elect, a >15% price move, or an equity, preferred, or convertible raise.

## RKLB · ASTS · BRUN

- **ASTS** — the only name in the scan with no transmission channel to AI capex, memory pricing, power prices, or defense appropriations. Genuinely uncorrelated; no current thesis.
- **BRUN** — retained but marked **non-informative consensus**: three analysts carry an identical $45.00 target and there is no estimate data. Zero dispersion is not agreement, it is an absence of independent modelling. **Cannot be scored under this framework until coverage broadens**, because no expectations baseline can be built.
- **RKLB** — dormant.

---

# New — Baseline Required

Added 2026-09-11. **No lane has run on any of these, and no numbers are recorded below on purpose.** Every figure in this file carries an as-of date; inventing one for a new name is the exact failure the 2026-09-09 restructure was written to stop.

There is also a structural reason these can't just be dropped into T2: **Delta treatment is defined as "changes since last scan," which has no referent for a name that has never been scanned.** Each needs a one-time baseline pass — minimum Lanes A and C, since no expectations baseline can be reverse-engineered without one — before it can be scored, gated, or counted in a theme's correlation math.

## AVGO — Broadcom
**Theme:** Compute buildout — hardware and interconnect · **Entry tier after baseline:** T2 — Delta

**Why it's here:** it is the named kill mechanism in the CRDO pre-mortem — *"a top-two hyperscaler moved its next-generation platform to an internal or Broadcom SerDes"* — and CRDO is the only **Core** position on the book. The framework is underwriting a 19/25 Core call whose primary downside scenario runs through a company it has never researched. AVGO is also the merchant-silicon counterparty in every hyperscaler custom-ASIC decision, which is the same decision governing MRVL's estimate push-out.

**Baseline pass must establish:** the Lane C expectations baseline and reverse-engineered implied path (nothing can be scored without it); the AI-ASIC versus networking versus infrastructure-software revenue split from the 10-K rather than from coverage; whether the retimer and SerDes sockets CRDO occupies are ones AVGO is actively taking or merely could take; and customer concentration, as the direct read-across to CRDO's 74% top-three.

**Standing instruction:** read alongside CRDO even in a window where AVGO shows no divergence of its own. It is a dependency of an open position, not an independent idea — the CRDO crux (is 64.5% gross margin commoditization or mix?) is substantially a question about AVGO's pricing behavior.

**✅ Concentration — established 2026-09-11, all T1 from the 10-Q filed 2026-09-10.** One distributor customer is **50% of FQ3 net revenue**, from 32% a year earlier, and top-five *end* customers ~55% from ~40%. **This is a trend, not an artifact:** 21% (FY23) → 27/29/26/28% (FY24) → 29/29/32/32% (FY25) → 42/42/**50**% (FY26), rising in eleven of twelve disclosed observations.

The buyer is **identifiable but not currently disclosed**. AVGO named it *once* — "Direct sales to **WT Microelectronics Co., Ltd.**, a distributor, accounted for 27%…" in the Q1 FY2024 10-Q, 2024-03-14 — and has used the anonymous "one customer, which is a distributor" in every filing since. Three independent chains of matching prior-year comparatives tie that named party to today's 50% line. **Carried as a high-confidence inference, not a disclosure.** WT Micro is a genuine broadline distributor, corroborated in Avnet's and Arrow's own filings — not a captive pass-through.

**Channel in form, demand-concentrated in substance.** 50% of $29,591M is $14,796M, which is **71% of the $20,839M semiconductor segment** (55.7% a year ago) and about **89% of the $16.7bn of AI semiconductor revenue**. A channel with diffuse end demand behind it cannot be 71% of the segment while top-five end customers are only ~55% of total revenue. AVGO discloses nothing about the composition. Note also that *all* distributors are 56% of revenue against 46% for this one YTD — every other distributor on earth combined is ~10 points, and AVGO's own risk factor concedes it sells "through an increasingly limited number of distributors."

**RPO is inflating and lengthening at once:** $27.5bn (2025-08-03) → $33.3bn → $45.0bn → **$164.6bn** (2026-05-03) → **$179.2bn**. The step change is the **+$119.6bn single quarter** AVGO attributes to a custom-AI-accelerator contract, so **that one contract is plausibly ~$120bn, two-thirds of the total** (inference). Meanwhile the share expected within 12 months has fallen from 49% to **25%**, leaving ~$134bn beyond a year with **no disclosed tail schedule**. "Firmly committed" is defined by exclusion — it omits contracts the customer may terminate for convenience — and **no customer attribution is given for any of it.**

## SKHY — SK hynix Inc. (Nasdaq ADS)
**Theme:** Memory supply cycle · **Entry tier after baseline:** T2 — Delta · **Candidate setup: Orphan**

**✅ Instrument RESOLVED 2026-09-11, and the first version of this entry was wrong.** It said "US exposure is via unsponsored OTC ADRs" and "Lane B is largely unavailable." **Both are incorrect.** Corrected from primary sources, all T1:

| Fact | Value | As of |
|---|---|---|
| SEC registrant | **SK hynix Inc., CIK 0002120882** — files with the SEC | 2026-09-11 |
| US line | **SKHY, Nasdaq Global Select Market** — a *sponsored* ADS, not an unsponsored ADR | 2026-07-09 (8-A12B + CERT) |
| Third line | **HXSCL is the *Luxembourg GDS*, not a legacy US OTC line** (corrected 2026-09-11). Citi labels it "SK HYNIX INC. (LUX: HXSCL)" and every price field matches LuxSE's `HYNSE` exactly — last $1,360 at 15:35 UTC, volume 664, high $1,385, low $1,315. **Three lines exist, not four**; LuxSE's database returns `nbEquities: 1` for the issuer, the only other GDS line (US4491303016) having been **delisted 2006-02-22**. ⚠ EDGAR's ticker metadata still tags HXSCL `OTC`; that metadata is not authoritative and the Luxembourg price match is exact, but a thin US OTC quote under the same symbol could not be ruled out because OTC Markets returned HTTP 403 | 2026-09-11 |
| ADS ratio | **1 ADS = one-tenth (1/10) of one common share**; depositary Citibank N.A. | F-6, 2026-07-01 |
| Primary listing | KRX KOSPI **000660**, unchanged | 2026-09-11 |
| **US IPO** | **177,900,000 ADSs at US$149.00**, net proceeds ~**US$26.2bn** | 424B4, 2026-07-10 |
| Shares sold | 17,790,000 common shares = **2.441% of the company** | 424B4 + 6-K, 2026-08-18 |
| Share count, post-offering | **728,865,500 outstanding** · 730,492,365 issued · 1,626,865 treasury | 424B4 (states 728,865,500 twice) |
| **No greenshoe** | **No over-allotment option exists — prohibited by Korean law**, so no stabilisation bid ever supported the price | 424B4 |
| Offering closed | **2026-07-14** (not 07-13); shares issued to Citibank N.A. by third-party allotment | 6-K, 2026-07-15 |
| Cornerstone | **Baillie Gifford Overseas** and others indicated up to **US$7bn**, non-binding | 424B4, 2026-07-10 |
| Use of proceeds | Capex of **KRW 45.5 trillion** | 424B4, 2026-07-10 |
| Disclosure cadence | ~20 **6-K** filings on EDGAR between 2026-07-15 and **2026-09-09** | 2026-09-11 |

**The arithmetic, in prose — corrected 2026-09-11.** The first version of this entry said the offering was **2.51%** of the company. It is **2.441%**, and the error was mine: I added the 17,790,000 new shares to the **2026-03-31** outstanding count of 708,297,021 when the offering closed in July. Between those dates SK hynix disposed of **2,778,479 treasury shares** (the half-year note records 9,383,980 disposed against 6,605,501 in Q1), lifting outstanding to **711,075,500 at 2026-06-30**. So 711,075,500 + 17,790,000 = **728,865,500**, and 17,790,000 ÷ 728,865,500 = **2.441%**. The prospectus states 728,865,500 itself, twice. A Q2 dividend of ₩375 per share totalling ₩273,324,801,750 implies 728,866,138 shares — within 638 of it, which is the independent check.

At $149.00 per ADS the gross raise is about $26.5bn (177,900,000 × $149 = $26,507,100,000 exactly, per the 6-K), netting ~$26.2bn. Ten ADSs to a share puts the offering at $1,490 per common share, which against 728,865,500 shares implies a **valuation near US$1.086 trillion** at the IPO price.

**What this corrects operationally:**
- **Lane A is far better positioned than the first version claimed.** SK hynix files 6-Ks on EDGAR — **T1, not T2** — so the primary-filings lane works here normally. The **F-1/424B4 prospectus is the single highest-value document available on this name**, because an IPO prospectus must disclose material contract terms to a standard quarterly reporting does not. That makes it the best available source on whether the HBM long-term agreements are price-committed or volume-only, which is *MU's crux asked of the other supplier*.
- **Lane B is partially available, not unavailable.** Exchange short interest **exists and is large**: 14,857,954 ADSs at 2026-07-15 rising to **26,560,289 at 2026-08-31 — 14.93% of the entire 177.9M ADS pool**, at 1.55 days to cover (T2, semi-monthly settlement dates). Listed US options exist (1,336 contract records with live open interest). 13F holdings will exist but **no quarter-end had closed on the listing until 2026-09-30, so the first clean read is ~2026-11-16** (the 45-day deadline of 11-14 is a Saturday). Reported institutional ownership is **one holder and 215 shares**, which is the absence itself rather than a measurement. **Form 4 will never exist — confirmed at T1, not assumed:** the prospectus states officers, directors and principal shareholders "are exempt from the short-swing profit recovery provisions contained in Section 16."

**Orphan setup — CONFIRMED from primary sources, no longer a candidate.** Index exclusion is now documented rather than inferred. **FTSE Russell published a formal notice on 2026-07-03**, *Treatment of SK Hynix ADS Listing*: "where only a DR is listed, the DR is generally not eligible for inclusion," and because the Korean line is already a constituent, the ADS "does not result in the ADS line becoming the primary eligible security." S&P excludes ADSs by security type *and* requires 10-K/10-Q/8-K filers, so it fails twice. Russell excludes depositary receipts by name. MSCI and FTSE both take one listing per company and prefer the liquid local line. **The only live possibility is the Nasdaq-100**, which admits ADRs — but ranks a "Non-Primary ADR" on *listed ADS value only*, about **US$33.9bn**, not the company's US$1.39tn, and its seasoning rule explicitly disregards prior foreign listing history. December 2026 is the first test and is genuinely borderline.

### 🛑 The ADS trades at a +41.1% premium to its own underlying, and the premium is structural

Resolved 2026-09-11 (the prior ⚠ deferring this to Lane C is cleared). One-tenth of the ₩1,812,000 KRX close is ₩181,200, which at ₩1,342.79/USD is **$134.94 of parity value against an ADS at $190.40 — a premium of 41.1%** for identical cash flows. Three lanes computed it independently and agree (41.1%, 36.6–41.2%, 36.8–40.4%).

**The mechanism, at T1.** SK hynix's convertible pool is capped at the shares it *initially deposited* — 17,790,000 shares, 177,900,000 ADSs — and the IPO consumed **100% of the quota**. Creating one more ADS needs the company's prior consent *plus* a fresh FSC securities registration which the prospectus says it is "under no obligation to file," adding: "It is possible that we may not give such consent." Withdrawal is uncapped and unsuspendable, but cancelling at a 41% premium means realising a **29.1% loss**, so no holder does it and headroom never appears. **Creating ADSs is the leg that closes a premium, and it is unavailable — not slow, not expensive.** Fees are $0.05 per ADS, 0.037% each way: the premium is roughly **555 times the frictional cost**, so if the channel were open this could not survive a day.

**Refined 2026-09-11, and the refinement is the whole mechanism: both facilities sit under the same Korean consent regime, but the benchmark the consent test is keyed to differs, and the two lines sit at opposite ends of it.** For the ADS the 424B4 test is whether a deposit "exceeds **the number of common shares initially deposited by us** for the issuance of ADSs." For the GDS, the 2005 listing particulars and 2006 offering circular both use a *revolving* benchmark — consent is needed only "if the number of such delivered GDSs exceeds that of **the shares already withdrawn from the GDS facility**" — so consent-free capacity accumulates one-for-one with every withdrawal. The GDS facility has then bled down for twenty years exactly as its own risk factor warned it would ("The number of outstanding GDSs will decrease to the extent that more common shares are withdrawn… than are deposited"): the 2005 tranche of 65,518,609 plus the 2006 tranche of 26,954,048 sum to 92,472,657 against LuxSE's recorded 93,100,437 issued, while only **13,729,041 remained listed at 2026-07-08** (T1) — leaving roughly **79.4 million shares of consent-free re-deposit headroom**. The ADS facility is the mirror image: created July 2026, 17,790,000 deposited, essentially nothing withdrawn, **headroom ≈ zero**. Two supports: the FETL requires the securities-issuance report for a two-way KRX/overseas line **"only once at the time of the initial listing"**, which the GDS made in 2005, so Seoul↔Luxembourg movement is a monthly reporting formality rather than a consent gate; and the gate is definitively not on the US side, since the F-6 registered 1.78bn ADSs. ⚠ The ~79.4m figure is a **well-supported inference, not a disclosed number** — LuxSE's issued-securities field is undated and appears to record cumulative issuance — and the empirical parity-versus-41% split is what actually settles this, not our construction of the clause.

**⚠ The F-6 is NOT the cap, and this is a genuine information edge.** The F-6 registered **1,780,000,000 ADSs** and is only **9.99% utilised**, leaving ~1.6bn of apparent headroom. Reasoning from it, a Shinhan Securities analyst described "additional issuance capacity of about 22.5% based on SEC registration standards" (T4) — and concluded the premium must collapse. **The SEC registration authorises the depositary to *issue*; Korean law governs whether shares may be *deposited*. Only the second binds.** Published sell-side analysis is wrong about the single most important feature of this instrument.

**Calibration proves it is name-specific, not a Korean-regime feature.** Five seasoned Korean ADRs, computed from same-date primary closes and 20-F ratios: **KB −0.34%, LPL −0.42%, KEP −0.93%, WF +0.36%, PKX +1.07%** — all within 1.1% of parity, because their quotas were set decades ago and have ample headroom. TSM at **+13.60%** is the instructive middle case: Taiwan partially constrains conversion, and a partially blocked channel sustains the low teens. SKHY at 41.1% is ~3x TSM and ~40x the Korean comparables — a fully shut channel.

**Two hypotheses ruled out.** The ten leveraged ETFs (SKUU, SKDD, SKHL, SKHU, SKHA, SKHN, SKHQ, SKHX, HYNX, SK — all 2x daily) hold about **$506M** in aggregate, roughly **$926M** of net long notional against a **$33.87bn** ADS float: **2.73% of float, 0.28 of one day's trading.** The largest fund holds no ADSs at all, using total-return swaps. And the book-closure transient has expired — Citibank's notice shut issuance and cancellation until 2026-07-29; the premium hit its **61.6% maximum on 07-30, the reopening date**, and has not converged in the six weeks since.

**Not converging.** Across 42 sessions the premium averaged **34.8%** (median 34.2%, SD **8.7 points**, range **15.8% to 61.6%**). First five sessions 30.1%, last five **40.9%**. It widened on 09-11 while the KRX line *fell* 2.21%. Note too that ~15% of the programme is already short and **the premium still widened** — shorts borrow from the same fixed pool, so that channel inherits the cap's capacity limit.

**⚠ Second market-cap trap.** The KRX line values the company at **$983.6bn**; the ADS implies **$1.388tn** — a **$404bn** disagreement. **Nasdaq publishes the ADS-derived figure as SKHY's market cap**, so anyone screening on it is handed the premium-inflated number. This sits alongside the broken per-share ratios on the same name (a vendor divides a per-ADS price by per-common-share EPS, publishing a 0.73x forward P/E).

**🛑 Instrument verdict: SKHY is not a sound expression of SK hynix earnings. The KRX line is the only clean one.** You would be paying $1.41 for $1.00 of identical cash flows, with no mechanism returning the difference; a buyer right about HBM and right about the cycle can still lose 29% on premium normalisation alone. "Structural" does not mean safe — the *level* is set by US demand against a fixed 2.441% float and has an 8.7-point standard deviation, an unhedgeable second factor uncorrelated with anything we have a view on. And **the company can expand the quota unilaterally** ("a specified maximum that we may establish from time to time"), which is a one-sided risk decided by a party whose interests are not ours — **but that risk is contractually suspended until 2026-10-08, and then it is not** (established 2026-09-11). The 424B4's 90-day underwriting lock-up restrains **the company itself**, barring it from issuing, from filing a registration statement, *and* from "publicly announc[ing] an intention to effect any such transaction." Ninety days from the 2026-07-10 prospectus date is **2026-10-08 `(confirmed)` from the document**. So the clean negative we have — **no F-3, no new F-1, no F-6 amendment and no shelf on EDGAR (33 filings total for CIK 0002120882, only 6-Ks after the 424B4), and no 증권신고서 or DR-issuance resolution on DART through 2026-09-11** — is real but **expected rather than informative**, because announcing was prohibited. The premium's structural protection therefore has a **known expiry three weeks before the estimated Q3 call**, where the company has already promised further capital-return detail. Anyone short the premium should treat 2026-10-08 as the date the signalling option reopens; anyone long the ADS should understand they are holding an instrument whose scarcity the issuer regains the right to end on a date certain. The sell-side targets betray the confusion: **+29.9% implied upside on the ADS against +76.5% on the KRX line** is not two views, it is one view plus a 41-point measurement error.

**Is it actionable at all? Yes, on the Korean line.** Korea abolished foreign investor registration effective **2023-12-14**, and foreign ownership of 000660 already sits at **50.55%** — this is a market foreigners operate in at scale, so KRX access is an operational question, not a barrier. **But if our mandate or custodian cannot hold KRX-listed equity, the honest answer is that SK hynix is not investable for us at any conviction level**, and it should be carried as a *research input* to the MU and SNDK theses rather than as a position. There is no acceptable synthetic workaround: every leveraged ETF references the ADS and therefore inherits the premium with 2x leverage on top. **Do not buy the accessible line because it is accessible — that is paying 41% for operational convenience.**

✅ **The control ran, and it confirms the mechanism decisively — tested 2026-09-11.** The **Luxembourg GDS** (LuxSE `HYNSE`, ISIN US78392B1070, 1 GDS = 1 common share, depositary **Citibank N.A.** — the same depositary as the ADS) closed at **$1,360 against parity of $1,349.43, a premium of +0.78%**, on the same date the Nasdaq ADS carried **+41.1%** for a claim on the identical share. Parity arithmetic: ₩1,812,000 ÷ ₩1,342.79/USD (ECB, T2) = $1,349.43, and $1,360 − $1,349.43 = $10.57, so 10.57 ÷ 1,349.43 = 0.78%.

Over 50 sessions from 2026-07-02 the Luxembourg premium averaged **+1.29%** (median +0.97%), and on the 15 sessions with an actual trade print, **+0.33%** (median +1.15%). **The two distributions do not overlap**: the ADS minimum of +15.8% sits 9.9 points above the Luxembourg maximum on traded marks (+5.93%). The series oscillates around zero with no drift; its wide dispersion (−9.3% to +16.0%) is symmetric and is explained by a **nine-hour session gap** — Luxembourg opens half an hour after Seoul closes — against a stock that moved >10% in a day repeatedly in this window. And a same-date T1 observation from the issuer's own 2006 offering circular shows the GDS at **−0.24%** to parity on 2006-06-23 ($28.33 against ₩27,100 ÷ ₩954.3 = $28.3978). **This line has traded at parity for two decades.**

So the 41% premium is **not** offshore-access scarcity, **not** a depositary-receipt artifact, and **not** anything about SK hynix. It is specific to the US programme. It also settles the direction: the US line values one common share at $1,904 while Luxembourg values it at $1,360 on the same day in the same currency, so **SKHY is ~40% rich, rather than Seoul being cheap** — which is the correct way to read the sell-side's +29.9%-on-ADS against +76.5%-on-KRX target gap.

**🛑 But it is not a usable substitute, so the KRX-only verdict stands and is strengthened.** Three disqualifiers, any one sufficient: it is a **Rule 144A / Regulation S restricted security, never SEC-registered** ("have not been registered under the Securities Act"), so US access is QIB-only at best; it trades on the **Euro MTF** (`EMTF`), not an EU regulated market, which fails many institutional mandates and UCITS tests; and liquidity is negligible — **13 of 16 trade prints in ten weeks were for ten GDSs or fewer** (sizes: 1, 1,679, 1, 6, 2, 1, 1, 1, 6, 1, 2, 2, 5, 1, 1, 13), median day volume **636 GDSs** (~$0.8m) against 2,620,477 shares on the KRX line on 2026-09-11 alone, and **LuxSE returns an empty bid array and an empty ask array** with both spread fields null. Citi/FactSet showed an indicative $1,275/$1,365 — a **6.82%** spread — which cannot be reconciled with the empty book and should not be treated as executable. **An excellent price signal and a useless execution venue.**

⚠ Two open items. Whether the current ISIN still carries the restrictive legend is a question for counsel, not a research desk. And Korean securities-transaction-tax exemption is enumerated for NYSE, Nasdaq, Tokyo, London and Deutsche Börse; **the Euro MTF is not named**, so GDS transfers may bear a tax the ADS does not — flagged, not asserted.

**Process note — this is the finding, not a footnote.** The offering priced **2026-07-09/10**; the 2026-09-09 scan's window opened **2026-07-13**, three days later. A **$26.5bn US listing** by the company that is the subject of the ledger's only resolved Structural Break prediction (P-002), in the book's core theme, **went entirely unremarked by that scan.** Logged for the retro.

**Why it's here:** two gaps that have been open a while. First, **P-002 is the ledger's only resolved Structural Break, and it was about SK Hynix** — the framework's cleanest graded prediction was made on a name it does not carry. Second, the 2026-09-09 catalyst calendar already lists SK Hynix's October Q3 results and capex as the test of *"whether competitor supply is arriving faster than qualification,"* which is the decisive input to MU's crux. It is being consumed as an MU input without being underwritten.

**Baseline pass must establish:** HBM capacity and capex trajectory from primary KRX/DART disclosure; whether its long-term agreements are price-committed or volume-only — the same question as MU's crux, asked of the other supplier; and an expectations baseline on whichever instrument is confirmed.

## SNOW — Snowflake
**Theme:** Enterprise software — the inverse leg · **Entry tier after baseline:** T2 — Delta

**Why it's here:** it tests whether the software bucket's bear thesis is about *software* or about *pricing models*. The demand-side software call rests on AI agents compressing seats; Snowflake is consumption-priced, so more AI workload is mechanically more revenue. If SNOW and CRM diverge, the bucket was mis-specified. If they move together, the de-rating is about the application layer regardless of how it bills.

**Baseline pass must establish:** the expectations baseline and implied path; consumption growth versus net revenue retention read from the filing rather than the shareholder letter; and the Transmission Check question — is this priced as AI infrastructure or as enterprise software? The answer decides which theme it belongs in.

## NET — Cloudflare
**Theme:** ✅ **Enterprise software — resolved 2026-09-11** · **Entry tier:** T2 — Delta · **Baseline complete:** `state/dossiers/NET.md`

**✅ The classification is settled, and the answer is the opposite of our Lane C read.** NET is **priced as premium security / edge software, at the very top of that bucket — not as AI infrastructure** (confidence 80%). At **33.50x forward P/S** it is the most expensive of eight software and security comps (above CRWD's 31.85x, the 100th percentile) and **3.78x the richest AI-infrastructure comparable** (NBIS at 8.87x); AI-infrastructure names carry *low* revenue multiples because they are capital- and depreciation-heavy, so a name cannot be priced as one at 3.8x the top of the range. Over 64 sessions its daily returns correlate **+0.60 to +0.64** with DDOG, ZS, FSLY, S, CRWD, MDB and FTNT, and **+0.11 to +0.17** with NBIS, IREN and CRWV — the AI-infrastructure cluster is statistically indistinguishable from no relationship. Capex intensity is *falling* (7.2% of revenue against 11.7% a year earlier), which is not what building infrastructure looks like. **The earlier read confused what management talks about with what the market pays for.**

**Sizing instruction: size on multiple percentile and duration, not on the AI narrative.** The software-bucket correlation figure may now include NET.

⚠ **The prior instruction to read the security-versus-developer-platform split from the 10-K is unsatisfiable and is withdrawn.** Note 14 states NET has a **single operating segment** and discloses revenue only by geography — no product split, no ARR, no AI-attributed revenue exists in primary disclosure. **Any AI revenue share for this name is inference.** It also means NET cannot be placed on the seat-versus-consumption axis at all: the security leg is disclosed as **per-seat** and the developer leg as **metered by requests and execution time**, both inside one segment with neither quantified.

**🛑 A pre-armed split trap — the highest-priority operational item on this name.** Stockholders have approved a **"Class C Split"** in which each Class A share "would be reconstituted and become one share of Class A common stock and one share of Class C common stock," and the company states the price "will decrease by **approximately one-half**" and that it anticipates implementing "**as early as September 2026**." **Not implemented as of 2026-09-11** (last 8-K is 2026-08-13, no Form 8-A or charter amendment, price series continuous, and **eight stockholder suits** pending). Our declared panel says verbatim *"This stock does not have any record of stock splits."* **Every per-share figure we hold is pre-split. The moment an implementation 8-K appears, treat all NET per-share levels and revision counts as suspect until re-verified and corroborate the sign against guidance actions, not counters.** Probability of implementation by 2026-12-31: **80%**. This is the CRWD failure mode armed in advance, plus a novel one — it creates a second listed line and adjusts the conversion rate on $5.79bn of converts.

**What the baseline found worth carrying:** revenue accelerating five straight quarters to **+35.9%**; **RPO +38.2% and current deferred revenue +48.6%**, both ahead of revenue, so backlog quality is good and billings are collected earlier — the opposite of the framework's warning sign; **no customer above 10% of revenue or receivables** (as of 2025-12-31), the antithesis of the AI-infra comps. Against that, **non-GAAP operating margin did not expand — 13.8% against 14.1% — despite 36% revenue growth**, because gross margin eroded 74.9% → 71.8% on **$30.1M of undefined "third-party technology services costs,"** the largest single cost-of-revenue driver. **Whether that line is resold inference compute is the single highest-value open question**, because it is the hinge between "expensive software that grows into it" and "expensive software with deteriorating unit economics."

**Positioning is the best-shaped on the watchlist and is not yet scored.** Institutions hold only **81.66%** — the least institutionally owned software name in the book against CRM at ~96.5% — leaving ~30.6M shares, about **10.4 days of volume**, in non-institutional hands. Short interest **fell 30.9%** from the 2026-07-15 peak to 6,794,677 at 2026-08-31 (1.91% of shares out, 2.27 days to cover) *through* the $2.5bn convert pricing, when convertible arbitrage would normally *add* shorts — so the notes likely went to outright funds rather than arb desks, removing an assumed source of selling pressure. All 42 Form 4s in the window are mechanical: **zero open-market purchases**, every sale under a 10b5-1 plan adopted before the May restructuring and the August convert, so the selling is noise under our own rule.

**Consensus is pinned to guidance** — FY2026 non-GAAP EPS consensus $1.26 against a guide of $1.25–1.26, with the low estimate at $1.25 exactly and revenue consensus at the *top* of the guided range. That is the PANW/AVAV pattern: **a beat is the base case and a miss is unpriced.** Declared panel is **S&P Global via stockanalysis.com, non-GAAP, forecast vintage 2026-08-27**. 🛑 Nasdaq's panel returns **FY2026 EPS of $0.03** against S&P Global's $1.26 — a **42x divergence on an identical period, and the second independent failure of the same panel that produced CRWD's false counts.** Never blend them.

⚠ **Q3 2026 earnings: early November 2026 `(est.)`, UNCONFIRMED** — `cloudflare.net` returned HTTP 403 on both the events page and root. Must not be stated as fact.

---



# Themes

Grouped by the **underlying bet**, because sizing happens at the theme level, not the ticker level (`framework/scoring.md` §Sizing).


| Theme                                            | Names                                             | The actual bet                                                                                                                                             |
| ------------------------------------------------ | ------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Memory supply cycle** | MU, SNDK, SKHY ᴺ | DRAM and NAND pricing holding as hyperscalers digest. SNDK is the levered expression of the identical bet — holding both is one position twice, and SKHY makes it three. SKHY is also the *supply* side of MU's crux, already consumed as an MU calendar input without being carried as a name — **and it raised ~$26.2bn in July 2026 earmarked for KRW 45.5tn of capex, which is the supply response arriving in cash terms.** 🛑 **But the US ADS line is not a sound instrument** (+41.1% premium to its own underlying, structurally non-arbitrageable — see its entry). If the memory bet is expressed here it must be on **KRX 000660**; otherwise SK hynix is a research input to MU and SNDK, not a third position |
| **Compute buildout — hardware and interconnect** | DELL, CRDO, ALAB, MRVL, AMD, AVGO ᴺ | Pace of rack and network buildout. **CRDO and AVGO are not independent holdings — but corrected 2026-09-11, and not for the reason first given.** The original read *"AVGO is the named mechanism that breaks CRDO's concentration."* That holds **only as a competition claim** (CRDO's FY2026 10-K names Broadcom a principal competitor), never as a counterparty claim: **AVGO names no end customer whatsoever**, having dropped its Apple ~20% disclosure after FY2023, and CRDO labels every customer by letter. **The filings are silent on shared buyers and probably cannot resolve it.** The real link is that both are long the same *absolute* market — a handful of hyperscalers' AI capex — and **competition operates on relative share inside that market, so it does not diversify.** One custom-XPU program slipping damages both at once, which means treating the rivalry as offsetting understates the joint downside. ⚠ **And the concentration comparison ran the wrong way round:** AVGO's 50% is a *distributor channel* figure, while its end-customer number is ~55% for the top **five** — against CRDO's **74% top-three and 84% top-four**. Like-for-like, **CRDO is the more concentrated name**, and CRDO's is *improving* while AVGO's deteriorates sharply |
| **Power for AI**                                 | CEG, VST, BE, VRT                                 | Data-center load converting into realized power prices — and increasingly a *rates* instrument, not a power story                                          |
| **AI-infrastructure financing access**           | IREN, NBIS, BRUN, DOCN (+ VST and DELL partially) | Continued cheap capital, not compute demand. **Cuts across sector labels and is the grouping most likely to be missed**                                    |
| **Powered land and grid interconnection** ᴳ | GLXY, HUT, CIFR, APLD | Scarcity of **energized** land and interconnection rights — not compute demand. A **landlord** bet: ASC 842 lease income on a 20–40 year asset with no technological obsolescence, where the *tenant* buys the GPUs. **Deliberately separated from AI-infrastructure financing access above, and the reason is the risk decomposition, not tidiness.** These names share that bucket's **financing-access** risk — serial equity and convertible issuance is near-universal here — but they do **not** carry its **GPU-obsolescence** risk, which sits with the tenant, nor its 3–6 year asset life. So a credit-spread shock hits both buckets together while a GPU-cycle shock hits only IREN and the neoclouds. Sizing them as one position overstates the correlation; sizing them as independent understates the shared funding channel. **Until a baseline pass runs, that decomposition is a reasoned expectation, not a measured correlation** — no return series has been computed for these four. **The bucket is also not regulatorily homogeneous:** APLD's footprint is largely MISO/SPP rather than ERCOT, and APLD additionally carries a live ASC 606 GPU-cloud segment, so it imports some of the obsolescence risk the other three shed. Treat it as a partial member, not a fourth interchangeable one. See `framework/valuing-powered-capacity.md` |
| **Enterprise software — the inverse leg** | CRM, NOW, SNOW ᴺ, NET ᴺ | The bucket where AI capex *accelerating* is the bear catalyst — the hypothesis being that this bites **seat-priced** models (CRM, NOW) but not **consumption-priced** ones (SNOW), where more AI workload is mechanically more revenue. **Tested 2026-09-11, and the verdict splits along exactly the Transmission Check line.** On *fundamentals* the axis holds: SNOW's consumption accelerated a third consecutive quarter, FY27 product revenue guidance was raised twice (+27% → +31% → **+36%**) with margin guidance rising alongside, and management attributes roughly half the acceleration to AI products. On *market behaviour* it fails: revision direction does not sort by billing model on headline numbers (seat-priced CRM +15.5% against consumption-priced SNOW +10.7%, though CRM's is substantially non-operating), 🛑 **and the one-day test I cited here was wrong — corrected 2026-09-11.** On close-to-close for 2026-09-10, **CRM fell 0.48%** ($244.16 → $243.00), **NOW was flat at +0.05%** ($131.11 → $131.17) and **SNOW fell 0.53%** — all three inside half a point of unchanged, with CRM down slightly *more* than SNOW. My figures (CRM +2.50%, NOW +0.81%, SNOW −0.78%) were **intraday prints read as closes**; CRM's intraday high was +1.78% over the prior close and NOW's +2.74%. So the claim "seat-priced names rose while the consumption-priced one fell" **does not survive**, and that day is **uninformative rather than evidence either way** — it must not be leaned on in either direction. What still stands is the revision finding, which is basis-independent: **billing model does not sort revision direction.** On that alone, **size on multiple percentile and duration rather than on billing model** — and note the conclusion now rests on revisions, not on tape behaviour, which is weaker support than this row previously claimed. The framework's logged lesson still applies: a sector's operational exposure is not its market exposure. Long the AI complex and short CRM remains one variable expressed twice, not diversification |
| **Security software** ⚠ | CRWD, PANW, RBRK | ⚠ **The stated justification for this split was retracted 2026-09-11: it rested on a false number.** It read *"the split is evidence-driven, not tidiness: CRWD ran 15 cuts / 0 raises and rose 10.6% while PANW ran 11 raises / 3 cuts and underperformed — the sharpest intra-sector divergence in the 2026-09-09 scan."* **CRWD ran 17 raises / 0 cuts** (see its entry). Corrected, CRWD and PANW sit on the **same** side of the revision axis, so the opposite-sign divergence never existed. The surviving hypothesis — that security budgets are non-discretionary in a way application budgets are not, making the bear catalyst consolidation and AI-native entrants rather than seat compression — is a claim about *transmission mechanism*, was never the evidence cited, and **may not inherit credibility from a falsified data point.** Held **provisional and unjustified**. Do not merge back either: merging on the strength of a corrected artifact is the same error with the sign flipped |
| **Defense autonomy**                             | AVAV, RKLB                                        | Program awards and appropriations timing. Genuinely idiosyncratic                                                                                          |
| **Uncorrelated**                                 | ASTS                                              | No transmission channel to anything else on this list                                                                                                      |


ᴳ = added 2026-09-15, and at a **weaker** evidentiary standard than the ᴺ names below. GLXY, HUT, CIFR and APLD have had **no baseline pass of any kind** — no filing read, no figure pulled, no consensus panel identified. The theme row above states how the *category* should be valued and where it sits in the correlation structure; it asserts nothing about the four companies. They are excluded from sizing math, from scoring, and from any report claim until the evidence bar in `framework/valuing-powered-capacity.md` §7 is met.

ᴺ = added 2026-09-11. Placed in a theme so the correlation question is visible, but **excluded from sizing math until a baseline pass has run.** Baselines are now complete for **AVGO, SKHY, SNOW and NET** (`state/dossiers/`); the ⚠ formerly on NET is removed — its classification resolved to Enterprise software on 2026-09-11. **What still blocks sizing is not the baseline but the absence of a declared consensus panel on AVGO, SNOW and KRX 000660**, without which Expectations-vs-Reality cannot be scored.

**Correlation finding (2026-09-09):** a single hyperscaler-capex shock moves **six of the eight gated names in the same direction** (MU, SNDK, DELL, CRDO, IREN, VST), with CRM moving opposite and AVAV not moving at all. A *different* shock — credit spreads widening — reorders the group entirely, hitting IREN, VST and DELL while leaving MU and SNDK comparatively untouched. Which shock arrives determines whether this book behaves as one position or three.

**This finding predates the 2026-09-11 additions and has not been recomputed.** Three of the four would change it if included: SK Hynix loads the same hyperscaler-capex shock the memory names already carry, AVGO sits on the same axis as CRDO and MRVL, and **NET's sign is now known — it loads the software factor, not the AI-infrastructure one** (correlations +0.60 to +0.64 against DDOG/ZS/CRWD, +0.11 to +0.17 against NBIS/IREN/CRWV, 64 sessions to 2026-09-11), so it belongs on the *opposite* side of a capex shock from the other three additions. Recompute at the next full scan rather than patching the sentence above.

⚠ **A caution on the 2026-09-09 finding itself, raised 2026-09-11.** That correlation work leaned on single-shock-day moves, and the NET baseline showed our 2026-09-10 day-move figures for CRM, NOW and SNOW were **intraday prints mistaken for closes** — the corrected closes differentiate by less than half a point and the day carries no signal. Single-day event studies in this file must be computed close-to-close and **corroborated against a multi-session correlation** before they are allowed to support a conclusion.

## New themes to track

1. **Data-center political backlash as a pricing-power risk.** Three states legislated in three months — North Carolina SB 730, Pennsylvania GRID standards, and a Massachusetts executive order (2026-09-08) requiring >25MW facilities to bring 100% clean power or pay into a ratepayer fund — and **Virginia segregates data-center power markets effective 2027-01-01**. This attacks the merchant-power thesis directly and was surfaced independently by two lanes.
2. **AI credit as a distinct factor.** AI-related bonds are ~4% of the high-yield index but **~40% of 2026 net new issuance**, with data-center and neocloud spreads *widening* since June while broad high yield tightened to 268bp. A separate risk axis from AI demand.
3. **Section 232 Phase 2.** Confirmed on the record 2026-09-02 — would extend semiconductor duties to **servers** and may eliminate the data-center exemption. No Federal Register text, no rates, no timeline. **Calendar it; do not model it.**
4. **The miner-to-landlord conversion (added 2026-09-15).** Bitcoin miners converting into lessors of energized land. The hypothesis worth testing: **replacement cost per MW is rising while replicability is falling**, which should raise the floor under already-energized capacity. Capex per MW is inflating (IREN disclosed data center and GPU capex requirements up ~15–20%, T1 2026-08-27) at the same time as interconnection is getting harder to obtain — ERCOT amended its large-load approval process and the Texas Governor ordered an audit of every data center in the queue. Screens miss it because these names still screen as miners and their revenue still sits largely under the wrong accounting standard. **Note this theme is in direct tension with theme 1 above**: the same statutory wave that threatens merchant power pricing also constrains new data-center load, which cuts *for* incumbent energized sites and *against* the pipeline. Whether the net is positive is the open question, and it resolves site by site and state by state rather than at the theme level. Entirely untested — see `framework/valuing-powered-capacity.md`.

---



# Data integrity — read before using any ownership figure

**The Q2 2026 13F aggregates are contaminated.** Vanguard and BlackRock both re-registered their 13F filer entities in 2026, so old and new CIKs appear in the same quarter and aggregate share counts inflate mechanically. Reported total institutional ownership **exceeded shares outstanding** at CEG (123%), ALAB (122%) and MRVL (116%). CALSTRS separately reported ~1.98bn shares of MU — about 176% of the company — and 4.3M shares of SNDK against a 1.7M prior; those rows were dropped.

Consequently **all total-ownership and holder-count deltas were discarded this quarter.** Every institutional figure in this file is either (a) a manager-level Q1→Q2 change matched by CIK or (b) an ownership *level* from an independent holdings summary, which is T4 with an imprecise as-of date and should be treated as approximate. The DELL level (86.0%) is demonstrably internally inconsistent with its own implied float, so non-institutional capacity is not computed there.

Procedure now written into `framework/sources.md` Lane B. Next clean read: **Q3 13Fs, due ~2026-11-14.**

**Also standing:** there is **not a single 13D across any name in this watchlist.** Every ownership filing since 2026-07-13 is a 13G or 13G/A — passive. No activist has taken a position, including Corvex at VST. That is a searched-and-confirmed absence, not a gap.

**And:** insider *buying* across all twelve scanned names was confined to two, both in power — VST's CEO and a CEG director. Ten of twelve had zero open-market purchases.