# T10 — Technical-Coordination Archive Characterisation

**Task card:** TC-04 (T10 archive characterisation, 3+ institutions).
**Parent:** scoping v0.2 §2 T10; T10 mechanism conjecture memo §6, §8, §9.
**Status:** Placeholder. Awaits TC-04 commissioning.
**Target completion:** 2027-06-30 (binding per T10 memo §9).

## Purpose

To compile layered archival data from at least three technical-coordination institutions, separating *technical-decision events* (fast layer) from *governance/legitimacy events* (slow layer), enabling tests of the M-Conjecture: technology operates on connectivity and reconciliation rate of knowledge stores, not on legitimacy-transfer.

## Recommended institutions

- **IETF** — RFC throughput per decade (technical layer) vs. governance evolution (IETF Administration LLC formation 2018, IAB structural reforms).
- **W3C** — Specification cycle times (technical layer) vs. 2023 reorganisation lead-up (governance layer).
- **ICANN/IANA** — Continuous IANA functions (technical layer) vs. 1998–2016 stewardship transition (governance layer).
- **Optional fourth: IAU** — Long-cycle technical-community case (e.g., 2006 Pluto reclassification and lead-up).

## Layered structure

The dataset must distinguish two event classes per institution:

- **Technical-layer events** — specifications produced, RFCs issued, recommendations published, etc. High-frequency, infrastructure-bound.
- **Governance-layer events** — charter revisions, mandate transitions, accountability reforms, sovereignty transitions. Low-frequency, legitimacy-bound.

Conflation invalidates the test.

## Source

Public archives:
- IETF: RFC index, IAB minutes, IETF Administration LLC documentation.
- W3C: Recommendation track, governance documents, 2023 reorganisation announcements.
- ICANN: Bylaws history, IANA stewardship transition documents (NTIA, ICANN, ISOC archives).

## Coverage

- **Temporal:** institution-specific. IETF from ~1986; W3C from 1994; ICANN from 1998; IAU from 1919.
- **Per-event fields:** see `schema.md`.

## Known limitations

- **Multi-domain legitimacy assessment:** ICANN's status is contested. The dataset must declare its criterion in writing (see QM1 in T10 memo).
- **Governance-event identification:** distinguishing genuine governance reform from administrative adjustment is itself a TC-07-class problem applied to T10.
- **Technical-layer throughput:** RFC count is a coarse proxy; refinement to weight by significance is a Sail-effort task.

## Licence

To be declared on dataset completion. Recommended: CC0 for raw event compilations; CC BY 4.0 for compiled, layered, sub-typed dataset.

## Cross-references

- Schema: `schema.md`
- Task card: `../../docs/task-cards/human-timescales-task-cards-v0.1.md` (TC-04)
- Memo: `../../docs/memos/t10-mechanism-conjecture-memo-v0.1.md`

---

*v0.1 placeholder · 2026-04-27.*
