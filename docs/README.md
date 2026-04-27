# Documentation

This directory holds the programme's written artifacts. Subdirectories separate document types per stance discipline and Breakwater protocol.

## Subdirectories

| Path | Purpose |
|---|---|
| `scoping/` | Versioned scoping documents. The current canonical scoping is `human-timescales-scoping-v0.2.md`. |
| `memos/` | Working memos: focused investigations of single threads, conjectures, or boundary cases. |
| `protocols/` | Binding methodological protocols. Specify operational rules; carry no empirical claim of their own. |
| `task-cards/` | Operational task cards specifying empirical pilots, methodological work, and synthesis deliverables. |
| `sails/` | Sail essays — interpretive arguments and applications of framework vocabulary. T4 kill-criterion applies. |
| `ledger-drafts/` | Draft Breakwater claim-ledger entries before submission to `../ledger/`. |

## Document type discipline

- **Scoping documents** define the programme's hypotheses, methodology, and risks. They are versioned (v0.1, v0.2, ...).
- **Memos** investigate specific threads or conjectures. They feed scoping document revisions and Breakwater entries.
- **Protocols** specify binding operational rules (e.g., commensurability, sub-typing, latency tracking). A protocol that begins to argue is split: argument → memo, rules → protocol.
- **Task cards** are self-contained operational specifications. Each carries a falsification handle where applicable.
- **Sails** are interpretive essays. Where they invoke ADM-EC vocabulary, the T4 kill-criterion applies.
- **Ledger drafts** are pre-submission Breakwater entries. Final versions move to `../ledger/`.

## Cross-referencing

Documents reference each other by relative path. Task cards reference parent scoping section IDs (e.g., "v0.2 §5 M1"). Ledger entries reference task cards by ID (TC-NN).

## FAIR reminders

- Every document carries a document-control section and stance log.
- Every claim carries a falsification handle.
- Documents inherit the non-prescription clause from the canonical scoping document unless they explicitly declare departure.

---

*v0.1 · 2026-04-27.*
