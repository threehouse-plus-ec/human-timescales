# Scout-stance review memo — TC-06 v0.1

*Endorsement Marker (provisional). Internal scoping work, not a Coastline. No external endorsement is asserted.*

**Date:** 2026-04-28  
**Stance:** Scout  
**Responding to brief:** RT-2026-001  
**Deliverable under review:** `docs/protocols/human-timescales-commensurability-protocol-v0.1.md` (TC-06)  

---

## Per-question verdicts

### Q1 — Does dual measurement resolve R8, or only surface it?
**Verdict: surfaces only.**

Protocol (iii) renders temporal-parallax divergence visible and tractable, but visibility is not resolution. The underlying risk — that calendar-year intervals are not commensurable constructs across eras — remains live because the protocol reports divergence without adjudicating which channel is "correct." A downstream stationarity claim that rests on calendar-time non-rejection while institution-internal-time rejects (or vice versa) is still exposed to R8; the protocol merely labels the exposure rather than removing it.

Additional discipline required before stationarity claims can be issued: every divergence-flagged interval must carry a *channel-dominance annotation* in the analytic memo — which channel is provisionally treated as authoritative for that interval, and why. Without this, TC-01 analysts will implicitly default to calendar time, re-importing the unexamined assumption the protocol was meant to discipline.

### Q2 — Q-CP2: promote the third (administrative-time) channel now?
**Verdict: promote now.**

The reserve criterion ("promote if divergence concentrated at era boundaries") is self-defeating: era-boundary divergence is exactly where administrative-time discontinuities are most likely to be load-bearing, and their absence from the measurement schema means the divergence evidence itself is biased toward false negatives. Waiting for the biased evidence to trigger promotion is a catch-22.

Minimal third-channel specification for v0.1: a binary `straddles_admin_boundary` flag per inter-event interval, plus an era-specific lookup table mapping fiscal/administrative year boundaries (Roman indiction, curial fiscal year, etc.) to the interval record. This is cheap to capture during TC-01 data extraction and expensive to reconstruct retrospectively.

### Q3 — Q-CP3: does the 10%/century effect-size floor make horizon sense?
**Verdict: consultative recommendation.**

The uniform floor is defensible as a first-order L₅ anchoring, but Scout's horizon view says it will mislead across the 16-century window. The medieval documentary gap (c. 700–1100) suppresses detectable trend power; the post-Reformation density acceleration inflates it. A single floor therefore applies differential methodological conservatism by era.

Consultative recommendation to Architect/Guardian: either (a) adopt a three-band era-stratified floor — late-antique/early-medieval (325–1100), high-medieval/early-modern (1100–1800), modern (1800–1965) — with band-specific slopes derived from the L₅ scale adjusted for documentary density; or (b) defend the uniform floor in writing with an explicit era-power audit. Absent either, the floor risks being read as precision it does not possess.

### Q4 — TC-06 × TC-07 cross-card coupling: systematic over-inconclusiveness?
**Verdict: propose modification.**

Yes. The interaction of TC-06 §5 condition 4 (channel concordance) with TC-07 §6 (strict multi-tagging) will systematically default to inconclusive or divergent verdicts on small sub-type-stratified subsets. With ~21 events total and multi-tagging distributing events across doctrinal / structural / disciplinary subsets, effective n per subset per channel falls to 8–12. At that scale, the concordance requirement is a power filter, not an evidentiary test.

Proposed modification: for sub-type subsets with n < 12, replace the strict concordance requirement with a *weak concordance* rule — non-rejection in at least one channel and no strong rejection (p < 0.01) in the other. This preserves methodological conservatism without making inconclusiveness the certain outcome of small strata. If Guardian rejects the weakening, the protocol should explicitly annotate that v0.1 errs toward inconclusive verdicts as a deliberate conservatism choice, so readers do not misread the pattern as empirical absence of stationarity.

### Q5 — T10 portability of the institution-internal-time channel
**Verdict: consultative recommendation.**

The channel is effectively per-institution and non-comparable across T10 institutions. "Charter revisions, executive-director appointments confirmed by the institution's own confirmation procedure, or equivalent" is too loose to yield a common dimension: IETF chair succession cycles, W3C director transitions, and ICANN board evolution are not the same construct, and their counts are not mutually commensurable. TC-06's generalisation to TC-04 therefore overstates portability.

Early-warning recommendation: TC-04 should treat institution-internal-time as three separate single-institution analyses, not as a cross-institution channel. TC-06 should add an explicit non-comparability annotation for TC-04, warning against aggregation of the institution-internal-time channel across T10 cases. If cross-T10 comparison is later desired, a fourth protocol iteration (or a TC-04-specific supplement) will be needed.

---

## Net-new horizon signals

**SF-8 — Coverage-correction divergence artifact.** If TC-01 applies coverage correction differently per channel (e.g., documentary-density proxies for calendar time, succession-completeness proxies for institution-internal time), channel divergence may be artifactual rather than substantive. Flagged for Guardian/Architect: require that coverage-correction methods be declared channel-explicit and that divergence-cause tags include `coverage-artifact` as a distinct category.

**SF-9 — Multi-tagging era-heterogeneity inflation.** Modern councils (Trent, Vatican I, Vatican II) have richer documentary records than early-medieval ones. Strict multi-tagging will therefore produce higher multi-tag rates in recent eras, creating era-correlated sub-type stratification that looks like temporal trend but is actually source-heterogeneity bias. Flagged for TC-07 review: inter-coder reliability should be tested with era-stratified samples, not only sub-type-stratified ones.

---

## Interaction with R8 — explicit closure call

**R8 status: procedurally-managed-but-live.**

Dual measurement does not close R8. It converts R8 from an unexamined assumption into an empirically reportable quantity, which is a significant methodological advance, but the temporal-parallax risk itself remains active wherever channels diverge. R8 closes only when a stable cross-channel calibration is demonstrated across at least two distinct institutional forms — i.e., after TC-04 results confirm that the dual-measurement pattern generalises beyond the papal-succession case. Until then, every stationarity claim issued under this protocol carries a live R8 residual that must be declared in the claim's annotation.

---

*Scout-stance memo. RT-2026-001 response. ~980 words.*
