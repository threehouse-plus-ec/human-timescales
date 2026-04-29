# Verifier-stance review response — RT-2026-006 (CONVENTIONS.md + FAIR.md ratification)

**Date:** 2026-04-29
**Stance:** Verifier (source-grounding and standards-compliance jurisdiction)
**Responding to brief:** RT-2026-006 (`governance-ratification-architect-verifier-review-v0.1.md` — DRAFT pre-stage at time of response; v0.2 issuance-ready lodged same day after Architect smell-test).
**Documents reviewed:** `CONVENTIONS.md`, `FAIR.md`, `CHANGELOG.md`, `CITATION.cff`, `LICENSE.md` — all at v0.2.2 in-tree state (commit `41d8169`).
**Status note.** Response lodged during DRAFT pre-stage of v0.1 brief; substance is durable across the v0.1 → v0.2 brief revision (Q8–Q10 wording unchanged in v0.2). Formal ratification of this response stands at the issuance Council decision when RT-2026-006 moves DRAFT → ACTIVE.

Verifier rules from the position that source-grounding and standards-compliance claims must be operationally testable, externally interpretable, and consistent between asserted and realised state. Findings below separate confirmed compliance, minor deviations (non-blocking), and binding violations (blocking for full ratification).

---

## Q8 — External citation and standards-reference accuracy

### Q8.1 — FAIR Guiding Principles citation

**Claim:** Wilkinson et al. 2016, *Scientific Data* vol. 3, doi `10.1038/sdata.2016.18`.

**Verdict: ✓ Accurate and correctly cited.** This is the canonical FAIR reference. Citation format aligns with FAIR.md intent. No correction required.

### Q8.2 — Keep a Changelog reference

**Claim:** `https://keepachangelog.com/en/1.1.0/` (CHANGELOG.md header).

**Verdict: ✓ Correct and current.** v1.1.0 is the latest stable specification; no newer formal release supersedes it.

### Q8.3 — Semantic Versioning reference

**Claim:** `https://semver.org/spec/v2.0.0.html` (CHANGELOG.md header).

**Verdict: ✓ Correct.** v2.0.0 remains the canonical SemVer spec.

### Q8.4 — CITATION.cff schema version

**Claim:** `cff-version: 1.2.0`.

**Verdict: ✓ Correct and current.** v1.2.0 is the latest official CFF schema version. **Minor issue (non-blocking):** full schema compliance must be machine-validated; human inspection alone is insufficient. See Q10.

### Q8.5 — "ADM-EC Constitution" reference

**Status: ❗ Undefined reference (BLOCKING).**

Appears multiple times in CONVENTIONS.md (notably §4, §5). Not present as: a repository document; a formally cited external publication; or a resolvable standard.

**Verifier classification:** Ambiguous authority reference.

**Required clarification (blocking for full ratification).** Declare exactly one of:

- **(a) Internal artefact.** Add explicit definition in CONVENTIONS.md and remove implication of external authority.
- **(b) External document.** Add full citation (author, version, location) and include in `CITATION.cff` `references` block or a CONVENTIONS appendix.
- **(c) Working term.** Rephrase to avoid "Constitution" authority implication (e.g., "Council-3 deliberation discipline" without external reference).

**Verdict:** → Binding correction required before ratification.

---

## Q9 — License triple compliance

### Q9.1 — License definitions in LICENSE.md

- **CC BY 4.0** — ✓ Correct standard reference.
- **Apache-2.0** — ✓ Correct standard reference.
- **CC0 1.0** — ✓ Correct standard reference.

### Q9.2 — Apache-2.0 "(when added)" clause

**Issue:** ambiguous trigger condition; not operationally testable.

**Required fix (non-blocking).** Define explicitly: what qualifies as "code"; where the license is declared (e.g., `/src/` subtree).

**Verdict:** ⚠ Minor structural ambiguity (non-blocking; patch acceptable post-ratification).

### Q9.3 — Data licensing boundary

**Current rule:** "CC0 where copyright would not apply; CC BY for compiled datasets."

**Issue:** "where copyright would not apply" is not operationally decidable; jurisdiction-dependent; introduces ambiguity in reuse.

**Verifier ruling: ❌ Not sufficiently testable. BLOCKING.**

**Required fix (one of):**
- Define default license per dataset class (raw / processed / compiled), OR
- Require explicit per-dataset license declaration in each `data/{dataset}/README.md`.

### Q9.4 — Per-artefact license marking

**Current state:** LICENSE.md defines global policy; artefacts are not individually marked.

**Verifier ruling: ❌ Non-compliant with FAIR Accessibility (A1). BLOCKING.**

FAIR requires *clear, accessible license information per resource*. Inheritance via top-level LICENSE.md is insufficient on its own; each resource must either carry a license header or inherit via an explicitly declared mechanism that a downstream consumer can interpret without context.

**Required fix (binding):** Each artefact MUST carry a license header OR inherit via an explicitly declared mechanism documented in CONVENTIONS.md or LICENSE.md.

### Q9 summary

| Item | Status |
|---|---|
| License texts | ✓ correct |
| Apache "when added" | ⚠ ambiguous (non-blocking) |
| Data license boundary | ❌ not testable (blocking) |
| Per-artefact marking | ❌ missing (blocking) |

**Verdict:** → Two binding corrections required for ratification (Q9.3 and Q9.4); one non-blocking item (Q9.2).

---

## Q10 — Standards-compliance claims vs. actual compliance

### Q10.1 — CHANGELOG format compliance with Keep a Changelog v1.1.0

**Observed deviations:** not all releases consistently structured with Added / Changed / Fixed / etc. headers; backfilled entries (the consolidated `[0.2.0]` entry covering 17 commits) violate chronological-integrity and incremental-discipline norms of Keep a Changelog.

**Verifier ruling: ❌ Partial non-compliance.**

**However.** Current state is now recoverable and aligned going forward. `[0.2.1]` and `[0.2.2]` entries follow the Added/Changed/Resolved/Outstanding structure correctly.

**Classification:** → Non-blocking (historical deviation, now corrected; future entries audit-trackable).

### Q10.2 — Semantic Versioning compliance

| Version | Audit's classification | Verifier verdict |
|---|---|---|
| 0.2.0 | MINOR (added functionality) | ✓ |
| 0.2.1 | PATCH (backwards-compatible fix) | ✓ |
| 0.2.2 | PATCH (metadata + tracker discipline) | ✓ |

**Verifier ruling: ✓ SemVer-compliant.** Pre-1.0 semantics allow flexibility; no violations detected.

### Q10.3 — FAIR compliance claim (FAIR.md)

**Critical observation.** FAIR.md states operational compliance with FAIR principles, but the realised state shows: (i) not all `data/` subdirectories carry schemas (`data/defunct-archives/` is a placeholder); (ii) license marking is incomplete (per Q9.4); (iii) schema formats are not standardised to a machine-readable specification (per Q8.4 / Q10.4).

**Verifier ruling: ❌ Overstated compliance claim. BLOCKING.**

**Required correction.** Replace any wording asserting *"repository complies with FAIR principles"* with *"repository implements a FAIR-aligned operational framework; full compliance is a target state."* Or equivalent wording that distinguishes asserted alignment from achieved compliance.

**Verdict:** → Binding wording correction required before ratification.

### Q10.4 — CITATION.cff schema compliance

**Status:** declared `cff-version: 1.2.0` is correct; full schema compliance not yet machine-validated.

**Verifier requirement:** must be validated against the official CFF v1.2.0 schema (e.g., via `cffconvert --validate` or equivalent).

**Verdict:** ⚠ Pending machine validation (non-blocking if scheduled for the post-ratification patch cycle).

---

## Final Verifier verdict

### Blocking issues (must be resolved before ratification)

1. **ADM-EC Constitution ambiguity** (Q8.5) — declare internal / external / working-term and remediate accordingly.
2. **Per-artefact license marking absent** (Q9.4) — add license headers or declare an explicit inheritance mechanism.
3. **Data license boundary not operationally defined** (Q9.3) — replace "where copyright would not apply" with operationally testable per-class defaults or per-dataset declarations.
4. **FAIR compliance overstated** (Q10.3) — soften wording from "complies with" to "aligned with / target state".

### Non-blocking issues (patch acceptable post-ratification)

- Apache-2.0 "(when added)" clarification (Q9.2).
- CHANGELOG historical deviations from Keep a Changelog (Q10.1) — already corrected going forward.
- CITATION.cff machine validation against CFF v1.2.0 schema (Q10.4) — schedule for post-ratification patch.

---

## Overall judgement

**Ratification status: CONDITIONAL.**

The documents are structurally sound and standards-aware. However, they currently:
- overstate compliance (Q10.3);
- contain ambiguous authority references (Q8.5);
- lack operational clarity in licensing (Q9.3, Q9.4).

These are not superficial issues — they affect external interpretability and reuse guarantees, i.e., core Verifier jurisdiction.

---

## Minimal remediation set (recommended)

To unlock ratification:

1. Resolve ADM-EC reference (define or cite or re-phrase).
2. Add per-artefact license mechanism (header or declared inheritance).
3. Make dataset licensing explicit and testable (per-class defaults or per-dataset declaration).
4. Downgrade FAIR claim to "aligned / in progress".

---

## Verifier offer (pending response-Architect or Council direction)

Verifier offers to draft the exact patch text for:
- **CONVENTIONS.md §4** (ADM-EC clarification — remediation per Q8.5).
- **FAIR.md** compliance-claim wording (Q10.3 remediation).
- **LICENSE.md** operational rules for datasets and per-artefact marking (Q9.3 + Q9.4 remediation).

If accepted, this would allow immediate transition to v0.3.0 (or whatever SemVer level applies per the v0.2 brief's §7 item 5) without another Verifier review cycle. Architect or Council to confirm acceptance of the offer.

---

## Citation-Violation flags

One flag raised per FAIR.md citation-discipline: Q8.5 (ADM-EC Constitution ambiguity) constitutes a Citation: Violation of Authority insofar as the term implies external standing without source.

---

## Document control

- **v0.1** (2026-04-29): Initial Verifier response on RT-2026-006 v0.1 brief at DRAFT pre-stage. Q8 (five sub-findings, four ✓ + one ❌); Q9 (four sub-findings, one ✓ + one ⚠ + two ❌); Q10 (four sub-findings, one ❌ historical-recoverable + one ✓ + one ❌ + one ⚠ pending). Four blocking issues identified; three non-blocking. Ratification verdict: CONDITIONAL. Verifier offers to draft remediation patches.
- **Pending:** Formal ratification of this response at RT-2026-006 issuance Council decision (response substance is durable across v0.1 → v0.2 brief revision since Q8–Q10 wording is unchanged in v0.2).
- **Linked:** `governance-ratification-architect-verifier-review-v0.1.md` (target brief at time of response); `governance-ratification-architect-verifier-review-v0.2.md` (issuance-ready brief, same Q8–Q10 wording); `governance-ratification-architect-smell-test-v0.1.md` (parallel Architect smell-test on same v0.1 brief).

**Stance log.** Drafted Verifier. Disposition: CONDITIONAL ratification. Four binding violations require remediation before unconditional ratification; Verifier offers to draft patch text for response-Architect or Council acceptance.

---

*Verifier-stance review response. ~1100 words. CONDITIONAL ratification verdict pending blocking-issue remediation.*
