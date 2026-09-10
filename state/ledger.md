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

| Metric | Value | Notes |
|---|---|---|
| Predictions recorded | 8 | All seeded from the 2026-07-13 scan |
| Resolved | 0 | — |
| Hit rate | — | Needs ≥10 resolutions to mean anything |
| Brier score | — | Lower is better; 0.25 = coin flip |
| Calibration | — | Of things called at 65%, roughly 65% should happen |
| Median lead time | — | Days between our flag and the market's move |

**Do not read anything into these numbers until there are at least 10–15 resolutions.** Until then, conviction language in reports is a hypothesis about our own process, not a track record.

### Hit rate by setup
| Setup | Recorded | Resolved | Hit rate |
|---|---|---|---|
| Muted Reaction | 0 | 0 | — |
| Fade the Pop | 0 | 0 | — |
| Slow Pivot | 0 | 0 | — |
| Misclassified | 2 | 0 | — |
| Sentiment Overshoot | 3 | 0 | — |
| Structural Break | 1 | 0 | — |
| Orphan | 0 | 0 | — |

### Decisive evidence by lane
| Lane | Times decisive |
|---|---|
| A Filings | — |
| B Positioning | — |
| C Expectations | — |
| D Sentiment | — |
| E Under-appreciated news | — |
| F Macro | — |

---

## Open Predictions

Seeded retroactively from the 2026-07-13 scan so the loop has something to grade. These were the report's actual implied claims; probabilities are reconstructed from the language used, which is itself a lesson — the original report asserted directionally without committing to numbers, which is exactly what this file is meant to fix.

**Status as of 2026-09-09: three are overdue and must be resolved in Phase 0 of the next scan. Five remain genuinely open.**

| ID | Date made | Ticker | Claim | P | Resolve by | Setup | Status |
|---|---|---|---|---|---|---|---|
| P-001 | 2026-07-13 | MU | The memory demand thesis holds: FQ4 revenue lands at or above the ~$50B guide with gross margin ≥84% | 65% | 2026-09-30 | Sentiment Overshoot | Open — resolves at FQ4 print |
| P-002 | 2026-07-13 | SKHY/MU | SK Hynix Q2 (Jul 29) reaffirms sold-out/undersupplied language rather than signalling balance returning | 65% | 2026-07-29 | Structural Break | **OVERDUE** |
| P-003 | 2026-07-13 | Sector | Late-July hyperscaler capex guidance (META/MSFT/GOOGL/AMZN) is raised or maintained, not cut — falsifying the "Meta Compute glut" narrative | 65% | 2026-08-05 | — | **OVERDUE** |
| P-004 | 2026-07-13 | CEG | Aug 6 Q2 confirms the power-demand thesis and CEG outperforms the S&P over the following 3 months (misclassification corrects) | 65% | 2026-10-13 | Misclassified | Open — Aug 6 leg resolvable now, price leg Oct 13 |
| P-005 | 2026-07-13 | VST | Aug 6 Q2 confirms merchant power tailwind; VST outperforms the S&P over the following 3 months | 50% | 2026-10-13 | Misclassified | Open — Aug 6 leg resolvable now, price leg Oct 13 |
| P-006 | 2026-07-13 | AVAV | Announces at least one new contract award >$100M within 90 days, consistent with the "unprecedented demand signals" commentary | 65% | 2026-10-13 | — | Open |
| P-007 | 2026-07-13 | CRM | Sep 2 earnings show Agentforce ARR growth still >100% YoY | 50% | 2026-09-05 | Sentiment Overshoot | **OVERDUE** |
| P-008 | 2026-07-13 | IREN | Sept 16 earnings show the contracted book intact (no material Microsoft or NVIDIA contract change) | 65% | 2026-09-20 | — | Open — event not yet occurred |

P-004 and P-005 are compound claims (an earnings test plus a relative-price test). Resolve the earnings leg now and carry the price leg to Oct 13. Compound predictions are harder to grade — prefer single-clause claims going forward.

---

## Resolved Predictions

*(none yet)*

Template for resolutions:

| ID | Ticker | Claim | P | Outcome | Brier | Decisive lane | Lesson |
|---|---|---|---|---|---|---|---|
| P-000 | XXXX | {claim} | 65% | Hit / Miss / Void | 0.12 | A | {one line — what generalizes} |

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
