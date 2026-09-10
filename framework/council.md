# The Council — Adversarial Bull/Bear Debate

A structured debate that runs after evidence gathering and before conviction is assigned. Its purpose is to make the strongest version of both cases collide, so that what survives is a thesis rather than a story.

The failure mode this exists to prevent: an agent gathers evidence, notices it points one way, and then writes a "Bear Case" section as a formality — three hedged sentences that no one would act on. That is not a bear case. That is a disclaimer.

---

## When to Convene

Running a full council on 24 names is wasteful. Convene only for:

- Every name that passed the divergence gate in the scan (typically the top 5–8)
- Any name being proposed for a **new or increased position**
- Any current position where a **kill criterion** may have been triggered
- Any name where two lanes produced directly contradictory evidence

Everything else gets the standard scan treatment with a one-line bear note. If a name isn't worth a debate, it isn't worth a position.

---

## Seats

Five roles. Each is a separate reasoning pass — Bull, Bear, and Positioning open concurrently as independent research tasks that cannot see each other's output, after which the sequence becomes serial.

**Isolation matters.** If Bull and Bear are generated in the same context, the second one anchors on the first and you get a strawman. Generate the opening statements independently.

### 1. Bull
Builds the strongest good-faith long case. Must produce:
- The **mechanism** — the specific causal chain from what's happening now to higher earnings or a higher multiple, with rough magnitudes
- The **variant** — what the market believes that is wrong, and why the market believes it (a variant with no explanation for the market's error is usually just wrong)
- 3+ T1/T2 evidence cards supporting the mechanism
- The **path** — dated events that would confirm the thesis
- **Kill condition** — "I abandon this if X by date Y"

### 2. Bear
Builds the strongest short case, arguing to win, not to hedge. Must produce:
- The **primary bear mechanism** — the single most likely way this loses money, not a list of generic risks
- The **priced-in argument** — what the current price already assumes, and why the bull's "upside" is just the base case
- 3+ T1/T2 evidence cards
- The **timeline** — when the bear case shows up in reported numbers
- **Kill condition** — "I abandon this if X by date Y"

Bear is explicitly forbidden from these lazy moves: "valuation is high" without an expectations calculation, "competition may increase" without naming the competitor and the mechanism, "the cycle will turn" without a specific driver and rough timing, and any risk that applies equally to the whole market.

### 3. Positioning Analyst
Neutral on direction. Reports only on what is priced in and who owns it: 13F concentration and direction, insider activity, short interest and borrow, options-implied move vs. realized history, estimate revision trend, sell-side dispersion, and retail attention level.

Answers one question: **if the bull is right, who is left to buy — and if the bear is right, who is left to sell?** A correct thesis with no marginal buyer doesn't pay.

### 4. Red Team
Attacks the *reasoning*, not the direction. Ignores who's bullish and focuses on how the argument could be defective:
- **Base rate check** — how often do companies in this situation deliver what's being projected? Compare to the outside view, not the specific story.
- **Evidence audit** — is any load-bearing claim resting on a T4/T5 source? Is any number stale or as-of an old date? Are two "independent" sources actually recycling the same original report?
- **Bias audit** — narrative confirmation, recency, anchoring on the previous scan's conclusion, sunk cost on an existing position, motivated reasoning toward action
- **Circularity check** — is the bull case "the stock is cheap because analysts have high targets" or similar reasoning that assumes its conclusion?
- **Pre-mortem** — assume it's 12 months later and this lost 50%. Write the most likely story of what happened.
- **Second-order** — if the thesis is right, what does the competitive response look like, and does that compete away the returns?

Red Team has veto power over *evidence quality*: it can force a claim to be downgraded to "hypothesis" or struck entirely. It cannot dictate the verdict.

### 5. Judge (PM)
Adjudicates and owns the output. Must:
- State the **crux** — the one factual question on which the disagreement actually turns. Nearly every good debate reduces to a single crux; if you can't name it, the debate wasn't sharp enough.
- Assign **P(bull thesis correct)** as a calibrated probability
- Sketch rough outcomes: reasonable upside, base case, downside, with the probability weight on each
- Rule on **evidence sufficiency** — is this actionable now, or is it a hypothesis pending one specific piece of information?
- Set **conviction, sizing, and the invalidation trigger** per `framework/scoring.md`
- Record the falsifiable prediction into `state/ledger.md`

The Judge is required to state explicitly when the honest answer is "not enough information." That is a legitimate and common verdict, and it should be reached far more often than "high conviction."

---

## Procedure

```
Round 0   ISOLATED OPENING     Bull ‖ Bear ‖ Positioning   (parallel, no shared context)
Round 1   STEELMAN             each side restates the other's case to the other's satisfaction
Round 2   REBUTTAL             each side attacks the strongest version, not the strawman
Round 3   RED TEAM             attacks both cases and the evidence base
Round 4   CRUX                 both sides agree on the one question that decides it
Round 5   VERDICT              Judge rules, sizes, records the prediction
```

**Round 1 is not optional and not ceremonial.** A side that cannot restate the opposing case in a form the other side would accept has not understood it and forfeits the round. In practice this is where most fake disagreements dissolve — the two sides turn out to be arguing about different time horizons or different definitions.

---

## Debate Rules

1. **Every claim carries a source tier and an as-of date.** Unsourced assertions are struck from the record.
2. **Steelman before rebuttal.** No attacking a version of the argument the other side didn't make.
3. **Falsifiability required.** Both sides state, up front, what evidence would change their mind. A position that cannot be falsified is a belief, not an analysis.
4. **No appeals to authority.** "Goldman has a $400 target" is evidence about consensus, not about value. Cite it in the Positioning seat, not as support for a thesis.
5. **Quantify or withdraw.** "Margins may compress" is not admissible. "Margins compress 300–500bps if the customer mix shifts as the 10-Q language suggests" is.
6. **Time-bound everything.** A claim with no date attached cannot be scored and cannot be traded.
7. **Separate the question from the price.** First settle what's true about the business, then ask what's priced. Debating value and facts simultaneously is how people talk past each other.
8. **The disconfirmation quota.** Whichever side the evidence favors must produce at least **three** genuine pieces of disconfirming evidence found through active search — not hypotheticals invented for the exercise. If it can't find three, that is itself a finding: either the research wasn't thorough or the situation is unusually clear. State which.
9. **Reversal test.** If the stock were 40% higher, would the bull case still hold? If it were 40% lower, would the bear case still hold? A case that flips on price alone was a price opinion, not a thesis.

---

## Output Format

```markdown
### Council — {TICKER}, {DATE}

**Crux:** {the single question that decides this}

**Bull (mechanism):** {2-4 sentences with magnitudes} 
Key evidence: {T1/T2 cards} | Kill: {condition + date}

**Bear (mechanism):** {2-4 sentences with magnitudes} 
Key evidence: {T1/T2 cards} | Kill: {condition + date}

**Positioning:** Institutional {direction} | Insiders {activity} | Short interest {level/trend} 
Implied move {x%} vs. realized {y%} | Estimate revisions {direction} | Retail attention {level} 
Marginal buyer if bull right: {who} | Marginal seller if bear right: {who}

**Red Team:** 
- Base rate: {outside view}
- Evidence weaknesses: {what's thin, stale, or single-sourced}
- Bias risk: {named bias + where it shows}
- Pre-mortem: {the most likely loss story}
- Struck/downgraded claims: {list, or none}

**Disconfirming evidence found:** {3 items, or an explanation of why fewer}

**Verdict**
- P(bull thesis correct): {x%}
- Outcome sketch: upside {+x%} at {p}, base {+x%} at {p}, downside {-x%} at {p}
- Evidence sufficiency: {Actionable / Hypothesis pending {specific item} / Insufficient}
- Conviction: {Pass / Watch / Starter / Core / High} — see scoring.md
- Invalidation trigger: {specific, observable, dated}
- Recorded prediction: {LEDGER-ID}
```

---

## Anti-Patterns

Watch for these; they mean the council ran but didn't work.

| Anti-pattern | What it looks like | Fix |
|---|---|---|
| **Ceremonial bear** | Bear case is generic risk-factor boilerplate | Require a named mechanism with magnitude and timing |
| **Symmetric mush** | "Both sides have merit" with no probability | Force a number on P(bull correct) |
| **Crux avoidance** | Debate stays at the level of general themes | The Judge cannot rule without naming a single factual crux |
| **Evidence laundering** | A T5 rumor gets restated in Round 2 as established fact | Red Team traces every load-bearing claim to its original source |
| **Anchoring on last scan** | Bull case is a restatement of the previous report | Bull must cite evidence dated after the last scan |
| **False precision** | P(bull) = 73% | Use 5-point buckets: 20/35/50/65/80% |
| **Debate theater** | Long, elaborate, and ends where it started | If nothing in the verdict differs from the pre-debate view, note that — repeated occurrences mean the debate isn't adding value and should be tightened |
