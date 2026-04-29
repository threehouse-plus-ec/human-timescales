# Review brief — Scout pass on TC-06 commensurability protocol v0.1

*Endorsement Marker (provisional). Internal scoping work, not a Coastline. No external endorsement is asserted.*

**Brief ID:** RT-2026-001
**Issued:** 2026-04-28
**Issuer:** Architect (drafter of the deliverable under review).
**Recipient stance:** Scout.
**Deliverable under review:** `docs/protocols/human-timescales-commensurability-protocol-v0.1.md` (TC-06).
**Companion deliverables (context, not under review here):** TC-07 reform-event sub-typing protocol v0.1; TC-08 defunct-archive feasibility memo v0.1.
**Due-by (recommended):** before TC-01 data-collection commencement; ideally Q2–Q3 2026 per the TC-06 card target.

---

## 1. Why Scout, why this card

Scout originated **R8 (temporal parallax)** as a horizon signal during the v0.1 review of the scoping document. R8 was promoted to a methodological constraint (E3) in v0.2 §5 M1, which in turn produced TC-06 as a binding gating prerequisite for TC-01.

TC-06's drafting under Architect stance has produced a candidate resolution (dual measurement, protocol (iii)). The question this brief asks is whether that resolution **actually closes R8**, or whether it nominally closes R8 while leaving the underlying horizon risk live.

This is Scout's specific jurisdiction: not the methodological soundness in isolation (that is Guardian's R8-discipline review pass) but the **cross-thread coupling and horizon-residual** check. Scout should not re-review what Architect has already decided; Scout should look for what Architect cannot see from the drafting position.

---

## 2. Questions

Five concrete questions. Each invites a verdict; "defer" is acceptable where the verdict requires data the protocol does not yet have.

### Q1. Does dual measurement actually resolve R8, or does it nominally close it?

The dual-measurement protocol computes calendar-time and institution-internal-time channels separately and reports divergence as data (TC-06 §3, §4.4). Scout's question: is reporting the divergence the same as resolving the temporal-parallax risk, or does it merely *render the risk visible*? If the latter, what additional discipline is needed before downstream stationarity claims can be issued?

A "yes — it resolves" verdict means the procedural visibility is enough. A "no — it surfaces but does not resolve" verdict obliges an additional protocol clause Scout should propose.

### Q2. Q-CP2 — should the third channel (administrative-time) be promoted now?

TC-06 §4.3 records liturgical / fiscal / administrative time variation as notes-only in v0.1 and holds promotion to a third channel in reserve, with promotion criterion "divergence concentrated at era boundaries that align with administrative-time discontinuities."

The protocol explicitly requests Scout review on whether to promote earlier — i.e., to install the third channel in v0.1 of the protocol so that TC-01 data extraction captures it from the start, rather than waiting for divergence evidence that may itself be biased by the channel's absence.

Scout's call: **promote now (yes/no)**, and if yes, what minimal third-channel specification suffices.

### Q3. Q-CP3 — does the 10%/century effect-size floor make horizon sense?

TC-06 §5 condition 5 sets a 10%-per-century effect-size floor (in slope of log-interval) below which non-rejection of stationarity counts as **inconclusive**, not stationary. Architect's justification: a 10%/century slope corresponds to roughly one L₅ generation of compression over the 16-century pilot window.

Scout's question: across the eras TC-01 will actually cover (Nicaea I 325 → Vatican II 1965), does this floor make sense uniformly, or are there sub-periods (e.g., medieval documentary gaps c. 700–1100; post-Reformation density acceleration) where the floor is differentially calibrated? If sub-period variation matters, Scout should propose either an era-stratified floor or a fixed defence of the uniform-floor choice.

(Architect invited Guardian veto on this number; Scout's input here is consultative, not decisional, but Scout's horizon view is the right view to produce it.)

### Q4. Cross-card coupling between TC-06 and TC-07

TC-06 §5 condition 4 requires **channel concordance** for any stationarity claim: rejection in one channel and non-rejection in the other yields a **divergent** verdict, not stationary. TC-07 §6 requires **strict multi-tagging** of reform events where evidence is positive.

Scout's question: do these two strictness choices interact in ways that produce systematic verdicts of "divergent" or "inconclusive" simply by accumulation of strictness, even when the underlying signal is genuinely stationary? Specifically: in the 8–12-event sub-type-stratified subsets that TC-07's multi-tagging will produce, does the channel-concordance test in TC-06 have enough power to escape default-inconclusive outcomes?

If yes (coupling produces over-inconclusiveness), Scout should propose either a power-floor modification to one of the protocols or an explicit acceptance that the v0.1 protocols err toward inconclusive verdicts as a deliberate methodological-conservatism choice.

### Q5. T10 portability of the institution-internal-time channel

TC-06 §4.2 generalises the institution-internal-time channel to T10 institutions via "charter revisions, executive-director appointments confirmed by the institution's own confirmation procedure, or equivalent." The protocol notes that the choice is per-T10-institution and is logged in the schema's `criterion_ref` field.

Scout's question: is the institution-internal-time channel actually portable to TC-04 (T10 archive characterisation), or does the absence of a single common authority-succession clock across IETF / W3C / ICANN make the channel effectively per-institution and non-comparable? If non-portable, this affects how TC-04's results can be aggregated and how TC-06 should be referenced from TC-04. Scout should give an early-warning verdict so TC-04 sequencing accommodates it.

---

## 3. Form of expected response

A short Scout-stance review memo, ~500–1000 words, lodged at `meta/review-tasks/tc06-scout-review-response-v0.1.md` (when ready). Structure:

- **Header.** Date; stance (Scout); brief ID being responded to (RT-2026-001).
- **Per-question verdicts.** Q1–Q5, one verdict each. Acceptable verdicts: *resolves* / *surfaces only* / *promote now* / *defer with named trigger* / *propose modification* / *consultative recommendation* / *defer to data*. One short paragraph per question explaining the verdict.
- **Net-new horizon signals.** Any horizon signals Scout raises during the review that are not currently in the programme's risk register or open questions. Each gets a label (e.g., "SF-8") and is flagged for Council deliberation.
- **Interaction with R8.** Explicit closure call: does R8 stay live as a horizon risk after TC-06 v0.1, become procedurally-managed-but-live, or close?

Scout is invited to be terse where terseness suffices. The review brief is asking for horizon-scanning judgement, not exhaustive coverage.

---

## 4. Out of scope for this brief

- Methodological soundness of the protocol *as a methodology* — that is Guardian's R8-discipline review pass (separate brief, not yet issued).
- Domain-consultant questions on Catholic-council source quality — that is the TC-07 review pass with a council-historiographer.
- Any modification to the 10%/century floor itself as a binding decision — Architect named that as a Guardian-veto target. Scout's input is consultative.

---

## 5. Document control

- **v0.1** (2026-04-28): Initial issuance under Architect stance, in response to user request to produce a clear Scout review task. Five questions tied to Scout's horizon-scanning role and prior horizon signals (R8, SF-7, the survivorship-bias signal). Q1 and Q5 are net-new questions for the protocol; Q2 and Q3 are explicitly invited by the protocol's own open-questions list (Q-CP2, Q-CP3); Q4 examines cross-card coupling that neither TC-06 nor TC-07 alone could address.

**Linked.** `docs/protocols/human-timescales-commensurability-protocol-v0.1.md` (TC-06, under review); `docs/protocols/human-timescales-reform-event-subtyping-protocol-v0.1.md` (TC-07, context); `docs/scoping/human-timescales-scoping-v0.2.md` §5 M1, R8, E3; `docs/task-cards/human-timescales-task-cards-v0.1.md` TC-06, TC-01, TC-04, TC-07.
