# Scoring, Conviction & Exits

## The Problem With The Old Rubric

In the 2026-07-13 scan, 24 names scored between 13 and 25 — but 20 of them landed in a 16–21 band, and half sat at 16–18. A score that assigns nearly every name the same value isn't ranking anything; it's laundering a gut feel through arithmetic. Three fixes below: re-anchored dimensions, a forced distribution, and separating *how good is this* from *how sure are we*.

---

## The Five Dimensions

Score each 1–5. The old "Valuation Support" is replaced by **Expectations Gap**, which is the actual question the framework cares about.

### 1. Information Edge
*Do we know something the market hasn't priced, and how did we come to know it?*

| Score | Anchor |
|---|---|
| 5 | Non-obvious insight from primary sources or cross-domain triangulation that we have not seen articulated anywhere else |
| 4 | Material new information from filings/regulatory data, thinly covered by the street |
| 3 | Real change, but widely reported — we're reading the same news as everyone |
| 2 | Incremental datapoints confirming a known trend |
| 1 | No new information; we're restating the consensus |

A 5 requires naming *which lane produced it* and *why others missed it*. If you can't, it's a 3.

### 2. Business Quality
*Would we want to own this for years if the multiple never changed?*

| Score | Anchor |
|---|---|
| 5 | Durable structural advantage, pricing power, high incremental ROIC, low customer concentration |
| 4 | Strong position with an identifiable moat; some concentration or cyclicality |
| 3 | Good business, competitive market, moat is execution rather than structure |
| 2 | Commodity economics, price-taker, or heavy capital intensity with mediocre returns |
| 1 | Structurally challenged, or economics depend on conditions that won't persist |

### 3. Expectations Gap
*How far is the trajectory from what the price implies?* Requires the reverse-engineered baseline from `framework/sources.md` Lane C. Without that work, cap this at 3.

| Score | Anchor |
|---|---|
| 5 | Price implies materially worse than the evidence supports; large gap with a clear closing mechanism |
| 4 | Meaningful gap, defensible under conservative assumptions |
| 3 | Roughly fairly priced for the visible trajectory |
| 2 | Price already assumes the bull case executes |
| 1 | Price requires assumptions beyond anything management has guided to |

### 4. Catalyst Path
*Is there a dated, observable sequence that forces the gap to close?*

| Score | Anchor |
|---|---|
| 5 | Multiple dated catalysts inside 6 months, each independently verifiable |
| 4 | Clear catalyst inside 6 months |
| 3 | Catalysts exist but are 6–12 months out or fuzzy |
| 2 | Story is real but nothing scheduled will prove it |
| 1 | Requires an unforecastable event, or the catalyst already passed |

A gap with no catalyst is a value trap. This dimension is what separates the two.

### 5. Positioning Asymmetry
*Which way is the crowd leaning, and who's the marginal buyer?* Uses Lanes B and D.

| Score | Anchor |
|---|---|
| 5 | Under-owned by institutions, retail indifferent, insiders buying, estimates starting to rise |
| 4 | Neglected or out of favor with early signs of positioning shift |
| 3 | Neutral positioning, no edge either way |
| 2 | Crowded long, consensus favorite, heavily owned |
| 1 | Euphoric — mania-level retail attention, insider selling, everyone already long |

**Total: /25.**

---

## Evidence Confidence — Scored Separately, Never Added In

Confidence is not a sixth dimension. It's a multiplier on how much the score is allowed to move real money.

| Level | Meaning |
|---|---|
| **High** | Thesis rests on T1/T2 sources, multiple lanes agree, no material gaps, council reached a clear crux |
| **Medium** | Core claims sourced, but one important lane was unavailable or one key claim is single-sourced |
| **Low** | Significant reliance on T3–T5, key data stale or missing, lanes contradict each other unresolved |

A 22/25 at Low confidence is not actionable. Say so explicitly rather than letting the number carry the day.

---

## Forced Distribution

Applied across every name in a full scan. This is the fix for compression.

- **At most 20%** of scanned names may score ≥20
- **At least 20%** must score ≤14
- No more than 40% may sit in any single 3-point band
- Ties are not allowed in the top 10 — break them by explicit pairwise comparison

Before publishing, run the **pairwise sanity check** on adjacent ranks: "would I rather own #4 or #5 today, and does the score ordering match that answer?" If it doesn't, the scores are wrong, not the preference.

If a score changes from the prior scan, state the reason in one line. Scores that drift without an explanation are noise.

---

## Conviction Tiers

Conviction is a function of score, confidence, and P(bull correct) from the council — not score alone.

| Tier | Requires | Meaning |
|---|---|---|
| **High** | ≥21/25, High confidence, P(bull) ≥65%, council verdict Actionable | Largest position size |
| **Core** | ≥19/25, ≥Medium confidence, P(bull) ≥55% | Standard full position |
| **Starter** | ≥17/25, or a high score at Medium/Low confidence, or a strong thesis awaiting one catalyst | Partial position; add on confirmation |
| **Watch** | Thesis identified but a gate is unmet | Must name the *specific trigger* that promotes it |
| **Pass** | Fails a disqualifier, or the gap has closed | Say why, so we don't re-research it next month |

**"Watch" is only legitimate with a named trigger and a date.** "Keep watching" as a way of avoiding a decision is banned — it is the most common way this kind of framework degrades into a newsletter.

---

## Sizing

Score sets the *rank*. Volatility and correlation set the *size*.

Adjust the tier's base size for:
- **Volatility** — a 5%-daily-move name at the same conviction as a 1.5% name gets less capital, not the same
- **Correlation** — CEG, VST, and BE are one power bet; MU and SNDK are one memory bet. Sum exposures at the *theme* level, not the ticker level, and cap theme exposure.
- **Liquidity** — position must be exitable in a stressed tape without moving the price
- **Event risk** — a full position built the day before earnings is a coin flip, not a thesis. Consider entering partially before and completing after.

Then run the **portfolio-level check**: if the single most likely macro shock hits (rates up 100bp, AI capex guidance cut, energy spike), how much of the book moves together? Concentration by *factor* is the risk that actually shows up, and a list of 8 "uncorrelated" AI names is usually one position.

---

## Exits — The Missing Half

Every position gets all four of these written down at entry. A position without them is not a position, it's a hope.

**1. Thesis invalidation.** The specific, observable event that means we were wrong. Not "the stock falls 20%" — that's a price move. Something like "Q3 shows HBM pricing down QoQ, contradicting the sold-out-through-2027 claim."

**2. Time stop.** By what date should the thesis have visibly progressed? If the catalyst passed and nothing happened, that *is* information — the market saw the same catalyst and shrugged. Re-underwrite from scratch rather than extending the deadline.

**3. Target / gap closure.** What condition means the opportunity is gone? Usually the expectations gap closing: consensus catches up, the multiple re-rates, the variant becomes the narrative. **Exit when you're right and it's priced**, not when you're bored. This is the discipline that separates the ALAB pattern (sell into the re-rating) from round-tripping it.

**4. Thesis drift check.** At every scan, ask: is the current reason to own this the same as the original reason? If the thesis quietly changed from "AI server inflection" to "it's cheap now," the original thesis failed and we're rationalizing. Close it and re-enter on the new thesis if it stands on its own.

---

## Disqualifier Gate

Run before scoring — it's the cheapest step and kills ideas fastest. See `framework/goal.md` §4. Any hit means Pass regardless of score. Log the disqualifier in the report so the name isn't re-researched next month.

---

## Prediction Recording

Every Core or High conviction call, and every Pass on a name that previously scored well, produces a ledger entry:

- The falsifiable claim, with a number
- Calibrated probability (buckets: 20 / 35 / 50 / 65 / 80%)
- Resolution date
- The setup name from `framework/goal.md` §3
- The lane that produced the decisive evidence

This is what makes the framework improvable rather than just repeatable. See `state/ledger.md`.
