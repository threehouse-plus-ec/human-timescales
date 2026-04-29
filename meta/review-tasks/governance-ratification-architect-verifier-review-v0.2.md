# Architect + Verifier review brief — CONVENTIONS.md + FAIR.md ratification

**Status:** DRAFT issuance-ready (provisional RT-2026-006).
**Date drafted:** 2026-04-29 (v0.2 revision applying Architect smell-test corrections).
**Predecessor:** `governance-ratification-architect-verifier-review-v0.1.md` (DRAFT pre-stage; smell-tested 2026-04-29).
**Drafter:** Architect (issuing brief on behalf of Council); user as Integrator-of-record for issuance.
**Target stances:** Architect (methodological-rigour, internal coherence) and Verifier (source-grounding, external-standards compliance). Per-jurisdiction split permitted on questions where one stance's verdict is independent of the other.
**Documents under review:**
- `CONVENTIONS.md` (current state: in-tree as of commit `41d8169`, v0.2.2).
- `FAIR.md` (current state: in-tree as of commit `41d8169`, v0.2.2).

**Inputs taken as binding context:**
- Consistency-audit findings (tier-5 surfaced from the second audit pass on 2026-04-28; carried forward in CHANGELOG `[0.2.2]` Outstanding).
- Council decisions 2026-001 through 2026-016 (decision register through v0.2.2).
- All review-task responses lodged to date (RT-2026-001 through RT-2026-005), as evidence of how the conventions have been applied in practice.
- The four append-only meta trackers' tracker-discipline headers added in v0.2.2 (which explicitly defer a §3 carve-out to this review).
- Architect smell-test response on v0.1 (`governance-ratification-architect-smell-test-v0.1.md`, 2026-04-29) — three blocking observations and seven recommended observations applied in this v0.2 revision. See §10 document control for change-log.

---

## §1. Why this brief exists

Both `CONVENTIONS.md` and `FAIR.md` have carried the same Endorsement Marker since the initial repository commit (`d5dbd35`, 2026-04-27): **"Stance: Guardian (drafting). Reviewed by: pending Architect/Verifier."** They have nevertheless been actively enforcing rules across every downstream artefact: every protocol, memo, task card, review brief, ledger entry, and meta tracker has been drafted under their conventions.

Two days into intensive programme work, the gap between **drafting stance** and **operationally enforced stance** has widened to a degree that warrants closure. The longer the unratified period persists, the more downstream artefacts depend on conventions that could in principle be revised by ratification — creating retrospective audit-trail risk for any prior Council decision whose framing assumed an as-yet-unratified rule.

The audit (consistency review, tier-5 finding) flagged this as a governance gap. Tier-1 through tier-4 cleanup closed everything that could be closed by documentation patching. Tier-5 cannot be closed by patching: it requires Council deliberation under the named review stances.

This brief asks Architect and Verifier to issue ratification verdicts on both files, with declared modifications where required, so that the Endorsement Markers can update to a ratified state and the unratified period can be closed.

---

## §2. Cross-binding mandates installed at issuance

Brief explicitly invokes the following cross-binding constraints:

- **Tier-4 deferred carve-out (binding on Architect Q1).** Tier-4 patch v0.2.2 added tracker-type headers to `meta/council-decisions.md`, `meta/falsification-tracker.md`, `meta/horizon-signals.md`, `meta/stance-log.md`, each declaring a "Document control deviation" because CONVENTIONS.md §3 per-version doc-control fields do not apply per-entry to append-only trackers. The headers explicitly note that a formal §3 carve-out is "pending tier-5 governance review of CONVENTIONS.md". Architect's Q1 ruling is therefore directly load-bearing for whether those tracker headers stand as written, are modified, or are superseded by a §3 revision.
- **Stance-classification ambiguity (binding on Architect Q2).** Council decision 2026-011 established Scout as the issuing stance for horizon signals (SF-NNN); Council decision 2026-012 lodged a Verifier ruling that included a binding methodological demotion (Spencer Stuart [12]). Both stances are listed as **advisory flags** in CONVENTIONS.md §4, but their actual operational role in the programme to date has been to issue primary verdicts within their jurisdictions. Architect Q2 must rule whether §4 wording is accurate as drafted, requires revision, or requires a clarifying sub-clause.
- **Per-jurisdiction split.** Architect rules on §3, §4, §5, §6 of CONVENTIONS and on the operational-discipline structure of FAIR.md. Verifier rules on external-citation accuracy and external-standards-compliance claims across both files. Where the two stances' verdicts are independent, single rulings issue per-stance; where they overlap (notably on FAIR.md operational claims), per-jurisdiction split rulings are permitted.
- **Self-issuance reframe permission (response-Architect empowerment).** Issuing Architect and response Architect occupy the same agent identity at different deliberation moments. Response Architect is explicitly empowered to **reframe or reject any question's framing** as well as rule on its content — this is not limited to ruling on options-as-presented. If the question itself has a structural flaw (false dichotomy, smuggled premise, missing option, mis-scoped jurisdiction), response Architect issues a framing-rejection verdict and either re-poses the question or escalates as RT-2026-007. Temporal separation between deliberation moments is otherwise the only safeguard against issuer-respondent-identity drift; this clause makes the safeguard explicit.

---

## §3. Architect questions (CONVENTIONS.md)

### Q1 — §3 (Document control section) scope and append-only-tracker carve-out

**§3 currently reads:** *"Every substantive document MUST carry a document control section declaring: Version and date; Stance under which it was drafted; Stance under which it was reviewed (or 'pending'); Linked deliverables (parents, dependencies, downstream); Change log entries (what changed in this version vs. the previous)."*

**Issue.** The four append-only trackers in `meta/` (council-decisions, falsification-tracker, horizon-signals, stance-log) are substantive documents but cannot satisfy §3 as written: they have no "version" (each entry is dated independently), no per-version "change log entries" (the entry history IS the change log), and no fixed "linked deliverables" (each entry links its own). Tier-4 patch v0.2.2 added tracker-type headers acknowledging this deviation explicitly; the patch deferred the formal §3 carve-out to this review.

**Ruling options:**
- **(a) §3 revised with explicit append-only-tracker carve-out.** Add a sub-clause: *"Append-only trackers (governance records logging discrete entries that accumulate over time) instead carry a tracker-type header declaring document type, established date, custodial stance, and a document-control deviation note. The history of entries serves as the change log."*
- **(b) §3 left as drafted; tracker-type headers in the four meta files retroactively endorsed as a §3-compliant alternative form.** No CONVENTIONS edit; per-file headers stand as canonical.
- **(c) §3 revised with stricter compliance requirement.** The four trackers must add proper per-entry document-control sections.
- **(d) §3 revised with broader carve-out.** Carve out append-only trackers AND any future log-shaped artefacts (e.g., a future per-decision rationale log, a future incident log). Architect drafts the broader sub-clause.

**Considerations (separate from question framing):**
- Operational entry-rate for the four trackers is high (≥10 entries in the first 48 hours); option (c) compliance burden should be weighed against this rate before ruling.
- Option (a) preserves the current tier-4 tracker headers without modification; option (d) may require the headers to be re-drafted to a broader template.

Architect ruling required. If (a) or (d) is selected, please draft the exact §3 sub-clause wording.

### Q2 — §4 (Stance discipline, Council-3) accuracy of Scout/Verifier "advisory" classification

**§4 currently reads:** *"Functional stances: Guardian, Architect, Integrator. Plus advisory flags: Scout, Verifier. ... Stance invocation: explicit tagging at start of analytical work. ... One stance per participant at a time. ... Vetoes: must cite the violated Core Function in writing."*

**Issue.** "Advisory flags" suggests Scout and Verifier offer non-binding input. In practice:
- **Scout** has issued primary verdicts: RT-2026-001 closed with five binding rulings on TC-06 v0.1, lodged SF-8 and SF-9 as horizon signals, and issued the original R8 closure-call (procedurally-managed-but-live, post-TC-04). Council 2026-011 ratified all of these.
- **Verifier** has issued a primary methodological demotion: RT-2026-003 §5 binding ruling that Spencer Stuart [12] is demoted from H₁ second-order anchor to descriptive-practitioner status, with three search-protocol tightenings declared binding for TC-11 v0.2. Council 2026-012 ratified.

Both are operationally primary in their jurisdictions, not merely advisory. The "advisory flags" wording understates their role in practice.

**Ruling options:**
- **(a) §4 revised to reclassify Scout and Verifier as primary in jurisdiction.** New wording: *"Functional stances: Guardian, Architect, Integrator (Council-3 deliberation core). Per-jurisdiction primary stances: Scout (horizon-signal jurisdiction), Verifier (source-grounding jurisdiction). All five operate under the stance-invocation, one-stance-at-a-time, and veto-justification disciplines below."*
- **(b) §4 revised with clarifying sub-clause on jurisdictional primacy.** Keep "advisory flags" as headline classification but add: *"Within their respective jurisdictions, Scout (horizon signals) and Verifier (source verification) issue rulings that are operationally primary; Council deliberation may modify or supersede such rulings only with written justification."*
- **(c) §4 left as drafted.** Architect rules that "advisory" remains accurate and prior Scout/Verifier rulings stand on the basis of Council ratification, not stance authority.

**Considerations (separate from question framing):**
- One downstream concern about option (c): if "advisory" wording stands, a future stance-discipline disagreement could try to discount a Scout or Verifier ruling on the basis that they are "only advisory". Whether this rescue surface is genuinely live — or counter-balanced by the ratification-of-record requirement that Council decisions provide — is for Architect to weigh on its own merits.

Architect ruling required.

### Q3 — §5 (Endorsement Marker) consistency check across in-tree artefacts and post-ratification wording

**§5 requires:** *"Every framework document carries an Endorsement Marker. For documents in this repository, the marker is provisional unless otherwise declared: 'This is internal scoping work, not a Coastline. No external endorsement is asserted.' Endorsement scope upgrades only on explicit decision logged in `meta/council-decisions.md`."*

**Issue (compliance spot-check).** Spot-check requested across:
- `docs/scoping/human-timescales-scoping-v0.2.md` — §5 marker present? Compliant?
- `docs/protocols/human-timescales-commensurability-protocol-v0.1.md` and `v0.2.md` — markers present?
- `docs/protocols/human-timescales-reform-event-subtyping-protocol-v0.1.md` — marker present?
- The five memos in `docs/memos/` (T10 mechanism, bibliography fill v0.1+v0.2, defunct-archive feasibility, dissolution-cohort anchor-house, era-band slope-floor) — markers present?
- The two task-card snapshots (v0.1 frozen, v0.2 current) — markers present?
- Review-task briefs and responses (`meta/review-tasks/`) — markers present? Are review-task artefacts "framework documents" under §5? Architect to rule on scope.

**Issue (post-ratification wording, surfaced by smell-test).** The proposed Endorsement Marker post-ratification form (see §7 item 1) reads: *"Stance: Guardian (drafting). Reviewed by: Architect [date], Verifier [date]."* This preserves Guardian as sole drafter even after Architect inserts new §7 (review-tasks codification per Q5(a)) or substantively modifies §4 (per Q2(a)). The Marker convention may need a "modified by" field — or a different drafter-attribution after substantive non-Guardian modifications. Architect to rule on whether a "modified by" field, a re-attribution rule, or some other mechanism is required.

Architect ruling required on both issues. If non-compliance is found in the spot-check, list affected files and prescribe remediation. If a Marker-convention extension is required, draft the exact wording.

### Q4 — §6 (Non-prescription clause) inheritance verification

**§6 requires:** *"All documents in this repository inherit the §0a non-prescription clause from `docs/scoping/human-timescales-scoping-v0.2.md`."*

**Issue.** Spot-check whether all `docs/scoping/`, `docs/protocols/`, `docs/memos/` artefacts either inherit (by explicit reference) or restate the non-prescription clause. Sample inspection: TC-06 commensurability protocol v0.2 §1 references it; TC-11 bibliography fill v0.2 inherits via header; TC-08 defunct-archive feasibility v0.1 — verify.

Architect ruling required. If inheritance is implicit-only (i.e., relies on §6 being binding without per-document acknowledgment), is that sufficient, or does §6 require per-document explicit-reference compliance?

### Q5 — Missing conventions; review-tasks framework codification

**Issue.** The review-tasks framework was established 2026-04-28 by Council decision 2026-011 (created `meta/review-tasks/`, established stance-specific brief + response artefact types). The horizon-signals tracker was established the same day by the same decision. Neither is mentioned in CONVENTIONS.md.

**Sub-questions:**
- **Q5(a)** Should CONVENTIONS.md gain a new §7 (or similar) codifying the review-tasks framework — naming brief artefacts, response artefacts, the RT-NNNN numbering convention, the pre-staging/issuance distinction, and the per-jurisdiction split discipline?
- **Q5(b)** Should CONVENTIONS.md gain explicit codification of horizon-signals (SF-NNN) as distinct from falsification handles (FH-NNN) and risk-register entries (R-N)?
- **Q5(c)** Are there other implicit conventions in current operational practice that should be codified? Architect free-form audit invited, **capped at ≤3 proposed new conventions** in this brief; spillover lodges as RT-2026-007 to keep this ratification round closeable.

Architect ruling required, with proposed additions where applicable.

---

## §4. Architect questions (FAIR.md)

### Q6 — FAIR operational claims vs. realised state

**Issue.** FAIR.md operationalises the FAIR principles as per-commit and per-release checklists. The audit spot-check raises both definitional and factual questions about the per-claim coverage; these are split below to avoid conflation.

**Q6.1 — Definitional.** FAIR.md states "every dataset carries a schema." Does the term "dataset" refer to:
- **(i)** Every directory under `data/` regardless of state (placeholder, populated, or in-progress); OR
- **(ii)** Only datasets with non-placeholder content; OR
- **(iii)** Some other operational definition (Architect to specify)?

The current `data/defunct-archives/` directory is a placeholder per its own README and does not carry a schema; the operational claim's bite depends on which definitional reading applies.

**Q6.2 — Factual (conditional on Q6.1).** Once Q6.1 is ruled, audit which datasets satisfy the chosen definitional reading and verify schema coverage:
- **F**indability: per Q6.1 ruling, do all qualifying datasets carry schemas?
- **A**ccessibility: standards compliance check on `LICENSE.md`, repository-code field in CITATION.cff (now points at `https://github.com/threehouse-plus-ec/human-timescales`), public-availability claims.
- **I**nteroperability: schema files use which schema language? Are they machine-readable? FAIR.md may need to declare a schema-language standard or accept the markdown-prose format currently used.
- **R**eusability: license triple compliance (CC BY 4.0 / Apache-2.0 / CC0). Are the licenses correctly applied per artefact class? Verifier overlap on Q9.

Architect ruling required on Q6.1 first; Q6.2 conditional findings prescribed accordingly.

### Q7 — Per-commit and per-release FAIR checklists: binding or aspirational?

**Issue.** FAIR.md `:124` (per the audit) explicitly asks "Is the CHANGELOG updated?" before release. The CHANGELOG was *not* updated for any of the 17 commits between [0.1.0] and [0.2.0]; the audit had to surface this gap, and tier-2 work backfilled the entire window into a single [0.2.0] release entry. This indicates the per-release checklist was not routinely run.

**Ruling options:**
- **(a) Checklists ratified as binding.** Pre-commit and pre-release checklist completion required; non-completion blocks the commit/release.
- **(b) Checklists ratified as binding-by-Council-decision.** Per-release checklist runs as part of any Council-decision commit moment (e.g., a Council decision authorising a release triggers the checklist).
- **(c) Checklists ratified as aspirational but audit-trackable.** Drift surfaces in audit passes (as it did here); audit cadence declared explicitly.
- **(d) Checklists rewritten with operational realism.** Architect to draft a revised checklist set that distinguishes "binding for release commits" from "aspirational for working commits".

Architect ruling required.

---

## §5. Verifier questions (CONVENTIONS.md + FAIR.md)

### Q8 — External citation and standards-reference accuracy

Verifier audit requested on:
- **CONVENTIONS.md** references "ADM-EC Constitution" (multiple times). Verify: is this a named external document with a specific version/source, an internal Open-Science-Harbour artefact, or a working term? If external, citation must be lodged in CITATION.cff or a references appendix.
- **FAIR.md** references the FAIR Guiding Principles. CITATION.cff `references` block lists Wilkinson et al. 2016, *Scientific Data* 3, doi 10.1038/sdata.2016.18. Verify citation accuracy (DOI resolves, journal/volume/year correct).
- **CHANGELOG.md** header references "Keep a Changelog" (`https://keepachangelog.com/en/1.1.0/`) and Semantic Versioning (`https://semver.org/spec/v2.0.0.html`). Verify version numbers cited match the standards' current authoritative releases.
- **CITATION.cff** declares `cff-version: 1.2.0`. Verify CFF v1.2.0 is the current standard and that the file is fully compliant with the v1.2.0 schema.

Verifier ruling required, with citation-violation flags raised per the FAIR.md citation-discipline rule.

### Q9 — License triple compliance

Verifier audit requested on:
- `LICENSE.md` correctness for the three license declarations:
  - Documentation, memos, task cards: CC BY 4.0 — verify license text or reference is correct.
  - Code (when added): Apache-2.0 — verify license text or reference is correct; verify "(when added)" clause is operationally clear.
  - Data: CC0 where copyright would not apply; CC BY 4.0 for compiled datasets — verify both license texts/references are correct, and verify the "where copyright would not apply" / "for compiled datasets" demarcation is operationally testable.
- Per-artefact license application: are individual artefacts marked with their applicable license, or is the LICENSE.md declaration carried by inheritance? FAIR.md §A (Accessibility) implicitly assumes per-artefact clarity. Verifier to rule on whether per-artefact marking is required.

Verifier ruling required.

### Q10 — Standards-compliance claims that may not actually comply

**Issue.** Both files make claims of compliance with external standards (FAIR principles in FAIR.md; SemVer and Keep a Changelog in CHANGELOG.md; CFF v1.2.0 in CITATION.cff; Council deliberation per ADM-EC Constitution in CONVENTIONS.md §4). Verifier free-form audit invited: identify any compliance claim that is asserted in writing but not, in fact, met by the realised repository state.

Examples to consider:
- The CHANGELOG.md `[0.1.0]` entry follows Keep a Changelog format; subsequent `[0.2.0]`, `[0.2.1]`, `[0.2.2]` entries — verify format compliance (Added / Changed / Deprecated / Removed / Fixed / Security headers; date format; version-tagging convention).
- SemVer compliance: is the 0.x.y vs 0.y.x distinction being applied correctly? Tier-2 release was 0.2.0 (treated as MINOR — added functionality); tier-3 was 0.2.1 (treated as PATCH — backwards-compatible fix); tier-4 was 0.2.2 (treated as PATCH — metadata + tracker discipline). Verifier to rule on whether these classifications are SemVer-compliant.
- CITATION.cff v1.2.0 schema strict compliance — run through the formal schema check.

Verifier ruling required.

---

## §6. Net-new risk catch-all

**Risk: ratification surfaces a binding modification that retroactively unsettles prior Council decisions.**

If Architect Q2 ruling reclassifies Scout/Verifier from advisory to primary, prior Council decisions that framed them as advisory (none currently do explicitly, but framing assumptions may be present) could in principle require amendment. Mitigation:
- All Architect-ruled modifications under this brief should be **prospective-only** by default. Any retrospective effect must be declared explicitly in the ratification ruling and lodged in `meta/council-decisions.md` as part of the issuance decision.
- The unratified period (2026-04-27 through ratification date) is a known audit-trail observation, captured in CHANGELOG `[0.2.2]` Outstanding and in the present brief. The ratification Council decision should explicitly close this observation rather than silently absorb it.

**Risk: ratification triggers cascading edits to CONVENTIONS.md and FAIR.md that themselves require their own review pass.**

If Architect's Q1 (§3 carve-out), Q2 (§4 reclassification), Q5 (review-tasks framework codification) all require non-trivial new wording, the post-ratification CONVENTIONS.md is a substantively different document. Ratification should explicitly cover the modifications, not just the as-drafted text. Verifier verifies external citations after modifications are applied, not before.

**Risk: Verifier ruling on Q10 (standards-compliance claims) surfaces a non-compliance that requires substantive corrective work.**

If, for example, the CHANGELOG format is found to deviate from Keep a Changelog v1.1.0, or the CITATION.cff is found to deviate from CFF v1.2.0 schema, corrective work could be in scope of this ratification or could be deferred to a subsequent patch release. Architect and Verifier to coordinate on whether such corrections are gated by ratification or run in parallel.

**Verdict on net-new risks.** No new horizon signals proposed at this stage; risks above are managed via the prospective-only default and explicit-declaration discipline. If Architect or Verifier surfaces a horizon-signal-eligible risk during the review pass, lodge as SF-12 or higher in the standard format.

---

## §7. What "ratified" means (deliverable specification)

On Architect and Verifier responses lodged, the following changes must occur:

1. **Endorsement Markers update.** Both files' Endorsement Markers move from `Stance: Guardian (drafting). Reviewed by: pending Architect/Verifier.` to a ratified form with any required modifications applied. The exact post-ratification wording is itself open under Q3 (smell-test surfaced that the as-drafted form `"Stance: Guardian (drafting). Reviewed by: Architect [date], Verifier [date]."` may not adequately capture cases where Architect inserts substantive new sections or modifies existing ones — a "modified by" field or re-attribution rule may be required).
2. **Modifications applied.** Any §3 carve-out, §4 reclassification, §5 endorsement-marker remediation or convention extension, §6 non-prescription-clause clarification, §7+ new conventions, FAIR-checklist revisions, citation corrections, or license-marking changes ruled by Architect or Verifier are drafted into the files.
3. **Council decision lodged.** A new `meta/council-decisions.md` entry (numbering: next available Council decision number) records: stance composition, brief reference (RT-2026-006), per-question rulings summarised, modifications applied, Endorsement Marker status updated, audit-observation closure.
4. **Stance log updated.** Architect issuance entry and Architect/Verifier response entries appended to `meta/stance-log.md`.
5. **CHANGELOG release at SemVer level appropriate to ruled modifications.** Released as PATCH if endorsement-marker-only (no convention text changes); MINOR if substantive convention modifications added (e.g., new §7 codifying review-tasks framework, §3 carve-out drafted, §4 reclassification); MAJOR if convention semantics change in a way that retroactively re-interprets prior decisions (avoid by default per the prospective-only mitigation in §6). The release level is **declared in the ratification ruling**, not pre-committed in this brief. CONVENTIONS.md and FAIR.md may release at different SemVer levels if their respective modification sets diverge: track each file's bump path independently and reconcile at release commit.
6. **Outstanding clear.** CHANGELOG `[0.2.2]` Outstanding section item ("CONVENTIONS.md and FAIR.md remain in 'Stance: Guardian (drafting). Reviewed by: pending Architect/Verifier'") moved to Resolved in the release-version entry.

---

## §8. Process and scheduling

- **Pre-issuance.** This brief is at DRAFT issuance-ready (v0.2 revision applying Architect smell-test corrections; see `governance-ratification-architect-smell-test-v0.1.md`). Issuance requires user/Council confirmation. Smell-test re-run unnecessary per Architect smell-test recommendation.
- **Issuance.** On user confirmation, brief moves DRAFT issuance-ready → ACTIVE; provisional RT-2026-006 confirmed; entry lodged in `meta/review-tasks/README.md` and `meta/stance-log.md`; Council decision (next available number) lodged at `meta/council-decisions.md` recording issuance.
- **Response window.** Architect and Verifier may respond independently (per-jurisdiction split) or jointly. Suggest tight turnaround given downstream work continues to accumulate under unratified conventions.
- **Cross-binding to tier-6.** Tier-6 substantive methodological concerns (Inverse-R4 fragility, R8/R3 status, TC-05 dependency scoping; surfaced in `docs/memos/tier6-audit-concerns-triage-memo-v0.1.md`) are downstream of TC-card work and out of scope for this brief. Tier-6 substantive rulings are gated by tier-5 closure (rulings are issued under conventions; the conventions should be ratified first); tier-6 preparatory work — drafting, scope refinement, optional pre-stage briefs — may continue in parallel with tier-5.

---

## §9. Out of scope

The following are explicitly NOT under review in this brief:
- Substantive methodological positions taken in `docs/scoping/`, `docs/protocols/`, `docs/memos/` artefacts (these are tier-6 territory).
- The hypotheses H₀, H₁, M-Conjecture themselves (these are claim-substance, not convention).
- The risk register R1–R10 in `docs/scoping/human-timescales-scoping-v0.2.md` §9 (entries are claim-substance; the register's *governance status* is tier-5-adjacent only insofar as horizon-signals tracker codification (Q5(b)) touches it).
- The empirical task cards' design (TC-01 through TC-11 substance is tier-6; the task-card *artefact convention* is tier-5 if Architect Q5(a) covers it).

---

## §10. Document control

- **v0.1** (DRAFT pre-stage, 2026-04-29; superseded by v0.2 same day): Initial brief drafted by Architect on behalf of Council to close the tier-5 audit observation. Five Architect questions on CONVENTIONS.md (§3 carve-out, §4 stance classification, §5 endorsement-marker compliance, §6 non-prescription clause, §7+ missing conventions); two on FAIR.md (operational claims, checklist binding-status); three Verifier questions (external-citation accuracy, license-triple compliance, standards-compliance claims). Cross-binding to tier-4 deferred §3 carve-out installed as Q1 binding context. Per-jurisdiction split permitted. Net-new risk catch-all flags ratification-cascade risks with prospective-only mitigation. Retained at `governance-ratification-architect-verifier-review-v0.1.md` for reference; smell-tested 2026-04-29 (`governance-ratification-architect-smell-test-v0.1.md`).
- **v0.2** (DRAFT issuance-ready, 2026-04-29): Smell-test corrections applied. Three blocking observations resolved: (★1) §2 reframe-permission clause added to empower response-Architect to reject question framing as well as rule on content; (★2) Q5(c) capped at ≤3 proposed new conventions with spillover routing to RT-2026-007; (★3) §7 item 5 SemVer pre-commitment replaced with conditional-on-ruled-modifications language, plus separate-bump-path provision for FAIR.md. Seven recommended observations applied: (△4) Q2 framing — "rescue surface" caveat moved from question text to separate considerations note; (△5) Q1 option (c) parenthetical foreclosure removed, weighed in considerations note; (△6) Q6 split into Q6.1 (definitional: what is a "dataset") and Q6.2 (factual: schema coverage conditional on Q6.1); (△7) Q3 expanded to include Endorsement Marker post-ratification wording question (modified-by field or re-attribution rule); (△8) §8 tier-6 gating softened from "must complete before tier-6 deliberation begins" to "tier-6 substantive rulings gated by tier-5 closure; preparatory work may continue"; (△9) Council decision number hardcode ("2026-017 if no other decisions have intervened") replaced with "next available"; (△10) §7 item 5 FAIR.md SemVer path explicitly carved as independently track-able from CONVENTIONS.md.
- **Pending:** User/Council confirmation for issuance. On issuance, status moves DRAFT issuance-ready → ACTIVE; RT-2026-006 confirmed; logged in council-decisions, stance-log, and meta/review-tasks/README.md.

**Stance log.** Drafted Architect (v0.1); revised Architect (v0.2 per Architect smell-test). Brief structure follows the RT-2026-002 / RT-2026-004 / RT-2026-005 pattern (binding-ruling questions, cross-binding mandates, per-jurisdiction split provision, net-new risk catch-all, deliverable specification, document control), with novel additions for the self-issuance case (§2 reframe-permission). No Guardian veto issued at draft. Integrator decision required on issuance.

---

*Architect-stance brief. Provisional RT-2026-006. v0.2 ~2900 words. DRAFT issuance-ready pending user confirmation.*
