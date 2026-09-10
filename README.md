# Finding Winners

A research framework for finding companies where **fundamentals are improving faster than expectations are being revised** — and acting before the market closes the gap.

There is no code here — no scripts, no dependencies, no config. It's a set of Markdown instructions for an AI agent with web access. Point an agent at the repo and tell it which skill to run.

It's deliberately portable: nothing in `skills/` or `framework/` names a vendor, tool, model, or harness, so the same files run unchanged on any agentic coding tool. `framework/execution.md` is the only file that discusses environments, and it defines the one capability the skills actually branch on.

---

## Layout

Four directories, split by what each one *is* rather than by topic:

```
AGENTS.md      orientation, auto-loaded by most agents
skills/        what to do    — executable procedures, pick one and follow it
framework/     how to think  — shared doctrine, referenced by every skill
state/         what we know  — mutable; the agent reads and writes this
reports/       what we said  — append-only history, never edited
```

The reason for the split: skills are verbs and there will be several of them, but they all share one set of nouns. Doctrine lives in `framework/` so a new skill inherits the source tiers, the debate protocol, and the scoring rubric for free instead of restating them.

### `skills/` — pick one per session

| Skill | Purpose |
|---|---|
| `catalyst-scan.md` | Scan the watchlist for catalysts and changes. A 7-phase parallel task graph. Weekly, plus delta/event/tripwire modes |
| `deep-dive.md` | Full underwriting of one company from scratch. Run before any Core/High position |
| `retro.md` | Audit the framework against its own results and rewrite it. No new company research |

### `framework/` — read as referenced

| File | Purpose |
|---|---|
| `goal.md` | Thesis, where our edge comes from, the setups we hunt, hard disqualifiers, case studies |
| `sources.md` | Where to look and how — SEC/EDGAR, 13F and insider data, expectations baseline, social sentiment, under-appreciated news. Defines the six research lanes and the source tiers |
| `council.md` | Adversarial bull/bear debate protocol that runs before conviction is assigned |
| `scoring.md` | Scoring rubric, conviction tiers, sizing, and exit discipline |
| `improve.md` | What gets measured, the error taxonomy, guardrails on changing the framework, and the changelog |
| `execution.md` | Portability — neutral vocabulary, the fallback for environments without task delegation, and the rules that keep this repo harness-agnostic |

### `state/` — mutable

| Path | Purpose |
|---|---|
| `watchlist.md` | Companies grouped by theme, with standing facts and tiers |
| `ledger.md` | Falsifiable predictions with probabilities and dates. The accountability record |
| `dossiers/` | Per-ticker accumulated state for Tier 1 names, so scans can run delta-only |

### `reports/` — append-only

`catalyst-scans/YYYY-MM-DD-{scope}.md` · `deep-dives/YYYY-MM-DD-{TICKER}.md` · `retros/YYYY-QN.md`

---

## How It Works

Six research lanes run **in parallel** because none of them depends on the others:

```
A Filings   B Positioning   C Expectations   D Sentiment   E Hidden news   F Macro
                                  ↓ join
                        Dossier → Divergence → [gate]
                                  ↓
                    Council debate → Sizing → Report → Ledger
```

The four ideas that make this different from "ask an AI about some stocks":

**Expectations first.** Nothing is cheap or expensive in the abstract. Every name gets a reverse-engineered baseline — what growth and margin does today's price already assume? — before any view is formed. The thesis is always a claim about the *gap*.

**Primary sources over coverage.** The highest-yield, least-crowded work is reading the actual 10-Q language diff, the proxy comp metrics, the 8-K exhibits, the FERC queue, and the Taiwanese supplier's monthly revenue — not reading articles about them.

**Argue against yourself, formally.** A five-seat council (Bull, Bear, Positioning, Red Team, Judge) debates every gated name, with the bull and bear cases generated in isolation so neither anchors on the other. It has to find a single crux and commit to a probability.

**Keep score.** Every conviction call becomes a dated, falsifiable prediction in `state/ledger.md`, resolved before the next scan begins. `framework/improve.md` turns those resolutions into edits to these files.

---

## Running a Scan

In any agent that can read the repo, say:

**Full weekly scan**
> Follow `skills/catalyst-scan.md` to run a full catalyst scan. Resolve any due ledger predictions first.

**Mid-week delta**
> Run a delta scan per `skills/catalyst-scan.md` — Tier 1 and 2 names, lanes A/C/E, what changed since the last report.

**Deep dive on one name**
> Deep dive on MU per `skills/deep-dive.md`.

**Event-driven**
> CEG reported this morning. Run an event scan per `skills/catalyst-scan.md`: affected lanes plus a full council on CEG and VST.

**Answer a specific question**
> Using `skills/catalyst-scan.md`, answer: is the memory trade still intact after this week's prints? Run the lanes you need and convene the council on MU and SNDK.

**Retro**
> Run a deep retro per `skills/retro.md`.

On a platform that supports concurrency, tell the agent explicitly to **run the Phase 1 lanes concurrently** if it starts working through them one at a time. That's the single biggest speed difference between a good run and a slow one.

---

## Portability

The skills are written against capabilities, not products. They assume only two things: **web access** and **file read/write in the repo**. Everything else has a stated fallback in `framework/execution.md`.

Exactly one capability the skills branch on: whether your environment can **delegate work to tasks with isolated contexts**. If it can, the six research lanes run concurrently and the council's bull and bear cases are generated independently. If it can't, the lanes run sequentially in a specified order and the council uses a documented mitigation — write the bear case first, commit it verbatim, disclose the lack of isolation in the report. Same graph, same output format, same report either way.

The one hard stop is **no web access**: don't run a scan, because a catalyst scan built from training data is confident stale fiction that gets written into the ledger as predictions. Run a retro instead, which only reads what's already recorded.

`AGENTS.md` is the canonical orientation file and is picked up automatically by tools that look for it. `CLAUDE.md` is a one-line pointer for tools that look for that name instead — delete it if you don't need it. `framework/execution.md` §"Portability Rules" constrains future edits so this doesn't drift back into lock-in.

---

## Conventions

**Source tiers.** T1 filings and transcripts, T2 government/exchange data, T3 specialist trade press, T4 sell-side and mainstream media, T5 social. T4/T5 can never be the sole support for a factual claim — they tell you what people *believe*, which is the expectations side of the equation, not the fact side.

**As-of dates.** Every number carries one. A figure without a date isn't usable.

**Access honesty.** If Reddit or X or EDGAR wasn't reachable, the report says so. A fabricated source check corrupts the ledger and breaks the entire feedback loop, which is worse than a gap in coverage.

**Watchlist entry schema.** New and updated entries use:

```markdown
### TICKER
- **Company:** name
- **Theme:** what bet this actually is
- **Tier:** 1 Deep / 2 Delta / 3 Tripwire
- **Setup:** which pattern from framework/goal.md §3
- **Thesis:** one sentence
- **Invalidation:** the observable event that means we're wrong
- **Tripwires:** what would promote this to a deeper tier
- **Notes:** standing facts, most recent first
```

Apply this incrementally as names get touched rather than rewriting the file in one pass.

---

## Cadence

| Frequency | Activity |
|---|---|
| Weekly | Full scan, all tiers |
| Mid-week | Delta scan on Tier 1/2, or event scans as they happen |
| Monthly | Monthly retro per `skills/retro.md` — resolve ledger, update the scoreboard, tier review |
| Quarterly | Deep retro per `skills/retro.md` — framework diffs and a changelog entry |
| Before a new position | Deep dive per `skills/deep-dive.md` |
| 13F season | Mid-Feb, mid-May, mid-Aug, mid-Nov: dedicated positioning pass 45 days after quarter end |

---

## Current State

The framework has produced eight scans between May and July 2026 with reasonable divergence detection, but until recently it recorded no falsifiable predictions, specified no exits, and produced scores that clustered too tightly to rank anything. `state/ledger.md` has been seeded with eight reconstructed predictions from the 2026-07-13 scan — **three are overdue and should be resolved at the start of the next run**; the other five carry resolution dates through mid-October. Treat conviction language in reports as hypothesis until the ledger has 10–15 resolutions behind it.
