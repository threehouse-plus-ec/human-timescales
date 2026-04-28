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

---

*Append below this line. Increment Decision ID yearly: 2026-NNN, 2027-NNN, ...*
