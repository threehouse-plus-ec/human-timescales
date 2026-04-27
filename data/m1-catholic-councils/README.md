# M1 — Catholic Ecumenical Councils

**Task card:** TC-01 (Empirical pilot: Catholic Ecumenical Councils Archaeology).
**Parent:** scoping v0.2 §5 M1, §11 S3.
**Status:** Placeholder. Awaits methodological prerequisites TC-06 (commensurability protocol) and TC-07 (reform-event sub-typing).
**Target completion:** 2026-12-31 (binding per scoping v0.2 M5).

## Purpose

To compile a structured, sub-typed, dated record of all Catholic ecumenical councils from Nicaea I (325) to Vatican II (1962–65), enabling tests of:
- Stationarity of inter-event intervals across the 16-century window (against constant Poisson and shock-clustered null models).
- Sub-type-stratified intervals (doctrinal / structural / disciplinary) to test whether L₅ stationarity holds within sub-types.
- Hypothesis H₀ at the L₅ legitimacy-transfer-generation scale.

## Source

Primary: ecumenical council records as recognised by the Catholic Church (21 events, Nicaea I 325 → Vatican II 1965).

Secondary: historiographic literature on contested council status (e.g., Pisa 1409, recognition variations between Catholic and Orthodox traditions for early councils).

## Coverage

- **Temporal:** 325 CE → 1965 CE.
- **Events:** 21 ecumenical councils (per Catholic recognition).
- **Per-event fields:** see `schema.md`.

## Collection method

To be specified by TC-01 drafter. Recommended:
1. Compile event list from Catholic Encyclopedia / Vatican archives.
2. Sub-type each event per TC-07 protocol.
3. Annotate external-shock context (e.g., Reformation precedes Trent; modernity precedes Vatican I/II).
4. Apply commensurability protocol per TC-06.
5. Compute inter-event intervals.
6. Run null-model tests.

## Known limitations

- **Disputed status:** Some councils (Pisa 1409, Constantinople IV 869–870) have contested ecumenical status across traditions. Inclusion criterion must be declared in writing.
- **Sub-typing ambiguity:** Many councils combine doctrinal, structural, and disciplinary work. Multi-tagging is required; collapse is not permitted.
- **Coverage gaps:** Documentary survival is not uniform across centuries. Coverage correction is a Sail-effort task within this pilot.
- **Survivorship bias:** The Catholic Church is a surviving institution. The defunct-archive control (TC-08) addresses the bias structurally; this dataset does not correct it internally.

## Licence

To be declared on dataset completion. Recommended: CC0 for the raw event list (factual public-domain dates and titles); CC BY 4.0 for compiled and sub-typed dataset.

## Provenance discipline

Every record will trace its source. Where multiple sources disagree on dates or status, all sources are recorded and the resolution is noted.

## Cross-references

- Schema: `schema.md`
- Task card: `../../docs/task-cards/human-timescales-task-cards-v0.1.md` (TC-01)
- Scoping: `../../docs/scoping/human-timescales-scoping-v0.2.md` (§5 M1)
- Methodological prerequisites: TC-06 (commensurability), TC-07 (reform-event sub-typing)
- Survivorship control: TC-08

---

*v0.1 placeholder · 2026-04-27. To be replaced by data-bearing v0.2 on TC-01 completion.*
