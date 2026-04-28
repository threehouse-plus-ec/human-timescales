# Changelog

All notable changes to this repository will be documented here.

The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

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
