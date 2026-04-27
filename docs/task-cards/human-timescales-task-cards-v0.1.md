# Human-System Timescales — Research Task Cards

**Version:** v0.1
**Stance:** Guardian (drafting); stance assignments embedded per card.
**Parent documents:** *Human-System Timescales: Scoping v0.2*; *T10 Mechanism-Conjecture Memo v0.1*.
**Date:** 2026-04-27

---

## 0. Card conventions

Each card is self-contained, independently executable to its specified completion, and explicitly cross-referenced. Card structure:

- **ID, Title, Type, Status**
- **Drafter / Reviewer stances**
- **Parent / Depends on / Feeds**
- **Deliverable** (what is produced)
- **Success criterion** (how done is recognised)
- **Falsification handle** (where applicable — what would weaken or kill the underlying claim)
- **Estimated scope**
- **Risks / open questions**

Statuses: PROPOSED · AUTHORISED · IN-PROGRESS · COMPLETE · BLOCKED · DEFERRED.

All cards inherit the §0a non-prescription clause and the T4 kill-criterion from v0.2.

---

## Critical-path overview

```
TC-06 ┐
TC-07 ├─→ TC-01 (Catholic councils M1 pilot) ┐
TC-08 ┘                                       ├─→ TC-09 (Breakwater ledger H₀+H₁+M)
TC-04 (T10 archive characterisation)  ────────┤
TC-05 (T2/SF-7 → L₅ mapping)  ────────────────┘

TC-02 (ICANN/IANA Sail)  ⟷ TC-03 (Vatican II Sail)   [either satisfies T4 kill-criterion]

TC-10 (Harbour latency protocol)        [independent]
TC-11 (Bibliography fill)               [independent]
```

Critical path to S2 deliverable (Breakwater ledger): **TC-06/07 → TC-01 → TC-09**, with TC-04 and TC-05 contributing in parallel.

---

## TC-01 — M1 Pilot: Catholic Ecumenical Councils Archaeology

**Type:** Empirical pilot (M1 method, v0.2 §5).
**Status:** PROPOSED.
**Drafter:** Architect (methodology) + domain consultant (Catholic council historiography).
**Reviewer:** Guardian (clarity / ethics) + Verifier (sources / grounding).

**Parent:** v0.2 §5 M1; §11 S3.
**Depends on:** TC-06 (commensurability protocol), TC-07 (reform-event sub-typing). TC-08 recommended in parallel.
**Feeds:** TC-09 (Breakwater ledger entry).

**Deliverable.** A pilot data file (CSV or equivalent) listing all 21 Catholic ecumenical councils (Nicaea I 325 → Vatican II 1962–65) with the following fields per event: dated start/end, sub-type classification (doctrinal / structural / disciplinary, per TC-07), preceding-event interval, external-shock context tag, documentary-ratification reference. Plus a short analytic memo applying the two null models from v0.2 §5 M1: (a) constant Poisson rate, (b) clustered events around external shocks. Plus an explicit cross-era commensurability protocol declaration (per TC-06).

**Success criterion.** Pilot data file complete; null-model tests executed; commensurability protocol declared in writing; sub-type-stratified results reported separately. Outcome reported in three forms: stationary (supports H₀), monotonically compressed (weakens H₀), shock-clustered (informs H₁).

**Falsification handle.** If the data show monotonic compression of inter-event intervals across centuries after coverage correction and under the declared commensurability protocol, H₀-L₅ is weakened.

**Target completion:** **2026-12-31** (binding per v0.2 M5).

**Estimated scope.** ~2 weeks of focused work assuming archival access; longer if primary-source verification of disputed dates is required for marginal events (e.g., Council of Sardica 343, Quinisext 692, recognition status of certain medieval councils).

**Risks / open questions.**
- Council of Pisa (1409) and other "councils" with contested ecumenical status: inclusion criterion must be declared.
- Sub-typing is not always clean (a single council can do doctrinal + disciplinary work). Multi-tag where needed; do not collapse.
- Coverage correction: medieval period has documentary gaps that may bias inter-event interval estimates.

---

## TC-02 — ICANN/IANA Pilot Sail (T4 kill-criterion candidate A)

**Type:** Sail essay; T4 kill-criterion candidate.
**Status:** PROPOSED.
**Drafter:** Author (UW) or technical-coordination domain consultant.
**Reviewer:** Guardian (T4 inflation risk) + Architect (causal-geometry mapping rigour).

**Parent:** T10 memo §10; v0.2 §6 (T4 Sail-status, kill-criterion installed).
**Depends on:** none.
**Feeds:** T4 kill-criterion decision; TC-09.

**Deliverable.** Short Sail essay (~3000–5000 words) applying ADM-EC causal-geometry vocabulary to the ICANN/IANA stewardship transition (1998–2016). Map L_source / L_apparatus / L_comparison onto generative event / deliberative body / horizon-of-validity. Quantify η_opt where data permit. Compare against what Olson (1982), North (1990), Mannheim (1928), and contemporary Internet-governance scholarship would predict for the same case.

**Success criterion.** The essay produces *at least one* prediction or distinction unavailable from the comparator frameworks. If yes: T4 survives, ADM-EC retains Sail status with the ICANN/IANA mapping as anchor. If no: T4 is dropped from the timescales programme (per v0.2 §6 kill-criterion).

**Falsification handle.** Self-applying. If the essay only re-describes what comparator frameworks already say, T4 dies cleanly. No rescue moves.

**Target completion:** Before TC-09 finalisation, ideally Q3 2026.

**Estimated scope.** ~1 week drafting + review cycle.

**Risks / open questions.**
- Sokal/Bricmont risk: importing physics vocabulary must yield real predictive distinction, not aesthetic re-labelling. Guardian R5 / R9 active.
- η_opt may not be operationalisable from public ICANN data; if so, the mapping itself becomes the prediction (architectural, not numerical).

---

## TC-03 — Vatican II Pilot Sail (T4 kill-criterion candidate B)

**Type:** Sail essay; T4 kill-criterion candidate.
**Status:** PROPOSED.
**Drafter:** Author (UW) or theological/ecclesial-history consultant.
**Reviewer:** Guardian + Architect.

**Parent:** v0.2 §6, §11 S5.
**Depends on:** none.
**Feeds:** T4 kill-criterion decision; TC-09.

**Deliverable.** Sail essay applying ADM-EC causal-geometry vocabulary to Vatican II (announced 1959, opened 1962, closed 1965, reception period 1965–~1985). Same structural ask as TC-02: map L_source / L_apparatus / L_comparison; produce a prediction or distinction unavailable from prior frameworks.

**Success criterion.** Same as TC-02. T4 needs *one* surviving anchor across TC-02 + TC-03; if both fail, T4 dies. If both succeed, the framework gains a temporally distant anchor pair (1962–65 ecclesial, 1998–2016 technical) — strong evidence for cross-domain mapping integrity.

**Falsification handle.** As TC-02.

**Target completion:** Parallel with TC-02.

**Estimated scope.** ~1 week + review.

**Risks / open questions.**
- Vatican II is theologically and politically charged; ethical sensitivity (R7) requires explicit non-prescriptive framing.
- "Reception period" extending to ~1985 is a contested historiographic boundary; declare the closure criterion explicitly.
- Drafting two parallel kill-criterion candidates is a structural hedge, not redundancy. Both running protects against either single case being non-decisive.

---

## TC-04 — T10 Archive Characterisation (3+ Institutions)

**Type:** Empirical pilot (M-Conjecture test).
**Status:** PROPOSED.
**Drafter:** Architect (methodology) + Internet-governance domain consultant.
**Reviewer:** Guardian + Verifier.

**Parent:** T10 memo §6, §8, §9.
**Depends on:** TC-02 informs methodology (recommended sequencing, not strict).
**Feeds:** TC-09; M-Conjecture falsification decision.

**Deliverable.** Layered characterisation of three or more T10 institutions, separating *technical-decision events* from *governance/legitimacy events*. Recommended set: IETF (RFC throughput per decade vs. IETF Administration LLC formation 2018 lead-up), W3C (specification cycle vs. 2023 reorganisation lead-up), ICANN (continuous IANA functions vs. 1998→2016 stewardship transition). Plus an optional fourth: IAU long-cycle technical-community case (2006 Pluto reclassification).

**Success criterion.** For each institution: (i) technical-layer cycle distribution measured and reported; (ii) governance-layer reform-event timeline characterised; (iii) layer separation explicit. Result classified as: M-Conjecture supported (technical fast, governance L₅-bound), M-Conjecture weakened (governance also fast), or mixed/inconclusive.

**Falsification handle.** F1 condition from T10 memo §9: *governance reform with broad multi-stakeholder legitimacy completed substantially below L₅ in a multi-domain-relevant institution.* One clean case is suggestive; pattern across three is decisive.

**Target completion:** **2027-06-30** (binding per T10 memo §9).

**Estimated scope.** ~3–4 weeks of focused work; major archives are public but require structured extraction.

**Risks / open questions.**
- Multi-domain-legitimacy assessment is itself contestable for ICANN; declare criterion in writing.
- W3C 2023 reorganisation: lead-up reportedly ~5 years of formal preparation. If confirmed, this sits below the lower L₅ edge and is informative either way (QM3 in T10 memo).
- IETF Administration LLC formation 2018: lead-up time is the data point, not the LLC creation itself.

---

## TC-05 — T2 / SF-7 → L₅ Mapping

**Type:** Cross-thread integration (existing dossier reanalysis).
**Status:** PROPOSED.
**Drafter:** Author (UW) — direct custodian of GLHC dossier.
**Reviewer:** Guardian (over-claiming risk).

**Parent:** v0.2 §11 S4; T2 thread.
**Depends on:** existing GLHC dossier; SF-7 stress-test results.
**Feeds:** TC-09.

**Deliverable.** Memo (~2000–3000 words) explicitly mapping the SF-7 custodial-attenuation envelope onto the L₅ legitimacy-transfer-generation definition. Determine: (a) does the existing 2–3 generation decay envelope correspond to L₅ legitimacy-transfer-generation, or to a different layer? (b) Is the existing tradition coverage sufficient, or does TC-05 identify the diversification gap (Architect M3: at least one non-artisanal, non-monastic tradition)?

**Success criterion.** Mapping declared in writing with explicit identification of correspondence or non-correspondence. Diversification gap stated if present, with named candidate traditions for future SF-7 application.

**Falsification handle.** If SF-7 envelope corresponds to L₃ or L₄ rather than L₅, the cross-instrument mutual reinforcement claim from v0.2 §6 weakens.

**Target completion:** Q3 2026 (parallel with TC-02/TC-03).

**Estimated scope.** ~3–5 days drafting from existing dossier.

**Risks / open questions.**
- Risk of forced fit: the existing dossier was not built with the L₅ definition in mind. The mapping must allow non-correspondence as an honest outcome.

---

## TC-06 — Cross-Era Commensurability Protocol

**Type:** Methodological infrastructure.
**Status:** IN-PROGRESS (deliverable v0.1 drafted 2026-04-27; awaiting Guardian + Scout review).
**Drafter:** Architect.
**Reviewer:** Guardian (R8 temporal-parallax discipline) + Scout.

**Deliverable location:** `docs/protocols/human-timescales-commensurability-protocol-v0.1.md`.

**Parent:** v0.2 §5 M1 (binding constraint, E3); R8.
**Depends on:** none.
**Feeds:** TC-01 (gating prerequisite); TC-04 (recommended).

**Deliverable.** A short methodological protocol (~1500 words) selecting and justifying one of the three candidate approaches in v0.2 §5 M1: (i) calendar-time only with construction-asymmetry acknowledgement, (ii) institution-internal time, (iii) dual measurement with divergence reporting. Or, if a fourth approach is identified, declared and defended.

**Success criterion.** Single chosen protocol declared in writing. Its handling of liturgical/fiscal/administrative time variation specified. Acceptance criteria for declaring a "stationary distribution" stated unambiguously.

**Falsification handle.** None (protocol is methodological, not empirical). However: any subsequent stationarity claim that does not declare its protocol is invalidated.

**Target completion:** Before TC-01 begins data collection. Ideally Q2–Q3 2026.

**Estimated scope.** ~3 days drafting + Council review.

**Risks / open questions.**
- Risk of selecting protocol (i) for convenience and importing measurement bias; protocol (iii) is methodologically safer but doubles workload.
- Recommendation (Guardian preference): adopt (iii) dual measurement; report both calendar-time and institution-internal-time stationarity separately. Do not aggregate.

---

## TC-07 — Reform-Event Sub-Typing Protocol

**Type:** Methodological infrastructure.
**Status:** PROPOSED.
**Drafter:** Architect.
**Reviewer:** Guardian + domain consultant for whichever archive is being studied.

**Parent:** v0.2 §5 M1; Architect M1 second bullet.
**Depends on:** none.
**Feeds:** TC-01 (gating prerequisite); TC-04 (recommended).

**Deliverable.** Operational definition of "reform event," with sub-typing into doctrinal / structural / disciplinary categories (or domain-equivalent for non-ecclesial archives). Inclusion criterion (what counts as a reform event vs. administrative adjustment vs. rebranding) declared. Multi-tagging procedure for events that fit multiple sub-types.

**Success criterion.** Protocol clear enough that two independent coders applying it to the same archive would agree on event inclusion and sub-typing in ≥80% of cases (operational benchmark, not statistical claim).

**Falsification handle.** None directly; failures here invalidate downstream stationarity claims.

**Target completion:** Before TC-01 begins. Ideally Q2 2026.

**Estimated scope.** ~2–3 days drafting; longer if pilot inter-coder reliability check is required.

**Risks / open questions.**
- Scout horizon signal 3: this is a Sail-effort-equivalent investment, not a footnote.
- Risk of over-narrow definition that excludes legitimate reform events; risk of over-broad definition that contaminates the archive with administrative noise.

---

## TC-08 — Defunct-Institution Archive Feasibility Check

**Type:** Survivorship-bias control.
**Status:** PROPOSED (recommended, not strictly binding).
**Drafter:** Author or historiographic consultant.
**Reviewer:** Guardian (R3 survivorship discipline).

**Parent:** v0.2 §5 M1 (Scout signal 2 / R3).
**Depends on:** none.
**Feeds:** TC-01 (in parallel; informs interpretation).

**Deliverable.** Short feasibility memo (~1500–2500 words) on reconstructing reform-cycle data from at least one defunct institutional archive. Primary candidate: Knights Templar (1119–1312), with substantial documentary trace including Papal bull *Vox in excelso* (1312). Secondary candidates: dissolved monastic orders with extant cartularies; failed corporations with documented restructuring histories. Memo identifies whether such reconstruction is feasible at the resolution required for null-model comparison.

**Success criterion.** Either: (i) feasibility confirmed, with at least one archive identified and characterised at the resolution needed for inter-event interval extraction; or (ii) feasibility declined, with explicit reasoning logged so the survivorship-bias risk (R3) is acknowledged but not pretended-away.

**Falsification handle.** N/A — this is a control measurement.

**Target completion:** Parallel with TC-01.

**Estimated scope.** ~1 week.

**Risks / open questions.**
- Templars are an over-determined case (papal suppression, political motive); may not represent generic dissolution dynamics. Diversify if feasible.
- Archive bias: dissolved institutions have asymmetric documentary survival depending on circumstance of dissolution.

---

## TC-09 — Breakwater Claim-Ledger Entry (Three-Claim Package)

**Type:** Breakwater ledger entry.
**Status:** PROPOSED.
**Drafter:** Council-3 joint (Guardian + Architect + Integrator).
**Reviewer:** Scout + Verifier flag pass.

**Parent:** v0.2 §5 M5, §11 S2; T10 memo §10.
**Depends on:** TC-01 (pilot data), TC-04 (T10 characterisation), TC-05 (SF-7 mapping). Partial completion of any subset acceptable for v0.1 of the entry; full ledger entry waits on all three.
**Feeds:** Permanent Breakwater archive.

**Deliverable.** Full Breakwater ledger entry following the v2.0 schema (claim → predictions → constraints → comparison → classification). Three-claim package:
- **Claim H₀:** Legitimacy-transfer-generation hypothesis.
- **Claim H₁:** Pressure corollary (second-order signatures).
- **Claim M:** Mechanism conjecture (technology acts on channels/stores, not on legitimacy-transfer, to first order on observed historical scales).

Each claim with its own predictions, discriminant condition, feasibility flag, and (default at ledger entry time) classification of UNDERDETERMINED.

**Success criterion.** Ledger entry meets v2.0 schema requirements. Self-reference exclusion respected. Discriminant conditions specified to the level that future evidence can change classification without rewriting the entry. Falsification timelines bound from TC-01 (2026-12-31) and TC-04 (2027-06-30) embedded.

**Falsification handle.** Each of the three claims has its own falsification handle, declared in the entry. The entry as artifact is not falsifiable; the claims it carries are.

**Target completion:** Initial ledger entry by Q4 2026 (after TC-01 pilot completion); revisions following TC-04 completion.

**Estimated scope.** ~1 week drafting + Council review cycle.

**Risks / open questions.**
- Three-claim packaging may obscure individual-claim falsification trajectories. Consider whether to file as one entry with three claims or three linked entries.
- Anti-aggregation discipline (Breakwater protocol): no claim's classification can be inferred from another's.

---

## TC-10 — Internal Harbour Latency-Tracking Protocol

**Type:** Methodological infrastructure (self-application).
**Status:** PROPOSED (Architect-recommended; Integrator decision pending per v0.2 §11 S7).
**Drafter:** Architect.
**Reviewer:** Guardian (non-feedback constraint).

**Parent:** v0.2 §6, §11 S7; Architect cross-cutting recommendation.
**Depends on:** none.
**Feeds:** Microscale calibration data for the timescales programme.

**Deliverable.** A protocol for recording latency between proposal-ledger entry and Council decision across multiple decisions in the Harbour itself. Specification of: events logged, time-stamps, no-feedback firewall (the data does not feed back into self-evaluation of Harbour pace).

**Success criterion.** Protocol drafted; firewall language explicit and Guardian-approved; one-month pilot logging period proposed before formal adoption.

**Falsification handle.** None at protocol level; the data eventually feeds tests of M-Conjecture in the participant-observer mode.

**Target completion:** Q3 2026 if authorised.

**Estimated scope.** ~2–3 days drafting + Council deliberation on adoption.

**Risks / open questions.**
- Self-evaluation drift: even with the firewall, the existence of latency tracking may bias Harbour pace toward the metric. Guardian reserves right to suspend the protocol if drift is observed.
- Integrator decision still required: this card is recommended, not yet authorised.

---

## TC-11 — Bibliography Fill: Contemporary Tenure-Trend Literature

**Type:** Auxiliary scholarship.
**Status:** PROPOSED.
**Drafter:** Author or research assistant.
**Reviewer:** Verifier.

**Parent:** v0.2 §12 (Architect bibliography gap).
**Depends on:** none.
**Feeds:** v0.3 bibliography; TC-09 evidentiary base.

**Deliverable.** Annotated bibliography (~10–15 sources) filling the Mannheim 1928 → present gap on generational replacement in organisations. Coverage: (i) demographic studies of CEO/legislator tenure trends; (ii) organisational ecology literature on founder effects and succession; (iii) at least one piece of contemporary empirical work on cohort-replacement timescales in scientific fields.

**Success criterion.** Bibliography assembled with annotations; ready for v0.3 §12 incorporation.

**Falsification handle.** N/A.

**Target completion:** Q3 2026.

**Estimated scope.** ~2–3 days.

**Risks / open questions.**
- Risk of selection bias in literature review; explicit search-strategy declaration recommended.

---

## Summary table

| ID | Title | Type | Target | Critical Path |
|---|---|---|---|---|
| TC-01 | Catholic councils M1 pilot | Empirical pilot | 2026-12-31 | ✓ |
| TC-02 | ICANN/IANA Sail | Sail essay (T4) | Q3 2026 | parallel |
| TC-03 | Vatican II Sail | Sail essay (T4) | Q3 2026 | parallel |
| TC-04 | T10 archive characterisation | Empirical pilot | 2027-06-30 | ✓ |
| TC-05 | T2/SF-7 → L₅ mapping | Cross-thread | Q3 2026 | feeds ledger |
| TC-06 | Commensurability protocol | Methodological | Q2–Q3 2026 | ✓ gates TC-01 |
| TC-07 | Reform-event sub-typing | Methodological | Q2 2026 | ✓ gates TC-01 |
| TC-08 | Defunct-archive feasibility | Survivorship control | Parallel TC-01 | recommended |
| TC-09 | Breakwater ledger entry | Ledger | Q4 2026, rev. 2027 | ✓ synthesis |
| TC-10 | Harbour latency protocol | Methodological | Q3 2026 if authorised | independent |
| TC-11 | Bibliography fill | Auxiliary | Q3 2026 | independent |

---

## Document control

- **v0.1** (2026-04-27): Initial card set drafted under Guardian invocation in response to user request to operationalise the research programme. Eleven cards covering empirical pilots (3), methodological infrastructure (3), cross-thread integration (1), survivorship control (1), synthesis (1), and auxiliary (2).
- **Pending:** Integrator authorisation per card; collaborator assignment for TC-01 (council historiography), TC-04 (Internet-governance), TC-05 (UW direct), TC-08 (historiographic).
- **Linked:** *Human-System Timescales: Scoping v0.2*; *T10 Mechanism-Conjecture Memo v0.1*.

**Stance log.** Drafted Guardian. Card structure follows discipline established in v0.2 (binding constraints, falsification handles, non-prescription clause inheritance). Recommended sequencing places methodological cards (TC-06/07) before empirical pilots; Sail essays (TC-02/03) parallel as kill-criterion hedge; ledger (TC-09) as synthesis. No Guardian veto issued. Integrator decisions required on per-card authorisation and on TC-10 adoption.
