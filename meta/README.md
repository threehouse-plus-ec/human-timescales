# Meta — Cross-Cutting Tracking Artifacts

This directory holds artifacts that span the programme as a whole rather than belonging to any single document, dataset, or task card.

## Files

| File | Purpose |
|---|---|
| `stance-log.md` | Running log of stance invocations across the programme. Populated from logbook entries. |
| `council-decisions.md` | Substantive decisions taken under Council deliberation, with date, stance composition, and decision text. |
| `falsification-tracker.md` | All falsification handles installed across the programme, with target dates, status, and resolution. |

## Discipline

- **Append-only structure** for all three files. Entries are added; entries are not modified except for typo corrections.
- **Cross-reference discipline.** Every entry references the artifacts it concerns by relative path.
- **Self-contained entries.** Each entry is comprehensible without external context (modulo cross-references).

## Why this is separate

These artifacts are repository-wide accountability infrastructure. Embedding them inside individual documents would make accountability invisible at programme scope. Separating them makes the programme's deliberation history, decision history, and falsification history independently auditable.

This separation is itself a Guardian-stance commitment: opacity at programme scope is a Citation: Violation of Clarity risk, and these files preempt it.

---

*v0.1 · 2026-04-27.*
