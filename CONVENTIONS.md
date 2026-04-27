# Conventions

This document declares the operational conventions for this repository. All artifacts in the repository are expected to conform.

---

## 1. Versioning

- **Semantic versioning** for the repository: MAJOR.MINOR.PATCH.
  - MAJOR: breaking change to programme architecture (e.g., hypothesis revision after falsification).
  - MINOR: substantive new content (new memo, new task card set, new dataset).
  - PATCH: corrections, clarifications, non-substantive edits.
- **Per-document versioning:** documents carry their own version (v0.1, v0.2, ...) in filename and document-control section.
- **Repository version:** declared in `CHANGELOG.md` and tagged in Git on each release.
- Initial scoping documents may use v0.1, v0.2, v0.3 progression. Frozen Coastline-equivalent documents use v1.0.0+.

## 2. Naming

- **Files and directories:** kebab-case (`human-timescales-scoping-v0.2.md`, not `Human_Timescales_Scoping_V0.2.MD`).
- **Versioned documents:** include version in filename (`-v0.2`).
- **Logbook entries:** ISO date format (`2026-04-27.md`).
- **Schema files:** always named `schema.md` within the dataset directory.

## 3. Document control section

Every substantive document MUST carry a document control section declaring:

- Version and date.
- Stance under which it was drafted.
- Stance under which it was reviewed (or "pending").
- Linked deliverables (parents, dependencies, downstream).
- Change log entries (what changed in this version vs. the previous).

## 4. Stance discipline (Council-3)

- **Functional stances:** Guardian, Architect, Integrator. Plus advisory flags: Scout, Verifier.
- **Stance invocation:** explicit tagging at start of analytical work (`[Stance: Guardian]`).
- **One stance per participant at a time.**
- **Vetoes:** must cite the violated Core Function in writing. See ADM-EC Constitution (referenced externally).
- **Stance log:** all stance invocations and decisions logged in `meta/stance-log.md`.

## 5. Endorsement Marker (Coastline Template v2.0)

Every framework document carries an Endorsement Marker. For documents in this repository, the marker is provisional unless otherwise declared:

> *This is internal scoping work, not a Coastline. No external endorsement is asserted.*

Endorsement scope upgrades only on explicit decision logged in `meta/council-decisions.md`.

## 6. Non-prescription clause (inheritance)

All documents in this repository inherit the §0a non-prescription clause from `docs/scoping/human-timescales-scoping-v0.2.md`:

> This document describes minimum coordination timescales as observed phenomena. It does not endorse them as correct, optimal, or politically legitimate. **A floor is not a target.** Any extracted prescriptive use is unauthorised.

Documents that depart from this discipline must declare the departure explicitly in their endorsement marker.

## 7. T4 kill-criterion (ADM-EC vocabulary)

Where ADM-EC / causal-geometry vocabulary (L_source, L_apparatus, L_comparison, η_opt) is used, the document must produce at least one prediction or distinction unavailable from prior frameworks. If it merely re-describes, it is dropped, not decorated.

This is operative for `docs/sails/` essays and any cross-domain mapping.

## 8. Falsification discipline

Every claim asserted in this repository carries:
- An explicit statement of what would weaken or falsify it.
- Where applicable, a binding falsification timeline.
- A trail to `meta/falsification-tracker.md`.

Soft formulations (e.g., "rarely", "tends to", "may only") are flagged for revision toward falsifiable structure.

## 9. Breakwater discipline

Claim-ledger entries (`ledger/`) follow Breakwater Schema v1.0-rc:

- Claim → Predictions → Constraints → Comparison → Classification.
- Three-value classification: COMPATIBLE / UNDERDETERMINED / INCONSISTENT.
- UNDERDETERMINED requires Discriminant Condition + feasibility flag.
- No post-verdict text.
- Self-reference exclusion.
- Anti-aggregation: classifications are independent.

## 10. Logbook discipline

Logbook entries (`logbook/`) are dated, append-only, and cross-reference artifacts touched. Template in `logbook/_template.md`.

## 11. Language

- **Working language:** Oxford British English (centre, organisation, recognise, behaviour).
- **Inline citations:** parenthetical author-date for academic references; explicit URL for online sources.
- **Mathematical notation:** UTF-8 inline (η, τ, L₅) preferred over LaTeX where possible; LaTeX permitted for complex expressions.

## 12. Data file formats

- Tabular: CSV (UTF-8, comma delimiter, RFC 4180), or TSV with explicit declaration.
- Structured: YAML or JSON.
- Documents: CommonMark Markdown.
- No proprietary formats committed to the repository.

## 13. File size and Git LFS

- Files >50 MB should not be committed to standard Git history. Use Git LFS or external archival.
- Raw archival material (e.g., scanned council documents) goes to external repositories with DOI; this repository carries metadata and processed extracts only.

## 14. Commits

- Commit messages follow Conventional Commits where practical (`feat:`, `docs:`, `data:`, `fix:`).
- Substantive content commits cross-reference the relevant task card (`TC-NN`) where applicable.

---

*Document control. v0.1 · 2026-04-27 · Stance: Guardian (drafting).*
