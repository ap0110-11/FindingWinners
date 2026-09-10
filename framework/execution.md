# Execution & Portability

This repo is plain Markdown and runs on any capable agentic coding tool. Nothing in `skills/` or `framework/` names a specific vendor, tool, model, or harness — this file is the only place that discusses them at all.

**The governing principle: the dependency graph is the contract; concurrency is an optimization.** A skill's phase order, gates, and output format are mandatory. *How* the work gets distributed is whatever your environment can do. A run that executes every lane sequentially in one context produces the same report as a run that fans out twelve workers — it just takes longer.

---

## Baseline Assumption

The skills assume **web access** and **file read/write in the repo**. That's it. Everything else is optional and has a stated fallback below.

**No web access is a hard stop, not a degradation.** A catalyst scan is by definition about what changed recently. Producing one from training data yields confident, plausible, stale claims — the most damaging failure this framework has, because it writes fiction into `state/ledger.md` and corrupts the one record that tells us whether any of this works. If you can't retrieve, say so and offer something that doesn't need retrieval, such as a retro over recorded predictions or a framework review.

---

## Vocabulary

Skills use these neutral terms. Map them to whatever your environment calls them.

| Term used in skills | Means | If your harness has delegation | If it doesn't |
|---|---|---|---|
| **research task** | One unit of work with its own instructions and its own clean context | A subagent, worker, or background task | A sequential pass: state the lane, do it, emit cards, drop the raw material, move on |
| **concurrently** | These tasks share no inputs and may run in any order or at the same time | Launch them together in one batch | Run them back to back in the order below |
| **isolated context** | This task must not see another task's output before producing its own | A separate task with no shared transcript | Write your output *before* reading the other side's, and don't revise it afterward |
| **orchestrator** | Whoever holds the plan and assembles results | The parent agent | You, in the main thread |

---

## Without Concurrency

Only the fan-out changes. Run the lanes **sequentially in this order**, which front-loads the ones that most often kill an idea early:

```
A Filings → C Expectations → E Under-appreciated news → B Positioning → D Sentiment → F Macro
```

Emit evidence cards at the end of each lane and move on without carrying the raw material forward — the context discipline matters as much as the speed. If a run gets long, **reduce scope rather than depth**: cut the Tier 2 list, don't cut lanes on Tier 1 names. A thin look at 20 names is worth less than a real look at 6.

---

## Without Isolated Contexts

This is the one capability that degrades badly, and it only affects the council. Bull and bear cases written in a single pass anchor on each other and you get a strawman instead of a debate.

Mitigation: write the **bear case first** — the direction the evidence usually doesn't favor, so it gets a fair hearing — commit it verbatim, and forbid yourself from editing it after writing the bull case. Then note in the report that the council ran without isolation. It's a real quality caveat, and the retro should be able to see it in the record rather than discovering later that half the debates were compromised.

---

## Data Access

Some environments issue raw HTTP requests with custom headers; others only browse rendered pages. Every source in `framework/sources.md` is reachable either way — prefer the structured endpoints when you can, use the human-facing UI when you can't. If neither works, that source goes in the availability note as unreachable. Never substitute recollection for retrieval.

---

## Portability Rules For Editing This Repo

When a retro changes these files, keep them portable:

1. **No vendor, tool, model, or harness names** in `skills/` or `framework/` — except in this file.
2. **No scripts, dependencies, or config formats.** Plain Markdown that a human can read and any model can follow.
3. **Describe capabilities, not products.** "A task with an isolated context," not the name of a particular tool's API.
4. **Assume no execution environment.** No shell, no interpreter, no notebook. If a computation matters, show the arithmetic in prose so it's auditable anywhere.
5. **Anything optional needs a stated fallback.** If a step only works with one specific capability, either give it a degradation path here or don't rely on it.
