# Retro — Framework Audit Skill

Grade the framework against its own results and rewrite it. **No new company research happens in a retro** — the temptation to drift into "but what about MU right now" is the main way these sessions fail.

**Read first:** `framework/improve.md` (metrics, error taxonomy, and the guardrails on changing things), `state/ledger.md`.

Output goes to `reports/retros/YYYY-QN.md` for deep retros, or `reports/retros/YYYY-MM.md` for monthly ones.

---

## Modes

| Mode | Cadence | Scope |
|---|---|---|
| **Monthly** | Monthly | Resolve due ledger entries, refresh the scoreboard, tier review, decide on pending changes |
| **Deep** | Quarterly | Full metric computation, error classification, framework diffs, changelog entry, one experiment |

The light per-scan version is just §12 Process Notes in the scan report — it doesn't need this skill.

---

## Procedure

1. **Resolve everything due** in `state/ledger.md`. Grade strictly; ambiguous resolves as a miss. Record the decisive lane and the setup for each.
2. **Compute the metrics** defined in `framework/improve.md` — outcome quality and process quality both. Show numbers, not impressions. If a metric can't be computed yet, say so and note what's needed.
3. **Classify every miss** using the error taxonomy. One category per miss; if two seem to apply, pick the earliest failure in the chain, since that's what a fix has to address.
4. **Read the winners too.** For each hit, decide whether it was process or luck. Unexamined wins build overconfidence faster than losses build caution.
5. **Check for recurring patterns.** Three instances of the same error type triggers a mandatory framework change under the three-instance rule.
6. **Work the standing questions** below.
7. **Draft the diffs.** Concrete edits to named files. "Be more careful about valuation" is not a diff; "cap Expectations Gap at 3 without a reverse-engineered baseline" is.
8. **Apply the changes and log them** in the `framework/improve.md` changelog with the motivating evidence.
9. **Set the verdict** on changes made at the *previous* retro — Helped, Neutral, or Reverted. A change nobody ever evaluated shouldn't have been made.
10. **Set one experiment** for next quarter: one specific thing to try differently, with a stated way to tell whether it worked.

---

## Standing Questions

Answer each explicitly. "No change" is a fine answer; skipping the question is not.

- **Are we early, on time, or late?** This is the entire edge from `framework/goal.md` §2. Measure lead time; don't estimate it.
- Are we finding things others aren't, or restating consensus with more words?
- Which lane earned its cost this quarter, and which didn't?
- Is the council changing verdicts or ratifying them?
- Are scores actually discriminating, or compressed again?
- Are we exiting on thesis, or on price and boredom?
- **What did we pass on that we should have taken?** Errors of omission are invisible unless you look for them — keep a running list of names considered and rejected so this question is answerable.
- What are we systematically avoiding because it's hard to research?
- Is the edge described in `framework/goal.md` §2 still the edge we're actually using?
- Which setups in `framework/goal.md` §3 are working, and should any be retired?

---

## Report Structure

```markdown
# Retro — YYYY-QN

## Verdict
Is the framework working? Two or three sentences, leading with the answer.

## Resolutions
Every ledger entry resolved this period: claim, probability, outcome, decisive lane, lesson.

## Metrics
Outcome quality (hit rate by tier and setup, Brier, calibration, lead time, miss magnitude)
and process quality (decisive lane attribution, council value-add, source availability,
cost per scan, divergence false-positive rate). Numbers, with prior-period comparison.

## Error Classification
Every miss, categorized. Recurring patterns called out.

## Wins Examined
Process or luck, for each hit.

## Standing Questions
Each answered.

## Changes Applied
The diffs, with motivation. Mirrored into the improve.md changelog.

## Prior Changes Evaluated
Helped / Neutral / Reverted for each change made last retro.

## Experiment For Next Quarter
One thing to try, and how we'll know if it worked.
```

---

## Discipline Notes

- **No new research.** If a resolution genuinely requires looking something up, look up only that specific fact and note it.
- **Grade before you explain.** Assign hit/miss first, then reason about why. Reasoning first produces generous grading.
- **Resist thrashing.** The guardrails in `framework/improve.md` exist because a framework rewritten every quarter never accumulates evidence about whether any version worked.
- **A retro that changes nothing is legitimate** if the evidence doesn't support a change — but say so explicitly, with the reasoning, rather than leaving it implied.
