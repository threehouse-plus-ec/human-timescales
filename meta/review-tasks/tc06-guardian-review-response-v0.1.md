# Guardian-stance review memo — TC-06 v0.1

*Endorsement Marker (provisional). Internal scoping work, not a Coastline. No external endorsement is asserted.*

**Date:** 2026-04-28
**Stance:** Guardian (R8 temporal-parallax discipline; with R4 motte-and-bailey discipline as cross-cutting lens)
**Responding to brief:** RT-2026-002
**Deliverable under review:** `docs/protocols/human-timescales-commensurability-protocol-v0.1.md` (TC-06)
**Scout response taken as input:** RT-2026-001 (`tc06-scout-review-response-v0.1.md`)

Guardian rules from the position that R8 is closed only when temporal parallax has been operationally evicted, not merely rendered visible. Scout's "surfaces only" verdict on Q1 of RT-2026-001 is taken as binding context: dual measurement is necessary but not sufficient. The five rulings below are calibrated to that premise.

---

## Per-question rulings

### Q1 — Effect-size floor (Q-CP3)

**Ruling: option (c), Guardian-modified.** Adopt era-stratified three-band floor as Scout-recommended, **with band boundaries pre-declared in TC-06 v0.2 §5 and locked against post-hoc revision except by Guardian re-authorisation.** Bands as Scout proposed: 325–1100 / 1100–1800 / 1800–1965. Band-specific slope floors derived from L₅ scale with documentary-density covariate adjustment (drafter to compute and submit for Guardian ratification under v0.2 review).

The lock matters more than the stratification. An era-stratified floor without pre-declared boundaries is a degree of freedom that motte-and-bailey moves can exploit — an analyst whose verdict is sensitive to the 1100/1800 thresholds can shift them under pressure. Pre-declaration with Guardian re-authorisation removes that degree of freedom.

**Boundary-fragility addendum (cross-references catch-all §3 below).** Any verdict whose effect-size determination falls within ±25 years of a band boundary must be reported under both adjacent bands' floors, with divergence flagged. This converts the discontinuity into reportable data rather than a hidden sensitivity.

### Q2 — Channel-dominance + cross-card coupling

**Q2(a) Channel-dominance annotation: ratify-with-modification.** Reject Scout's per-interval analyst-declaration framing in favour of a stronger discipline: **presumptive channel-dominance by era band**, matching the Q1 stratification. Calendar-time presumptive-authoritative for the 325–1100 band (institution-internal records sparse; calendar dating is the more reliable construct); institution-internal-time presumptive-authoritative for the 1100–1800 band (papal succession well-documented and the construct under examination); both channels co-authoritative for 1800–1965 with mandatory concordance. Analyst override permitted with declared reason; override across more than one band's worth of intervals requires Guardian re-authorisation. This binds Q1 and Q2(a) into a single stratification design.

**Q2(b) Weak-concordance for n < 12: replaced with three-tier power rule.** Scout's binary n < 12 / n ≥ 12 cut-off is itself a degree of freedom. Replacement:

- **n < 8:** strict concordance retained; verdicts default to **inconclusive** with explicit power-flag annotation. No rescue.
- **8 ≤ n < 15:** weak concordance permitted (Scout's definition: non-rejection in one channel, no rejection at p < 0.01 in the other), with **mandatory minimum-detectable-effect-size reporting** in the analytic memo.
- **n ≥ 15:** strict concordance binding.

The tiered structure makes the conservatism gradient continuous, removes the n=11/n=12 cliff, and forces the small-n regime (where rescue temptations are highest) into transparent under-power admission.

**Q2(c) Boundary-case combined annotation: ratified.** When both presumptive channel-dominance and weak-concordance apply to the same verdict, both annotations appear in the analytic memo. Architect's recommendation accepted as drafted.

### Q3 — §6 procedural-falsification + §4.4 motte-and-bailey audit

**Tighten §6: yes, specific revision.** Replace the §6 sentence with: *"Any subsequent stationarity claim issued by TC-01, TC-04, or downstream M1-method work that does not declare its protocol per this document, OR that declares this protocol but fails any of the six §5 acceptance conditions while nevertheless asserting stationarity, is invalidated."* Nominal-invocation-with-condition-failure is the canonical motte-and-bailey move R4 exists to discipline; making it textually invalidating closes the rescue route.

**§4.4 tag-set audit: insufficient as drafted.** The four-tag set with `none-identified` as residual is too easy a default — under empirical pressure, `tenure-trend` will absorb signals that should land in `none-identified`, and `none-identified` itself will absorb signals that an honest analyst would call "examined and confirmed-as-R8-residual." Required revision:

- Add **`coverage-artifact`** (per SF-8 prescription, already lodged in horizon-signals).
- Add **`R8-residual-confirmed`** — a positive tag for intervals where the per-interval audit has examined and ruled out alternative explanations, distinct from `none-identified`'s passive-residual reading.

Six-tag set in TC-06 v0.2: `tenure-trend`, `succession-contested`, `coverage-gap`, `coverage-artifact`, `R8-residual-confirmed`, `none-identified`.

**Pre-declaration of per-interval tags: required.** Per-interval divergence-cause tag must be declared *before* the stationarity test result is examined for that interval. Deviation from the pre-declared tag requires Guardian re-authorisation. This is the load-bearing R4 discipline; without it, the tag set is decorative.

### Q4 — R8 closure call

**Modify Scout's call: R8 closure requires both TC-04 *and* TC-08, plus Guardian-pre-declared operational definition of "stable cross-channel calibration."** Scout's "post-TC-04" call addresses portability; TC-08 (defunct-archive paired-case) addresses survivor-vs-defunct robustness. Both are needed; either alone leaves a residual.

Operational definition of "stable cross-channel calibration" (binding for v0.2 §6):

1. **Channel-ratio bound.** The per-interval ratio between calendar-time and institution-internal-time channels, taken across all paired intervals in TC-04 and TC-08, varies by no more than a factor of 2 from its cross-case median.
2. **No tag-cluster dominance.** Neither `tenure-trend` nor `R8-residual-confirmed` is the modal divergence-cause tag in any single TC-04 case or in the TC-08 paired-case set; if either tag is modal, the R8 residual is not closed for that subset.
3. **Cross-form coverage.** At least one cross-institution case (TC-04) and at least one defunct-case (TC-08) have been characterised under the protocol without invoking weak-concordance (Q2(b) lower tier) as the modal verdict-issuance regime.

Until all three conditions hold, R8 status remains **procedurally-managed-but-live** as Scout determined; on satisfaction, R8 status moves to **closed-conditional-on-thresholds**, with the three thresholds themselves subject to Guardian re-authorisation if any TC-04 or TC-08 finding exposes their fragility.

**Cross-brief implication.** This ruling tightens the gating relationship between TC-08 and R8 closure. The pre-staged TC-08 Guardian R3 brief (RT-2026-004 provisional, drafted 2026-04-28) §1 should be updated to reflect that TC-08 is gating to R8 closure as well as R3 closure. Architect to revise pre-issuance.

### Q5 — Q-CP4 small-sample default

**Ruling: option (b), Guardian-modified — sample-size pre-rule with pre-registration fallback.** Pre-declare in TC-06 v0.2 §5 condition 1: n < 30 → exact permutation test against Poisson null (default, not analyst-discretional); n ≥ 30 → Anderson–Darling. Deviation from the size-rule requires written declaration *before data examination* and Guardian re-authorisation.

Analyst-declaration as drafted (option a) is the soft motte-and-bailey opportunity Architect flagged in the brief itself; pre-registration as the universal default (option c) is heavier than required. The size-rule pre-commits the test; pre-registration is reserved for the deviation case where the analyst has methodological reason to depart from default. This matches the structural logic of Q1 and Q2(a): pre-declaration of structure, with named override mechanism.

---

## Net-new R8-discipline risks

**SF-10 — Boundary-condition fragility.** Era-band boundaries (Q1), n-tier cutoffs (Q2(b)), and sample-size cutoffs (Q5) introduce step-function discontinuities. An analyst whose sample is n = 14 vs n = 15 picks different concordance rules; an interval at year 1099 vs year 1101 picks different effect-size floors and channel presumptions. This is a generic R8/R4 rescue surface across the v0.2 design.

Mitigation built into rulings above: Q1 boundary addendum (verdicts within ±25 yr of a band boundary reported under both adjacent rules); Q2(b) tier-overlap reporting; Q5 written-deviation requirement. **Verdict: lodge in horizon-signals as SF-10. Status: PROCEDURALLY-MITIGATED-IN-V0.2-DESIGN; LIVE pending v0.2 ratification.**

**Closure-condition gameability (Q4 thresholds).** The three thresholds in Q4's operational definition (factor of 2; tag-modality; weak-concordance modality) are themselves degrees of freedom. Architect to pre-declare numerically in TC-06 v0.2 §6; modification requires Guardian re-authorisation. **Verdict: ratified as TC-06 v0.2 procedural mitigation; not promoted to risk register; not horizon-signal-eligible (it is the closure mechanism's own internal threshold structure, not an external risk).**

---

## Citation-Violation flags

None raised in this review.

---

## Authorisation for TC-06 v0.2 drafting

**Architect may proceed to TC-06 v0.2** incorporating the Scout response (RT-2026-001) and this Guardian response (RT-2026-002), subject to the following design-coherence requirement:

- The era-stratification design (Q1) and the presumptive channel-dominance design (Q2(a)) must be co-designed, not designed independently. Band boundaries match across Q1 and Q2(a). The combined design lands in TC-06 v0.2 §4.2 + §5.
- The expanded six-tag set (Q3) and the sample-size pre-rule (Q5) must be cross-checked for consistency with TC-08 v0.2 once the TC-08 Guardian R3 review (RT-2026-004 pending) has issued its rulings. If consistency is unachievable, Architect issues a council deliberation request before TC-06 v0.2 is finalised.
- SF-10 procedural mitigations (Q1 ±25 yr addendum; Q2(b) tier-overlap reporting) are drafted into TC-06 v0.2 §5 conditions, not added as appendix.

No items require pre-v0.2 re-deliberation. RT-2026-002 is closed on response receipt.

---

*Guardian-stance memo. RT-2026-002 response. ~1180 words.*
