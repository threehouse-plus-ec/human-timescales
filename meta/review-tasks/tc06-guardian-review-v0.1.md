# Review brief — Guardian (R8) pass on TC-06 commensurability protocol v0.1

**Brief ID:** RT-2026-002
**Issued:** 2026-04-28
**Issuer:** Architect (drafter of the deliverable under review).
**Recipient stance:** Guardian (R8 temporal-parallax discipline).
**Deliverable under review:** `docs/protocols/human-timescales-commensurability-protocol-v0.1.md` (TC-06).
**Related prior review:** RT-2026-001 (Scout pass on TC-06), responded 2026-04-28 — `meta/review-tasks/tc06-scout-review-response-v0.1.md`. Scout response is **input** to this brief, not under review here.
**Companion deliverable for cross-card coupling:** `docs/protocols/human-timescales-reform-event-subtyping-protocol-v0.1.md` (TC-07).
**Due-by (recommended):** before TC-06 v0.2 revision; ideally Q2–Q3 2026 per the TC-06 card target.

---

## 1. Why Guardian, why this card, why now

The TC-06 card names Guardian alongside Scout as reviewer, with Guardian's specific jurisdiction being **R8 (temporal parallax) discipline**. R8 is Scout-originated but Guardian-disciplined: Scout flags horizon risks; Guardian rules on whether the methodology actually contains them or merely re-labels them.

Scout's pass (RT-2026-001) is now lodged. Scout deliberately deferred several questions to Guardian — Q3 (effect-size floor) is consultative-pending-Guardian; Q4 (cross-card coupling) proposes a modification that needs Guardian ratification; the R8 closure call ("procedurally-managed-but-live, post-TC-04") is Scout's recommendation but R8-discipline jurisdiction is Guardian's.

This brief asks Guardian to rule on those deferred items, and additionally to perform R8-discipline scrutiny that Scout's horizon-scanning role was not the right voice for. Architect is holding TC-06 v0.2 revision until both reviews land (council decision 2026-011(e)).

---

## 2. Questions

Five concrete questions. Each invites a binding ruling. "Defer" is acceptable only where the ruling depends on data the protocol does not yet have.

### Q1. Effect-size floor (Q-CP3) — binding decision

TC-06 §5 condition 5 sets a uniform 10%-per-century slope floor below which non-rejection of stationarity counts as **inconclusive**, not stationary. Architect's justification: corresponds roughly to one L₅ generation of compression over the 16-century pilot window. Architect explicitly invited Guardian veto on the threshold (Q-CP3 in TC-06 §7).

Scout's consultative recommendation: three-band era-stratified floor — late-antique/early-medieval (325–1100), high-medieval/early-modern (1100–1800), modern (1800–1965) — with band-specific slopes derived from the L₅ scale adjusted for documentary density. Or, if the uniform floor is retained, an explicit era-power audit defending why differential conservatism by era is acceptable.

**Ruling required.** Three options:

- (a) **Adopt era-stratified three-band floor** as Scout-recommended. Architect to draft the band-specific slopes under Guardian R8-discipline supervision in TC-06 v0.2.
- (b) **Retain uniform 10%/century floor**, with Architect required to draft a written era-power audit (in TC-06 v0.2 §5) defending the differential-conservatism-by-era acceptance.
- (c) **Modify both proposals** — Guardian proposes a third path (e.g., uniform floor with era-stratified power reporting, or two-band rather than three-band stratification).

The decision binds TC-06 v0.2 directly; it cannot be deferred to TC-01 analyst-time without re-importing the differential-conservatism risk Scout flagged.

### Q2. Channel-dominance discipline + Q4 cross-card coupling — combined ruling

Scout's two proposals at the verdict-issuance layer:

- **Channel-dominance annotation** (Q1 of Scout brief). Every divergent interval must carry an annotation in the analytic memo declaring which channel is provisionally treated as authoritative for that interval, and why. Without this, TC-01 analysts implicitly default to calendar time, re-importing the unexamined assumption R8 was meant to discipline.
- **Weak-concordance rule for n < 12 sub-type subsets** (Q4 of Scout brief). Strict channel-concordance (TC-06 §5 condition 4) combined with strict multi-tagging (TC-07 §6) systematically over-includes inconclusive verdicts on small subsets. Scout proposes: for n < 12, replace strict concordance with a **weak concordance** rule — non-rejection in at least one channel and no strong rejection (p < 0.01) in the other.

Both proposals bear directly on R8-discipline: the channel-dominance annotation prevents back-door temporal-parallax re-importation; the weak-concordance rule trades methodological conservatism for evidentiary tractability on small strata.

**Ruling required.** Three components, each independently rulable:

- (a) **Channel-dominance annotation: ratify, ratify-with-modification, or replace with stronger discipline** (e.g., presumptive channel by era band, where the era band defaults the dominance assignment unless analyst overrides with declared reason).
- (b) **Weak-concordance for n < 12: accept, reject (with strict concordance retained and explicit conservatism annotation), or propose alternative** (e.g., a tiered rule with three power bands rather than the n < 12 / n ≥ 12 binary).
- (c) **Boundary case treatment.** When Q2(a) and Q2(b) interact — e.g., channel-dominance is annotated *and* the verdict was issued under weak concordance — does Guardian require both annotations to appear in the analytic memo? (Architect's recommendation: yes; Guardian to ratify.)

### Q3. Procedural-falsification adequacy (§6) and motte-and-bailey audit (§4.4)

TC-06 §6 states the procedural-falsification: "any subsequent stationarity claim … that does not declare its protocol per this document … is invalidated." Guardian's R4 and R8 disciplines flag two questions:

- **Does §6 also invalidate claims that invoke the protocol but fail one of the six §5 acceptance conditions?** The current text reads as if no-declaration is the only invalidating failure. R4 motte-and-bailey discipline says scope-narrowing post-hoc is itself invalidating; the §5 acceptance conditions are the methodological scope, and a claim that fails them (e.g., an unstratified analysis presented as stationarity) should be procedurally invalidated regardless of whether the protocol was nominally invoked. Architect's recommendation: tighten §6 in TC-06 v0.2 to explicitly cover this case. Guardian to ratify or propose stronger language.

- **Motte-and-bailey audit of §4.4 divergence-cause tags.** The four divergence-cause tags (`tenure-trend`, `succession-contested`, `coverage-gap`, `none-identified`) could become rescue-by-relabelling moves under pressure: a stationarity claim weakened by divergence could be rescued by tagging the divergence as `tenure-trend` ("not a real signal, just internal-clock drift") rather than `none-identified` ("genuine R8 residual"). Guardian: audit whether the v0.1 tag set is sufficiently disciplined, and whether the eventual analytic memo should be required to declare the per-interval tag *before* the stationarity test result is examined, not after.

**Ruling required.** Tighten §6 (yes/no/specific revision); audit §4.4 tag discipline (yes/no/specific revision); rule on pre-declaration of divergence-cause tags.

### Q4. R8 closure call — ratify or modify

Scout's call: R8 status is **procedurally-managed-but-live**, closes only when stable cross-channel calibration is demonstrated across at least two distinct institutional forms (i.e., post-TC-04).

Guardian's R8-discipline jurisdiction means Guardian decides whether the closure-condition is sufficient. Two specific Guardian considerations:

- Should the closure-condition require *both* TC-04 (cross-institution at the technical-coordination layer) *and* TC-08 (defunct-archive paired-case)? TC-04 demonstrates portability; TC-08 demonstrates survivor-vs-defunct robustness. Scout's call addresses portability but not survivorship.
- Is "stable cross-channel calibration" operationally defined enough to be a closure-condition, or is it itself a methodological hand-wave that Guardian should sharpen before ratifying?

**Ruling required.** Ratify Scout's call as-is; modify to require TC-04 AND TC-08; or propose Guardian-specified operational definition of "stable cross-channel calibration."

### Q5. Q-CP4 small-sample default — binding decision

TC-06 §7 (Q-CP4) flags that the Anderson–Darling default in §5 condition 1 may be inappropriate for the n ≈ 21 Catholic-councils sample, and permits a small-sample alternative (exact permutation test against a Poisson null) "by declaration" of the TC-01 analyst.

Architect's intent: keep flexibility for the analyst. Guardian's R8-discipline lens may say differently: a per-analyst declaration is a soft motte-and-bailey opportunity (the analyst could pick the test that yields the desired verdict, or change tests retroactively).

**Ruling required.** Three options:

- (a) **Ratify analyst-declaration permission as-is** (Architect's intent).
- (b) **Pre-declare default by sample-size rule** (e.g., n < 30: exact permutation; n ≥ 30: Anderson–Darling; declared in TC-06 v0.2, not by analyst).
- (c) **Require pre-registration**: analyst declares chosen test in writing before seeing the data, with deviation requiring explicit Guardian re-authorisation.

---

## 3. Net-new R8 risks (catch-all)

Guardian is invited to surface any net-new R8-discipline risks not currently in the protocol's open questions, the Scout response, or the existing risk register R1–R10. Each surfaced risk gets an explicit verdict: lodge in horizon-signals (SF-NN); promote to risk register (R11+); or ratify TC-06 v0.2 procedural mitigation.

---

## 4. Form of expected response

A Guardian-stance review memo, ~500–1000 words, lodged at `meta/review-tasks/tc06-guardian-review-response-v0.1.md` (when ready). Structure:

- **Header.** Date; stance (Guardian); brief ID being responded to (RT-2026-002).
- **Per-question rulings.** Q1–Q5, one ruling each. Acceptable forms: explicit choice from the named options, or a Guardian-specified alternative with reasoning. One short paragraph per question.
- **Net-new R8-discipline risks** (§3 of this brief).
- **Citation-Violation flags** raised during the review, if any.
- **Authorisation for TC-06 v0.2 drafting.** Explicit: Architect may proceed to v0.2 revision incorporating both Scout's response (RT-2026-001) and this Guardian response, OR specific items must be re-deliberated before v0.2.

Guardian is invited to be terse where terseness suffices.

---

## 5. Out of scope for this brief

- Horizon-scanning beyond R8 — Scout's pass already completed.
- Domain-consultant questions on Catholic-council historiography — those belong to the TC-07 review (separate brief, not yet issued).
- TC-09 ledger-entry-readiness questions — premature; ledger entry depends on TC-01 / TC-04 results.
- TC-04 design implications — Q5 of Scout's brief and Q4 of this brief touch them, but full TC-04 design is its own future deliverable.

---

## 6. Document control

- **v0.1** (2026-04-28): Initial issuance under Architect stance, in response to user authorisation following Scout's RT-2026-001 response. Five binding-ruling questions plus net-new-risk catch-all. Q1 and Q5 are Architect-named Guardian-veto targets carried forward; Q2 consolidates Scout's Q1 and Q4 at the verdict-issuance layer; Q3 is Guardian's R4/R8-discipline audit of §6 and §4.4; Q4 ratifies or modifies Scout's R8 closure call. Scout response (RT-2026-001) is named as input.

**Linked.** `docs/protocols/human-timescales-commensurability-protocol-v0.1.md` (TC-06, under review); `docs/protocols/human-timescales-reform-event-subtyping-protocol-v0.1.md` (TC-07, cross-card coupling context); `meta/review-tasks/tc06-scout-review-v0.1.md` (RT-2026-001 brief); `meta/review-tasks/tc06-scout-review-response-v0.1.md` (RT-2026-001 response, input to this brief); `meta/horizon-signals.md` (SF-8, SF-9, R8 status); `docs/scoping/human-timescales-scoping-v0.2.md` §9 R4, R8; `docs/task-cards/human-timescales-task-cards-v0.1.md` TC-06.
