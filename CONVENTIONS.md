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

**Append-only-tracker carve-out** (per Council 2026-017, RT-2026-006 Q1 ruling). Append-only trackers — substantive documents whose form is a chronologically-accumulating sequence of independently-dated entries, where the entry history itself constitutes the change log — are exempt from the per-version document-control fields above. Such trackers instead carry a tracker-type header declaring: document type, established date, custodial stance, entry-numbering convention, and a document-control deviation note acknowledging this carve-out. Future artefact classes claiming this exemption must demonstrate the append-only structural pattern in their tracker-type header; classes that diverge from the pattern require §3 amendment.

## 4. Stance discipline (Council-3 + per-jurisdiction primaries)

Functional stances: Guardian, Architect, Integrator constitute the Council-3 deliberation core. Per-jurisdiction primary stances: Scout (horizon-signal jurisdiction) and Verifier (source-grounding jurisdiction) issue rulings primary within those jurisdictions, ratified by Council decision. The Council-3 core retains cross-jurisdiction veto authority — Guardian on clarity-and-ethics violations; Architect on structural-coherence violations; Integrator on flow violations — exercised in writing with explicit citation of the violated Core Function. Per-jurisdiction primaries do not hold cross-jurisdiction veto authority. All five stances operate under the stance-invocation, one-stance-at-a-time, and veto-justification disciplines below.

- **Stance invocation:** explicit tagging at start of analytical work (`[Stance: Guardian]`).
- **One stance per participant at a time.**
- **Vetoes:** must cite the violated Core Function in writing, naming the stance whose function is at issue and the specific violation.
- **Stance log:** all stance invocations and decisions logged in `meta/stance-log.md`.

**Stance-log cadence** (per Council 2026-017, RT-2026-006 Q5(c)-1 ruling). Stance-log entries are mandatory at: (i) brief issuance (issuing stance), (ii) ruling lodgement (target stance), (iii) veto invocation (vetoing stance). Optional but encouraged for: smell-test responses, framing-rejection invocations, and Integrator coordination decisions. Cadence violations surface in audit as observation-class findings.

## 5. Endorsement Marker (Coastline Template v2.0)

Every framework document carries an Endorsement Marker. For documents in this repository, the marker is provisional unless otherwise declared:

> *This is internal scoping work, not a Coastline. No external endorsement is asserted.*

Endorsement scope upgrades only on explicit decision logged in `meta/council-decisions.md`.

**Post-review marker form** (per Council 2026-017, RT-2026-006 Q3 ruling). Post-review Endorsement Markers take the form: *"Stance: [drafter] (drafting). Reviewed by: [reviewer-stance(s)] [date(s)]. Modified by: [stance(s)] [date(s)] (where review-stage modifications are substantive)."* A modification is substantive if it changes what the document binds, permits, or prohibits. Cosmetic modifications (typography, formatting, citation correction without semantic change) do not trigger the "Modified by" field.

## 6. Non-prescription clause (inheritance)

All documents in this repository inherit the §0a non-prescription clause from `docs/scoping/human-timescales-scoping-v0.2.md`:

> This document describes minimum coordination timescales as observed phenomena. It does not endorse them as correct, optimal, or politically legitimate. **A floor is not a target.** Any extracted prescriptive use is unauthorised.

Documents that depart from this discipline must declare the departure explicitly in their endorsement marker.

**Hybrid inheritance** (per Council 2026-017, RT-2026-006 Q4 ruling). Inheritance is implicit by default. Documents that engage directly with prescription-eligible questions — those where a careful but non-deep reader could plausibly mistake methodological description for policy prescription — must carry an explicit reference to the §0a non-prescription clause in their opening section. Test for the explicit-reference requirement: would a non-deep reader, encountering this document outside its repository context, plausibly read methodological claims as prescriptive? If yes, explicit reference required. Application: TC-cards engaging policy-relevant outcomes (most TC-cards) → required. Bibliography fill memos, methodology-only protocols → implicit inheritance sufficient.

## 7. Review-tasks framework

(Per Council 2026-017, RT-2026-006 Q5(a) ruling. Established by Council decision 2026-011.)

Substantive review of artefacts (task cards, protocols, briefs, ledger entries, datasets, framework documents) issues as a Review Task (RT-NNNN, sequential). Each Review Task lodges as:

- (i) a brief artefact, drafted in the issuing stance and naming the target stance(s);
- (ii) one or more response artefacts, one per target stance ruling.

Briefs follow the pre-staging discipline DRAFT pre-stage → DRAFT issuance-ready → ACTIVE on user/Council confirmation; smell-test review at pre-stage is recommended for substantive briefs and may be skipped only for procedural ones. Per-jurisdiction split is permitted where target stances rule on independent question sets; verdicts may then issue independently. Each Review Task is logged at `meta/review-tasks/README.md` (issuance entry) and `meta/stance-log.md` (per-stance turns).

**Self-issuance reframe-permission.** Where issuing stance and target stance share agent identity, the brief invokes the reframe-permission clause: target stance is empowered to reject or re-frame any question, not only to rule on options as presented.

## 8. Tracker artefact types

(Per Council 2026-017, RT-2026-006 Q5(b) ruling. Cross-references §3 append-only-tracker carve-out.)

Three tracker artefact types are operationally distinguished and non-substitutable:

- **Falsification handles (FH-NNN)** — claim-level falsification predicates lodged in `meta/falsification-tracker.md`.
- **Horizon signals (SF-NNN)** — emergent risks or opportunities outside immediate falsification scope, lodged in `meta/horizon-signals.md` by Scout stance per Council decision 2026-011.
- **Risk-register entries (R-N)** — methodological or operational risks scoped to a specific deliverable, lodged in that deliverable's risk-register section.

A horizon signal is not a falsification handle reformulated, and a risk-register entry is not a horizon signal scoped down. Cross-tracker linkage is permitted (and encouraged) when the same underlying concern surfaces in more than one tracker; cross-links must be lodged bidirectionally to prevent asymmetric drift.

## 9. T4 kill-criterion (causal-geometry vocabulary)

Where ADM-EC causal-geometry vocabulary (a working internal framework: L_source, L_apparatus, L_comparison, η_opt) is used, the document must produce at least one prediction or distinction unavailable from prior frameworks. If it merely re-describes, it is dropped, not decorated.

This is operative for `docs/sails/` essays and any cross-domain mapping.

## 10. Falsification discipline

Every claim asserted in this repository carries:
- An explicit statement of what would weaken or falsify it.
- Where applicable, a binding falsification timeline.
- A trail to `meta/falsification-tracker.md`.

Soft formulations (e.g., "rarely", "tends to", "may only") are flagged for revision toward falsifiable structure.

## 11. Breakwater discipline

Claim-ledger entries (`ledger/`) follow Breakwater Schema v1.0-rc:

- Claim → Predictions → Constraints → Comparison → Classification.
- Three-value classification: COMPATIBLE / UNDERDETERMINED / INCONSISTENT.
- UNDERDETERMINED requires Discriminant Condition + feasibility flag.
- No post-verdict text.
- Self-reference exclusion.
- Anti-aggregation: classifications are independent.

## 12. Logbook discipline

Logbook entries (`logbook/`) are dated, append-only, and cross-reference artifacts touched. Template in `logbook/_template.md`.

## 13. Language

- **Working language:** Oxford British English (centre, organisation, recognise, behaviour).
- **Inline citations:** parenthetical author-date for academic references; explicit URL for online sources.
- **Mathematical notation:** UTF-8 inline (η, τ, L₅) preferred over LaTeX where possible; LaTeX permitted for complex expressions.

## 14. Data file formats

- Tabular: CSV (UTF-8, comma delimiter, RFC 4180), or TSV with explicit declaration.
- Structured: YAML or JSON.
- Documents: CommonMark Markdown.
- No proprietary formats committed to the repository.

## 15. File size and Git LFS

- Files >50 MB should not be committed to standard Git history. Use Git LFS or external archival.
- Raw archival material (e.g., scanned council documents) goes to external repositories with DOI; this repository carries metadata and processed extracts only.

## 16. Commits

- Commit messages follow Conventional Commits where practical (`feat:`, `docs:`, `data:`, `fix:`).
- Substantive content commits cross-reference the relevant task card (`TC-NN`) where applicable.

---

*Document control. v0.3.0 · 2026-04-29 · Stance: Guardian (drafting). Reviewed by: Architect 2026-04-29, Verifier 2026-04-29. Modified by: Architect 2026-04-29 (Q1 §3 append-only-tracker carve-out; Q2 §4 stance reclassification; Q3 §5 "Modified by" extension; Q4 §6 hybrid inheritance; Q5(a) new §7 review-tasks framework; Q5(b) new §8 tracker artefact types; Q5(c)-1 §4 stance-log cadence sub-clause), Verifier 2026-04-29 (Q8.5 ADM-EC clarification: §4 in-line Core Function definitions, §9 working-framework label).*
