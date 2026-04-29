# Changelog

All notable changes to this repository will be documented here.

The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

---

## [0.3.0] — 2026-04-29

Tier-5 governance ratification release. Closes the unratified-conventions gap that has stood since the initial 2026-04-27 commit. Ratified by Council decision 2026-017 (RT-2026-006), integrating Architect Q1–Q7 + Verifier Q8–Q10 rulings + Verifier follow-up patches in a single integrated commit per the cross-jurisdiction integrated-commit discipline.

### Added

- `meta/review-tasks/governance-ratification-architect-review-response-v0.1.md` — Architect Q1–Q7 ruling response.
- `meta/review-tasks/governance-ratification-verifier-followup-patches-v0.1.md` — Verifier follow-up patches drafted on user Path-1 acceptance of Verifier offer.
- `meta/council-decisions.md` 2026-017 — ratification decision lodged.
- **CONVENTIONS.md** new sections:
  - §3 append-only-tracker carve-out sub-clause (Architect Q1 option (a)-modified).
  - §4 stance-log cadence sub-clause (Architect Q5(c)-1).
  - §5 post-review marker form with "Modified by" field (Architect Q3 ruling on post-ratification wording).
  - §6 hybrid inheritance with prescription-eligibility test (Architect Q4 ruling).
  - **New §7** — Review-tasks framework codification, including self-issuance reframe-permission clause (Architect Q5(a)).
  - **New §8** — Tracker artefact types codification: FH-NNN / SF-NNN / R-N non-substitutability and bidirectional cross-link discipline (Architect Q5(b)).
- **FAIR.md** new sections:
  - F2 dataset vs. dataset-slot distinction with schema-language declaration (Architect Q6.1 + Q6.2).
  - Compliance status section explicitly distinguishing operational alignment from full compliance (Verifier Q10.3).
  - Three-tier checklist (Tier I working/aspirational, Tier II release/binding, Tier III Council-decision/binding) replacing the prior single-checklist form (Architect Q7 option (d)).
- **LICENSE.md** new sections:
  - Per-class data defaults (raw → CC0 1.0; processed → CC BY 4.0; derived → CC BY 4.0; documentation → CC BY 4.0) with per-dataset README override discipline (Verifier Q9.3).
  - License inheritance discipline section satisfying FAIR-A1 per-resource license-accessibility requirement (Verifier Q9.4).
- Endorsement Markers added to 14 framework files that lacked them (Q3 spot-check remediation): `docs/memos/tier6-audit-concerns-triage-memo-v0.1.md`; `docs/task-cards/human-timescales-task-cards-v0.{1,2}.md`; all 11 `meta/review-tasks/*-v0.1.md` files lacking markers.

### Changed

- **CONVENTIONS.md** §4 stance reclassification (Architect Q2 option (a) integrated with Verifier Q8.5 ADM-EC patch). "Advisory flags: Scout, Verifier" replaced with "Per-jurisdiction primary stances: Scout (horizon-signal jurisdiction) and Verifier (source-grounding jurisdiction)". Council-3 core (Guardian, Architect, Integrator) retains cross-jurisdiction veto authority defined in-line (Guardian on clarity-and-ethics; Architect on structural-coherence; Integrator on flow); per-jurisdiction primaries do not. "ADM-EC Constitution (referenced externally)" reference removed; Core Function definitions self-contained in §4 text.
- **CONVENTIONS.md** §9 (renumbered from §7; T4 kill-criterion) — "ADM-EC vocabulary" reference clarified as "a working internal framework" to remove external-authority implication (Verifier Q8.5).
- **CONVENTIONS.md** sections renumbered: existing §7–§14 → §9–§16 to accommodate new §7 and §8.
- **FAIR.md** line 5 — "implements them as follows" replaced with "implements an operational framework aligned with the FAIR principles, with full compliance as a target state" (Verifier Q10.3).
- **LICENSE.md** Data section — "where copyright would not apply" replaced with operationally testable per-class defaults from path (Verifier Q9.3).
- **Endorsement Markers** on CONVENTIONS.md, FAIR.md, LICENSE.md updated to ratified form per new §5 extension: "Stance: Guardian (drafting). Reviewed by: Architect 2026-04-29, Verifier 2026-04-29. Modified by: Architect 2026-04-29 (specific modifications listed), Verifier 2026-04-29 (specific modifications listed)."
- `meta/review-tasks/README.md` — RT-2026-006 moved from Pending to Closed.
- `meta/stance-log.md` — Verifier follow-up entry and Council-decision-2026-017 entry appended.
- `CITATION.cff` — version bumped to 0.3.0; date-released 2026-04-29.
- `README.md` closing-line bumped to v0.3.0.

### Resolved (from [0.2.2] Outstanding)

- CONVENTIONS.md and FAIR.md ratification gap (tier-5 audit follow-up): both files now ratified via Council decision 2026-017 with substantive modifications applied; Endorsement Markers updated to ratified form. The unratified period (2026-04-27 through 2026-04-29) is closed as an audit observation, prospective-only per §6 default.

### Outstanding (carried into 0.3.0)

- **RT-2026-007 lodgement within two weeks** — Two Q5(c) candidates routed by Architect ruling: (i) decision-register-citation verification (Council decisions are referenced by number throughout artefacts; no convention currently requires the cited number to exist or to bind what is claimed); (ii) cross-tracker linkage symmetry enforcement (new §8 requires bidirectional cross-links; no audit mechanism currently checks for asymmetric drift).
- **Tier-6 substantive methodological concerns** — Inverse-R4 fragility, R8/R3 procedurally-managed-but-live status, TC-05 GLHC-dossier dependency-scoping gap. Triage memo at `docs/memos/tier6-audit-concerns-triage-memo-v0.1.md`. Tier-6 substantive rulings now unblocked (tier-5 closure satisfied per Architect Q7 EC ruling on tier-5/tier-6 gating).
- **Q1 tracker-header housekeeping** — entry-numbering convention should be added to the four append-only tracker headers at next housekeeping pass (non-blocking; current headers compliant in substance per §3 carve-out).
- **CITATION.cff machine validation** — schema validation against CFF v1.2.0 (Verifier Q10.4 non-blocking item).
- **Apache-2.0 "(when added)" clarification** — operational trigger condition for the Code license (Verifier Q9.2 non-blocking item).

---

## [0.2.2] — 2026-04-28

Metadata-and-tracker-discipline patch. Closes the remaining low-severity items from the consistency-audit triage.

### Added

- ORCID linkage in `CITATION.cff` (`https://orcid.org/0000-0001-8081-9718`), honouring the FAIR.md commitment.
- Tracker-type headers in the four append-only meta files (`council-decisions.md`, `falsification-tracker.md`, `horizon-signals.md`, `stance-log.md`) — each declares document type (append-only tracker), established date, custodial stance, and an explicit document-control deviation note recording that CONVENTIONS.md §3 per-version doc-control fields do not apply per-entry. A formal §3 carve-out is deferred to tier-5 governance review of CONVENTIONS.md.

### Changed

- `CITATION.cff` version and `README.md` closing line bumped to 0.2.2.

### Outstanding (deferred to tier 5)

- `CONVENTIONS.md` and `FAIR.md` themselves remain in "Stance: Guardian (drafting). Reviewed by: pending Architect/Verifier" — they are enforcing rules they have not been formally ratified under. Resolution requires Council pass (Architect + Verifier review of both files), not a documentation patch.

---

## [0.2.1] — 2026-04-28

Governance-cleanup release. Resolves the v0.1 task-card in-place-mutation discrepancy flagged in the [0.2.0] Known issues, and backfills the Council-decisions register.

### Added

- `docs/task-cards/human-timescales-task-cards-v0.2.md` — versioned snapshot of the task-card set as of 2026-04-28, with status-field refresh per RT-2026-001..005 outcomes and `Deliverable location:` field added to TC-06, TC-07, TC-08, TC-11. No card added, removed, or restructured relative to v0.1.
- `meta/council-decisions.md` 2026-015 (Guardian RT-2026-002 response) and 2026-016 (Guardian RT-2026-004 response) — backfill entries closing the audit-trail gap.

### Changed

- `docs/task-cards/human-timescales-task-cards-v0.1.md` — restored to the original 2026-04-27 frozen state. The 2026-04-28 status-field and deliverable-location mutations applied during 0.2.0 are preserved in the new v0.2 snapshot above.
- `docs/task-cards/README.md` — directory README updated to list v0.2 as current and v0.1 as retained-for-reference.
- Forward-looking task-card references updated v0.1 → v0.2: `data/m1-catholic-councils/README.md`, `data/m1-catholic-councils/schema.md`, `data/t10-archive/README.md`, `docs/memos/bibliography-fill-tenure-trends-memo-v0.2.md` (Linked. section), `docs/protocols/human-timescales-commensurability-protocol-v0.2.md` (Linked. section). Historical references in v0.1-dated review briefs, protocols, memos, logbook, stance-log, and council-decisions left unchanged.
- `README.md` closing line and `CITATION.cff` version bumped to 0.2.1 / 2026-04-28.
- Stale TC-08 status text in v0.2 snapshot fixed (previously read "awaiting Guardian R3 review"; updated to reflect RT-2026-004 closed, anchor-house feasibility memo drafted).

### Resolved (from [0.2.0] Known issues)

- Council-decisions register entries for Guardian RT-2026-002 and RT-2026-004 responses now lodged.
- `docs/task-cards/human-timescales-task-cards-v0.1.md` filename/internal-version/body discrepancy resolved by versioned-snapshot bump (v0.2 created; v0.1 restored to its 2026-04-27 frozen state).

---

## [0.2.0] — 2026-04-28

### Added

- Protocols subdirectory `docs/protocols/` with README and three protocols:
  - `human-timescales-commensurability-protocol-v0.1.md` (TC-06 v0.1; dual-measurement).
  - `human-timescales-commensurability-protocol-v0.2.md` (TC-06 v0.2; triple-measurement, era-stratified, three-tier power rule, R8 closure-condition cross-binding to TC-04 + TC-08).
  - `human-timescales-reform-event-subtyping-protocol-v0.1.md` (TC-07 v0.1; inclusion/exclusion tests + three sub-types with multi-tagging).
- Five memos:
  - `defunct-archive-feasibility-memo-v0.1.md` (TC-08; Templar primary + English Dissolution secondary).
  - `bibliography-fill-tenure-trends-memo-v0.1.md` and `v0.2.md` (TC-11; v0.2 = 27 entries across nine sub-bands, RT-2026-003 Verifier integration).
  - `dissolution-cohort-anchor-house-feasibility-v0.1.md` (TC-08; Canterbury > Glastonbury verdict).
  - `era-band-slope-floor-derivation-memo-v0.1.md` (TC-06 v0.2.1 binding follow-up).
- Review-tasks framework `meta/review-tasks/` with README and eight artefacts covering RT-2026-001 through RT-2026-005 (Scout/Guardian/Verifier briefs and responses on TC-06, TC-07, TC-08, TC-11).
- Horizon-signals tracker `meta/horizon-signals.md` — signals SF-8 through SF-11.
- Logbook entry `logbook/2026-04/2026-04-28.md`.

### Changed

- `README.md` quick map refreshed to reflect protocol set and memo growth.
- `meta/council-decisions.md` — Scout (RT-2026-001) and Verifier (RT-2026-003) decisions logged.
- `meta/stance-log.md` updated.
- `docs/README.md`, `docs/memos/README.md`, `meta/README.md` updated to reflect new content.
- `docs/task-cards/human-timescales-task-cards-v0.1.md` body updated with 2026-04-28 events (filename and internal version unchanged — see Known issues).

### Status

- Hypotheses H₀ and H₁ remain frozen at v0.2; M-Conjecture remains v0.1.
- All hypotheses pre-falsification; binding timelines unchanged (TC-01 by 2026-12-31, TC-04 by 2027-06-30).

### Known issues (carried into 0.2.0)

- Council-decisions register lacks entries for the Guardian responses RT-2026-002 (TC-06) and RT-2026-004 (TC-08); outcomes are recorded in `meta/horizon-signals.md`, `meta/stance-log.md`, and the response files, but not in the authoritative decision register.
- `docs/task-cards/human-timescales-task-cards-v0.1.md` was mutated in place with 2026-04-28 content while filename and internal version header still read v0.1 / 2026-04-27 — a CONVENTIONS.md §3 discrepancy pending Council resolution.

---

## [0.1.0] — 2026-04-27

### Added

- Initial repository structure with documentation, data, analysis, ledger, logbook, and meta directories.
- Top-level governance files: `README.md`, `LICENSE.md`, `CITATION.cff`, `CONVENTIONS.md`, `FAIR.md`, `CHANGELOG.md`, `.gitignore`.
- Scoping document `docs/scoping/human-timescales-scoping-v0.1.md` (kickoff draft).
- Scoping document `docs/scoping/human-timescales-scoping-v0.2.md` (E1–E6 integration after Scout/Architect/Integrator review).
- Memo `docs/memos/t10-mechanism-conjecture-memo-v0.1.md` (T10 reframed from boundary case to mechanism evidence; ICANN/IANA case anchored).
- Task card set `docs/task-cards/human-timescales-task-cards-v0.1.md` (eleven cards covering empirical pilots, methodological infrastructure, synthesis, and auxiliary).
- Logbook entry `logbook/2026-04/2026-04-27.md` (initial entry capturing programme state).
- Logbook template `logbook/_template.md`.
- Meta files: `meta/stance-log.md`, `meta/council-decisions.md`, `meta/falsification-tracker.md`.
- Per-directory README files with FAIR discipline reminders for `data/`, `analysis/`, `ledger/`, `logbook/`, `meta/`, `docs/`.
- Schema templates for M1 Catholic councils dataset (`data/m1-catholic-councils/schema.md`) and T10 archive dataset (`data/t10-archive/schema.md`).

### Status

- Hypotheses H₀ and H₁ frozen at v0.2; M-Conjecture stated v0.1 in T10 memo.
- All hypotheses pre-falsification.
- Binding falsification timelines: TC-01 by 2026-12-31, TC-04 by 2027-06-30.

---

*Format reminder.* Future entries follow the pattern: **Added / Changed / Deprecated / Removed / Fixed / Security**, under a version header with date.
