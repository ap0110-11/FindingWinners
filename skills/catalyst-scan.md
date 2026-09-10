# Catalyst Scan — Research Skill

You are the **orchestrator** of a structured research process. Your job is not to do all the research in one undifferentiated pass — it is to decompose the work into a dependency graph, run the independent parts as separate research tasks, join the results, run an adversarial debate on what survives, and commit to falsifiable calls.

The graph below is the contract. Whether you execute it with concurrent tasks or sequentially in one context depends on your environment; `framework/execution.md` covers both.

**Read first:** `framework/goal.md` (thesis and edge), `framework/sources.md` (where to look), `framework/council.md` (debate protocol), `framework/scoring.md` (rubric and exits).

---

## Operating Principles

1. **Separate everything without a dependency.** Filings, positioning, sentiment, news, and macro do not depend on each other, so each gets its own research task with its own clean context. Run them concurrently where the platform allows — that's the main source of wasted wall-clock time — but the isolation matters even when the execution is sequential, because carrying one lane's raw material into the next is how context gets exhausted and how early findings anchor later ones.
2. **Delta-first.** Standing facts belong in `state/watchlist.md` and the per-ticker dossiers. A scan chases *what changed since the last scan*, not the company's whole history. Re-researching known facts is the main source of wasted tokens.
3. **Tier the watchlist.** Not every name deserves equal effort every week. Most of the budget goes to a handful of names.
4. **Gate before you spend.** Cheap filters first (disqualifiers, tripwires), expensive analysis (council) only on survivors.
5. **Structured hand-offs.** Research tasks return evidence cards, not prose. The orchestrator should never need to read a raw web page.
6. **Establish the baseline before forming a view.** What's priced in comes before what's true.
7. **Honest gaps beat fabricated coverage.** Every unreachable source gets named.

---

## The Workflow Graph

```
┌─ PHASE 0 ── PLAN ─────────────────────────────────── serial, cheap
│   scope · tier · read prior report + open ledger entries · set questions
└────────────────────────────────────────────────────────────────────
                              │
┌─ PHASE 1 ── FAN-OUT ────────────────────── ALL PARALLEL, no deps
│   A Filings      B Positioning    C Expectations
│   D Sentiment    E Under-appreciated news   F Macro/Regime
└────────────────────────────────────────────────────────────────────
                              │  join
┌─ PHASE 2 ── DOSSIER ──────────────── per ticker, parallel across tickers
│   merge cards · resolve conflicts · tag confidence · flag staleness
└────────────────────────────────────────────────────────────────────
                              │
┌─ PHASE 3 ── DIVERGENCE ────────────────────────────── per ticker
│   fundamentals vs price vs positioning vs narrative
│   ══ GATE: only top 5-8 divergences advance ══
└────────────────────────────────────────────────────────────────────
                              │
┌─ PHASE 4 ── COUNCIL ──────── parallel across tickers, serial within
│   Bull ‖ Bear ‖ Positioning → steelman → rebut → red team → crux → verdict
└────────────────────────────────────────────────────────────────────
                              │
┌─ PHASE 5 ── PORTFOLIO ────────────────────────────── serial
│   forced distribution · correlation · sizing · exits
└────────────────────────────────────────────────────────────────────
                              │
┌─ PHASE 6 ── WRITE + RECORD ───────────────────────── serial
│   report · ledger predictions · watchlist/dossier updates
└────────────────────────────────────────────────────────────────────
```

---

## Phase 0 — Plan

Serial and deliberately cheap. Do not start searching yet.

1. **Read state:** `framework/goal.md`, `state/watchlist.md`, the most recent report in `reports/catalyst-scans/`, and all OPEN entries in `state/ledger.md`.
2. **Resolve due predictions.** Any ledger entry past its resolution date gets resolved *first* — before new research, so today's findings can't contaminate the judgment. This is non-negotiable; skipping it is how the feedback loop dies.
3. **Assign tiers** for this run:

| Tier | Criteria | Treatment | Typical count |
|---|---|---|---|
| **T1 — Deep** | Current positions, live catalysts inside 30 days, unresolved theses, prior-scan conviction changes | All 6 lanes, full dossier, council | 4–8 |
| **T2 — Delta** | Rest of the watchlist | Lanes A/C/E only, changes since last scan | 10–15 |
| **T3 — Tripwire** | Dormant names | Automated check only: earnings date, >15% price move, 8-K filed, analyst action. Promote to T1/T2 only if a tripwire fires | remainder |

4. **Write the scan questions.** Two to four specific questions this scan exists to answer, e.g. "Did late-July hyperscaler capex kill or confirm the glut thesis?" A scan without questions produces a summary; a scan with questions produces a decision. Include any question the user asked directly.
5. **Emit the task graph** — the actual list of parallel tasks about to launch — so the run is auditable.

---

## Phase 1 — Parallel Fan-Out

Run all six lanes **concurrently** if your platform supports it — they share no inputs, so nothing is gained by finishing lane A before starting lane B. If it doesn't, run them sequentially in the fallback order in `framework/execution.md`; the graph is unchanged, only the wall-clock time.

Batch tickers within a lane (4–6 per research task) so you're running roughly 6–12 tasks, not 100. Give each task: the tickers, the lane spec from `framework/sources.md`, the lookback window, the scan questions, and the evidence card format.

| Lane | Focus | Spec |
|---|---|---|
| **A — Filings** | 10-K/Q, 8-K, proxy, S-1/3, language diffs, cash conversion, share count | `framework/sources.md` Lane A |
| **B — Positioning** | 13F deltas, 13D/G, Form 4, short interest, options-implied move | `framework/sources.md` Lane B |
| **C — Expectations** | Consensus + revision trend, multiple vs. history, PT dispersion, reverse-engineered implied trajectory | `framework/sources.md` Lane C |
| **D — Sentiment** | Reddit (stock subs *and* practitioner subs), X, StockTwits, Seeking Alpha, Glassdoor | `framework/sources.md` Lane D |
| **E — Under-appreciated news** | Hiring, government contracts, FERC/ISO queues, permits, patents, Asian supplier monthly revenue, trade press, second-order chains | `framework/sources.md` Lane E |
| **F — Macro/Regime** | Rates, rotation, credit, energy, regulation — one lane for the whole scan, not per ticker | `framework/sources.md` Lane F |

**Lookback:** since the last scan (primary), plus last 30 days and since last earnings for context. State the window in the report.

**Beyond the watchlist:** Lanes A and E should surface non-watchlist companies fitting the setups in `framework/goal.md` §3 — especially second-order supply chain names implied by watchlist companies' announcements. Route these into Watchlist Changes.

### Evidence Card Format

Every research task returns cards, never narrative:

```
TICKER | LANE | as-of YYYY-MM-DD | T{1-5}
CLAIM: {one sentence, with the number}
SOURCE: {URL or filing accession}
SO-WHAT: {why it changes the thesis, or "context only"}
CONFIDENCE: {high/medium/low} | NEW-SINCE-LAST-SCAN: {yes/no}
```

Each research task also reports **what it could not access**. That list goes into the report verbatim.

---

## Phase 2 — Dossier Assembly

Join the lanes per ticker. Parallel across tickers, serial within one.

- **Deduplicate**, and check whether "independent" sources are recycling one original report. Three outlets covering the same Reuters story is one source.
- **Resolve conflicts** by tier. When T1 and T4 disagree, T1 wins and the disagreement itself gets noted — the gap between the filing and its coverage is often the opportunity.
- **Flag staleness.** Anything older than the last earnings report is background, not news.
- **Downgrade** any claim resting only on T4/T5 to "hypothesis."
- **Update** `state/dossiers/{TICKER}.md` for T1 names so the next scan starts from the delta rather than from zero.

Output per ticker: a compact dossier with what changed, the expectations baseline, positioning, sentiment, open questions, and the confidence rating.

---

## Phase 3 — Divergence Detection

The core analytical step. For each ticker, compare the four axes:

```
FUNDAMENTALS (Lane A)  ──vs──  PRICE (Lane C)
      │                              │
POSITIONING (Lane B)   ──vs──  NARRATIVE (Lanes D+E)
```

Classify each name:

| Class | Pattern |
|---|---|
| **Divergence — Positive** | Fundamentals improving, price/positioning/narrative not reflecting it |
| **Divergence — Negative** | Narrative and price strong, fundamentals or filings deteriorating |
| **Confirmation** | All four axes agree — no edge, but useful for tracking existing positions |
| **Noise** | Nothing material changed |
| **Contested** | Lanes disagree in a way Phase 2 couldn't resolve — needs the council to settle |

Then run the **misclassification check** from `framework/goal.md`: which bucket is the market trading this in, and is that bucket right? Also run the **magnitude check**: compare the stock's move to the *business* change, not to the stock's own history. A 17% move against a 757% segment inflection is a muted reaction (the DELL lesson).

Apply the **disqualifier gate** (`framework/goal.md` §4) and drop failures now.

**GATE:** the top 5–8 divergences by magnitude × confidence advance to the council. Everything else gets a one-paragraph entry. Being explicit about what *didn't* advance, and why, is part of the output.

---

## Phase 4 — Council

Run `framework/council.md` in full for each gated name. Across tickers this is parallel; within a ticker it's serial after the isolated openings.

Critically: **Bull, Bear, and Positioning open in isolated contexts** — three separate research tasks that cannot see each other's output, brought together afterward for the steelman, rebuttal, red team, crux, and verdict. If you generate them in one pass, the second argument anchors on the first and the debate is theater. If your platform can't isolate contexts, use the mitigation in `framework/execution.md` and disclose it in the report.

---

## Phase 5 — Portfolio Synthesis

Serial, and this is where a list of ideas becomes a book.

1. Score every name per `framework/scoring.md`, then apply the **forced distribution** and the pairwise sanity check.
2. **Correlation:** group by underlying bet, not by ticker. Power (CEG/VST/BE), memory (MU/SNDK), compute supply, demand-side software, defense. Size at the theme level.
3. **Factor exposure:** how much of the book is one rate-duration bet? One AI-capex bet?
4. **Sizing and exits** per `framework/scoring.md` — all four exit conditions written for every Core/High name.
5. **Shock test:** name the single most likely adverse shock and estimate how much of the book moves together under it.

---

## Phase 6 — Write & Record

Write to `reports/catalyst-scans/YYYY-MM-DD-{scope}.md`, append predictions to `state/ledger.md`, and update `state/watchlist.md` and the T1 dossiers.

### Report Structure

```markdown
# Catalyst Scan — YYYY-MM-DD
Previous scan: {date} · Window: {range} · Scope: {tiers/tickers} · Lanes run: {A-F}

## 0. Prediction Scorecard
Resolutions of ledger entries due since the last scan: what we said, what happened,
what it teaches. Running hit rate and Brier score. **This section comes first, always.**

## 1. Scan Questions & Answers
The 2-4 questions from Phase 0, each answered in a short paragraph with the decisive
evidence. Lead with the answer.

## 2. What Changed
| Ticker | Change | Direction | Source tier | New? |
Delta table since the last scan. Omit anything that didn't change.

## 3. Regime
One paragraph. Which buckets it helps, hurts, and leaves alone. Separate discount-rate
moves from demand moves explicitly.

## 4. Ranked Book
| Rank | Ticker | Score | Δ | Confidence | P(bull) | Conviction | Setup | Divergence | One-liner |
Forced distribution applied. Score changes carry a one-line reason.

## 5. Council Verdicts
Full council output (council.md format) for each gated name.

## 6. Other Names
One paragraph each for T2/T3 names that didn't gate, and a line on which tripwires fired.

## 7. Positions & Exits
| Ticker | Thesis | Invalidation trigger | Time stop | Gap-closure target | Drift check |
Includes names where an exit condition is now close or triggered.

## 8. Catalyst Calendar
| Date | Ticker | Event | What it decides | Our prediction |
Forward-looking. Every entry should resolve something we claimed.

## 9. New Predictions
Falsifiable claims with probabilities and dates, appended to ledger.md.

## 10. Watchlist Changes
Adds (with the setup they fit), removes (with the reason so we don't re-research them),
tier promotions/demotions, new themes.

## 11. Source Availability
Which sources were reachable this run and which were not. Verbatim from the research tasks.

## 12. Process Notes
Which lanes produced the decisive evidence, what was slow or low-yield, and anything
that should change in the framework. Feeds improve.md.
```

---

## Efficiency Rules

- **Never re-derive standing facts.** If it's in the dossier and hasn't changed, cite it and move on.
- **Batch tickers within a lane.** One research task per lane per 4–6 tickers.
- **Cap research task output.** Evidence cards only; the orchestrator reads summaries, not sources.
- **Stop early on disqualifiers.** Kill a name in Phase 3 rather than carrying it to Phase 5.
- **Skip lanes that don't apply.** No 13F work on a name with no institutional ownership question; no supply chain lane on a pure software name.
- **Time-box the council.** If a debate hasn't found its crux in three rounds, the verdict is "Insufficient information" and the specific missing item goes in the calendar. That's a real answer.

## Honesty Rules

- Never claim to have checked a source you couldn't reach.
- Every number carries an as-of date.
- Distinguish "we found no evidence" from "we found evidence of absence."
- If the answer is "nothing actionable changed," say that in one paragraph and stop. A scan that manufactures activity to justify itself is worse than no scan.
- Report confidence honestly even when it undercuts an appealing conclusion.

---

## Scan Modes

Modes of *this* skill:

| Mode | Trigger | Phases |
|---|---|---|
| **Full** | Weekly | All, all tiers |
| **Delta** | Mid-week | 0 → 1 (lanes A/C/E) → 2 → 3, T1/T2 only, no council unless a gate fires |
| **Event** | Earnings, 8-K, shock | Phase 0 → affected lanes → council on affected names only |
| **Tripwire** | Automated | Phase 0 + T3 checks. Output is a single line unless something fires |

Separate skills, not modes of this one:

- **`skills/deep-dive.md`** — full underwriting of one name from scratch. Run before any Core/High position.
- **`skills/retro.md`** — audit the framework against its own results. No new company research.
