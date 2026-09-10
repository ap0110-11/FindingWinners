# Self-Improvement Loop

A research framework that never changes is a research framework that never learns. This file defines how the system audits itself and rewrites its own instructions.

The governing rule: **every deep retro must produce either a concrete edit to a framework file, or an explicit written statement that no change is warranted and why.** A retro that ends in "we should be more careful next time" has done nothing.

---

## Cadence

| Level | When | Effort | Output |
|---|---|---|---|
| **Light** | End of every scan | 5 min | §12 Process Notes in the report |
| **Medium** | Monthly | 30 min | Resolve ledger entries, update scoreboard, decide on pending changes |
| **Deep** | Quarterly | 2 hrs | Full audit against the metrics below; framework diffs; changelog entry |

Deep retros write to `reports/retros/YYYY-QN.md`.

---

## What Gets Measured

### Outcome quality
- **Hit rate by conviction tier.** High-conviction calls must beat Core, which must beat Starter. If they don't, the conviction assignment is noise and the tiering is decorative.
- **Brier score and calibration.** Group predictions by stated probability and check whether ~65% of the 65% calls hit. Systematic overconfidence is the most common failure and the easiest to fix — just shift the buckets down.
- **Hit rate by setup** (`framework/goal.md` §3). Some setups will work and some won't. Retire the ones that don't.
- **Lead time.** Days between our flag and the market's move. This is the direct measure of whether the time-arbitrage edge is real. If lead time is consistently negative, we're chasing, not anticipating.
- **Miss magnitude.** Losing calls should lose less than winning calls win. If they don't, the exit discipline is broken regardless of hit rate.

### Process quality
- **Decisive lane attribution.** Which lane produced the insight that actually mattered? Lanes that never produce decisive evidence should be cut or run less often. Lanes that consistently do should get more budget. This is the highest-leverage efficiency metric in the system.
- **Council value-add.** How often did the debate change the verdict versus rubber-stamp the pre-debate view? Under ~20%, the council is theater and needs tightening. Over ~60%, the pre-debate analysis is too weak.
- **Source availability trend.** Which sources are chronically unreachable? Either find a workaround or stop pretending the lane exists.
- **Cost per scan.** Wall-clock time and token spend, split by phase. Where is the budget going, and is that where the decisive evidence came from?
- **False-positive rate on divergences.** How many flagged divergences turned out to be the market being right?

---

## Error Taxonomy

Classify every miss. The category determines the fix, and different categories need very different responses.

| Type | Definition | Typical fix |
|---|---|---|
| **Research miss** | The information existed and we didn't find it | Add a source or lane to `framework/sources.md` |
| **Reasoning error** | We had the information and drew the wrong conclusion | Add a check to `framework/council.md` or a case to `framework/goal.md` |
| **Calibration error** | Right direction, wrong confidence | Shift probability buckets; adjust conviction thresholds |
| **Timing error** | Right thesis, wrong horizon | Revisit Catalyst Path scoring and time stops |
| **Sizing error** | Right call, wrong size — or right on the small ones and wrong on the big ones | Revisit `framework/scoring.md` sizing and correlation caps |
| **Exit error** | Right entry, gave it back | Tighten gap-closure discipline |
| **Process failure** | The workflow didn't execute as designed | Fix `skills/catalyst-scan.md` |
| **Bad luck** | Correct process, unforecastable outcome | **No change.** This category must be used honestly and sparingly. |

The two ways to corrupt this: classify every miss as bad luck (learn nothing), or classify every miss as a process failure (thrash). Both are common. A ~10–25% bad-luck rate is plausible for genuinely probabilistic calls.

---

## Guardrails Against Overfitting

The framework should be hard to change, or it will chase noise.

1. **Three-instance rule.** Don't change a rule off one bad outcome. Require three instances of the same error type, *or* a clearly identified causal mechanism that would have prevented it.
2. **Process over outcome.** Judge the decision as it looked with the information available at the time. A good process can produce a bad outcome; a bad process can get lucky. Grade the process.
3. **Additions must have a removal candidate.** The framework can't grow without limit. Before adding a rule, name the rule or lane it replaces, or justify the added cost against the decisive-lane data.
4. **Keep it portable.** Any change must satisfy the editing rules in `framework/execution.md` — no vendor, tool, or harness names in `skills/` or `framework/`, no scripts or dependencies, and no reliance on a capability that only one environment has.
5. **Changelog everything.** Every framework change gets a dated entry with the evidence that motivated it, so a future retro can tell whether the change helped.
6. **No regime-chasing.** "AI names went down this quarter, so de-emphasize AI" is not learning. Distinguish a broken *thesis* from an unfavorable *regime*.

---

## Running A Retro

The executable procedure lives in `skills/retro.md`. This file defines *what gets measured and how changes are justified*; that file defines *how to run the session*. Every change it produces gets logged in the changelog below.

---

## Framework Changelog

| Date | File | Change | Motivation | Verdict |
|---|---|---|---|---|
| 2026-09-09 | all | Restructured single-file skill into a composable set: `goal` / `skill` / `sources` / `council` / `scoring` / `ledger` / `improve` | Instructions had grown past what one file could hold clearly, and the workflow needed to be executable as a parallel task graph rather than a linear checklist | Pending |
| 2026-09-09 | `skills/catalyst-scan.md` | Linear per-company loop replaced with a 7-phase dependency graph; independent lanes now fan out in parallel | Filings, positioning, sentiment, news, and macro share no inputs, so running them sequentially wasted both wall-clock time and context | Pending |
| 2026-09-09 | `skills/catalyst-scan.md` | Added watchlist tiering (Deep / Delta / Tripwire) and a divergence gate before the council | Scanning 24 names at equal depth spent most of the budget on names that were never going to be acted on | Pending |
| 2026-09-09 | `framework/sources.md` | New file: SEC/EDGAR endpoints and filing-diff technique, 13F/Form 4/short interest, expectations baseline, social sentiment, under-appreciated news | Prior process leaned on general web search and sell-side coverage; the primary-source and positioning lanes were missing entirely, and they're where the edge is | Pending |
| 2026-09-09 | `framework/council.md` | New file: five-seat adversarial debate with isolated openings, mandatory steelman, disconfirmation quota, and a named crux | Bear cases in prior reports read as disclaimers rather than arguments — a formality after the conclusion was already reached | Pending |
| 2026-09-09 | `framework/scoring.md` | "Valuation Support" → "Expectations Gap"; added forced distribution, separated evidence confidence from score, added mandatory exit conditions | Scores compressed into a 16–21 band across 24 names, and no report ever specified a sell discipline | Pending |
| 2026-09-09 | `state/ledger.md` | New file, seeded with 8 reconstructed predictions from the 2026-07-13 scan | Months of directional calls with nothing falsifiable recorded, so the framework had no way to find out if it was any good | Pending |
| 2026-09-09 | `framework/improve.md` | New file: this loop | No mechanism existed for the framework to learn from its own results | Pending |
| 2026-09-09 | layout | Reorganized into `skills/` (procedures) · `framework/` (doctrine) · `state/` (mutable) · `reports/` (append-only), added `AGENTS.md` | Flat root couldn't accommodate multiple skills, and mixing stable doctrine with per-run mutable state made it unclear what an agent was allowed to write to | Pending |
| 2026-09-09 | `skills/deep-dive.md` | Extracted single-name underwriting from a one-line "mode" into a real skill with an expectations model and a quality-of-earnings review | Establishing a Core position off a scan-depth look was the largest unmanaged risk in the process | Pending |
| 2026-09-09 | `skills/retro.md` | Split the retro *procedure* out of `framework/improve.md`, which keeps the metrics, taxonomy, guardrails, and changelog | Same procedure/doctrine split as the rest of the repo; the runnable checklist belongs with the other skills | Pending |
| 2026-09-09 | `framework/execution.md` | New file: neutral vocabulary, the sequential fallback for the research lanes, the no-isolation council mitigation, and editing rules that keep the repo harness-agnostic. Removed tool-specific instructions from the skills | Skills hardcoded one harness's task API and assumed delegation was always available, and nothing addressed a scan running without web access — which would have written stale fiction into the ledger | Pending |

Set **Verdict** to Helped / Neutral / Reverted at the next deep retro. A change that can't be evaluated shouldn't have been made.
