# Agent Orientation

Equity research repo. No code, no dependencies, no scripts — these files are instructions for you, in plain Markdown, and are meant to work on any model or platform. Deliberately short so it can be loaded every session; follow the links for detail.

## Layout

```
skills/       what to do    — executable procedures, pick one and follow it
framework/    how to think  — shared doctrine, referenced by every skill
state/        what we know  — mutable; you read and write this
reports/      what we said  — append-only, never edit past reports
```

## Pick a skill

| Ask | Skill |
|---|---|
| Scan the watchlist for catalysts and changes | `skills/catalyst-scan.md` |
| Underwrite one company thoroughly | `skills/deep-dive.md` |
| Audit whether the framework is working | `skills/retro.md` |

## Before starting

The skills assume web access and file read/write, and nothing else. Say in one line whether you can **delegate work to tasks with isolated contexts** — that determines whether the research lanes run concurrently or sequentially, and it's the only capability the skills branch on. `framework/execution.md` covers both paths.

One absolute: **no web access means no scan.** Say so and offer a retro instead. A catalyst scan built from training data produces confident, stale fiction and writes it into the ledger.

## Rules that hold regardless of skill or platform

1. **Resolve due predictions in `state/ledger.md` before doing new research.** Once you've read today's news you can no longer grade last month's call honestly.
2. **Run independent work concurrently** if your platform allows it; otherwise run it sequentially in the order given in `framework/execution.md`. The dependency graph is mandatory, the concurrency is an optimization.
3. **Source tiers** (`framework/sources.md`): T1 filings, T2 government/exchange data, T3 specialist trade press, T4 sell-side and media, T5 social. **T4 and T5 can never be the sole support for a factual claim** — they establish what people believe, which is a different thing.
4. **Every number carries an as-of date.**
5. **Never claim to have checked a source you couldn't reach.** Write what was unavailable. A fabricated source check corrupts the ledger and breaks the feedback loop, which is worse than a gap.
6. **Commit to falsifiable claims.** Conviction goes in `state/ledger.md` with a probability and a resolution date, or it doesn't count.
7. **"Nothing actionable changed" is a valid output.** Don't manufacture findings to justify the run.

## Conventions

Reports: `reports/catalyst-scans/YYYY-MM-DD-{scope}.md`, `reports/deep-dives/YYYY-MM-DD-{TICKER}.md`, `reports/retros/YYYY-QN.md`.

Probabilities use five buckets only: 20 / 35 / 50 / 65 / 80%.

Show arithmetic in prose rather than relying on code execution, so any platform can follow and audit it.
