# Cross-Era Commensurability Protocol

**Version:** v0.1
**Stance:** Architect (drafting). Reviewers: Guardian (R8 temporal-parallax discipline) + Scout. Pending.
**Parent documents:** *Human-System Timescales: Scoping v0.2* (§5 M1, E3, R8); *Task Cards v0.1* (TC-06).
**Feeds:** TC-01 (Catholic ecumenical councils pilot — gating prerequisite); TC-04 (T10 archive characterisation — recommended).
**Date:** 2026-04-27

---

## 0. Endorsement Marker (provisional)

Internal methodological infrastructure. Not a Coastline. No external endorsement is asserted. This protocol is operational; it carries no empirical claim of its own. Its function is to fix the conditions under which downstream stationarity claims may be issued.

## 0a. Non-prescription clause (inherited)

Per `CONVENTIONS.md` §6 and `docs/scoping/human-timescales-scoping-v0.2.md` §0a. Reform-cycle measurements made under this protocol describe minimum coordination timescales as observed phenomena. They do not endorse any pace as correct, optimal, or politically legitimate. **A floor is not a target.**

---

## 1. Purpose

Reform-cycle archaeology (M1) requires inter-event interval measurements that are commensurable across centuries. The premise that calendar-year intervals are simply commensurable across the 16-century window of TC-01 is the chief temporal-parallax risk (R8, promoted from risk register to methodological constraint via E3 in scoping v0.2). Institutions construct time differently across eras — liturgical, fiscal, administrative, regnal — and the same calendar-year span can correspond to materially different quantities of institutional life.

This protocol fixes how cross-era commensurability is to be handled in TC-01 and any downstream M1-method work. It is binding: under v0.2 §5 M1, no stationarity claim is admissible without an explicit commensurability protocol declaration, and the protocol declared must be one of those specified here (or a fourth, named and defended in writing).

---

## 2. The three candidate approaches (recap)

From scoping v0.2 §5 M1:

- **(i) Calendar-time only**, with construction-asymmetry acknowledgement. Inter-event intervals are measured in years (Julian or proleptic Gregorian, declared per record). The asymmetry between, say, an early-medieval administrative year and a twentieth-century one is acknowledged in prose but not absorbed into the measurement.
- **(ii) Institution-internal time.** Inter-event intervals are measured in units constructed by the institution itself: papal successions, regnal-tenure boundaries, charter-revision counts. The institution's own clock of authority succession indexes events.
- **(iii) Dual measurement.** Both channels are computed and reported separately. Divergence between them is the central object of analysis, not an artefact to be smoothed away.

A fourth approach was considered during drafting (event-density-normalised time, where intervals are scaled by documentary-output volume per period). It is not adopted in v0.1; it conflates the protocol question with the coverage-correction question, and the latter is handled separately under TC-01's null-model machinery.

---

## 3. Selected protocol: dual measurement (iii)

**Decision.** Adopt protocol (iii). Both calendar-time and institution-internal-time channels are computed for every inter-event interval. Divergence is reported, not aggregated.

**Justification.**

- Approach (i) imports an unexamined assumption (calendar-year commensurability) and is the most exposed to R8. It is fast and cheap, but its results cannot distinguish "the underlying process is stationary" from "the underlying process is non-stationary in calendar time but stationary in institution-internal time, or vice versa."
- Approach (ii) absorbs the asymmetry but loses the only externally-validated time axis the programme has. Institution-internal time is itself non-stationary — papal tenures lengthened markedly in the modern period — so a claim that inter-event intervals are stationary in institution-internal time may simply be detecting tenure trends.
- Approach (iii) doubles workload but renders the asymmetry visible. A finding that *both* channels yield stationary distributions is stronger evidence for H₀ than either alone. A finding that the channels diverge is itself a substantive result: it tells us where the temporal-parallax risk is doing real work.

This is the Guardian-preferred protocol per the TC-06 card. It is methodologically conservative; it is also the only protocol of the three that allows the temporal-parallax risk to be empirically interrogated rather than assumed away.

---

## 4. Operational specification

### 4.1 Calendar-time channel

- **Time origin.** ISO 8601 dates, recorded per event in `start_date` and `end_date` columns of the M1 schema.
- **Calendar.** Julian for events with Julian-calendar primary sources; proleptic Gregorian for cross-era arithmetic. Each record declares which calendar its source dates are in via the `start_julian` boolean. Cross-era intervals are computed in proleptic Gregorian.
- **Inter-event interval.** Years between the previous council's `end_date` and the current council's `start_date`. Negative intervals (overlapping events) are flagged for review and not coerced.
- **Partial dates.** Where `start_date` or `end_date` carries `YYYY-MM-XX` or `YYYY-XX-XX` precision, the interval inherits the worst-case precision and is reported with an explicit uncertainty band (±month, ±year).

### 4.2 Institution-internal-time channel

- **Authority-succession clock.** For TC-01 (Catholic ecumenical councils), the natural internal clock is the apostolic-succession sequence: each council is indexed not only by date but by the papal-succession ordinal at council midpoint, and inter-event intervals are computed as the count of papal successions between consecutive councils.
- **Why successions, not tenure-years.** Tenure-years would re-import calendar time through the back door. Succession counts are dimensionless and institution-defined.
- **Multi-claim periods.** Where the apostolic succession is contested (Avignon papacy 1309–1378, Western Schism 1378–1417, anti-pope episodes), the protocol records the count under both the Roman and the contested lines, declared per record, and treats divergence as data.
- **Generalisation to TC-04 (T10 institutions).** The authority-succession clock for T10 institutions is the count of charter revisions, executive-director appointments confirmed by the institution's own confirmation procedure, or equivalent. Each T10 institution declares its own internal clock per record; the choice is logged in the schema's `criterion_ref` field.

### 4.3 Handling liturgical, fiscal, and administrative time variation

A council convened in (e.g.) December 1215 and another convened in (e.g.) January 1216 are roughly six weeks apart in calendar time but may straddle two distinct institutional fiscal or liturgical years.

- **Liturgical time** (church year, beginning Advent) is recorded but not used as the primary internal clock. It is too domain-specific to generalise across the M1 → TC-04 transition.
- **Fiscal/administrative time** (the institution's own year-boundary, where one exists) is recorded as a derived column where the schema is extended to support it; for v0.1 of TC-01 it is captured in `subtype_notes` or `external_shock_notes` where load-bearing.
- **Regnal time** (where applicable to council convening — e.g., emperor-convened councils of the early period) is recorded in the same notes channel.

These finer time-constructions inform interpretation of marginal cases but do not produce a third measurement channel in v0.1. They may be promoted to a third channel in v0.2 of this protocol if the dual-measurement results show large divergence concentrated at era boundaries that align with administrative-time discontinuities.

### 4.4 Divergence reporting

For every inter-event interval in TC-01, the analytic memo reports:

- The calendar-time interval with declared calendar.
- The institution-internal-time interval (succession count, with branch declarations where applicable).
- A divergence flag: `concordant` (both channels classify the interval to the same quantile of the empirical distribution within ±10 percentile points), `mild-divergent` (10–25 points), `strong-divergent` (>25 points).
- A divergence-cause tag where identifiable: `tenure-trend`, `succession-contested`, `coverage-gap`, `none-identified`.

Divergent intervals are not excluded; they are the headline.

---

## 5. Acceptance criteria for declaring a stationary distribution

A "stationary distribution" claim under this protocol requires *all* of the following:

1. **Both channels independently tested.** A test of the inter-event interval distribution against a constant-rate (Poisson) null is performed for each channel separately. The test family is declared in the analytic memo (default: Anderson–Darling against an exponential interval distribution; trend test via Mann–Kendall on inter-event intervals ordered by event index).
2. **Sub-type stratification.** Tests are run separately on the doctrinal / structural / disciplinary sub-typed subsets per TC-07. Multi-tagged events appear in each subset they are tagged for. Aggregation across sub-types is forbidden when the sub-type-specific tests give different verdicts.
3. **Multiple-comparison correction.** Where multiple tests are reported, p-values are corrected via Benjamini–Hochberg at false-discovery-rate q = 0.10, with the uncorrected values also shown.
4. **Concordance requirement.** A "stationary distribution" verdict requires non-rejection of the constant-rate null in *both* channels for the relevant sub-type. Non-rejection in one channel and rejection in the other is reported as **divergent**, not stationary, regardless of which channel yielded which result.
5. **Effect-size floor.** A non-rejection with sample-size-driven low power is not a stationarity claim. The memo reports the smallest monotone trend (in slope of log-interval per century) the test was powered to detect at the declared α and sample size; if that detectable effect size exceeds 10% per century, the verdict is **inconclusive**, not stationary.
6. **Coverage-correction declaration.** Coverage correction is applied per TC-01 and declared in writing. A stationarity claim that survives only the uncorrected analysis but fails under coverage correction is reported as **coverage-fragile**, not stationary.

A claim that does not meet all six conditions is not a stationarity claim under this protocol. It may still be a useful empirical finding; it is logged as such, with the missing condition named.

---

## 6. Falsification handle

None at the protocol level — this is methodological infrastructure, not an empirical claim. However: **any subsequent stationarity claim issued by TC-01, TC-04, or downstream M1-method work that does not declare its protocol per this document, or declares this protocol but fails one of the six acceptance conditions in §5, is invalidated.** The invalidation is procedural, not evidentiary; the underlying data may be re-analysed under a corrected protocol invocation.

---

## 7. Open questions / known limits

- **Q-CP1.** Generalisation to defunct-archive cases (TC-08) is not specified in v0.1. The institution-internal clock for a dissolved institution truncates at dissolution; whether to extrapolate is deferred to TC-08's feasibility memo.
- **Q-CP2.** The third channel for liturgical/fiscal/administrative time is held in reserve. Promotion criterion: divergence concentrated at era boundaries that align with administrative-time discontinuities. Scout review requested on whether to promote earlier.
- **Q-CP3.** The 10%-per-century effect-size floor in §5 condition 5 is a working choice, not a derived figure. Architect notes that this floor is justifiable from the L₅ scale (a 10%-per-century slope corresponds to roughly one L₅ generation of compression over the 16-century pilot window), but invites Guardian veto on the threshold.
- **Q-CP4.** The Anderson–Darling default in §5 condition 1 may be inappropriate for samples of n ≈ 21 (the Catholic-councils case). A small-sample alternative (exact permutation test against a Poisson null) may be substituted by TC-01's analyst on declaration.

---

## 8. Document control

- **v0.1** (2026-04-27): Initial draft under Architect invocation, in response to TC-06 authorisation. Selected dual-measurement protocol (iii) per Guardian preference and methodological-conservatism argument. Six acceptance conditions specified for stationarity claims. Liturgical/fiscal/administrative time variation handled in v0.1 as recorded-but-not-channelled, with promotion criterion installed.
- **v0.2 horizon:** review pass by Guardian (R8 discipline) and Scout. Possible promotion of administrative-time channel. Possible recalibration of §5 condition 5 effect-size floor.

**Stance log.** Drafted Architect, with the dual-measurement selection consciously following Guardian preference as recorded on TC-06. The selection is methodological, not jurisdictional — Architect reserves the right to recommend protocol (i) for downstream T10 work in TC-04 if dual measurement turns out to be operationally infeasible at T10 scale (charter-revision counts may not exist for all T10 institutions). Any such departure must be logged in the relevant card's stance log.

**Linked.** `docs/scoping/human-timescales-scoping-v0.2.md` §5 M1, E3, R8; `docs/task-cards/human-timescales-task-cards-v0.1.md` TC-06, TC-01, TC-04, TC-07, TC-08; `data/m1-catholic-councils/schema.md`; `data/t10-archive/schema.md`.
