# Valuing Powered Capacity — Land, Grid, and Shell

Added 2026-09-15. A valuation playbook for companies whose asset is **energized land with a grid interconnection**, not compute. Written because the watchlist added GLXY, HUT and CIFR, and applying neocloud or tech multiples to them produces nonsense in both directions.

The core claim: **these are real-estate and infrastructure assets wearing a technology ticker.** Value them on asset life, contract duration, and tenant credit. The multiple is an output, never an input.

---

## 1. First, Decide Which Business You Are Actually Looking At

Two businesses are routinely reported under one ticker and the market blends them. Separate them before anything else.

| | **Powered-shell landlord** | **Neocloud / compute reseller** |
|---|---|---|
| What is sold | Space, power, cooling, interconnection | GPU-hours as a service |
| Revenue standard | **ASC 842** operating lease income | **ASC 606** services revenue |
| Who buys the GPUs | **The tenant** | **The company** |
| Core asset | Land, substation, interconnect rights, shell | GPUs |
| Asset life | 20–40 years; no technological obsolescence | 3–6 years, with a live obsolescence cycle |
| Typical contract | 10–20 years | 2–5 years |
| Recurring capex | Low after stabilization | **Enormous and permanent** — you re-buy the fleet each cycle |
| Revenue per MW (IT) | Low | High — IREN disclosed above $20M/MW for the full stack (T1, 2026-08-27) |
| Right comp set | Data center REITs, IPPs, toll infrastructure | Nobody good. IT services at best |
| Right method | **Cap rate on NOI, plus a development pipeline** | DCF on return-on-capex, with an obsolescence haircut |

A high revenue-per-MW figure is **not** evidence of a better business. It usually means the company bought the depreciating asset instead of the tenant. Compare returns on invested capital, never revenue per MW across the two models.

### The accounting is the tell, and it is auditable

You do not have to take management's characterization. The filings distinguish these two businesses mechanically:

- **Pull the revenue disaggregation footnote.** Revenue sitting under ASC 606 is service revenue. Revenue sitting under ASC 842 is rent.
- **Pull the lease footnote and read it as a *lessor*.** Most analysts read lease footnotes looking for the company's own obligations. For a landlord, the lessor disclosures — future minimum lease payments by year, lease classification, and whether any lease revenue has been recognized yet — are the whole story.
- **Compare the two backlog numbers.** A company reporting both an ASC 606 remaining-performance-obligation figure and a separate ASC 842 lease-arrangement figure is telling you the mix, and they are not interchangeable.

**Worked example, verified from filings during the 2026-09-09 scan.** IREN's FY26 10-K (T1, filed 2026-08-27) disclosed $5.1B of unsatisfied ASC 606 RPO *and separately* $11.4B of ASC 842 lease arrangements — so roughly two-thirds of the contracted book is structured as a lease, meaning IREN is more landlord than neocloud on its largest contract. The same filing showed $1,623.5M of "deferred lease revenue — operating leases" with **no lease revenue recognized in any period presented.** Under ASC 842 the cost of the build hits the income statement while the revenue waits for the service term to commence. That is a timing convention, not a business failure — and it is also not a hidden asset. It cuts both ways and you must say which way you are reading it.

**Rule:** a company reporting revenue under both standards requires a sum-of-the-parts. A blended EV/Sales or EV/EBITDA multiple on such a company is meaningless and should never appear in a report.

---

## 2. Normalize the Megawatts Before You Do Any Arithmetic

Companies in this vertical quote at least five different MW numbers that differ from each other by three to five times. Using the wrong one is the single most common way to be off by 300%.

| Term | What it means | Trap |
|---|---|---|
| **Nameplate / gross power** | Size of the interconnection agreement | Largest number; always the one in the headline |
| **Critical IT load (MW IT)** | What the tenant actually receives, after PUE and electrical losses | **The only number that maps to revenue.** Use this |
| **Energized** | Power physically delivered to the site today | The only number that can generate revenue *this year* |
| **Contracted / leased** | Signed with a tenant | Ask whether the tenant is paying yet |
| **Pipeline / LOI / queue** | Aspirational | Often has no interconnection agreement, no water, no fiber, no tenant |

**Always state the gross-to-IT conversion factor you used and where it came from.** A 1.3x PUE assumption versus 1.6x is a 23% difference in derived revenue per MW.

**This trap has already bitten us once.** IREN stated capacity as "480MW gross for 2026 and 1.2GW gross for 2027" in its July 20 and August 13 releases, then as "~0.3GW (IT) for 2026 and ~0.8GW (IT) for 2027" on August 27 — **the unit changed mid-window with no reconciliation** (T1, all three dates). That is a 1.6x difference in the same company's guidance inside five weeks. Assume every company in this vertical does the same thing, and normalize before comparing any two of them.

---

## 3. The Method: Sum of Four Parts, Not a Multiple

These companies are a stack of assets at different maturities with genuinely different risk. Value each separately and show the arithmetic in prose.

### Part 1 — Energized, leased capacity → cap rate on NOI

This is real estate and should be valued like it.

1. Annual contracted lease revenue per MW IT
2. **Less the opex the landlord actually bears.** This depends entirely on lease structure: triple-net pushes property tax, insurance and maintenance to the tenant; modified gross does not. Read the lease terms, do not assume.
3. = NOI per MW
4. Value = NOI ÷ cap rate

**Choosing the cap rate is where most of the answer comes from, so it must be defended explicitly.** Anchor it as a spread over the long real yield rather than the nominal — this is a long-duration contracted asset, and the long *real* rate is what discounts it. As of 2026-09-09 the 10-year real yield was 2.41%, having risen only ~5bp over the scan window while the 2-year real yield went from 0.51% to 2.08% (T2). That distinction matters enormously here: **front-end rate moves do very little damage to a 15-year lease's present value, and the market routinely sells these names as though they do.** That gap is a recurring Misclassified setup in this vertical.

Rough underwriting ladder, to be re-derived from live comps rather than taken as fixed:

| Situation | Cap rate treatment |
|---|---|
| Stabilized, investment-grade tenant, 15yr+ lease, multiple sites | Tightest — data center REIT territory |
| Single tenant, investment-grade, 10–15yr | Add a concentration premium |
| Single tenant, venture-funded or non-rated | Add a large credit premium. A non-rated AI tenant and a hyperscaler are the *same megawatt at completely different values* |
| Development-stage operator, no lease-up track record | Widest |

Sensitivity is brutal and must always be shown: the difference between a 6% and a 9% cap rate is roughly 50% of the value. If a report states one cap rate without a range, the report is hiding the assumption that drives the conclusion.

### Part 2 — Energized but unleased capacity → replacement cost, haircut for lease-up

Value at what it would cost to build today, then discount for the time and risk of finding a tenant. Components, roughly in ascending order of scarcity: land, shell, electrical distribution and switchgear, cooling (liquid cooling for AI raises this materially), and **grid interconnection plus substation, which is the scarce part and usually the largest.**

Two cautions that pull in opposite directions:

- **Replacement cost is a floor only if the asset can actually be replicated.** It frequently cannot. An energized interconnection that took four years to secure is not reproducible at cost in a market where ERCOT amended its large-load interconnection approval process and the Texas Governor ordered an audit of every data center in the queue — both disclosed as new risk factors in IREN's FY26 10-K (T1, 2026-08-27). For already-energized sites, replacement cost **understates** value.
- For sites still in the queue, replacement cost **overstates** value, because you are pricing an asset that may never energize.

Also note that capex per MW is inflating. IREN disclosed data center and GPU capex requirements up approximately 15–20% (T1, 2026-08-27). Rising replacement cost raises the floor under existing energized capacity — which is the strongest structural argument in this vertical and the one least reflected in screens.

### Part 3 — The interconnection queue → an option, priced as an option

This is where the stocks actually trade and where the fiction lives. The market assigns a dollar value per MW of "pipeline" that frequently includes megawatts with no interconnection agreement, no water rights, no fiber, and no prospective tenant.

**For every claimed MW, require a documentary answer to four questions.** No answer means the MW is excluded from the base case and noted in the report as excluded.

1. **Is there a signed interconnection agreement, and at what stage?** Queue position, completed system impact study, and an executed large-generator or large-load interconnection agreement are three very different assets.
2. **Is the power available on the claimed date, or is it a queue slot subject to reform?** Queue reform is live policy risk, not a tail risk.
3. **Is there a tenant, and what is their credit?** This sets the cap rate on the entire part.
4. **Who pays for the GPUs and the cooling?** This determines whether the megawatt is a lease or a service — see §1 — and therefore which method applies.

Treat the residual pipeline as an option with an explicit probability, using the framework's five buckets (20/35/50/65/80%). Never fold pipeline into a base case at 100%.

### Part 4 — The legacy business → value separately, and check the sign

Most companies entering this vertical arrived from bitcoin mining. That legacy segment needs its own valuation and it is frequently worth **less than zero on an opportunity-cost basis**, because every megawatt burned on mining is a megawatt not leased to a tenant at a higher and contracted rate. Compute mining gross profit per MW and compare it to lease NOI per MW. If leasing wins, the mining fleet is a liability that happens to generate revenue, and the correct valuation is the fleet's liquidation value less the decommissioning cost.

**This is observable, not theoretical.** IREN's FY26 disclosed $638.8M of impairments, $450.4M of it in Q4, primarily from decommissioning mining hardware, plus a $110.6M decrease in the fair value of assets held for sale, with management flagging that further such charges "could be material" (T1, 2026-08-27). The conversion is real and it is expensive, and companies mid-conversion will keep taking these charges.

### Then the corporate layer

Add cash, subtract debt, and — critically — **account for the dilution overhang properly.** This vertical is financed by serial equity and convertible issuance. Count anti-dilutive potential shares, convertible-linked shares, and registered resale shelves, not just the basic count. For scale, IREN's excluded anti-dilutive shares totalled 146.1M weighted-average, roughly 37% of shares outstanding, including 71.8M from convertible notes (T1, 2026-08-27).

---

## 4. The Screen: EV per MW, Computed Three Ways

The single most useful first-pass metric, and it must be shown in all three forms:

- **EV ÷ energized-and-leased MW IT** — the harsh version. What you are paying per megawatt that is actually earning today.
- **EV ÷ energized MW IT** — the near-term version.
- **EV ÷ total claimed pipeline MW** — the flattering version, and the one in the pitch deck.

**The ratio between the harsh and the flattering number is the finding.** If it is 5x, then four-fifths of the equity value is an option on capacity that does not yet exist. That is not automatically a sell — options have value — but it must be stated as an option rather than presented as an asset. A company trading at a modest EV per pipeline MW and an extreme EV per leased MW is a development story, and it should be underwritten, sized and exited as one.

---

## 5. Disqualifiers, Translated for This Vertical

The `framework/goal.md` §4 disqualifiers need restating here, because the generic versions either misfire or miss.

| Generic disqualifier | How it reads in this vertical |
|---|---|
| Serial equity issuance funding operations | **Near-universal, so it cannot be a blanket disqualifier.** The real test: does the $/MW of *energized* capacity added per year exceed the dilution per share? If issuance funds capacity that earns above the cost of capital, it is growth; if it funds SG&A and interest, it is a treadmill |
| Thesis rests on a single customer | **Structurally true for almost every name here.** Replace the test with tenant credit rating, lease term, and the remedies on default — not with "diversification" |
| Circular revenue | Live and specific in this cycle: a chip vendor invests in an AI startup, the startup leases capacity, the landlord books contracted revenue, the vendor books chip revenue. **Trace the cash and name every party** |
| Related-party transactions | Very common in miner-to-landlord conversions. Read the related-party footnote before anything else |

**Two additions specific to this vertical:**

**Naked energy exposure.** If the landlord sells power to tenants at a fixed rate while buying at merchant prices, it has written an uncovered energy option. This is the mechanism that kills these companies in an energy spike, and it is disclosed in the power-purchase discussion rather than the risk factors. Brent rose roughly 25% between July 13 and September 9, 2026 (T2), so this is a live condition, not a hypothetical. Require either a matched hedge, a pass-through clause, or owned generation.

**Regulatory capture of the demand.** A landlord's pricing power depends on data-center load being allowed to bid freely for power. That is now changing by statute. Three states legislated restrictions in three months — North Carolina SB 730, Pennsylvania GRID standards, and a Massachusetts executive order (2026-09-08) requiring facilities above 25MW to bring 100% clean power or pay into a ratepayer fund — and **Virginia segregates data-center power markets effective 2027-01-01** (T2/T3, verified in the 2026-09-09 scan). Oklahoma's Data Center Customer Ratepayer Protection Act of 2026 applies to new loads of 75MW+ contracted after July 1, 2026. Before underwriting any site, check the statute in its state.

---

## 6. Apply the Transmission Check

`framework/scoring.md` requires naming the mechanism by which an operational tailwind reaches the share price before scoring Catalyst Path above 3. In this vertical the answer is unusually clean, which is the attraction:

**A signed, long-dated lease with a credit tenant converts directly into contracted cash flow on a dated schedule.** There is no appropriation to wait for and no budget line to be approved. That is a genuinely stronger transmission path than the defense or demand-side software cases that failed in July.

But three things can sever it, and each must be named:

1. **The lease commencement date, not the signature date.** Cost precedes revenue under ASC 842, so the P&L looks worse before it looks better. The market reads the interim quarters as deterioration. This is the recurring **Misclassified** opportunity in the vertical, and also the recurring value trap — the two are distinguished only by whether commencement actually arrives.
2. **Rates, via the wrong end of the curve.** Long contracted cash flow trades as a rate instrument. Check whether a de-rating was driven by the *long real* yield, which actually discounts the asset, or by the front end, which does not. The July 2026 utilities lesson applies directly.
3. **Grace periods and delivery slack.** Read the contract terms for permitted slip. IREN's Microsoft agreement contains grace periods extending delivery from mid-Q4 CY2026 to the beginning of Q2 CY2027 — roughly two quarters of permitted delay without breach (T1, 2026-08-27). A milestone that can slip two quarters without penalty is not a dated catalyst, and Catalyst Path must be capped accordingly.

---

## 7. Minimum Evidence Bar Before Any Name Here Gets Scored

A name in this vertical **cannot be scored** until all of the following are pulled from T1 or T2 sources, each with an as-of date:

1. Revenue disaggregated by ASC 606 versus ASC 842
2. Lessor lease footnote, including future minimum lease payments by year
3. MW normalized to critical IT load, with the conversion factor stated, split into energized / leased / in-queue
4. Tenant identity and credit standing, plus lease term and escalators
5. Interconnection agreement stage per site, and the governing state statute
6. Power procurement structure — fixed, merchant, hedged, or owned generation
7. Capex per MW actually incurred, from the cash flow statement rather than a presentation
8. Full dilution: anti-dilutive potential shares, convertibles, registered resale shelves
9. Related-party footnote
10. Legacy segment gross profit per MW, compared to lease NOI per MW

Until then the name sits at Tier 3 with no score. **A score built on a presentation deck is worse than no score**, because it enters the ledger and corrupts the calibration record.
