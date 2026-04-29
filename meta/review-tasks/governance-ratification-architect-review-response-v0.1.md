# Architect-stance review response — RT-2026-006 v0.2 (CONVENTIONS.md + FAIR.md ratification)

**Date:** 2026-04-29
**Stance:** Architect (methodological-rigour, internal coherence; per-jurisdiction primary on §3, §4, §5, §6 of CONVENTIONS and on FAIR.md operational structure)
**Responding to brief:** RT-2026-006 v0.2 (`governance-ratification-architect-verifier-review-v0.2.md` — DRAFT issuance-ready)
**Inputs taken as binding:**
- Architect smell-test on v0.1 (`governance-ratification-architect-smell-test-v0.1.md`) — all ten observations applied in v0.2; no further framing-rejection invoked under §2 reframe-permission clause.
- Verifier response on Q8–Q10 (`governance-ratification-verifier-review-response-v0.1.md`) — noted as Verifier-jurisdiction; out of scope for this turn. Verifier's blocking issues remain outstanding pending patch acceptance.
- Architect's draft-text rulings below are prospective-only per §6 default; prior Council decisions stand under conventions-as-applied at the time.

---

## A — Analog

Ratification is the moment the scaffolding comes off and the wall is declared load-bearing. The wall has been bearing weight for two days; what ratification does is not change what it carries but acknowledge what it has carried, with corrective patches where the carried weight has stressed the design beyond the as-drafted specification. Six of the seven rulings below patch; one (Q2) re-pours.

---

## D — Digital. Per-question rulings.

### Q1 — §3 append-only-tracker carve-out

**Ruling: option (a), modified.** Explicit append-only-tracker carve-out, with language general enough that future log-shaped artefacts fitting the same structural pattern can claim the exemption without §3 re-amendment. Option (c) rejected (operationally infeasible at the observed entry rate). Option (b) rejected (CONVENTIONS.md should not stay silent on a recurring exception class). Option (d) absorbed in spirit but not in form (broader carve-out introduces a definitional question — "what is a log-shaped artefact?" — that the narrow form avoids).

**Draft §3 sub-clause (additional paragraph):**

> *Append-only trackers — substantive documents whose form is a chronologically-accumulating sequence of independently-dated entries, where the entry history itself constitutes the change log — are exempt from the per-version document-control fields above. Such trackers instead carry a tracker-type header declaring: document type, established date, custodial stance, entry-numbering convention, and a document-control deviation note acknowledging this carve-out. Future artefact classes claiming this exemption must demonstrate the append-only structural pattern in their tracker-type header; classes that diverge from the pattern require §3 amendment.*

The four current tier-4 tracker headers stand without re-drafting (verified: each declares document type, established date, custodial stance, deviation note; entry-numbering convention is implicit and should be added at the next housekeeping pass — non-blocking).

### Q2 — §4 stance classification

**Ruling: option (a).** Reclassification, not patching. "Advisory flags" is a misdescription of operational reality; corrective sub-clauses (option b) preserve the misdescription as headline. Option (c) rejected on accuracy grounds, independently of the rescue-surface caveat.

**Draft §4 replacement wording (first paragraph):**

> *Functional stances: Guardian, Architect, Integrator constitute the Council-3 deliberation core. Per-jurisdiction primary stances: Scout (horizon-signal jurisdiction) and Verifier (source-grounding jurisdiction) issue rulings primary within those jurisdictions, ratified by Council decision. The Council-3 core retains cross-jurisdiction veto authority per Article III; per-jurisdiction primaries do not. All five stances operate under the stance-invocation, one-stance-at-a-time, and veto-justification disciplines below.*

**Retrospective scope:** prospective-only per §6 default. Prior Council decisions ratifying Scout and Verifier rulings (2026-011, 2026-012) stand; the reclassification changes the framing under which future rulings are evaluated, not the validity of past ones. Lodge as explicit declaration in the ratification Council decision.

### Q3 — §5 Endorsement Marker (compliance + post-ratification wording)

**Ruling on compliance spot-check:** Architect cannot do file-by-file inspection in this turn; structural ruling instead. §5 binds all framework documents — definitionally:

- Scoping, protocol, memo artefacts: framework documents, must carry markers.
- Task-card snapshots (frozen and current): framework documents, must carry markers.
- Review-task briefs and responses: framework documents (they issue or solicit binding rulings), must carry markers.
- Meta trackers: not framework documents in §5 sense; they are governance records and carry the tracker-type header per Q1 carve-out.

Issuance commit must include a literal spot-check across the file paths listed in v0.2 §3 Q3; any non-compliance lodges as a remediation patch within the same release.

**Ruling on post-ratification wording:** §5 extended with "Modified by" field. Activation rule: substantive review-stage modifications trigger; cosmetic do not.

**Draft §5 extension:**

> *Post-review Endorsement Markers take the form: "Stance: [drafter] (drafting). Reviewed by: [reviewer-stance(s)] [date(s)]. Modified by: [stance(s)] [date(s)] (where review-stage modifications are substantive)." A modification is substantive if it changes what the document binds, permits, or prohibits. Cosmetic modifications (typography, formatting, citation correction without semantic change) do not trigger the "Modified by" field.*

For RT-2026-006 itself: Architect modifications under Q1, Q2, Q5(a), Q5(b), Q5(c) are substantive. Post-ratification Marker on CONVENTIONS.md reads: *"Stance: Guardian (drafting). Reviewed by: Architect [date], Verifier [date]. Modified by: Architect [date]."* FAIR.md: substantive modifications under Q6 (definitional split) and Q7 (three-tier checklist restructure) — same Marker structure.

### Q4 — §6 non-prescription clause inheritance

**Ruling: hybrid.** Implicit inheritance via §6 declaration is structurally sufficient for documents whose content is methodological or descriptive. Explicit per-document reference is required for documents that bear directly on prescription-eligible questions — that is, documents where a non-deep reader could plausibly mistake content for policy prescription.

**Draft §6 extension:**

> *Inheritance is implicit by default. Documents that engage directly with prescription-eligible questions — those where a careful but non-deep reader could plausibly mistake methodological description for policy prescription — must carry an explicit reference to §0a in their opening section.*

**Test for explicit-reference requirement:** would a non-deep reader, encountering this document outside its repository context, plausibly read methodological claims as prescriptive? If yes, explicit reference required. Application: TC-cards engaging policy-relevant outcomes (most TC-cards) → required. Bibliography fill memos, methodology-only protocols → implicit inheritance sufficient.

Per-file audit delegated to issuance commit, parallel to Q3 spot-check.

### Q5 — Missing conventions

**Q5(a) — review-tasks framework codification: ruling YES.** Add new §7.

**Draft §7:**

> *§7 Review-tasks framework. Substantive review of artefacts (task cards, protocols, briefs, ledger entries, datasets, framework documents) issues as a Review Task (RT-NNNN, sequential, established by Council decision 2026-011). Each Review Task lodges as: (i) a brief artefact, drafted in the issuing stance and naming the target stance(s); (ii) one or more response artefacts, one per target stance ruling. Briefs follow the pre-staging discipline DRAFT pre-stage → DRAFT issuance-ready → ACTIVE on user/Council confirmation; smell-test review at pre-stage is recommended for substantive briefs and may be skipped only for procedural ones. Per-jurisdiction split is permitted where target stances rule on independent question sets; verdicts may then issue independently. Each Review Task is logged at meta/review-tasks/README.md (issuance entry) and meta/stance-log.md (per-stance turns). Self-issuance — issuing stance and target stance share agent identity — invokes the reframe-permission clause: target stance is empowered to reject or re-frame any question, not only to rule on options as presented.*

**Q5(b) — tracker artefact types codification: ruling YES.** Add new §8 (preferred over §7.x to keep §7 focused on review-tasks).

**Draft §8:**

> *§8 Tracker artefact types. Three tracker artefact types are operationally distinguished and non-substitutable:*
> - *Falsification handles (FH-NNN) — claim-level falsification predicates lodged in `meta/falsification-tracker.md`.*
> - *Horizon signals (SF-NNN) — emergent risks or opportunities outside immediate falsification scope, lodged in `meta/horizon-signals.md` by Scout stance per Council decision 2026-011.*
> - *Risk-register entries (R-N) — methodological or operational risks scoped to a specific deliverable, lodged in that deliverable's risk-register section.*
>
> *A horizon signal is not a falsification handle reformulated, and a risk-register entry is not a horizon signal scoped down. Cross-tracker linkage is permitted (and encouraged) when the same underlying concern surfaces in more than one tracker; cross-links must be lodged bidirectionally to prevent asymmetric drift.*

**Q5(c) — free-form audit, ≤3 cap.** Architect proposes one new convention here; two further candidates route to RT-2026-007 to keep RT-2026-006 closeable.

**Proposed (Q5(c)-1): Stance-log cadence.** Add as §4 sub-clause:

> *Stance-log entries are mandatory at: (i) brief issuance (issuing stance), (ii) ruling lodgement (target stance), (iii) veto invocation (vetoing stance). Optional but encouraged for: smell-test responses, framing-rejection invocations, and Integrator coordination decisions. Cadence violations surface in audit as observation-class findings.*

This codifies what currently happens by participant memory; absent the rule, drift is invisible until audit catches it.

**Routed to RT-2026-007:**
- *Decision-register-citation verification.* Council decisions are referenced by number throughout artefacts; no convention currently requires the cited number to exist or to bind what is claimed. Tracker-discipline gap.
- *Cross-tracker linkage symmetry enforcement.* Q5(b) §8 requires bidirectional cross-links; no audit mechanism currently checks for asymmetric drift. Operational verification gap.

Both candidates are real but require operational testing before codification. Architect's recommendation: lodge RT-2026-007 within two weeks, scoped to these two plus any further candidates surfaced during the v0.3.0 release window.

### Q6 — FAIR operational claims

**Q6.1 — Definitional ruling: option (ii).** "Dataset" refers only to directories with non-placeholder content. Placeholder directories are "dataset slots" — operational-structural artefacts declaring intent, distinct from datasets bearing data.

**Q6.2 — Factual ruling, conditional on Q6.1(ii):**
- Findability claim *"every dataset carries a schema"*: compliant. `data/m1-catholic-councils/` and `data/t10-archive/` are datasets and carry schemas; `data/defunct-archives/` is a dataset slot per its README.
- Interoperability sub-question: schema-language acceptability needs explicit declaration in FAIR.md. **Architect ruling:** markdown-prose with structured YAML front-matter acceptable as short-term floor; formal schema language (JSON Schema, frictionless-data, or domain-equivalent) preferred medium-term and required for any dataset whose schema is referenced by code.

**Draft FAIR.md extension (Findability section):**

> *Datasets carry schemas. A dataset is a directory under `data/` containing non-placeholder content; a dataset slot is a placeholder directory awaiting content. Schema requirements bind on first content commit, not on slot creation. Schema language: markdown-prose with YAML front-matter is acceptable; formal schema languages (JSON Schema, frictionless-data) are preferred and required where schemas are referenced by code.*

### Q7 — FAIR checklists binding/aspirational

**Ruling: option (d), with three-tier structure.** Options (a) and (c) fail on opposite extremes. Option (b) is too narrow (most release commits are not Council decisions; most failed checklist runs were on routine commits).

**Draft FAIR.md re-structure (replacing current single-checklist form):**

> *Three commit-type tiers, each with its own checklist:*
>
> *Tier I — Working commits (commits that do not bump SemVer and do not ratify a Council decision). Pre-commit checklist is **aspirational**. Drift surfaces in audit as observation-class findings; non-completion does not block the commit.*
>
> *Tier II — Release commits (commits that bump SemVer, i.e., create a new release tag). Pre-release checklist is **binding**: CHANGELOG entry drafted; CITATION.cff date and version bumped; README closing-line bumped; outstanding items reconciled. Non-completion blocks the release tag.*
>
> *Tier III — Council-decision commits (commits that ratify a Council decision). Pre-decision checklist is **binding**: meta/council-decisions.md entry lodged with stance composition, brief reference, per-question rulings, modifications applied, audit-observation closure where applicable; meta/stance-log.md entries lodged for issuing and ruling stances; brief artefact reference linked. Non-completion blocks the decision-ratification commit.*

The 17-commit window gap between [0.1.0] and [0.2.0] would, under this structure, have surfaced at the release commit (Tier II) — which is where the audit eventually caught it. Post-hoc validation that the tiering matches operational reality.

---

## M — Memory

Closest precedent on stance-discipline reclassification is Council decision 2026-011 (Scout horizon-signal authority, ratified). The Q2 reclassification ratification proceeds in the same direction — making explicit what is already operationally true. No precedent for self-issuance ratification; RT-2026-006 sets it. The §2 reframe-permission clause in v0.2 is the convention for future self-issuance cases — codify it explicitly in the new §7 (drafted above as part of the §7 review-tasks framework).

---

## EC — Error-Correction. Consequences and residuals.

**SemVer declarations (per §7 item 5 of v0.2 brief).**
- CONVENTIONS.md: **MINOR bump** (v0.2.2 → v0.3.0). Substantive convention modifications added: Q1 §3 sub-clause, Q2 §4 reclassification, Q3 §5 "Modified by" extension, Q4 §6 inheritance refinement, Q5(a) new §7, Q5(b) new §8, Q5(c)-1 §4 stance-log cadence sub-clause.
- FAIR.md: **MINOR bump** (v0.2.2 → v0.3.0). Substantive: Q6 dataset/dataset-slot distinction, schema-language declaration; Q7 three-tier checklist restructure.

**Retrospective scope.** All rulings prospective-only per §6 default. Explicit declaration in the ratification Council decision: prior decisions stand under conventions-as-applied at the time; future decisions issue under v0.3.0 conventions.

**Issuance-commit checklist (Tier III binding, per Q7 ruling self-applied):**
1. Spot-check Q3 file-by-file Endorsement Marker compliance; remediation patch lodged in same release where non-compliance found.
2. Spot-check Q4 explicit-reference compliance for prescription-eligible documents; remediation patch lodged in same release.
3. Council decision lodged in `meta/council-decisions.md` (next available number) per §7 deliverable spec.
4. Stance-log entries lodged for Architect ruling (this turn) and Verifier ruling (already in).
5. CHANGELOG `[0.3.0]` entry drafted per Keep a Changelog format.
6. CHANGELOG `[0.2.2]` Outstanding closure moved to Resolved.

**Residual flags (no veto, no blocking from Architect jurisdiction):**
- Q1 tracker headers should add entry-numbering convention at next housekeeping pass (non-blocking; current headers compliant in substance).
- RT-2026-007 to be lodged within two weeks for Q5(c) routed candidates.
- Q6 medium-term migration to formal schema language is a horizon signal candidate (SF-12+) — Architect refrains from lodging unilaterally; Scout to consider.

**Out-of-jurisdiction note (Verifier blocking issues remain outstanding).** Architect rulings above do not override Verifier's CONDITIONAL ratification verdict. Four Verifier-blocking issues remain unresolved at this response: ADM-EC ambiguity (Q8.5), per-artefact license marking (Q9.4), data-license-boundary testability (Q9.3), FAIR overstated-compliance wording (Q10.3). Verifier offered to draft remediation patches; acceptance pending. Until Verifier patches are accepted and applied, the v0.3.0 ratification commit cannot reconcile both stances' verdicts. Architect's draft text above is the Architect-jurisdiction component of the eventual ratification; Verifier patches are the Verifier-jurisdiction component; both must land together in a single ratification commit.

**No Architect veto issued.** All seven rulings within structural-coherence jurisdiction; no Guardian clarity/ethics territory surfaced; no Integrator flow violations.

---

## Document control

- **v0.1** (2026-04-29): Initial Architect ruling on RT-2026-006 v0.2. Seven binding rulings: Q1 option (a)-modified with draft §3 sub-clause; Q2 option (a) with draft §4 replacement (reclassification, prospective-only); Q3 spot-check delegated to issuance + §5 "Modified by" extension drafted; Q4 hybrid inheritance rule with prescription-eligibility test; Q5(a)+(b) new §7 (review-tasks framework) and §8 (tracker artefact types) drafted; Q5(c) one new convention (stance-log cadence) with two routed to RT-2026-007 (decision-register-citation verification, cross-tracker linkage symmetry); Q6.1 dataset/slot distinction with FAIR.md draft; Q6.2 conditional compliance verified; Q7 three-tier checklist restructure drafted (Tier I aspirational, Tier II + III binding). CONVENTIONS.md and FAIR.md both at MINOR bump (v0.3.0). Prospective-only retrospective scope. No veto. Out-of-jurisdiction note: Verifier blocking issues remain unresolved; v0.3.0 ratification commit must reconcile both stances' verdicts.
- **Pending:** Verifier patch acceptance + drafting; integrated ratification commit applying both Architect and Verifier modifications; Council decision lodgement; v0.3.0 release.
- **Linked:** `governance-ratification-architect-verifier-review-v0.2.md` (target brief); `governance-ratification-architect-smell-test-v0.1.md` (Architect smell-test on v0.1, all observations applied in v0.2); `governance-ratification-verifier-review-response-v0.1.md` (parallel Verifier response, CONDITIONAL pending blocking-issue remediation).

**Stance log.** Drafted Architect. Disposition: seven rulings lodged with draft text; v0.3.0 SemVer declared for both files; ratification commit gated on Verifier patches landing in same commit per cascading-modification discipline (v0.2 §6 risk catch-all). No veto.

---

*Architect-stance review response. ~1900 words. Seven rulings + draft text + SemVer declarations. CLOSED on response receipt; ratification commit pending Verifier patches.*
