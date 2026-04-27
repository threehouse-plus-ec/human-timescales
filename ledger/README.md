# Breakwater Claim Ledger

This directory holds submitted Breakwater claim-ledger entries. Drafts in progress live in `../docs/ledger-drafts/`.

## Breakwater protocol

Per the Breakwater Layer architecture (referenced from the broader Open-Science Harbour ecosystem):

- The Claim Analysis Ledger is **outside the Harbour core**. It measures claims; it never routes, ranks, or aggregates.
- Outputs are purely descriptive.
- **Self-reference exclusion:** a ledger entry cannot reference its own classification recursively.
- Schema v1.0-rc structure: **Claim → Predictions → Constraints → Comparison → Classification.**
- Three-value classification: **COMPATIBLE / UNDERDETERMINED / INCONSISTENT.**
- UNDERDETERMINED requires a Discriminant Condition and a feasibility flag.
- No post-verdict text.
- Selection mode: REQUEST / SWEEP. Domain and (optional) scope declared.
- **Anti-aggregation:** classifications are independent. Self-audit cannot alter past classifications.

## Entry naming

Entries are named by date and short ID: `YYYY-NNN-short-name.md` (e.g., `2026-001-h0-l5-stationarity.md`).

The numbering is sequential within a calendar year; new entries get the next available number.

## Active entries

- *(none yet)*

## Pending drafts

- TC-09 — three-claim package (H₀ + H₁ + M). Drafted in `../docs/ledger-drafts/` after TC-01 pilot data and TC-04 partial completion.

## FAIR discipline

Each ledger entry:

- [ ] Declares its claims explicitly.
- [ ] Declares predictions, constraints, and discriminant condition.
- [ ] Carries a feasibility flag where UNDERDETERMINED.
- [ ] Cross-references parent task cards and source documents by relative path.
- [ ] Is dated and version-stamped.
- [ ] Carries a stance log.

## What this ledger is not

- It is not a register of opinions.
- It is not a knowledge base.
- It is not a decision log (decisions live in `../meta/council-decisions.md`).

It is a measurement record of claims under explicit protocols.

---

*v0.1 · 2026-04-27.*
