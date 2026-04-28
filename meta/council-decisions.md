# Council Decisions

Substantive decisions taken under Council-3 deliberation. Append-only.

**Document type:** Append-only tracker (governance record).
**Established:** 2026-04-27.
**Stance:** Guardian (custodial); each entry tagged with its issuing stance composition.
**Document control deviation.** This file operates as an append-only tracker rather than a versioned document. The history of entries is itself the change log; CONVENTIONS.md §3 doc-control fields (per-version, change log entries) do not apply per-entry. A formal §3 carve-out for tracker files is pending tier-5 governance review of CONVENTIONS.md (currently in Guardian-drafting stance, Architect/Verifier ratification pending).

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

## 2026-015

**Date:** 2026-04-28 (decision); 2026-04-28 (backfill entry).
**Stance composition:** Guardian (R8 temporal-parallax discipline + R4 motte-and-bailey cross-cutting); Architect (drafter of TC-06 v0.1, recipient); user as Integrator-of-record.
**Context:** Guardian-pass response to RT-2026-002 (TC-06 commensurability protocol v0.1, R8 review). Five per-question rulings + one net-new horizon signal. **Backfilled** to register: outcomes were durable (TC-06 v0.2 design, SF-10, R8 closure-condition tightening) but the response decision itself was not previously logged here.
**Decision:** (a) Q1 — adopt era-stratified three-band effect-size floor with Guardian-locked band boundaries (325–1100 / 1100–1800 / 1800–1965) and ±25 yr boundary addendum. (b) Q2(a) — presumptive channel-dominance by era band (calendar-time 325–1100; institution-internal 1100–1800; both co-authoritative 1800–1965); analyst override permitted with declared reason. (c) Q2(b) — replace Scout's binary n<12 cut-off with three-tier power rule (n<8 strict+inconclusive; 8≤n<15 weak concordance with mandatory MDE; n≥15 strict). (d) Q3 — tighten §6 procedural-falsification to invalidate nominal-invocation-with-condition-failure; expand divergence-cause tag set to six (`tenure-trend` / `succession-contested` / `coverage-gap` / `coverage-artifact` / `R8-residual-confirmed` / `none-identified`); pre-declaration of per-interval tags binding. (e) Q4 — R8 closure requires TC-04 *and* TC-08 plus three Guardian-pre-declared thresholds (factor-of-2 channel-ratio bound; no tag-cluster dominance; cross-form coverage). Until satisfied, R8 status is **procedurally-managed-but-live**. (f) Q5 — sample-size pre-rule for the Poisson-null test (n<30 exact permutation; n≥30 Anderson–Darling); deviation requires Guardian re-authorisation. (g) Lodge SF-10 (boundary-condition fragility) as horizon signal, status PROCEDURALLY-MITIGATED-IN-V0.2-DESIGN, LIVE pending v0.2 ratification.
**Justification:** Guardian rules from the position that R8 is closed only when temporal parallax has been operationally evicted, not merely surfaced. Each ruling closes a specific motte-and-bailey rescue surface: Q1 locks band boundaries to remove a degree of freedom; Q2(b) makes the small-n regime transparent rather than rescue-eligible; Q3 closes the nominal-invocation rescue route at the falsification layer; Q4 makes R8 closure conditional on operationally testable thresholds rather than declaration; Q5 pre-commits the test choice. The cross-binding to TC-08 (R8 closure requires TC-08, not just TC-04) tightens the gating relationship between the two task cards.
**Affected artifacts:** `meta/review-tasks/tc06-guardian-review-response-v0.1.md` (response document; RT-2026-002 status closed); `meta/review-tasks/README.md` (RT-2026-002 moved to closed); `meta/horizon-signals.md` (SF-10 lodged; R8 status updated); `meta/stance-log.md` (Guardian response entry); `docs/protocols/human-timescales-commensurability-protocol-v0.2.md` (subsequent integration of all five rulings); `meta/review-tasks/tc08-guardian-review-v0.1.md` (R8-closure-precondition cross-binding installed at brief stage per Q4 cross-brief implication); `logbook/2026-04/2026-04-28.md` (Guardian response session).

## 2026-016

**Date:** 2026-04-28 (decision); 2026-04-28 (backfill entry).
**Stance composition:** Guardian (R3 survivorship-bias discipline + R8-closure-precondition cross-binding scrutiny); Author (drafter of TC-08 v0.1, recipient); user as Integrator-of-record.
**Context:** Guardian-pass response to RT-2026-004 (TC-08 defunct-archive feasibility memo v0.1, R3 review with R8-closure-precondition cross-binding mandate per RT-2026-002 Q4). Five per-question rulings, one per-discipline split on Q2, and one net-new horizon signal. **Backfilled** to register: outcomes were durable (R3 first formal status update, SF-11, anchor-house feasibility blocker installed) but the response decision itself was not previously logged here.
**Decision:** (a) Q1 — joint-concordance requirement (no R3 finding from either case alone; logical AND between Templar and Dissolution-cohort) + pre-declared endogenous-vs-external-attack interpretive frame, declared before extraction. (b) Q2 per-discipline split — R3-discipline accepts pre-declared band-presumption override for Templar (papal-ratification dominant); R8-closure-precondition rules hard exclusion of Templar from R8-closure standing on the grounds that internal-channel documentary-survival suppression cannot satisfy the factor-of-2 threshold even under override. Consequence: TC-08's R8 contribution rests on Dissolution cohort alone. (c) Q3 — pre-declared interpretive rule on doctrinal absence: reportable as finding only when accompanied by positive structural-or-disciplinary-rate signal differing non-trivially from Poisson null and from Catholic-councils baseline; otherwise coverage gap. (d) Q4 — Guardian-specified alternative on Dissolution-cohort sampling: stratified-by-size design (4 large / 4 medium / 4 small by ≥1535 income), cohort minimum size = 12, order distribution as covariate (≥3 distinct orders), and binding n≥15 anchor-house clause (one large house with ≥15 documentable pre-Dissolution reform episodes); without anchor, threshold (iii) fails and TC-08 cannot contribute to R8 closure. (e) Q5 — R3 status is **procedurally-managed-but-live** (parallel to R8); R3 closure structure inherits from R8 with R3-tuned thresholds (rate-ratio bound; no rescue-by-relabelling modal pattern; cross-form coverage shared with R8). (f) Lodge SF-11 (meta-survivorship in candidate-set selection — documentary-survival pre-filter + historiographic-fashion pre-filter) as horizon signal, status PROCEDURALLY-MITIGATABLE-IN-V0.2, LIVE pending v0.2 mitigation.
**Justification:** Guardian rules from the position that R3 is closed only when survivor-vs-defunct comparison has been operationally executed, not when the absence of comparison has been declared in writing — the same surfacing-vs-resolving discipline applied to R8 in RT-2026-002. The per-discipline split on Q2 is structurally novel but methodologically defensible: R3 and R8-closure-precondition genuinely ask different questions about the Templar documentary-asymmetry case. The anchor-house clause on Q4 is load-bearing: without n≥15 anchor, the entire cohort runs in the weak-concordance band and threshold (iii) fails. R3 first formal status entry brings R3 into parity with R8 in the risk register, both now procedurally-managed-but-live with parallel closure-condition structures.
**Affected artifacts:** `meta/review-tasks/tc08-guardian-review-response-v0.1.md` (response document; RT-2026-004 status closed); `meta/review-tasks/README.md` (RT-2026-004 moved to closed); `meta/horizon-signals.md` (SF-11 lodged; R3 first formal status update); `meta/stance-log.md` (Guardian response entry); subsequent: `docs/memos/dissolution-cohort-anchor-house-feasibility-v0.1.md` (Q4 anchor-house feasibility check; verdict: Canterbury > Glastonbury); `meta/review-tasks/tc07-guardian-review-v0.1.md` (RT-2026-005 cross-binding to RT-2026-004 Q3 → Q4 installed at issuance per refinement 2.1); `logbook/2026-04/2026-04-28.md` (Guardian response session).

---

*Append below this line. Increment Decision ID yearly: 2026-NNN, 2027-NNN, ...*
