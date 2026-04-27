# FAIR Principles — Operational Discipline

This repository commits to the FAIR principles for research outputs: **F**indable, **A**ccessible, **I**nteroperable, **R**eusable. This file is not a manifesto — it is an operational checklist that disciplines what goes into the repository and how.

The FAIR principles were articulated by Wilkinson et al. (2016, *Scientific Data* 3:160018). This repository implements them as follows.

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
- Data: CC0 where copyright does not apply; CC BY 4.0 for compiled datasets where attribution is appropriate.
- See `LICENSE.md`.

**R1.2. (Meta)data are associated with detailed provenance.**

- Every dataset traces its sources back to primary archives where possible.
- Where derivative, the derivation script or procedure is referenced explicitly.
- Logbook entries (`logbook/`) provide chronological provenance for decisions and modifications.

**R1.3. (Meta)data meet domain-relevant community standards.**

- For historiographic data: explicit dating conventions (Julian / Gregorian / proleptic), explicit handling of disputed events.
- For institutional-history data: explicit handling of contested ecumenical / multistakeholder / authoritative status.
- For cross-era data: declaration of the commensurability protocol (per scoping v0.2 §5 M1 / TC-06).

---

## Operational discipline (per-commit)

Before any commit that adds or modifies a dataset, ask:

- [ ] Is the dataset in an open format (CSV, JSON, plain text)?
- [ ] Does it have a `README.md` and a `schema.md`?
- [ ] Does the schema declare units, types, and controlled vocabularies?
- [ ] Is provenance traceable (source archive, collection date, collector, method)?
- [ ] Is the licence declared?
- [ ] If derivative: is the derivation script committed and reproducible?

Before any commit that adds or modifies a document, ask:

- [ ] Does it carry a stance log?
- [ ] Does it carry a document control section with version and date?
- [ ] Does it carry the non-prescription clause inheritance (where applicable)?
- [ ] Does it carry falsification handles for any new claim?

Before any release, ask:

- [ ] Is the CHANGELOG updated?
- [ ] Is CITATION.cff current?
- [ ] Is a Zenodo deposit prepared?
- [ ] Are all internal cross-references valid?

---

## What this discipline protects against

- Silent loss of provenance when data are reorganised.
- Schema drift between datasets that should be comparable.
- Implicit licensing assumptions when data are reused.
- Loss of stance / deliberation context when documents are extracted.
- Falsification handles disappearing as documents evolve.
- Findability degradation as the repository grows.

---

## References

- Wilkinson, M. D., et al. (2016). The FAIR Guiding Principles for scientific data management and stewardship. *Scientific Data*, 3, 160018. https://doi.org/10.1038/sdata.2016.18
- GO FAIR initiative: https://www.go-fair.org/fair-principles/
- Citation File Format: https://citation-file-format.github.io/

---

*Document control. v0.1 · 2026-04-27 · Stance: Guardian (drafting). Reviewed by: pending Architect/Verifier.*
