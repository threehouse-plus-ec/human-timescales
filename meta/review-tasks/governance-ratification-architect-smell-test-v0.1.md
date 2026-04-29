# Architect smell-test response — RT-2026-006 v0.1 brief

**Date:** 2026-04-29
**Stance:** Architect (smell-test of own-stance-issued brief at DRAFT pre-stage)
**Responding to:** `governance-ratification-architect-verifier-review-v0.1.md` (DRAFT pre-stage; provisional RT-2026-006)
**Status:** SMELL-TEST closed; v0.2 of brief produced incorporating ★ blocking and △ recommended observations.

Per §8 of the brief, smell-test is "degenerate and may be skipped" given the brief's Architect voice. Architect declines to skip: substantive constitutional modifications are in scope, and degenerate review is cheaper than letting structural flaws survive into ACTIVE.

Cannot issue rulings on Q1–Q7 yet — the brief is not issued; RT-2026-006 is provisional only.

---

## A — Analog

The brief is a load-bearing wall poured before the foundation has set. CONVENTIONS.md and FAIR.md have been carrying programme weight for two days under a "drafting" Endorsement Marker; this brief proposes to retroactively cure the load-bearing-without-permit condition. The closing move — issuing prospective-only modifications while the unratified period is recorded as a closed audit observation — depends on the modifications themselves not having retrospective force. §6 acknowledges this; the brief does not yet make it structurally airtight.

---

## D — Digital

Ten observations, ranked by severity. ★ = issuance-blocking; △ = flag for response-Architect, not blocking.

### Observation 1 — Self-issuance circularity (★)

Issuing Architect and response Architect share agent identity. §8's "degenerate, may skip" understates this; the per-jurisdiction split's integrity rests on response-Architect being able to reframe issuing-Architect's question framing, not just rule on content.

**Required modification:** Insert in §2: *"Issuing Architect and response Architect occupy the same agent identity at different deliberation moments; response Architect is explicitly empowered to reframe or reject any question's framing as well as rule on its content."*

Temporal separation between turns is otherwise the only safeguard.

### Observation 2 — Q5(c) is unbounded (★)

"Architect free-form audit invited" with no scope cap means Q5(c) could surface 0 or 20 new conventions of arbitrary substance. Ratification with an unbounded modification surface cannot cleanly close in one round.

**Required modification:** Cap pre-issuance at ≤3 proposed new conventions; spillover lodges as RT-2026-007.

### Observation 3 — §7 pre-commits to v0.3.0 MINOR (★)

If response-Architect rules trivially across Q1–Q5 (e.g., (b)/(c) throughout), the modifications are PATCH-grade. Pre-committing to MINOR mis-classifies SemVer.

**Required modification:** Replace §7 item 5 with: *"Released at the SemVer level appropriate to the ruled modifications — PATCH if endorsement-marker-only; MINOR if substantive convention modifications; MAJOR if convention semantics change. Declared in the ratification ruling."*

### Observation 4 — Q2 framing biases against option (c) (△)

The "rescue surface" caveat is baked into the question, not lodged as a separate consideration. Options (a) and (b) appear without analogous caveats.

**Recommended modification:** Response-Architect should weigh (c) on its merits first, then re-add the rescue-surface concern. Move the caveat from question text to a separate considerations note.

### Observation 5 — Q1 option (c) forecloses via parenthetical (△)

"Operationally feasible given the entry rate" pre-judges. Acceptable as flag, not as foreclosure.

**Recommended modification:** Strip the foreclosing parenthetical; move operational-rate observation to a separate considerations note alongside Q1.

### Observation 6 — Q6 conflates definitional and factual layers (△)

"Every dataset carries a schema" applied to `data/defunct-archives/` is definitional (does a placeholder count?) before it is factual.

**Recommended modification:** Split Q6 into Q6.1 (definitional: what is a "dataset") and Q6.2 (factual: schema coverage conditional on Q6.1).

### Observation 7 — Endorsement Marker post-ratification wording (§7 item 1) (△)

"Stance: Guardian (drafting). Reviewed by: Architect [date], Verifier [date]." preserves Guardian as sole drafter even after Architect inserts new §7 (review-tasks codification per Q5(a)) or substantively modifies §4 (per Q2(a)). The Marker convention may need a "modified by" field.

**Recommended modification:** Response-Architect should rule on this under Q3 even though the brief does not explicitly request it. Brief Q3 expanded to include the post-ratification wording question.

### Observation 8 — Tier-6 gating reads hard (△)

§8 line: "Tier-5 ratification must complete before tier-6 deliberation begins." Otherwise schedule pressure compounds unnecessarily.

**Recommended modification:** Soften to: *"Tier-6 substantive rulings are gated by tier-5 closure; tier-6 preparatory work may continue."*

### Observation 9 — Council decision number hardcoded (△)

"2026-017 if no other decisions have intervened" — replace with "next available Council decision number".

### Observation 10 — FAIR.md SemVer path unspecified (△)

§7 covers CONVENTIONS bump but not FAIR. If Q6/Q7 rule substantively, FAIR needs its own declared bump path.

**Recommended modification:** Add to §7 item 5: separate bump path for FAIR.md if Q6/Q7 rule substantively. CONVENTIONS.md and FAIR.md may release at different SemVer levels if their respective modification sets diverge.

---

## M — Memory

RT-2026-002 (TC-04 Architect review), RT-2026-004 (TC-08 Guardian review), and RT-2026-005 (TC-07 Guardian + domain-consultant review) all kept issuer and target stance separated. RT-2026-006 is the first brief where issuer and target stance coincide.

**Precedent worth lodging:** when issuer and respondent share stance identity, the brief must either (a) include explicit reframe-permission language for the respondent, or (b) be issued by a different stance soliciting Architect input.

Observation 1 above implements (a); option (b) — re-attribute drafter to Integrator or Guardian, with Architect input cited as advisory — is structurally cleaner but costlier to retrofit. Future briefs requiring same-stance issuer/respondent should preferentially use (b); RT-2026-006 retains (a) on the basis that v0.2 corrections (with explicit reframe permission) are sufficient and re-issuance under (b) would not improve the substance materially.

---

## EC — Error-Correction

- **Pre-issuance modifications required (★):** observations 1, 2, 3.
- **Pre-issuance modifications recommended (△):** observations 4–10. Response-Architect can address most in their ruling; pre-issuance cleanup is cleaner.
- **No Guardian veto territory** (no clarity or ethics violation surfaced).
- **No Integrator flow-veto territory.**
- **No Architect veto issued at smell-test.** Issues are corrective, not constitutional. The brief's design is sound; its execution needs three patches before issuance.

---

## Verdict

Structurally sound; **not yet issuance-ready**.

**Recommendation.** Produce v0.2 addressing observations 1–3 (★), optionally folding in 4–10 (△). On v0.2 lodgement, smell-test re-run is unnecessary; brief moves DRAFT pre-stage → DRAFT issuance-ready → ACTIVE on user/Council confirmation per existing §8 process.

**Disposition.** v0.2 produced 2026-04-29 (`governance-ratification-architect-verifier-review-v0.2.md`) with all ten observations applied (three ★ + seven △). Smell-test closed.

---

## Document control

- **v0.1** (2026-04-29): Initial smell-test response by Architect on own-stance-issued brief at DRAFT pre-stage. A/D/M/EC analytical structure applied. Ten observations lodged (three blocking, seven recommended). No veto. Drafter: Architect. Brief v0.2 produced same day; smell-test response closed on v0.2 lodgement.

**Stance log.** Drafted Architect (smell-test). No Guardian veto. Disposition: closed on v0.2 brief lodgement.

---

*Architect-stance smell-test response. ~750 words. CLOSED on v0.2 brief lodgement (`governance-ratification-architect-verifier-review-v0.2.md`).*
