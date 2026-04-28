# Council Decisions

Substantive decisions taken under Council-3 deliberation. Append-only.

Format:
- **Decision ID:** YYYY-NNN
- **Date.**
- **Stance composition.** Which stances participated.
- **Context.** What triggered the decision.
- **Decision.** What was decided.
- **Justification.** Brief reasoning.
- **Affected artifacts.**

---

## 2026-001

**Date:** 2026-04-27.
**Stance composition:** Guardian (drafting); Scout, Architect, Integrator-voice (review).
**Context:** First scoping document for the human-timescales programme.
**Decision:** Adopt L₅ legitimacy-transfer-generation as the binding hypothesis, with multi-domain-legitimacy scope restriction. Reject "rarely" softening.
**Justification:** Architect's L₅ definition makes the hypothesis empirically operational. The "rarely" softening would undermine falsifiability.
**Affected artifacts:** `docs/scoping/human-timescales-scoping-v0.2.md` §1, §3.

## 2026-002

**Date:** 2026-04-27.
**Stance composition:** Guardian (recommendation); user as Integrator-of-record.
**Context:** Six binding edits E1–E6 emerging from v0.1 review.
**Decision:** Authorise v0.2 freeze with E1–E6 applied. Optional improvements (survivorship-bias control, Architect M3 diversification, Harbour latency protocol) recommended but not gated.
**Justification:** v0.1 review surfaced load-bearing structural improvements that should not be deferred.
**Affected artifacts:** `docs/scoping/human-timescales-scoping-v0.2.md`.

## 2026-003

**Date:** 2026-04-27.
**Stance composition:** Guardian (analysis); user as Integrator-of-record.
**Context:** Mechanism conjecture: technology operates on connectivity and reconciliation, not on legitimacy-transfer.
**Decision:** Adopt M-Conjecture with α-weakening ("to first order, on observed historical scales"). Reframe T10 from boundary case to mechanism evidence.
**Justification:** The strong "may only" form would collapse on a single counter-example. The α-weakened form preserves falsifiability and accommodates known excluded effects (lifespan extension, AI-mediated authority as live edge).
**Affected artifacts:** `docs/memos/t10-mechanism-conjecture-memo-v0.1.md`.

## 2026-004

**Date:** 2026-04-27.
**Stance composition:** Guardian (request); user as Integrator-of-record.
**Context:** Sequencing decision: S2 (Breakwater ledger) vs. S6 (T10 memo).
**Decision:** Promote S6 ahead of S2. Draft the T10 memo before the Breakwater ledger entry, so the mechanism conjecture can join the ledger as a third claim.
**Justification:** The mechanism conjecture, if it survives T10 archive examination, is more theoretically valuable than the ledger entry it would feed. Drafting the ledger first would either omit M or speculate on it.
**Affected artifacts:** `docs/memos/t10-mechanism-conjecture-memo-v0.1.md`; future TC-09.

## 2026-005

**Date:** 2026-04-27.
**Stance composition:** Guardian (proposal); user as Integrator-of-record.
**Context:** Operationalising the programme.
**Decision:** Authorise drafting of eleven task cards (TC-01 through TC-11), covering empirical pilots, methodological infrastructure, synthesis, and auxiliary work. Per-card authorisation deferred.
**Justification:** Task cards make the programme legible and assignable; without them, the scoping document remains aspirational.
**Affected artifacts:** `docs/task-cards/human-timescales-task-cards-v0.1.md`.

## 2026-006

**Date:** 2026-04-27.
**Stance composition:** Guardian (proposal); user as Integrator-of-record.
**Context:** Repository structure and FAIR discipline.
**Decision:** Set up Open-Science Harbour-style repository structure with FAIR principles woven in as operational checklists (per-commit, per-release). Three-licence split (CC BY 4.0 / Apache 2.0 / CC0).
**Justification:** Without operational FAIR discipline, the programme accumulates tacit knowledge that defeats reuse. Without a proper repository, the artifacts cannot be cited or archived to Zenodo.
**Affected artifacts:** Entire repository structure.

## 2026-007

**Date:** 2026-04-27.
**Stance composition:** Architect (drafting); user as Integrator-of-record (authorisation issued via "go" on Guardian's TC-06 next-step recommendation).
**Context:** TC-06 (cross-era commensurability protocol) authorisation and protocol selection.
**Decision:** (a) Authorise TC-06 deliverable drafting and move card status PROPOSED → IN-PROGRESS. (b) Adopt dual-measurement protocol (iii) — calendar-time + institution-internal-time channels, divergence reported as data — per Guardian-preferred option on the TC-06 card. (c) Establish `docs/protocols/` as a peer subdirectory to `docs/memos/` to house TC-06, and prospectively TC-07 and TC-10 deliverables.
**Justification:** Protocol (iii) is the only one of the three candidates that allows R8 (temporal parallax) to be empirically interrogated rather than assumed away. Doubled workload is acceptable cost; the alternative (i or ii) cannot distinguish stationarity from time-construction asymmetry. The new `protocols/` directory cleanly separates binding operational rules from analytical exploration (memos), preventing the protocol from being mistaken for a memo or a sail.
**Affected artifacts:** `docs/protocols/human-timescales-commensurability-protocol-v0.1.md` (created); `docs/protocols/README.md` (created); `docs/task-cards/human-timescales-task-cards-v0.1.md` (TC-06 status updated); `docs/README.md`, `README.md` (subdirectory map updated).

## 2026-008

**Date:** 2026-04-27.
**Stance composition:** Architect (drafting); user as Integrator-of-record (authorisation issued via "yes" to commit-and-continue offer).
**Context:** TC-07 (reform-event sub-typing protocol) authorisation, immediately after TC-06 commit.
**Decision:** (a) Authorise TC-07 deliverable drafting and move card status PROPOSED → IN-PROGRESS. (b) Adopt strict inclusion (three necessary conditions, all required: documentary ratification, structural change in decision rights or membership rules, multi-domain-legitimacy applicability). (c) Adopt strict multi-tagging (multi-tag where evidence is positive; predominance-based single-tagging forbidden in v0.1). (d) Set ≥80% raw inter-coder agreement on both inclusion and sub-typing as the operational benchmark, with Cohen's κ ≥ 0.6 as supplementary check.
**Justification:** Inclusion-strict + sub-typing-permissive (within the included set) trades event count for inter-coder reliability. The trade is deliberate: TC-01's value rests on sub-type-stratified results being reproducible across coders, not on a maximal event count. Predominance-based single-tagging would defeat reliability, since "predominant character" is precisely where coders disagree.
**Affected artifacts:** `docs/protocols/human-timescales-reform-event-subtyping-protocol-v0.1.md` (created); `docs/protocols/README.md` (updated); `docs/task-cards/human-timescales-task-cards-v0.1.md` (TC-07 status updated).

## 2026-009

**Date:** 2026-04-27.
**Stance composition:** Author (drafting); user as Integrator-of-record (authorisation issued via "go" continuation after TC-07 commit).
**Context:** TC-11 (bibliography fill: contemporary tenure-trend literature) authorisation, in parallel with the gating prerequisites already drafted, since TC-11 is independent of the critical path and unblocks v0.3 §12 work.
**Decision:** (a) Authorise TC-11 deliverable drafting and move card status PROPOSED → IN-PROGRESS. (b) Lodge the deliverable in `docs/memos/` as a working memo (not a protocol), since it carries annotations that argue rather than operational rules. (c) Adopt explicit Verifier-pass discipline: post-1980 citations spot-verified via web search at drafting time; pre-1980 canonical citations lodged for Verifier confirmation. (d) Acknowledge four named coverage gaps in the v0.1 fill (post-2015 contemporary empirical, religious-order succession, AI-mediated coordination, comparative-international) with Verifier mandate to close them in v0.2.
**Justification:** Citation fabrication is a known LLM-failure mode; the search-strategy declaration and explicit Verifier-pending status protect the programme's source-verification discipline. Lodging in `docs/memos/` (not a new directory) avoids structural over-engineering for a single document; the memo discipline accommodates focused investigations that argue, which is what annotated entries do.
**Affected artifacts:** `docs/memos/bibliography-fill-tenure-trends-memo-v0.1.md` (created); `docs/memos/README.md` (updated); `docs/task-cards/human-timescales-task-cards-v0.1.md` (TC-11 status updated).

## 2026-010

**Date:** 2026-04-27.
**Stance composition:** Author (drafting); user as Integrator-of-record (authorisation issued via "as you suggest" on Guardian's TC-05 → TC-08 pivot recommendation, after TC-05 was identified as drafter-blocked due to dependency on the GLHC dossier).
**Context:** TC-08 (defunct-institution archive feasibility check) authorisation, in lieu of TC-05 which depends on dossier material the drafting agent does not have access to. TC-08 was drafter-feasible because the Templar archive and the English Dissolution archive are publicly documented.
**Decision:** (a) Authorise TC-08 deliverable drafting and move card status PROPOSED → IN-PROGRESS. (b) Adopt paired-case approach: Knights Templar (1119–1312) as primary defunct-archive case, English Dissolution monastic cohort (1536–1541) as secondary, with cohort-level rather than singleton-Glastonbury analysis preferred. (c) Decline Society of Jesus as a defunct-archive case on the grounds that the Order survived in Russia and Prussia during 1773–1814 suppression and is therefore not in fact defunct. (d) Decline failed corporations as defunct-archive cases on the grounds that they are out of H₀ multi-domain-legitimacy scope. (e) Refuse to draft TC-05 in this session because the drafter is named as UW-direct-custodian and the deliverable depends on the GLHC dossier, which the drafting agent cannot fabricate without violating the card's explicit forced-fit risk note.
**Justification:** R3 survivorship-bias control requires *paired* defunct-case analysis to triangulate dissolution dynamics. Singleton Templar analysis is vulnerable to over-determination of the 1307–1312 dissolution; cohort-level Dissolution analysis is vulnerable to externally-imposed dissolution but offers the unique benefit of within-cohort documentary-survival heterogeneity. The pairing addresses both vulnerabilities.
**Affected artifacts:** `docs/memos/defunct-archive-feasibility-memo-v0.1.md` (created); `docs/memos/README.md` (updated); `docs/task-cards/human-timescales-task-cards-v0.1.md` (TC-08 status updated).

## 2026-011

**Date:** 2026-04-28.
**Stance composition:** Architect (issuance of brief); Scout (response); user as Integrator-of-record.
**Context:** Scout-pass review of TC-06 commensurability protocol v0.1 (RT-2026-001). Response lodged with five verdicts and two net-new horizon signals.
**Decision:** (a) Establish `meta/review-tasks/` as the directory housing stance-specific review briefs and responses. (b) Establish `meta/horizon-signals.md` as the durable register for Scout-flagged horizon signals (SF-NNN) and risk-register status updates emerging from review passes; distinct from `falsification-tracker.md` (formal handles) and from inline scoping-document risk register. (c) Lodge SF-8 (coverage-correction divergence artifact) and SF-9 (multi-tagging era-heterogeneity inflation) as LIVE horizon signals. (d) Update R8 status in the horizon-signals register to **procedurally-managed-but-live**, with binding effect: every stationarity claim issued under TC-06 must annotate the R8 residual until cross-channel calibration is demonstrated post-TC-04. (e) Hold TC-06 v0.2 revision until the Guardian R8 review pass also lands, so Q1/Q2/Q4 modifications can be incorporated in a single revision pass with both reviewers' inputs.
**Justification:** Scout's response is consequential and surfaces issues that neither Architect (drafter) nor Guardian (R8 discipline reviewer alone) could see — particularly Q4 (TC-06 × TC-07 cross-card coupling) and the SF-8/SF-9 horizon signals. Lodging the signals durably prevents drift; holding TC-06 v0.2 until Guardian's parallel pass lands prevents revision churn.
**Affected artifacts:** `meta/review-tasks/README.md`, `meta/review-tasks/tc06-scout-review-v0.1.md`, `meta/review-tasks/tc06-scout-review-response-v0.1.md`; `meta/horizon-signals.md` (created); `meta/README.md` (updated); `meta/stance-log.md` (Scout entry); `logbook/2026-04/2026-04-28.md` (Scout response session).

## 2026-012

**Date:** 2026-04-28.
**Stance composition:** Verifier (response to brief); Author (drafter of TC-11); user as Integrator-of-record.
**Context:** Verifier-pass response to RT-2026-003 (TC-11 bibliography fill memo v0.1). Response lodged with full citation/page-level confirmation, twelve new sources closing four named gaps, three search-protocol tightenings, and a binding methodological demotion of practitioner source [12].
**Decision:** (a) Adopt the Verifier ruling: Spencer Stuart [12] is demoted from H₁ second-order-signature anchor to descriptive-practitioner status. In TC-11 v0.2 and onwards, [12] documents current levels/patterns only; any H₁ second-order claim (variance growth, kurtosis, reversal frequency) must be anchored in academic series (Kaplan & Minton; Russell Reynolds [A3]; CEO-effect variance studies) with [12] as triangulating point. Where memo v0.1 currently treats [12] as evidence for H₁, v0.2 either softens to "prima facie consistent with" or moves the point into a demarcated practitioner-insight box. (b) Adopt three search-protocol tightenings as binding for TC-11 v0.2 and any future bibliography work: inverse-citation sweeps for anchor articles; non-English (German + French) search round on institutional-longevity and parliamentary-tenure literatures; hostile-to-thesis band requirement (sources arguing against growing tenure volatility or against AI-induced coordination brittleness). (c) Adopt Q-BF1 ratification with tightening (practitioner sources permitted where peer-reviewed not available, subject to Verifier-level methods check, never as sole anchor for hypothesis-bearing claims). (d) Adopt Q-BF2 ruling: v0.3 §12 incorporation is not blocked by cohort-replacement-in-science thinness; flag v0.2.1 follow-up task to add at least one source on cohort effects in mathematics or theoretical physics. (e) Adopt Q-BF3 ruling: comparative-historical band closed by Verifier without dedicated domain consultant for §12 level. (f) Authorise TC-11 v0.2 drafting incorporating §1 confirmations, §2 page-level anchors, §3 twelve new sources, §4 policy rulings, §5 selection-bias tightenings and [12] demotion.
**Justification:** Verifier-pass discipline is the named source-verification stance; the demotion of [12] is a methodological-rigour move that protects FH-005-adjacent claims from over-attribution to a single practitioner source. The three search-protocol tightenings address selection-bias risk that the v0.1 search strategy did not fully cover, especially the Western-centric default and the absence of explicit hostile-to-thesis sourcing. v0.3 §12 incorporation remains a separate Council-decision moment downstream of TC-11 v0.2.
**Affected artifacts:** `meta/review-tasks/tc11-verifier-review-v0.1.md` (RT-2026-003 brief, status now closed); `meta/review-tasks/tc11-verifier-review-response-v0.1.md` (created); `meta/review-tasks/README.md` (RT-2026-003 moved to closed); `meta/stance-log.md` (Verifier entry); `logbook/2026-04/2026-04-28.md` (Verifier response session); pending: `docs/memos/bibliography-fill-tenure-trends-memo-v0.2.md` (TC-11 v0.2 drafting authorised).

## 2026-013

**Date:** 2026-04-28.
**Stance composition:** Architect (issuance + refinement application); user as Integrator-of-record (authorisation issued via "go" on Architect's three-item smell-test recommendation: keep Q2(d), apply refinements 2.1 + 2.2, issue now rather than hold for TC-04).
**Context:** RT-2026-004 (Guardian R3 review on TC-08 with cross-binding R8-closure-precondition mandate) issuance. Brief had been pre-staged 2026-04-28 awaiting RT-2026-002 verdicts (which closed earlier same day) and Architect smell-test.
**Decision:** (a) Issue RT-2026-004 to Guardian R3 review queue 2026-04-28. (b) Apply refinement 2.1 at issuance: §1 threshold (ii) → Q3 mapping made explicit, naming the `R8-residual-confirmed` tag as the interpretation pathway by which a ratified absence-as-finding ruling can land Templar intervals on a modality-forbidding tag and expose threshold (ii). (c) Apply refinement 2.2 at issuance: §1 threshold (iii) bite description expanded to note Templar n=7–8 straddles the n<8 / 8≤n<15 boundary itself (SF-10 boundary-fragility case applied to TC-08), tightening the small-n power floor argument and pre-empting any Guardian objection that the entire-paired-case-set claim assumes Templar n=8. (d) Retain Q2 four-option structure including (d) declared per-discipline split: the §1 cross-binding mandate authorises such splits where R3-discipline and R8-closure-precondition diverge on the same TC-08 design choice; striking (d) would contradict the §1 framing. (e) Issue now rather than hold for TC-04 design: TC-08's critical-path role (informs TC-01 by 2026-12-31) outranks TC-04 simultaneity benefit; Guardian can rule conditionally on Q4 sub-questions where TC-04 design genuinely matters, with named-trigger deferrals where the abstract ruling is genuinely impossible.
**Justification:** The two refinements are clarity wins, not substantive changes; applying them at issuance avoids a v0.1.1 cycle. Q2(d) retention preserves the §1 cross-binding mandate's explicit permission for per-discipline rulings, which is structurally novel but methodologically defensible (R3 and R8-closure-precondition genuinely ask different questions on the Templar documentary-asymmetry case). Holding for TC-04 design would invert the critical-path dependency: TC-04 is a 3–4 week deliverable not yet drafted; TC-08 informs TC-01's 2026-12-31 target; serialising would push TC-08 past TC-01's deadline.
**Affected artifacts:** `meta/review-tasks/tc08-guardian-review-v0.1.md` (status moved DRAFT pre-stage → ACTIVE issued; document control v0.1 (issued) entry appended; refinements 2.1 and 2.2 applied to §1); `meta/review-tasks/README.md` (RT-2026-004 moved from pending to active; pending list now contains TC-07 Guardian + domain-consultant only); `meta/stance-log.md` (Architect issuance entry); `logbook/2026-04/2026-04-28.md` (RT-2026-004 issuance session).

## 2026-014

**Date:** 2026-04-28.
**Stance composition:** Architect (smell-test + issuance); user as Integrator-of-record (authorisation issued via "go for Architect smell-test on RT-2026-005 and stage issuance").
**Context:** RT-2026-005 (Guardian R3+R4 + domain-consultant review on TC-07 reform-event sub-typing protocol v0.1) issuance. Brief had been pre-staged earlier same day awaiting Architect smell-test and named-domain-consultant identification.
**Decision:** (a) Issue RT-2026-005 to Guardian R3+R4 review queue 2026-04-28. (b) Apply refinement 2.1 at issuance: §1 cross-binding mandate map extended to include RT-2026-004 Q3 → Q4 binding, since the pre-declared-interpretive-rule structure (Q3 of RT-2026-004's ruling on doctrinal absence) carries over to TC-07 inclusion-test ambiguity (Constance Haec sancta and other boundary cases) — proceduralisation rather than case-by-case judgement preserves the methodological-conservatism gradient. (c) Apply refinement 2.2 at issuance: Q4 prompts expanded to include Trent (1545–1563) as the canonical multi-session × multi-tagging × multi-decade test case. Trent fills the chronological gap between the Constance (1414–1418) and Vatican II (1962–1965) prompts; its eighteen-year run with three convocations under multiple popes exercises Q1's multi-session ruling on the longest council in the canonical 21; doctrinal canons (justification, sacraments) and disciplinary canons (residence, formation, seminaries) are textually distinct in the council acts, making Trent the canonical multi-tagging stress test. (d) Retain Q1, Q2, Q3, Q5 as written; retain §3 inverse-R4 catch-all in catch-all position with structured Guardian-verdict requirement (lodge as SF-12, promote to R11+, or ratify v0.2 procedural mitigation). (e) Defer named-domain-consultant identification as a v0.2 follow-up rather than pre-issuance blocker: Guardian-primary questions (Q2/Q3/Q5) do not require domain-consultant participation; historiographic-interpretation questions (Q1/Q4) can receive provisional Guardian-only response with domain-consultant addendum once engaged.
**Justification:** The two refinements are clarity wins, not substantive changes; applying them at issuance avoids a v0.1.1 cycle. Q4 without Trent would leave the canonical multi-session × multi-tagging stress case unprobed; the chronological gap between Constance and Vatican II would silently signal that no medieval-to-early-modern multi-session test case mattered. RT-2026-004 Q3 → Q4 cross-binding extension closes a real interpretive-rule consistency gap: ruling Constance Haec sancta case-by-case rather than via pre-declared rule would re-open the very rescue-by-relabelling surface that RT-2026-004 Q3 was installed to close. Deferring named-domain-consultant identification (rather than holding) preserves review-system progress while domain-consultant engagement proceeds in parallel.
**Affected artifacts:** `meta/review-tasks/tc07-guardian-review-v0.1.md` (status moved DRAFT pre-stage → ACTIVE issued; document control v0.1 (issued) entry appended; refinements 2.1 and 2.2 applied to §1 cross-binding mandate map and Q4 prompts); `meta/review-tasks/README.md` (RT-2026-005 moved from pending to active; pending list now empty — review-brief queue fully populated); `meta/stance-log.md` (Architect issuance entry); `logbook/2026-04/2026-04-28.md` (RT-2026-005 issuance session).

---

*Append below this line. Increment Decision ID yearly: 2026-NNN, 2027-NNN, ...*
