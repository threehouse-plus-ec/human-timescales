# FAIR Principles — Operational Discipline

This repository commits to the FAIR principles for research outputs: **F**indable, **A**ccessible, **I**nteroperable, **R**eusable. This file is not a manifesto — it is an operational checklist that disciplines what goes into the repository and how.

The FAIR principles were articulated by Wilkinson et al. (2016, *Scientific Data* 3:160018). This repository implements an operational framework aligned with the FAIR principles, with full compliance as a target state. Per-principle implementation discipline follows.

---

## F — Findable

**F1. (Meta)data are assigned a globally unique and persistent identifier.**

- Every release of this repository will be archived to Zenodo and assigned a DOI.
- Pre-release artifacts use the Git commit hash as a content-addressable identifier.
- Internal artifacts (task cards, ledger entries, logbook entries) carry version strings and dates in their filename and document control section.

**F2. Data are described with rich metadata.**

- Every dataset directory carries a `README.md` describing the dataset purpose, source, schema, and provenance.
- Every dataset carries a `schema.md` defining columns, types, controlled vocabularies, and unit conventions.
- Every analysis carries metadata declaring inputs, outputs, dependencies, and seed values where applicable.

**Dataset vs. dataset slot** (per Council 2026-017, RT-2026-006 Q6.1 ruling). A *dataset* is a directory under `data/` containing non-placeholder content; a *dataset slot* is a placeholder directory awaiting content. Schema requirements bind on first content commit, not on slot creation. Schema language: markdown-prose with YAML front-matter is acceptable as the current floor; formal schema languages (JSON Schema, frictionless-data, or domain-equivalent) are preferred medium-term and required for any dataset whose schema is referenced by code.

**F3. Metadata clearly and explicitly include the identifier of the data they describe.**

- Schema files reference dataset paths explicitly.
- README files cross-reference task card IDs (TC-NN) and parent documents.

**F4. (Meta)data are registered or indexed in a searchable resource.**

- On release: Zenodo for archival; GitHub for active development; ORCID linkage on CITATION.cff.

---

## A — Accessible

**A1. (Meta)data are retrievable by their identifier using a standardised communications protocol.**

- HTTPS / Git protocol throughout. No proprietary access mechanisms.

**A1.1. The protocol is open, free, and universally implementable.**

- Git, HTTPS, plain-text Markdown, CSV, JSON. All open standards.

**A1.2. The protocol allows for an authentication and authorisation procedure where necessary.**

- Public read access by default. Write access via standard Git authentication where required.

**A2. Metadata are accessible, even when the data are no longer available.**

- Schemas, README files, and document-control sections are committed to the repository regardless of whether the underlying data are present, deferred, or restricted.
- For data that cannot be released (e.g., contested archival materials, unpublished consultations), the metadata describing that the data exist, why they are restricted, and under what conditions they could be made available is committed.

---

## I — Interoperable

**I1. (Meta)data use a formal, accessible, shared, and broadly applicable language for knowledge representation.**

- Documents in CommonMark Markdown.
- Tabular data in CSV (UTF-8) or TSV with explicit delimiter declaration.
- Structured metadata in YAML or JSON.
- Citations in CFF (Citation File Format) v1.2.0.

**I2. (Meta)data use vocabularies that follow FAIR principles.**

- Controlled vocabularies declared in `schema.md` for each dataset.
- For institutional-history datasets: explicit declaration of taxonomies (reform sub-types, legitimacy domains, era boundaries).
- Where possible, alignment with established vocabularies (ISO date formats, ORCID for persons, ROR for institutions).

**I3. (Meta)data include qualified references to other (meta)data.**

- Cross-references between artifacts use explicit relative paths within the repository or DOIs/URLs for external references.
- Provenance chains are traced in dataset README files.

---

## R — Reusable

**R1. (Meta)data are richly described with a plurality of accurate and relevant attributes.**

- Each dataset README covers: purpose, source, collection method, coverage period, known limitations, intended use, and reuse cautions.

**R1.1. (Meta)data are released with a clear and accessible data usage license.**

- Documentation: CC BY 4.0.
- Code: Apache-2.0.
- Data: per-class defaults (raw → CC0 1.0; processed → CC BY 4.0; derived → CC BY 4.0) with per-dataset overrides; see `LICENSE.md`.
- Per-artefact license accessibility is satisfied via the declared inheritance mechanism in `LICENSE.md` (artefact license is determinable from path).

**R1.2. (Meta)data are associated with detailed provenance.**

- Every dataset traces its sources back to primary archives where possible.
- Where derivative, the derivation script or procedure is referenced explicitly.
- Logbook entries (`logbook/`) provide chronological provenance for decisions and modifications.

**R1.3. (Meta)data meet domain-relevant community standards.**

- For historiographic data: explicit dating conventions (Julian / Gregorian / proleptic), explicit handling of disputed events.
- For institutional-history data: explicit handling of contested ecumenical / multistakeholder / authoritative status.
- For cross-era data: declaration of the commensurability protocol (per scoping v0.2 §5 M1 / TC-06).

---

## Compliance status

(Per Council 2026-017, RT-2026-006 Q10.3 ruling.)

This repository implements an operational framework aligned with FAIR principles. Full compliance is a target state, not a current achievement. Specifically as of v0.3.0:

- **F1 (DOIs via Zenodo):** conditional on release-time deposit; active for tagged releases only.
- **F4 (ORCID linkage):** present in CITATION.cff as of v0.2.2.
- **I1–I3 (vocabularies, formal schema languages):** markdown-prose with YAML front-matter is the current floor; formal schema languages (JSON Schema, frictionless-data) are preferred medium-term and required where schemas are referenced by code (per Architect Q6.2 ruling).
- **Per-artefact license accessibility (R1.1, A1):** satisfied via declared-inheritance mechanism in LICENSE.md (per Verifier Q9.4 patch).
- **Other principles:** implementation aligned but ongoing audit cadence (per the three-tier operational discipline below) is the discipline that surfaces drift.

---

## Operational discipline (three-tier checklist)

(Per Council 2026-017, RT-2026-006 Q7 ruling. Replaces the prior single-checklist form.)

Three commit-type tiers, each with its own checklist:

### Tier I — Working commits

Commits that do not bump SemVer and do not ratify a Council decision. Pre-commit checklist is **aspirational**. Drift surfaces in audit as observation-class findings; non-completion does not block the commit.

Aspirational pre-commit checklist (Tier I):

- [ ] If the commit modifies a dataset: open format (CSV, JSON, plain text); README and schema present; provenance traceable; licence determinable from path or per-dataset README.
- [ ] If the commit modifies a document: stance log entry where mandated by §4 cadence rule; document control section with version and date; non-prescription clause inheritance (where applicable); falsification handles for any new claim.
- [ ] If the commit modifies a derivative: derivation script committed and reproducible.

### Tier II — Release commits

Commits that bump SemVer (i.e., create a new release tag). Pre-release checklist is **binding**: non-completion blocks the release tag.

Binding pre-release checklist (Tier II):

- [ ] CHANGELOG entry drafted in Keep a Changelog format (Added / Changed / Deprecated / Removed / Fixed / Security headers as applicable).
- [ ] CITATION.cff `version` and `date-released` fields bumped.
- [ ] README closing-line version stamp bumped.
- [ ] Outstanding items from the prior release reconciled (closed in this release's Resolved section, or carried forward in Outstanding with explicit reason).
- [ ] All internal cross-references valid (no stale paths to renamed/removed artefacts).
- [ ] Zenodo deposit prepared (or explicitly deferred with reason).

### Tier III — Council-decision commits

Commits that ratify a Council decision (substantive deliberation outcome lodged in `meta/council-decisions.md`). Pre-decision checklist is **binding**: non-completion blocks the decision-ratification commit.

Binding pre-decision checklist (Tier III):

- [ ] `meta/council-decisions.md` entry lodged with: stance composition, brief reference (RT-NNNN), per-question rulings summarised, modifications applied, audit-observation closure where applicable.
- [ ] `meta/stance-log.md` entries lodged for issuing stance and ruling stance(s).
- [ ] Brief artefact reference linked from the Council decision entry.
- [ ] Where the decision triggers file modifications: edits applied in the same commit (integrated commit discipline) or in a same-release follow-up commit referenced in the decision.
- [ ] Endorsement Marker on modified framework documents updated per §5 post-review form (Stance / Reviewed by / Modified by).

---

## What this discipline protects against

- Silent loss of provenance when data are reorganised.
- Schema drift between datasets that should be comparable.
- Implicit licensing assumptions when data are reused.
- Loss of stance / deliberation context when documents are extracted.
- Falsification handles disappearing as documents evolve.
- Findability degradation as the repository grows.
- Compliance overstatement (per Q10.3 ruling: aligned ≠ complies; the three-tier checklist is the audit cadence that surfaces drift).

---

## References

- Wilkinson, M. D., et al. (2016). The FAIR Guiding Principles for scientific data management and stewardship. *Scientific Data*, 3, 160018. https://doi.org/10.1038/sdata.2016.18
- GO FAIR initiative: https://www.go-fair.org/fair-principles/
- Citation File Format: https://citation-file-format.github.io/

---

*Document control. v0.3.0 · 2026-04-29 · Stance: Guardian (drafting). Reviewed by: Architect 2026-04-29, Verifier 2026-04-29. Modified by: Architect 2026-04-29 (Q6 dataset/slot distinction + schema-language declaration; Q7 three-tier checklist restructure), Verifier 2026-04-29 (Q10.3 alignment-vs-compliance wording + new Compliance status section).*
