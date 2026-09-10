# Deep Dive — Single-Name Research Skill

Full underwriting of **one** company, from scratch. Where `catalyst-scan.md` asks "what changed across the basket," this asks "do we actually understand this business well enough to own it, and at what size."

Run this before establishing any Core or High conviction position, and any time a scan produces a thesis nobody has stress-tested.

**Read first:** `framework/goal.md`, `framework/sources.md`, `framework/council.md`, `framework/scoring.md`.

Output goes to `reports/deep-dives/YYYY-MM-DD-{TICKER}.md`, and the durable facts land in `state/dossiers/{TICKER}.md`. Phases marked concurrent may be run sequentially if your environment can't delegate — see `framework/execution.md`.

---

## How This Differs From A Scan

| | Catalyst scan | Deep dive |
|---|---|---|
| Scope | Whole watchlist, tiered | One ticker |
| Lanes | Tier-dependent | All six, no exceptions |
| History | Delta since last scan | Multi-year, from first principles |
| Gate | Top 5–8 advance to council | No gate — council always runs |
| Valuation | Reverse-engineered baseline | Full expectations model with a bridge |
| Primary artifact | Report | Dossier + position proposal |

The point of no gate and no tiering is that a deep dive is what you run when you've *already* decided the name deserves the budget. Don't hedge it.

---

## Workflow

### Phase 0 — Frame (serial)
Write down, before researching: what you currently believe, why, and what the single question is that would change the answer. Recording the prior explicitly is what makes it possible to notice later that you only confirmed it.

Read the existing dossier and every prior mention of the name in `reports/`.

### Phase 1 — Business Understanding (concurrent)
Independent tracks with no shared inputs:

- **Unit economics** — what exactly is sold, to whom, at what price and margin, and what drives the incremental margin. Build the revenue bridge: volume × price × mix. If you can't write the revenue equation, stop and fix that before continuing.
- **Filing history** — last 8 quarters of 10-Q/10-K, plus the proxy. Run the language diffs across the whole series, not just the most recent pair; a phrase that drifted over six quarters is more informative than one that changed once.
- **Transcript series** — last 4–6 earnings calls plus any investor day. Track how management's own framing changed, and specifically what they stopped talking about. Read the analyst Q&A for what the street keeps probing, because that's where consensus doubt lives.
- **Competitive map** — who else does this, who is winning share, and what the customers say. Read the competitors' and customers' calls for mentions of this company.
- **Capital allocation history** — what they've done with cash over 5 years and what returns it earned. Past allocation is the best available predictor of future allocation.

### Phase 2 — Full Lane Sweep (concurrent)
All six lanes from `framework/sources.md` at maximum depth. Unlike a scan, this covers the full history, not the delta: complete 13F holder evolution over several quarters, multi-year insider record, the whole patent and hiring trajectory, all reachable regional and trade press.

### Phase 3 — Expectations Model (serial)
The analytical core. Do not shortcut this into a multiple comparison.

1. What does today's price imply for revenue growth, margin, and returns over the next 3–5 years? Show the arithmetic.
2. What does the evidence support instead? Build low, base, and high cases with explicit assumptions.
3. Where exactly does our view diverge from the implied path, and **which single variable carries the divergence**? Almost every thesis reduces to one or two variables; naming them tells you what to monitor.
4. Sensitivity: how wrong can that variable be before the thesis stops working?

### Phase 4 — Council (mandatory, full protocol)
Run `framework/council.md` end to end, with Bull, Bear, and Positioning opening in isolated contexts. For a deep dive, extend the Red Team seat to include a **quality-of-earnings review**: cash conversion across the full period, accrual trends, capitalization and depreciation policy, segment allocation, and any change in accounting estimates.

### Phase 5 — Position Proposal
Score per `framework/scoring.md`, then write the proposal:

- Thesis in three sentences, with the divergent variable named
- Conviction tier, size, and the reasoning behind the size specifically
- All four exit conditions
- The monitoring plan: which metric, from which source, checked at what cadence
- Ledger entries with probabilities and dates

---

## Report Structure

```markdown
# Deep Dive — {TICKER} · YYYY-MM-DD

## Verdict
Conviction, size, and the thesis in three sentences. Lead with the answer.

## What This Business Actually Is
Revenue equation, customers, unit economics, incremental margin.

## What Changed Over Time
Multi-quarter filing and transcript drift. What management stopped saying.

## Expectations Model
Implied path vs. our cases. The divergent variable and its sensitivity.

## Positioning
Full holder evolution, insider record, short interest, options-implied.

## Council
Full council output including the quality-of-earnings review.

## Position Proposal
Score, conviction, size, exits, monitoring plan.

## What Would Change This
The specific observable that flips the verdict.

## Open Questions
What we still don't know, and whether it's knowable from public sources.

## Source Availability
```

---

## Discipline Notes

- **Prior recorded in Phase 0 gets revisited in Phase 5.** If the conclusion matches the prior exactly, that's worth a sentence of suspicion — a deep dive that never surprises you probably wasn't one.
- **"Insufficient information" is a valid verdict** and a common one. Name the missing item and when it becomes available.
- **A deep dive that finds no divergence is a success**, not wasted work. It tells you the name is fairly priced and saves the position. Record it as a Pass with the reason so it isn't re-researched next quarter.
