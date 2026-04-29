# Tier-6 substantive concerns — Council triage memo

*Endorsement Marker (provisional). Internal scoping work, not a Coastline. No external endorsement is asserted.*

**Date drafted:** 2026-04-29.
**Drafter:** Architect (surfacing audit observations for Council deliberation).
**Status:** DRAFT for Council triage.
**Source:** Consistency-audit second pass, "Methodological & Architectural Observations" section (2026-04-28); carried forward in CHANGELOG `[0.2.2]` Outstanding as tier-6.

---

## §1. Purpose

The audit surfaced three concerns that cannot be closed by documentation patching (tiers 1–4) and are not governance-rule questions (tier-5 RT-2026-006). Each is a substantive research-design concern affecting specific task cards. Council ruling required per concern: (i) is it real, (ii) what remedy mechanism applies, (iii) sequencing.

This memo surfaces the concerns and lays out remedy options. It does not propose remedies — that is Council's call.

---

## §2. Concern 1 — Inverse-R4 fragility (TC-06 × TC-07 × small-n coupling)

**The concern.** TC-07's strict multi-tagging combined with TC-06 v0.2's three-tier power rule (n<8 inconclusive default; 8≤n<15 weak concordance; n≥15 strict) may *procedurally guarantee* inconclusive verdicts on the M1 Catholic ecumenical councils archive (n≈21). Multi-tagging splits the 21 events into sub-type buckets that, conservatively, leave the largest single bucket (likely doctrinal) at n≈12–15 and structural / disciplinary sub-buckets below n=8. TC-01's central deliverable (sub-type-stratified stationarity verdicts) defaults to inconclusive *not because the data is inconclusive, but because the protocol stack guarantees it for n=21 populations*.

This is the inverse of R4: rather than rescuing a too-strong claim under pressure, the procedure mandates a too-weak verdict regardless of what the data says.

**Audit framing (paraphrased).** *Rigid sub-typing of a small finite population artificially shrinks n per bucket, practically guaranteeing 'inconclusive' as a procedural rather than empirical outcome.*

**Where it lives now.** RT-2026-005 §3 catch-all flags an "inverse-R4" risk and asks Guardian for a structured verdict (lodge as SF-12, promote to R11+, or ratify v0.2 procedural mitigation). Council should consider whether RT-2026-005's existing handling is sufficient.

**Remedy options.**
- **(a)** Trust RT-2026-005 §3 to handle this; close as audit-noted-but-already-in-process.
- **(b)** Lodge as SF-12 horizon signal — TC-06 × TC-07 cross-protocol coupling fragility for n<30 populations.
- **(c)** Promote to risk register as new structural R11+ entry; triggers TC-06 / TC-07 v0.3 revision.
- **(d)** Architect-led pre-extraction calibration memo: project realised n-per-bucket distribution under multi-tagging on the 21-council population with quantitative MDE projections, before TC-01 extraction begins.
- **(e)** Close as audit-noted-not-actionable (the inconclusive default *is* the protocol working as designed; conservatism is deliberate).

---

## §3. Concern 2 — R8 and R3 status thinness ("procedurally-managed-but-live")

**The concern.** R8 (temporal parallax) and R3 (survivorship bias) are currently parked as "procedurally-managed-but-live" with closure conditional on TC-04 + TC-08 joint completion plus three Guardian-pre-declared thresholds each (Council 2026-015, 2026-016). The parking position converts unexamined assumptions into reportable quantities — a methodological advance. But the audit observes that the underlying mitigations are thin in places:

- **R3 specifically.** The TC-08 defunct-archive memo acknowledges the Knights Templar dissolution was externally over-determined (papal suppression, political motive), not an endogenous reform-cycle terminus. Paired-case mitigation rests on Templar + English Dissolution cohort, but the Templar half is methodologically compromised. The Q2 per-discipline split (R3-discipline band-presumption override for Templar) acknowledges this — visibility without mathematical resolution.

**Audit framing (paraphrased).** *Relying on 'explicit declaration in the eventual TC-09 ledger entry' as mitigation renders the bias visible without resolving it. The residuals are unresolved methodological debt that compounds across downstream claims.*

**Remedy options.**
- **(a)** Close as audit-noted-but-already-in-process; the parking position is *the* point and the closure conditions are explicit.
- **(b)** Tighten R3: add a third paired case (e.g., dissolved Buddhist monastic lineage; dissolved trading-company corporate form) before TC-08 v0.2 §4.2 commitment. Architect drafts a pre-extraction triangulation memo.
- **(c)** Lodge SF-12+ horizon signal tracking residual-compounding across downstream claims (the residual is annotated per claim but never aggregated; SF surfaces this for periodic review).
- **(d)** Issue a Guardian R3-status review at TC-09 ledger-drafting time, with joint-concordance Templar + Dissolution findings in hand. Defers to a natural future Council moment.
- **(e)** Promote R3 to risk register above procedural status if no third paired case is feasibility-checked by Q3 2026.

---

## §4. Concern 3 — Pre-assignment dependency scoping (TC-05 GLHC-dossier precedent)

**The concern.** Council 2026-010 records that on 2026-04-27, the assigned drafter for TC-05 (T2/SF-7 → L₅ mapping) lacked access to the prerequisite GLHC dossier; TC-08 was substituted. TC-05 remains BLOCKED for the same reason. The same gap could repeat for any TC card with non-trivial data dependencies (TC-04 T10 archives, TC-08 v0.2 anchor-house material, TC-01 historiography access).

**Audit framing (paraphrased).** *The TC-05 pivot reveals a gap in Integrator-stance operational planning — task prerequisites and data accessibility were not verified before Author assignment. The Integrator stance lacks an operational checklist.*

**Remedy options.**
- **(a)** Add pre-assignment dependency-scoping to TC-card authorisation: each card's "Depends on" field must declare accessibility verified-by-Integrator before status moves PROPOSED → AUTHORISED. Codify in CONVENTIONS.md (cross-binds to RT-2026-006 Q5(c) "missing conventions").
- **(b)** One-time dependency-accessibility pass across the eleven TC cards as a memo deliverable; surfaces all currently-stalled-or-stallable cards.
- **(c)** Close as audit-noted-not-actionable: the TC-05 case was a one-off (UW-direct-custodian dependency), and the Council pivoted appropriately.
- **(d)** Combine (a) and (b): one-time accessibility pass surfaces current state; codification prevents recurrence.

---

## §5. Sequencing

Tier-5 ratification (RT-2026-006) precedes tier-6 — all tier-6 rulings are issued under conventions, which should be ratified first. Within tier-6: Concern 3 is cheap and prevents recurrence; Concern 1 gates TC-01 (target 2026-12-31); Concern 2 gates TC-09 ledger work (longer timeline). Suggested order: tier-5 → Concern 3 → Concern 1 → Concern 2.

---

## §6. Out of scope

- Hypotheses H₀, H₁, M-Conjecture (claim-substance, not audit-flagged).
- Empirical findings (none yet — pre-falsification phase).
- Sail kill-criterion viability (TC-02, TC-03) — author/drafter availability is a Concern 3 cross-bind, not a separate audit observation.

---

## §7. Document control

- **v0.1** (DRAFT for Council triage, 2026-04-29): Initial triage memo surfacing three methodological/architectural concerns from the consistency-audit second pass. Each concern paired with audit framing, remedy-mechanism options, and sequencing. Memo does not propose remedies; Council ruling required per concern.
- **Pending:** Council deliberation on remedy-mechanism selection. Downstream artefacts (per chosen mechanisms): Architect-led coordination memos, SF-12+ horizon-signal entries, R11+ risk-register promotions, or CONVENTIONS.md amendments.
- **Linked:** CHANGELOG.md `[0.2.2]` Outstanding (tier-6 framing); `meta/review-tasks/governance-ratification-architect-verifier-review-v0.1.md` (RT-2026-006, prerequisite); `meta/review-tasks/tc07-guardian-review-v0.1.md` §3 (RT-2026-005 inverse-R4 catch-all, cross-binds to Concern 1); Council decisions 2026-010 (TC-05 → TC-08 pivot, Concern 3 precedent), 2026-015 (R8 Q4 closure structure, Concern 2 context), 2026-016 (R3 Q5 closure structure, Concern 2 context).

**Stance log.** Drafted Architect on behalf of Council triage. No Guardian veto issued at draft. Integrator decision required on Council deliberation scheduling and remedy-mechanism selection per concern.

---

*Architect-stance triage memo. ~950 words. DRAFT for Council deliberation.*
