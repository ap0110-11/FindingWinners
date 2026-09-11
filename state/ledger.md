# Prediction Ledger

Every Core/High conviction call and every notable Pass gets recorded here **before** the outcome is known. This file is the only thing that can tell us whether the framework works.

Rules:

- Written at the time of the call, never edited retroactively. Corrections are appended, not overwritten.
- Claims must be falsifiable by a stated date, with a number where possible. "MU will do well" is not an entry. "MU FQ1 revenue ≥ $50B" is.
- Probabilities use 5 buckets: **20 / 35 / 50 / 65 / 80%**. False precision is worse than coarse honesty.
- Resolutions happen in Phase 0 of the *next* scan, before new research, so today's findings can't contaminate the judgment.
- Record the **lane** that produced the decisive evidence and the **setup** from `framework/goal.md` §3. Over time this tells us which parts of the process actually pay.

---

## Scoreboard

*Last updated 2026-09-09.*

| Metric | Value | Notes |
|---|---|---|
| Predictions recorded | 8 | All seeded from the 2026-07-13 scan |
| Resolved | 5 | P-002, P-003, P-006, P-007, P-008 |
| Hit rate | 5/5 | Far too small a sample to mean anything |
| Brier score | **0.148** | Lower is better; 0.25 = coin flip |
| Calibration | **Underconfident** | 5/5 hit on calls averaging 62%. Stated probabilities were too low |
| Median lead time | — | Not yet measurable |

**Do not read anything into these numbers until there are at least 10–15 resolutions.** Five-for-five is as consistent with an easy batch as with a good process. The one genuinely informative signal so far is the *direction* of the calibration error: claims called at 65% behaved like claims closer to 80%, which argues for raising stated probabilities when the evidence is this one-sided rather than reflexively hedging to 65%.

The counter-example is worth as much as the hits: **P-005 (VST) is the only call currently failing**, and it's the one whose compound structure was copied from P-004 (CEG) rather than reasoned independently.

### Hit rate by setup
| Setup | Recorded | Resolved | Hit rate |
|---|---|---|---|
| Muted Reaction | 0 | 0 | — |
| Fade the Pop | 0 | 0 | — |
| Slow Pivot | 0 | 0 | — |
| Misclassified | 2 | 0 | Both legs open to Oct 13 |
| Sentiment Overshoot | 3 | 1 | 1/1 (P-007) |
| Structural Break | 1 | 1 | 1/1 (P-002) |
| Orphan | 0 | 0 | — |

### Decisive evidence by lane
| Lane | Times decisive |
|---|---|
| A Filings | **5** (P-002, P-003, P-004 earnings leg, P-007, P-008) |
| B Positioning | 1 (P-005 price gap) |
| C Expectations | — |
| D Sentiment | 0 |
| E Under-appreciated news | 1 (P-006) |
| F Macro | — |

**Early read on lane productivity: Lane A (primary filings) settled almost everything.** One resolution cycle is not enough to cut a lane, but if this pattern holds, the filings lane deserves more budget and the sentiment lane needs to justify its cost.

---

## Open Predictions

Seeded retroactively from the 2026-07-13 scan so the loop has something to grade. These were the report's actual implied claims; probabilities are reconstructed from the language used, which is itself a lesson — the original report asserted directionally without committing to numbers, which is exactly what this file is meant to fix.

**Status as of 2026-09-09: three remain open.**

| ID | Date made | Ticker | Claim | P | Resolve by | Setup | Status |
|---|---|---|---|---|---|---|---|
| P-001 | 2026-07-13 | MU | FQ4 revenue **≥ $50.0B** with non-GAAP gross margin ≥84% | 65% | 2026-09-30 | Sentiment Overshoot | Open — FQ4 print is **Sept 30**, the deadline itself |
| P-004 | 2026-07-13 | CEG | Aug 6 Q2 confirms the power-demand thesis **and** CEG outperforms the S&P over the following 3 months | 65% | 2026-10-13 | Misclassified | Open — earnings leg **HIT on the income statement, contested on cash** (H1 FCF ≈ −$968m, OCF *down* YoY); price leg **+12.3pts ahead**, tracking hit. Council must rule on whether "confirms the thesis" survives the cash-flow read before this resolves. |
| P-005 | 2026-07-13 | VST | Aug 7 Q2 confirms merchant power tailwind **and** VST outperforms the S&P over the following 3 months | 50% | 2026-10-13 | Misclassified | Open — earnings leg **PARTIAL**; price leg **−6.2pts behind**, currently failing |

### Added 2026-09-09 from the second scan

Eight new claims, written under the rules in `framework/scoring.md` §Prediction Recording. Every one is single-clause, every threshold is a number rather than a description, and every resolution date sits past the event with slack. **Only P-010's event date is company-confirmed** (Micron FQ4, Sept 30, after close); the rest resolve well past an *estimated* print date precisely because the date is estimated.

| ID | Date made | Ticker | Claim | P | Resolve by | Setup | Lane | Status |
|---|---|---|---|---|---|---|---|---|
| P-009 | 2026-09-09 | CRDO | FQ2 FY27 10-Q discloses top-three customer concentration **below 74%** of revenue | 50% | 2027-01-15 | Sentiment Overshoot | A+C | Open |
| P-010 | 2026-09-09 | MU | The Sept 30 FQ4 print guides FQ1 FY27 revenue **at or above $52.0B** | 65% | 2026-10-07 | Structural Break | A+C | Open |
| P-011 | 2026-09-09 | CRM | Q3 FY27 GAAP income from operations **exceeds the year-ago quarter in absolute dollars** | 50% | 2026-12-31 | Misclassified | A | Open |
| P-012 | 2026-09-09 | IREN | The Q1 FY27 10-Q recognizes operating-lease revenue **greater than zero** | 65% | 2026-12-15 | — | A | Open |
| P-013 | 2026-09-09 | AVAV | Obligated (not ceiling) DoD dollars to AVAV or BlueHalo **above $150M** with action dates after 2026-07-13 appear in USAspending.gov | 50% | 2026-12-31 | — | A+E | Open |
| P-014 | 2026-09-09 | SNDK | The FQ1 FY2027 10-Q discloses ASC 606 remaining performance obligations **below $70bn** | 50% | 2026-12-15 | Structural Break | A | Open |
| P-015 | 2026-09-09 | VST | **No** common equity offering is priced off the 2026-09-09 S-3ASR | 80% | 2026-12-31 | — | B+D | Open |
| P-016 | 2026-09-09 | DELL | Q3 FY27 true free cash flow (operating cash flow less capex) is **below $2.0B** | 65% | 2026-12-15 | — | A | Open |

Two deliberate departures from the July set, both responses to logged errors. **Six of eight are claims about a disclosed fact rather than about price** — gradable from a single primary source, per rule 6, after the July compound price-claims (P-004, P-005) proved the hardest to grade honestly. And **80% appears for the first time** (P-015): the July calibration read underconfident at 5/5 on calls averaging 62%, so reflexively hedging to 65% when the evidence is one-sided is itself the error the ledger identified.

### Amendments made before resolution (legitimate; recorded for audit)

- **P-001, 2026-09-09:** the original wording "at or above the ~$50B guide" was ambiguous between the $50.0B midpoint and the $49.0B low end of the $50.0B ± $1.0B guide. **Fixed to ≥ $50.0B**, the stricter reading. Amended *before* the event, which is the only time disambiguation is honest — resolving an ambiguous claim after the fact is how ledgers get quietly graded generously.
- **P-004 / P-005, 2026-09-09:** the governing price anchor is **2026-07-13**, the date the prediction was made, not the earnings date. This matters materially for P-005: anchored to July 13 it is losing by 6.2 points, anchored to Aug 6 it is winning by 7.7. Fixing the anchor in advance removes the temptation to pick the flattering one in October.

---

## Resolved Predictions

Resolved 2026-09-09.

| ID | Ticker | Claim | P | Outcome | Brier | Decisive lane | Lesson |
|---|---|---|---|---|---|---|---|
| P-002 | SK Hynix | Q2 call reaffirms tightness rather than signalling balance returning | 65% | **HIT** | 0.12 | A | Scoping a prediction to *what management says* rather than to price made it cleanly gradable even though the stock fell 10% on the print |
| P-003 | Sector | Hyperscaler capex raised or maintained, not cut | 65% | **HIT** | 0.12 | A | When a capex figure moves, check whether the *definition* moved with it — MSFT's headline drop was a finance-to-operating lease reclassification, not a spending cut |
| P-006 | AVAV | New contract award >$100M within 90 days | 65% | **HIT** | 0.12 | E | Trade press routinely re-dates contract awards to their own coverage date; anchor to the IR page or wire timestamp |
| P-007 | CRM | Agentforce ARR growth still >100% YoY | 50% | **HIT** | 0.25 | A | Salesforce *widened* the metric definition the same quarter it reported it; grade against restated math and log the change, because the cushion that saves you now may not exist next time |
| P-008 | IREN | Earnings show contracted book intact | 65% | **HIT** | 0.12 | A | A wrong event date made a resolved outcome look open — IREN's FY ends June 30 and it reported Aug 27, not Sept 16 |

**Brier for a single binary prediction:** `(P_stated − outcome)²`, where outcome is 1 for hit and 0 for miss. Called at 65% and hit → 0.12. Called at 65% and missed → 0.42.

### Detail worth carrying forward

**P-002 (SK Hynix).** Management was more explicit than the prediction required: *"it appears difficult for the supply-demand balance to improve meaningfully in the near term"* and *"with tight supply-demand conditions expected to persist for a considerable period."* Long-term agreements concluded with ~10 customers on typically five-year terms with deposits. 2027 HBM volume and pricing talks *"progressing smoothly."* The stock still fell ~10% because records missed elevated expectations — the divergence between the language and the tape is itself the setup.

**P-003 (hyperscalers).** GOOGL raised FY26 capex to $195–205B from $180–190B. AMZN raised 2026 to ~$220B from ~$200B, with Jassy saying capacity still won't meet demand in 2026 or 2027 and that 2028 demand is "striking." META narrowed to $130–145B, lifting the floor. MSFT's calendar-2026 figure fell to ~$175B purely on lease reclassification while FY27 capex was guided higher and Q1 FY27 above $50B. Two of the four cited *memory prices* as a driver — the same tightness SK Hynix described, appearing on the buyer's income statement.

**P-007 (CRM).** Agentforce ARR >$1.5B, +240% YoY. But effective Q2 FY27 the metric now includes Slackbot and Headless 360. For like-for-like growth to fall below 100%, those additions would need to contribute over $620M of the $1.5B — implausible given Slackbot only just crossed 1M users. Clears on restated math, but the definition change is logged.

**P-008 (IREN).** Reported Aug 27, not Sept 16. Microsoft formally *accepted* Horizon 1 on Aug 13 (starting the contractual service term under the $9.7bn deal) and NVIDIA granted Exemplar Cloud status on GB300 NVL72. Both relationships strengthened. The $788M co-CEO RSU grant remains contested with a say-on-pay vote pending, but that was disclosed July 1, twelve days *before* the prediction, so it's a pre-existing condition rather than a resolution factor.

**Void** is only for predictions made unresolvable by an unforeseeable external event (acquisition, delisting, exchange halt). Void is *not* for "it's complicated" — resolve ambiguous ones as misses. Generous self-grading is the fastest way to make this file useless.

**Brier for a single binary prediction:** `(P_stated − outcome)²`, where outcome is 1 for hit and 0 for miss. Called at 65% and hit → 0.12. Called at 65% and missed → 0.42.

**Void** is only for predictions made unresolvable by an unforeseeable external event (acquisition, delisting, exchange halt). Void is *not* for "it's complicated" — resolve ambiguous ones as misses. Generous self-grading is the fastest way to make this file useless.

---

## Lessons Log

Durable, generalizable lessons extracted from resolutions. One line each. When a lesson recurs three times, promote it into `framework/goal.md`, `framework/sources.md`, or `framework/scoring.md` per `framework/improve.md`.

| Date | Lesson | Source | Promoted to |
|---|---|---|---|
| 2026-09-09 | The framework generated directional views for months without recording a single falsifiable, dated claim, so none of it could be graded. Conviction language without a ledger entry is unverifiable by construction. | Framework audit | `skills/catalyst-scan.md` Phase 6, this file |
| 2026-09-09 | Scores compressed into a 16–21 band across 24 names, which means the rubric wasn't discriminating between ideas. | 2026-07-13 scan | `framework/scoring.md` forced distribution |
| 2026-09-09 | Reports recommended entries but never specified exits, so there was no way to be wrong on the sell side. | Framework audit | `framework/scoring.md` Exits |
| 2026-09-09 | **Three of eight predictions carried wrong event dates** (P-001 assumed Sept 22 vs. actual Sept 30; P-005 assumed Aug 6 vs. actual Aug 7; P-008 assumed Sept 16 for a company whose fiscal year ends June 30 and which reported Aug 27). The P-008 error made a *resolved* prediction look open. **Three instances triggers the mandatory-change rule.** | 2026-09-09 resolution | `framework/scoring.md` — date verification now required |
| 2026-09-09 | Compound predictions (earnings leg + relative-price leg) must name their price anchor explicitly. P-005 wins by 7.7 points anchored to the earnings date and loses by 6.2 anchored to the prediction date — the anchor decides the grade. | P-004 / P-005 | `framework/scoring.md` — single-clause claims preferred |
| 2026-09-09 | **Copying a prediction's structure across two names in the same theme hides the dispersion inside the theme.** CEG and VST shared a thesis, a quarter, and a template, and produced a 20-point spread in relative performance. The copied one is the only failing call. | P-004 vs. P-005 | `framework/council.md` — reason each name independently |
| 2026-09-09 | Scoping a prediction to *what management says* rather than to *what the price does* makes it gradable from a single primary source even when the tape disagrees violently. | P-002 | — |
| 2026-09-09 | When a company redefines a disclosed metric in the same quarter it reports it, grade against restated math and log the definition change. | P-007 | — |
| 2026-09-09 | Stated probabilities were systematically too low: 5/5 hits on calls averaging 62%. Reflexively hedging to 65% when the evidence is one-sided is itself a calibration error. | 2026-09-09 resolution | Watch; needs more resolutions before changing buckets |
| 2026-09-09 | **Three July bucket calls were wrong with one shared root cause: treating a sector's operational exposure as its market exposure.** Defense demand rose while the primes fell 13–30% because appropriations stalled; power demand hit records while utilities lagged because duration governs; software results were strong while the bucket de-rated on a competitor's model launch. **Three instances triggers the mandatory-change rule.** | 2026-09-09 macro lane | `framework/scoring.md` — Transmission Check |
| 2026-09-09 | The July "rate shock" framing was directionally right and is now confirmed: semis fell 29% from Jun 22 to Jul 29 while Q2 semiconductor earnings expectations *rose* from +126% to +144%, with the low marked by a hedge-fund margin call. Selling paid nothing; holding paid everything. | 2026-09-09 macro lane | — |
| 2026-09-09 | **A correction applied to one artifact did not propagate to downstream task briefs, and one stale date became a false finding.** Four dates were wrong across two lane briefs — MU FQ4 "~Sept 22" (actual Sept 30), VST Q2 "Aug 6" (actual Aug 7), IREN "reports Sept 16" (actual: reported Aug 27), CRM "reports Sept 2" (actual Aug 26) — **despite this ledger holding all four correctly**, including an explicit prior note that IREN reported Aug 27. The filings lanes caught all four from primary sources, but not before the IREN date reached the macro lane, which built a "Sept 16 earnings collide with the FOMC" event-risk finding on it. That finding is retracted. Fixing the record is not the same as fixing the inputs copied out of it, and a bad date in a brief returns as a conclusion. | 2026-09-09 Lanes A1, A2, F | `skills/catalyst-scan.md` Phase 1 — brief dates must be copied from the ledger or dossier and pending events checked at IR before the brief goes out |
| 2026-09-09 | Headline nominal yields overstate discount-rate damage to long-duration equities. The 10-year rose ~22bp but the 10-year **real** yield rose ~5bp, while the 2-year real yield went 0.51%→2.08%. Decompose nominal into real, breakeven, and term premium before concluding terminal-value math is impaired. | 2026-09-09 macro lane | Candidate for `framework/sources.md` Lane F |
