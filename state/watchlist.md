# Watchlist

Candidates for research and investment. **Restructured 2026-09-09** after the July entries carried stale prices and wrong earnings dates into the September scan. The old format was free-text notes with no as-of dates; four wrong dates propagated from it into lane briefs, and one produced a false finding. This schema exists to stop that.

**Last full scan:** [2026-09-09](../reports/catalyst-scans/2026-09-09-all.md) · **Previous:** 2026-07-13

## How to read this file

Tiers set effort per `skills/catalyst-scan.md` Phase 0:

| Tier | Treatment |
|---|---|
| **T1 — Deep** | All six lanes, full dossier, council |
| **T2 — Delta** | Lanes A/C/E only; changes since last scan |
| **T3 — Tripwire** | Automated check only — earnings date, >15% move, 8-K, analyst action. Promote only if a tripwire fires |

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

| Fact | Value | As of |
|---|---|---|
| Price | $167.92 (−29.1% since Jul 13) | 2026-09-09 |
| Forward P/E | 23.0x vs own FY22–26 range 38.7–112.7x | 2026-09-09 |
| FY Apr-27 consensus EPS | **+3.7% over 30 days**, 5 raises / 1 cut | 2026-09-09 |
| Mean target | $281 (n=19), 68% above spot, range $185–$350 | 2026-09-09 |
| Top-3 customer concentration | **74%** of revenue (top two 61%) | 2026-09-01 (T1) |
| GAAP gross margin | 64.5%, from 68.2% | 2026-09-01 (T1) |
| Short interest | 3.26% of shares out, 1.43 days to cover, **flat through the drawdown** | 2026-08-14 |
| Institutional ownership | 80.2% — least owned of the connectivity group; ~8.7 days of volume in non-institutional hands | ~2026-06-30 |
| Next earnings | FQ2 FY27, ~Dec 2026 **(est. — confirm at IR)** | — |

**Thesis:** Fell 29% (−20% the day after a beat-and-raise) while forward estimates *rose* 3.7% and short interest stayed flat at 6.01M→6.13M shares — long liquidation, not a fundamental break. Optical guided above $600M carries the H2 FY27 inflection.
**Crux:** Is 64.5% gross margin (from 68.2%) price commoditization at the top-two customers, or deliberate mix into lower-rate, higher-dollar-content optics?

**Exit conditions (all four, per `framework/scoring.md`):**
1. *Invalidation* — FQ2 FY27 10-Q shows top-two concentration above 65%, or FY27 growth guidance cut below 60%
2. *Time stop* — FQ3 FY27 print, late March 2027. If optical is not a disclosed line by then, re-underwrite from zero
3. *Gap closure* — forward multiple back above 40x, or the mean-target gap closing below 20%
4. *Drift check* — is the reason still "estimates rose while price fell," or has it become "it bounced"?

**Open predictions:** P-009 (top-three concentration below 74%, 50%, resolves 2027-01-15)

## MU — Micron Technology
**Theme:** HBM · DRAM · NAND · AI memory
**Score:** 18/25 (unchanged) · **Confidence:** **High** (best evidence quality in the scan) · **P(bull):** 65%
**Conviction:** **Starter** · **Setup:** Structural Break · **Divergence:** Positive

| Fact | Value | As of |
|---|---|---|
| Price | $1,027.77 (+9.7% since Jul 13) | 2026-09-09 |
| Forward P/E | 7.2x; **6.5x** on FY Aug-27 consensus $158.01; own FY21–25 range 7.1–12.8x | 2026-09-09 |
| FY Aug-26 consensus | EPS $60.14→$73.40 (**+22.0%**), revenue $112.04B→$129.74B (+15.8%) over 84 days | 2026-09-09 |
| Implied durable EPS @12x | $85.65 = **117% of FY26 consensus**, 54% of FY27 — the market pays for ~FY26 in perpetuity | 2026-09-09 |
| Consensus shape | Peaks FY28 at $165.94, **falls to $139.33 in FY29** | 2026-09-09 |
| **Audited ASC 606 backlog** | **$5B** — ~1/10th the cited "$100bn," which is a minimum-volume construct | FY26 filings (T1) |
| FQ3 actual | Revenue $41.46B (+346%), non-GAAP EPS $25.11 | 2026-06-24 (T1) |
| FQ4 guide | $50B ± $1B, ~86% gross margin, EPS ~$31 | 2026-06-24 (T1) |
| Short interest | 2.66% of shares out, **1.0 days to cover** — squeeze mechanically impossible | 2026-08-14 |
| Institutional ownership | ~88.0%; long-only sold ~20.6M shares, fast money bought | ~2026-06-30 |
| Options | ~7.5% implied earnings move vs 8.1% realized four-quarter mean | 2026-09-09 |
| **Next earnings** | **FQ4, 2026-09-30, after market close (confirmed)** | — |

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

| Fact | Value | As of |
|---|---|---|
| Price | $244.16 (+42.6% since Jul 13, essentially all on one +22.6% session Aug 27) | 2026-09-09 |
| Forward P/E — headline | 14.7x on FY Jan-27 non-GAAP EPS $16.65; below its entire FY22–26 range of 16.8–56.0x | 2026-09-09 |
| **Forward P/E — ex-gain** | **~19x.** Strip $3,171M of H1 strategic-investment gains (~$3.86/sh) from the $16.67–16.71 guide → ~$12.8 | 2026-09-09 |
| Q2 FY27 non-GAAP EPS | $5.90 (+103%) — but **$2.53 of it is gains on strategic investments**; ex-gain ~$3.37 | 2026-08-26 (T1) |
| **Income from operations** | **$2,331M vs $2,332M** — flat in absolute dollars on 11% revenue growth | 2026-08-26 (T1) |
| Anthropic stake | ~45% of the $11,324M strategic portfolio (from ~22%); implied carrying value ~$5.1B from ~$1.7B | 2026-08-26 (T1) |
| cRPO | $33.5B, +14% — three points ahead of revenue growth | 2026-08-26 (T1) |
| FY27 cash guidance | OCF and FCF growth **maintained at ~4–5%**; GAAP operating margin guidance **cut** to 20.1% | 2026-08-26 (T1) |
| Diluted shares | 821M vs 962M (−14.7%) on a $25.0B ASR at $198.34; final settlement Oct 2026 | 2026-08-26 (T1) |
| Revision breadth | FY **15 raises / 0 cuts** (+23.2% in 30 days) — but the **Jan-27 quarter took 10 cuts / 0 raises** | 2026-09-09 |
| Short interest | **−43.0%** to 3.22% of shares out, 2.12 days to cover — ~20M shares of covering already spent | 2026-08-14 |
| Institutional ownership | ~96.5%; **390 exits vs 171 initiations** (worst ratio in the watchlist), growth→value handoff | ~2026-06-30 |
| Retail | Lowest attention of any name (0.011 msg/hr per 1,000 watchers); soured to 58.6% bullish while up 49% | 2026-09-09 |
| Next earnings | Q3 FY27, ~Dec 2026 **(est. — confirm at IR)** | — |

**Metric caution (T1):** the Agentforce ARR definition was **widened** effective Q2 FY27 to include Slackbot and Headless 360, in the same quarter it was reported at +240%, and the company says it may update it again. The core Agentforce Apps bucket (Sales, Service, Marketing, Commerce, Slack) grew only **8%** to $7,193M.
**Crux:** Does operating income resume growing in absolute dollars, or is flat operating profit on 11% revenue growth the new structural state?
**Live risk:** OpenAI's GPT-6 Astra launched Sept 4; CRM fell ~4% on Sept 8 with no company news. A February 2026 version of this trade erased ~$1T of software market cap in a week. **Repriceable by something that isn't a number**, which caps Catalyst Path at 3 under the Transmission Check.

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

| Fact | Value | As of |
|---|---|---|
| Price | $1,764.17 (+5.4% since Jul 13; YTD **+643%**); fell to $1,212 Aug 7 then rallied 45.5% | 2026-09-09 |
| Forward P/E | 8.2x vs 9.9–14.4x since the Feb-2025 spin | 2026-09-09 |
| **Backlog** | **$31.3bn of new contracts** (10-K subsequent-events footnote) **on top of $59.8bn RPO** = ~$91bn vs $20.2bn revenue | FY26 10-K (T1) |
| Counter in the same filing | A **brand-new risk factor** warning those agreements carry significant execution and market risk | FY26 10-K (T1) |
| FY Jun-27 consensus | $37.51B/$137.07 → $48.96B/$214.10 in 127 days (+30.5%/+56.2%) — largest revision in the group | 2026-09-09 |
| Growth composition | FQ4's 372% growth was roughly **two-thirds price, one-third volume** | 2026-09-09 (T3/T4) |
| Implied net margin in base | **51.2%** — no precedent in a pure-play NAND business; at 35% the required revenue is $99B | 2026-09-09 |
| Short interest | **+12.5%** to 5.26% of shares out, but **1.0 days to cover** — the squeeze narrative is unsupported | 2026-08-14 |
| Institutional | FMR **−41.3%** (confirmed past quarter-end by 13G/A Aug 6); discretionary −11.1%; only ~2.2 days of volume in non-institutional hands | 2026-08-06 |
| Retail | **Mania** — 4.46 msg/hr per 1,000 watchers, ~400x the quietest name; 82.4% bullish | 2026-09-09 |
| Sector | TrendForce: NAND supply **loosening in 2H27** while DRAM stays tight | 2026-07-30 (T3) |
| Next earnings | FQ1 FY2027, ~Nov 2026 **(est. — confirm at IR)** | — |

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
*Framework case study (Fade the Pop) — see `framework/goal.md` §5. As of this scan it is also the first recorded **successful** exit: right, and priced.*

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
**Score:** 10/25 · **Conviction:** **Pass** · **Divergence:** Negative
The worst combination on the list: **15 estimate cuts and 0 raises** on the current year, 14 cuts on FY28, yet the stock rose 10.6% and EV/Sales sits **above its own five-year peak**. The contrast with PANW in the same window — 11 raises / 3 cuts, and PANW *underperformed* — is the sharpest intra-sector expectations divergence in the scan.

## BE — Bloom Energy
**Score:** 11/25 · **Conviction:** **Pass** — gap closed
Mean target $275.08 against a $269.28 price is **2.2% upside**, with estimates completely flat (0 raises / 0 cuts) after a 210% YTD move and EV/Sales at 25.5x against a 3.2–10.6x history. Joins the S&P 500 on Sept 21 — a mechanical bid, not a thesis. Structurally still the cleanest beneficiary of states mandating bring-your-own-generation.

## NOW — ServiceNow
**Score:** not scored (insufficient work this run) · **Conviction:** **Watch**
Pure multiple compression: 28.9x forward against a 39.5–96.2x five-year range, estimates completely static, 3.4x target dispersion alongside two outright sell ratings. Fell ~5% on Sept 8 with CRM on the Astra launch. **Worth a dossier next scan** — the most under-researched name relative to its setup quality.

## AMD · VRT · PANW · RBRK · DOCN · NBIS
Delta-tracked, no material change this window. Two data-quality flags rather than theses:
- **NBIS** — analyst count dropped 14 → 4 in a month. Almost certainly a vendor coverage-mapping change, not ten firms dropping the stock. Treat all NBIS consensus as suspect until re-verified.
- **PANW** — the positive-revision counterexample to CRWD; worth promoting if the multiple compresses.

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

## RKLB · ASTS · BRUN
- **ASTS** — the only name in the scan with no transmission channel to AI capex, memory pricing, power prices, or defense appropriations. Genuinely uncorrelated; no current thesis.
- **BRUN** — retained but marked **non-informative consensus**: three analysts carry an identical $45.00 target and there is no estimate data. Zero dispersion is not agreement, it is an absence of independent modelling. **Cannot be scored under this framework until coverage broadens**, because no expectations baseline can be built.
- **RKLB** — dormant.

---

# Themes

Grouped by the **underlying bet**, because sizing happens at the theme level, not the ticker level (`framework/scoring.md` §Sizing).

| Theme | Names | The actual bet |
|---|---|---|
| **Memory supply cycle** | MU, SNDK | DRAM and NAND pricing holding as hyperscalers digest. SNDK is the levered expression of the identical bet — holding both is one position twice |
| **Compute buildout — hardware and interconnect** | DELL, CRDO, ALAB, MRVL, AMD | Pace of rack and network buildout. CRDO is the high-beta leg on 74% top-three concentration |
| **Power for AI** | CEG, VST, BE, VRT | Data-center load converting into realized power prices — and increasingly a *rates* instrument, not a power story |
| **AI-infrastructure financing access** | IREN, NBIS, BRUN, DOCN (+ VST and DELL partially) | Continued cheap capital, not compute demand. **Cuts across sector labels and is the grouping most likely to be missed** |
| **Demand-side software — the inverse leg** | CRM, NOW, CRWD, PANW, RBRK | The only bucket where AI capex *accelerating* is the bear catalyst. Long the AI complex and short CRM is one variable expressed twice, not diversification |
| **Defense autonomy** | AVAV, RKLB | Program awards and appropriations timing. Genuinely idiosyncratic |
| **Uncorrelated** | ASTS | No transmission channel to anything else on this list |

**Correlation finding (2026-09-09):** a single hyperscaler-capex shock moves **six of the eight gated names in the same direction** (MU, SNDK, DELL, CRDO, IREN, VST), with CRM moving opposite and AVAV not moving at all. A *different* shock — credit spreads widening — reorders the group entirely, hitting IREN, VST and DELL while leaving MU and SNDK comparatively untouched. Which shock arrives determines whether this book behaves as one position or three.

## New themes to track

1. **Data-center political backlash as a pricing-power risk.** Three states legislated in three months — North Carolina SB 730, Pennsylvania GRID standards, and a Massachusetts executive order (2026-09-08) requiring >25MW facilities to bring 100% clean power or pay into a ratepayer fund — and **Virginia segregates data-center power markets effective 2027-01-01**. This attacks the merchant-power thesis directly and was surfaced independently by two lanes.
2. **AI credit as a distinct factor.** AI-related bonds are ~4% of the high-yield index but **~40% of 2026 net new issuance**, with data-center and neocloud spreads *widening* since June while broad high yield tightened to 268bp. A separate risk axis from AI demand.
3. **Section 232 Phase 2.** Confirmed on the record 2026-09-02 — would extend semiconductor duties to **servers** and may eliminate the data-center exemption. No Federal Register text, no rates, no timeline. **Calendar it; do not model it.**

---

# Data integrity — read before using any ownership figure

**The Q2 2026 13F aggregates are contaminated.** Vanguard and BlackRock both re-registered their 13F filer entities in 2026, so old and new CIKs appear in the same quarter and aggregate share counts inflate mechanically. Reported total institutional ownership **exceeded shares outstanding** at CEG (123%), ALAB (122%) and MRVL (116%). CALSTRS separately reported ~1.98bn shares of MU — about 176% of the company — and 4.3M shares of SNDK against a 1.7M prior; those rows were dropped.

Consequently **all total-ownership and holder-count deltas were discarded this quarter.** Every institutional figure in this file is either (a) a manager-level Q1→Q2 change matched by CIK or (b) an ownership *level* from an independent holdings summary, which is T4 with an imprecise as-of date and should be treated as approximate. The DELL level (86.0%) is demonstrably internally inconsistent with its own implied float, so non-institutional capacity is not computed there.

Procedure now written into `framework/sources.md` Lane B. Next clean read: **Q3 13Fs, due ~2026-11-14.**

**Also standing:** there is **not a single 13D across any name in this watchlist.** Every ownership filing since 2026-07-13 is a 13G or 13G/A — passive. No activist has taken a position, including Corvex at VST. That is a searched-and-confirmed absence, not a gap.

**And:** insider *buying* across all twelve scanned names was confined to two, both in power — VST's CEO and a CEG director. Ten of twelve had zero open-market purchases.
