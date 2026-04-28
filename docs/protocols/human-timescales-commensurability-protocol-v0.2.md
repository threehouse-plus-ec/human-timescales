# Cross-Era Commensurability Protocol

**Version:** v0.2 (RT-2026-001 Scout + RT-2026-002 Guardian integration)
**Stance:** Architect (drafting). Reviewers: Scout (RT-2026-001 closed 2026-04-28) + Guardian R8-discipline (RT-2026-002 closed 2026-04-28). Both responses integrated below.
**Parent documents:** *Human-System Timescales: Scoping v0.2* (§5 M1, E3, R8); *Task Cards v0.1* (TC-06).
**Companion deliverables (cross-card-coherence cross-checked):** TC-07 reform-event sub-typing protocol v0.1 (six-tag set and sample-size pre-rule cross-checked against TC-08 v0.2 design space per Guardian authorisation §3 design-coherence requirement (2)); TC-08 defunct-archive feasibility memo v0.1 + RT-2026-004 ruling (anchor-house n≥15 clause and per-discipline split feed back into §6 R8 closure thresholds).
**Feeds:** TC-01 (Catholic ecumenical councils pilot — gating prerequisite); TC-04 (T10 archive characterisation — per-institution, non-comparable institution-internal-time channel per Scout Q5).
**Date:** 2026-04-28

---

## 0. Endorsement Marker (provisional)

Internal methodological infrastructure. Not a Coastline. No external endorsement is asserted. This protocol is operational; it carries no empirical claim of its own. Its function is to fix the conditions under which downstream stationarity claims may be issued.

v0.2 integrates Scout (RT-2026-001) and Guardian R8-discipline (RT-2026-002) review responses in full. Three design-coherence requirements from Guardian's authorisation §3 are honoured:
1. Era-stratification (§4.3) and presumptive channel-dominance (§4.5) are **co-designed** — band boundaries match across §4 and §5.
2. Six-tag set (§4.6) and sample-size pre-rule (§5 condition 1) **cross-checked against TC-08 v0.2 design space** following RT-2026-004 issuance; consistent.
3. SF-10 boundary-fragility mitigations (Q1 ±25 yr addendum; Q2(b) tier-overlap reporting) are drafted **into §5 conditions, not as appendix**.

## 0a. Non-prescription clause (inherited)

Per `CONVENTIONS.md` §6 and `docs/scoping/human-timescales-scoping-v0.2.md` §0a. Reform-cycle measurements made under this protocol describe minimum coordination timescales as observed phenomena. They do not endorse any pace as correct, optimal, or politically legitimate. **A floor is not a target.**

---

## 1. Purpose

Reform-cycle archaeology (M1) requires inter-event interval measurements that are commensurable across centuries. The premise that calendar-year intervals are simply commensurable across the 16-century window of TC-01 is the chief temporal-parallax risk (R8, promoted from risk register to methodological constraint via E3 in scoping v0.2). Institutions construct time differently across eras — liturgical, fiscal, administrative, regnal — and the same calendar-year span can correspond to materially different quantities of institutional life.

Scout's RT-2026-001 Q1 verdict (*surfaces only*) bound v0.2 to the recognition that dual measurement renders R8 visible but does not resolve it. v0.2 therefore tightens the verdict-issuance discipline to prevent back-door temporal-parallax re-importation: era-stratified channel-dominance, expanded divergence-cause tag set with per-interval pre-declaration, era-stratified effect-size floors, three-tier power rule, and explicit R8 closure thresholds requiring TC-04 *and* TC-08 satisfaction.

This protocol is binding: under v0.2 §5 M1, no stationarity claim is admissible without an explicit commensurability protocol declaration; under v0.2 §6 of *this* document (tightened), a stationarity claim that invokes the protocol but fails any of the six §5 acceptance conditions is also invalidated.

---

## 2. The three candidate approaches (recap)

From scoping v0.2 §5 M1:

- **(i) Calendar-time only**, with construction-asymmetry acknowledgement.
- **(ii) Institution-internal time.** Inter-event intervals measured in units constructed by the institution itself (papal successions, regnal-tenure boundaries, charter-revision counts).
- **(iii) Dual measurement.** Both channels computed and reported separately; divergence reported, not aggregated.

A fourth approach (event-density-normalised time) was considered and rejected at v0.1 drafting on grounds that it conflates the protocol question with the coverage-correction question.

v0.2 retains protocol (iii) as the base architecture and **promotes a third (administrative-time) channel** to a measurement channel of its own per Scout Q2 ruling (*promote now*) and Guardian Q3 ratification (`coverage-artifact` tag inclusion in the expanded set). v0.2 is therefore a *triple-measurement* protocol with one of the three channels conditional on era-band-specific data availability.

---

## 3. Selected protocol: dual measurement + third channel (v0.2)

**Decision.** Adopt protocol (iii) **with administrative-time third channel promoted** per Scout Q2 / Guardian Q3 ratification. All three channels — calendar-time, institution-internal-time, administrative-time — are computed for every inter-event interval where data permits. Divergence is reported, not aggregated. Per-interval tags are pre-declared (§4.6) before stationarity test results are examined.

**Justification (carried forward from v0.1, with v0.2 additions).**

- Approach (i) imports an unexamined assumption (calendar-year commensurability) and is the most exposed to R8.
- Approach (ii) absorbs the asymmetry but loses the only externally-validated time axis the programme has; institution-internal time is itself non-stationary (papal tenures lengthened markedly in the modern period).
- Approach (iii) renders the asymmetry visible. A finding that channels yield concordant stationary distributions is stronger evidence for H₀ than any single channel alone. A finding that channels diverge is itself a substantive result — Scout's RT-2026-001 Q1 verdict makes this empirical interrogation possible.
- **The administrative-time third channel** addresses Scout's Q2 reasoning that "era-boundary divergence is exactly where administrative-time discontinuities are most likely to be load-bearing" — waiting for biased divergence evidence to trigger promotion would be a catch-22.

**Methodological posture.** v0.2 is consciously conservative. Where conservatism produces inconclusive verdicts on small subsets, the protocol **states the conservatism in writing** rather than hiding it (per Guardian Q2(b) ruling); inconclusive is not failure of evidence, it is honest acknowledgement of insufficient power.

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
- **TC-04 portability — non-portable across institutions** (per Scout RT-2026-001 Q5 verdict). Institution-internal-time clocks for T10 institutions (IETF chair succession; W3C director transitions; ICANN board evolution) are *per-institution and non-comparable* across the T10 set. **TC-04 must therefore treat institution-internal-time as three separate single-institution analyses, not as a cross-institution channel.** TC-06 v0.2 carries an explicit non-comparability annotation against any aggregated cross-T10 institution-internal-time measure; if cross-T10 comparison is later desired, a fourth protocol iteration (or a TC-04-specific supplement) will be needed.

### 4.3 Era-stratified three-band design and presumptive channel-dominance

Co-designed per Guardian R8-discipline rulings (RT-2026-002 Q1 + Q2(a), with band boundaries matching across the era-stratified effect-size floor in §5 condition 5 and the channel-dominance presumption in this section).

**Era bands (pre-declared and locked; Guardian re-authorisation required for any modification):**

| Band | Years | Documentary regime | Presumptive channel-dominance |
|---|---|---|---|
| **B1 Late-antique / early-medieval** | 325–1100 | Internal records sparse; calendar dating relatively reliable construct | **Calendar-time presumptive-authoritative** |
| **B2 High-medieval / early-modern** | 1100–1800 | Papal succession well-documented and the construct under examination | **Institution-internal-time presumptive-authoritative** |
| **B3 Modern** | 1800–1965 | Both channels well-documented; no presumption needed | **Both channels co-authoritative; mandatory concordance** |

**Presumption mechanics.** "Presumptive-authoritative" means: where the analytic memo cannot reasonably reconcile divergent channel results within an era band, the presumed channel's verdict stands as the band-default and the divergence is logged as a per-interval annotation. Analyst override is permitted with declared reason. Override across more than one band's worth of intervals requires Guardian re-authorisation.

**±25 yr boundary addendum (SF-10 mitigation, Guardian Q1 boundary-fragility ruling).** Any verdict whose effect-size determination falls within ±25 calendar-years of a band boundary (i.e., 1075–1125 or 1775–1825) **must be reported under both adjacent bands' floors and dominance presumptions**, with divergence flagged. This converts the boundary discontinuity into reportable data rather than a hidden sensitivity. The discipline applies to both effect-size floor (§5 condition 5) and channel-dominance (this section).

**Cross-band events.** An event that spans a band boundary (e.g., a council whose start is pre-1100 and end is post-1100) is assigned to the band of its midpoint, with the cross-band annotation appearing in the event record.

### 4.4 Administrative-time third channel (promoted in v0.2)

Per Scout RT-2026-001 Q2 verdict (*promote now*) and Guardian RT-2026-002 Q3 ratification of the `coverage-artifact` divergence-cause tag.

**Minimal v0.2 specification:**

- **`straddles_admin_boundary` boolean** captured per inter-event interval. Set to TRUE if the calendar-time interval crosses an administrative-time boundary (institutional fiscal-year start, regnal-year transition, liturgical-year start where load-bearing) of either of the two adjacent events.
- **Era-specific administrative-time lookup table.** A per-era specification of the relevant administrative-time boundary, declared in TC-01 v0.2 data extraction. For the Catholic-councils archive: Roman indiction cycles (early period); curial fiscal year (high-medieval onward); Gregorian-calendar-year-aligned modern period.
- **Channel function.** The administrative-time channel does not produce a stand-alone interval-distance measure in v0.2; instead it operates as a **divergence-cause attribution** mechanism — when the calendar-time and institution-internal-time channels diverge for an interval *and* the interval straddles an administrative boundary, the divergence is candidate for `coverage-artifact` tagging (§4.6).
- **Promotion to interval-distance channel deferred.** Full administrative-time interval-distance computation (where each interval is measured in administrative-year units) is deferred to v0.3 of this protocol pending evidence from TC-01 extraction whether the boundary-straddle effect is dispositive enough to warrant the full third-channel promotion.

### 4.5 Channel-dominance annotation discipline (Scout Q1 + Guardian Q2(a) consolidated)

For every divergent interval (defined in §4.6 below), the analytic memo must carry a **channel-dominance annotation** declaring which channel is treated as authoritative for that interval and why. Without this annotation, TC-01 analysts implicitly default to calendar time, re-importing the unexamined assumption R8 was meant to discipline.

**Default mechanism.** The era-band presumption (§4.3) supplies the default channel-dominance assignment per interval. The annotation either ratifies the era-band presumption ("default applies; reason: [brief]") or overrides it ("override: [channel] dominance, reason: [explicit]"). Override across more than one band's worth of intervals requires Guardian re-authorisation; ad-hoc per-interval overrides are permitted with declared reason.

**Pre-declaration.** The dominance annotation must be lodged *before* the stationarity test result for that interval is examined (per Guardian Q3 pre-declaration discipline). Deviation from the pre-declared dominance assignment after test results are seen requires Guardian re-authorisation.

### 4.6 Divergence reporting (six-tag set; per-interval pre-declaration required)

For every inter-event interval, the analytic memo reports:

- The calendar-time interval with declared calendar.
- The institution-internal-time interval (succession count, with branch declarations where applicable).
- The administrative-time `straddles_admin_boundary` boolean.
- The channel-dominance annotation (§4.5).
- A divergence flag: `concordant` (both channels classify the interval to the same quantile of the empirical distribution within ±10 percentile points), `mild-divergent` (10–25 points), `strong-divergent` (>25 points).
- A divergence-cause tag from the **expanded six-tag set** (per Guardian Q3 §4.4 audit ruling):
  - `tenure-trend` — divergence driven by changes in succession-rate (tenure lengths) over time
  - `succession-contested` — divergence driven by formally-contested or ambiguous succession (anti-pope, schism)
  - `coverage-gap` — divergence driven by gaps in documentary coverage on one channel
  - `coverage-artifact` — divergence driven by per-channel coverage-correction asymmetries (SF-8, RT-2026-001)
  - `R8-residual-confirmed` — *positive* tag for intervals where the per-interval audit has examined and ruled out alternative explanations; the divergence is genuine residual temporal parallax
  - `none-identified` — passive residual; alternative explanations not exhausted

**Per-interval tag pre-declaration required (Guardian Q3 binding).** Per-interval divergence-cause tag must be declared *before* the stationarity test result is examined for that interval. Deviation from the pre-declared tag after test results are seen requires Guardian re-authorisation. This is the load-bearing R4 discipline; without it, the tag set is decorative.

**`tenure-trend` and `R8-residual-confirmed` modality-forbidding** for R8 closure (§6 thresholds). If either of these tags is the modal divergence-cause in any case under TC-04 or TC-08, the R8 residual is not closed for that subset.

Divergent intervals are not excluded; they are the headline.

---

## 5. Acceptance criteria for declaring a stationary distribution

A "stationary distribution" claim under this protocol requires *all six* conditions. The conditions in v0.2 are substantively revised from v0.1.

### Condition 1 — Test-family pre-rule (Guardian Q5 ruling)

A test of the inter-event interval distribution against a constant-rate (Poisson) null is performed for each channel separately. **Test family is pre-declared by sample-size rule, not analyst-discretional:**

- **n < 30:** **exact permutation test against a Poisson null** (default; not analyst-declarable to avoid the soft motte-and-bailey opportunity Architect flagged in RT-2026-002 Q5).
- **n ≥ 30:** Anderson–Darling against an exponential interval distribution; trend test via Mann–Kendall on inter-event intervals ordered by event index.

Deviation from the size-rule requires written declaration *before* data examination, with explicit Guardian re-authorisation. Ad-hoc test-family choice after seeing results is invalidating under §6.

### Condition 2 — Sub-type stratification (unchanged from v0.1)

Tests are run separately on the doctrinal / structural / disciplinary sub-typed subsets per TC-07. Multi-tagged events appear in each subset they are tagged for. Aggregation across sub-types is forbidden when the sub-type-specific tests give different verdicts.

### Condition 3 — Multiple-comparison correction (unchanged from v0.1)

Where multiple tests are reported, p-values are corrected via Benjamini–Hochberg at false-discovery-rate q = 0.10, with the uncorrected values also shown.

### Condition 4 — Three-tier power rule (Guardian Q2(b) replacing v0.1's binary concordance)

Channel-concordance is required, with strictness graded by sample size:

- **n < 8:** **strict concordance retained**; verdicts default to **inconclusive** with explicit power-flag annotation. No rescue.
- **8 ≤ n < 15:** **weak concordance permitted** — non-rejection in at least one channel, no rejection at p < 0.01 in the other — with **mandatory minimum-detectable-effect-size (MDE) reporting** in the analytic memo. The MDE figure quantifies the smallest monotone trend the test was powered to detect; if the MDE exceeds the era-stratified floor (§5 condition 5) for the relevant band, the verdict is downgraded to **inconclusive**.
- **n ≥ 15:** **strict concordance binding.**

**SF-10 mitigation (boundary-fragility ruling, Guardian §3 catch-all):** Verdicts whose subset size falls within the n=8 or n=15 boundary regions report under both adjacent tiers, with divergence flagged. The boundary regions are n ∈ {7, 8, 9} (around the n=8 cutoff) and n ∈ {14, 15, 16} (around the n=15 cutoff). This **tier-overlap reporting** converts the discontinuity into reportable data.

**Boundary-case combined annotation (Guardian Q2(c) ratified).** When channel-dominance annotation (§4.5) and weak-concordance verdict (this condition) both apply to the same interval, both annotations appear in the analytic memo.

### Condition 5 — Era-stratified three-band effect-size floor (Guardian Q1 ruling)

The uniform 10%/century floor of v0.1 is replaced by an **era-stratified three-band floor**, pre-declared and locked, matching the band boundaries of §4.3.

**Bands and provisional slope floors (subject to Guardian re-authorisation under v0.2 review):**

| Band | Years | Provisional slope-floor (slope of log-interval per century) | Documentary-density covariate adjustment |
|---|---|---|---|
| **B1** | 325–1100 | 15%/century | Reduced detectable trend power; floor relaxed accordingly |
| **B2** | 1100–1800 | 10%/century | Standard L₅-derived floor |
| **B3** | 1800–1965 | 7%/century | Higher detectable trend power; floor tightened |

The band-specific slopes are derived from the L₅ scale adjusted for documentary density (Architect to compute and submit for Guardian ratification under v0.2 review pass; provisional slopes above are placeholder values pending derivation). **A non-rejection with sample-size-driven low power** is not a stationarity claim if the smallest monotone trend the test was powered to detect *exceeds* the band-specific floor — verdict is **inconclusive**.

**±25 yr boundary addendum (SF-10 mitigation; Guardian Q1):** Any verdict whose effect-size determination falls within ±25 calendar-years of a band boundary (1075–1125 or 1775–1825) must be reported under both adjacent bands' floors, with divergence flagged.

**Pre-declaration and lock.** Band boundaries and band-specific slopes are pre-declared in this protocol (v0.2 §5 condition 5) and locked against post-hoc revision except by explicit Guardian re-authorisation. An era-stratified floor without pre-declared boundaries is a degree of freedom that motte-and-bailey moves can exploit (per Guardian Q1 ruling).

### Condition 6 — Coverage-correction declaration (channel-explicit per SF-8)

Coverage correction is applied per TC-01 and declared in writing. **Coverage-correction methods must be declared channel-explicit** (per SF-8 in `meta/horizon-signals.md` and Guardian Q3 / SF-8 ratification): documentary-density proxies for calendar-time channel; succession-completeness proxies for institution-internal-time channel; administrative-boundary frequency for administrative-time channel. A coverage-correction method that conflates channels (e.g., applies a single proxy across all three) is **invalidating** under §6.

A stationarity claim that survives only the uncorrected analysis but fails under coverage correction is reported as **coverage-fragile**, not stationary. Where divergence-cause tagging assigns `coverage-artifact` for an interval, the per-channel coverage-correction methods are responsible for that interval's flag and must be itemised.

A claim that does not meet all six conditions is not a stationarity claim under this protocol. It may still be a useful empirical finding; it is logged as such, with the missing condition named.

---

## 6. Procedural falsification + R8 closure thresholds

### 6.1 Procedural falsification (tightened per Guardian Q3)

**Any subsequent stationarity claim issued by TC-01, TC-04, or downstream M1-method work that does not declare its protocol per this document, OR that declares this protocol but fails any of the six §5 acceptance conditions while nevertheless asserting stationarity, is invalidated.**

The v0.1 text covered only the no-declaration case. v0.2 explicitly invalidates the canonical motte-and-bailey rescue path: nominal-invocation-with-condition-failure. The invalidation is procedural, not evidentiary; the underlying data may be re-analysed under a corrected protocol invocation.

**Motte-and-bailey audit of §4.6 tag discipline (Guardian Q3 audit ruling).** The pre-declaration requirement for per-interval divergence-cause tags (§4.6) is the load-bearing R4 discipline. Tag re-assignment after seeing test results is invalidating regardless of whether the protocol was nominally invoked.

### 6.2 R8 closure thresholds (Guardian Q4 ruling)

R8 (temporal parallax) closure requires *both* TC-04 *and* TC-08 to have been characterised under this protocol, plus satisfaction of three Guardian-pre-declared operational thresholds (per RT-2026-002 Q4):

1. **Channel-ratio bound.** The per-interval ratio between calendar-time and institution-internal-time channels, taken across all paired intervals in TC-04 and TC-08, **varies by no more than a factor of 2 from its cross-case median**.
2. **No tag-cluster dominance.** **Neither `tenure-trend` nor `R8-residual-confirmed`** is the modal divergence-cause tag in any single TC-04 case or in the TC-08 paired-case set; if either tag is modal, the R8 residual is not closed for that subset.
3. **Cross-form coverage without weak-concordance modal regime.** At least one TC-04 case **and** at least one TC-08 case have been characterised under the protocol *without invoking the §5 condition 4 weak-concordance lower tier (8 ≤ n < 15)* as the modal verdict-issuance pathway.

**Until all three thresholds hold, R8 status remains *procedurally-managed-but-live***, as Scout RT-2026-001 determined and the horizon-signals register records. **On satisfaction**, R8 status moves to **closed-conditional-on-thresholds**, with the three thresholds themselves subject to Guardian re-authorisation if any TC-04 or TC-08 finding exposes their fragility.

**Stationarity-claim annotation discipline.** Until R8 closure, every stationarity claim issued under this protocol carries a **live R8 residual annotation** declared in the claim's reporting. The annotation explicitly states: "R8 residual: live (TC-04 / TC-08 closure pending)" or, post-closure, "R8 residual: closed-conditional-on-thresholds (TC-04 / TC-08 satisfied [date])."

**Cross-card binding.** TC-08 is now a binding component of the R8 closure pathway (per RT-2026-004 Guardian R3 + R8-closure-precondition response). The pre-extraction anchor-house feasibility for TC-08 v0.2 §4.2 commitment (`docs/memos/dissolution-cohort-anchor-house-feasibility-v0.1.md`) is therefore a feasibility precondition for this protocol's R8 closure pathway, not only for TC-08's R3-discipline standing.

---

## 7. Open questions / known limits

- **Q-CP1 (resolved partially).** Generalisation to defunct-archive cases (TC-08) is now substantively addressed via §6.2 Q4 cross-card binding. However, institution-internal-time clock truncation at dissolution, and the per-discipline split between R3 (Templar band-presumption override permitted) and R8-closure-precondition (Templar hard-excluded from R8 standing) per RT-2026-004 Q2, requires v0.3 protocol revision once TC-08 v0.2 extraction lands.
- **Q-CP2 (resolved).** Administrative-time third channel promoted in v0.2 §4.4 per Scout Q2 ruling.
- **Q-CP3 (substantively resolved).** Effect-size floor era-stratified per Guardian Q1 ruling; provisional band-specific slopes (15% / 10% / 7% per century) pending Architect derivation and Guardian ratification under v0.2 review pass.
- **Q-CP4 (resolved).** Test-family pre-rule (n < 30 → exact permutation; n ≥ 30 → Anderson–Darling) installed in §5 condition 1 per Guardian Q5 ruling.
- **Q-CP5 (new, v0.2).** Whether the v0.2 administrative-time channel's `straddles_admin_boundary` boolean should be promoted to a full interval-distance channel in v0.3, conditional on TC-01 extraction evidence about the boundary-straddle effect's dispositive weight. Drafter recommendation: promote conditionally on TC-01 extraction yielding ≥ 5 intervals where the boundary-straddle attribution is the difference between concordant and divergent verdicts.
- **Q-CP6 (new, v0.2).** Whether the era-band slope-floor placeholders (15% / 10% / 7%) survive the documentary-density covariate adjustment Architect is now obliged to perform. If the derivation produces materially different slopes, v0.2 must be revised to v0.2.1 *before* TC-01 extraction begins.
- **Q-CP7 (new, v0.2).** Whether the cross-card binding of TC-08 to R8 closure (§6.2) creates a circular dependency with TC-08 v0.2's own R8-closure-precondition standing per RT-2026-004 Q2 per-discipline split. Drafter recommendation: not circular — TC-08 *contributes* to R8 closure but its contribution is gated by the anchor-house feasibility (Dissolution cohort, Templar excluded), and TC-08's R3-discipline standing proceeds independently. The dependency is sequential, not circular.
- **Known limit (carried forward).** v0.2 administrative-time channel is a divergence-cause attribution mechanism, not yet a full interval-distance channel. Full promotion deferred to v0.3 conditional on TC-01 extraction evidence (Q-CP5).
- **Known limit (new in v0.2).** TC-04 portability of institution-internal-time channel is per-institution, non-comparable across T10 institutions per Scout Q5. The cross-T10 institution-internal-time aggregation that v0.1 nominally permitted is forbidden under v0.2.

---

## 8. Document control

- **v0.1** (2026-04-27): Initial draft under Architect invocation, in response to TC-06 authorisation. Selected dual-measurement protocol (iii) per Guardian preference and methodological-conservatism argument. Six acceptance conditions specified for stationarity claims. Liturgical/fiscal/administrative time variation handled as recorded-but-not-channelled, with promotion criterion installed.
- **v0.2** (2026-04-28): RT-2026-001 Scout + RT-2026-002 Guardian R8-discipline integration. Substantive changes:
  - **§3:** Triple-measurement architecture (calendar-time + institution-internal-time + administrative-time third channel promoted per Scout Q2).
  - **§4.2:** TC-04 institution-internal-time portability declared per-institution, non-comparable per Scout Q5.
  - **§4.3 (new):** Era-stratified three-band design (325–1100 / 1100–1800 / 1800–1965) with presumptive channel-dominance per Guardian Q2(a); ±25 yr boundary addendum per Guardian Q1 + SF-10 mitigation.
  - **§4.4 (new):** Administrative-time third channel via `straddles_admin_boundary` boolean + era lookup; full interval-distance promotion deferred to v0.3.
  - **§4.5 (new):** Channel-dominance annotation discipline with pre-declaration requirement per Scout Q1 + Guardian Q3.
  - **§4.6:** Six-tag set replacing v0.1's four (`tenure-trend`, `succession-contested`, `coverage-gap`, `coverage-artifact` per SF-8, `R8-residual-confirmed`, `none-identified`); per-interval tag pre-declaration required before stationarity test results examined per Guardian Q3.
  - **§5 condition 1:** Test-family pre-rule (n<30 → exact permutation; n≥30 → Anderson–Darling) per Guardian Q5.
  - **§5 condition 4:** Three-tier power rule (n<8 strict + inconclusive default; 8≤n<15 weak concordance with mandatory MDE reporting; n≥15 strict) per Guardian Q2(b); SF-10 tier-overlap reporting at n=8 and n=15 boundaries.
  - **§5 condition 5:** Era-stratified three-band floor (provisional 15% / 10% / 7% per century) per Guardian Q1; ±25 yr boundary addendum.
  - **§5 condition 6:** Coverage-correction methods declared channel-explicit per SF-8 / Guardian Q3.
  - **§6.1:** Procedural falsification tightened to invalidate nominal-invocation-with-condition-failure per Guardian Q3.
  - **§6.2 (new):** R8 closure thresholds — TC-04 *and* TC-08 required, plus three Guardian-pre-declared thresholds (channel-ratio bound; no tag-cluster dominance; cross-form coverage without weak-concordance modal); R8 residual annotation discipline binding on every stationarity claim until closure; cross-card binding to TC-08 anchor-house feasibility per RT-2026-004 Q4.
  - **§7:** Q-CP1–Q-CP4 substantively resolved; Q-CP5–Q-CP7 newly logged.
- **v0.2.1 horizon (binding):** Architect derivation of era-band slope-floors with documentary-density covariate adjustment (Q-CP6); to land *before* TC-01 extraction begins.
- **v0.3 horizon:** Possible promotion of administrative-time channel to full interval-distance computation per Q-CP5 conditional on TC-01 evidence; resolution of TC-08-related Q-CP1 v0.3 revision per RT-2026-004 ruling once TC-08 v0.2 extraction lands.

**Stance log.** Drafted Architect, integrating Scout (RT-2026-001 closed) and Guardian R8-discipline (RT-2026-002 closed) review responses in full. Three design-coherence requirements from Guardian's authorisation §3 honoured: era-stratification (§4.3) and presumptive channel-dominance (§4.5) co-designed with matching band boundaries; six-tag set (§4.6) and sample-size pre-rule (§5 cond. 1) cross-checked against TC-08 v0.2 design space following RT-2026-004 issuance and found consistent (TC-08 paired-case set sits in 8≤n<15 weak-concordance band per RT-2026-004 §1; v0.2 three-tier power rule accommodates this with mandatory MDE reporting; threshold (iii) cross-form coverage without weak-concordance modal is the operational binding); SF-10 mitigations drafted into §5 conditions 4 and 5, not appendix. **No items required pre-v0.2 re-deliberation.** RT-2026-001 and RT-2026-002 are closed on receipt; v0.2 represents Architect's good-faith integration of both responses subject to the v0.2.1 binding (Q-CP6 era-band slope-floor derivation before TC-01 extraction).

**Linked.** `docs/scoping/human-timescales-scoping-v0.2.md` §5 M1, E3, R8; `docs/task-cards/human-timescales-task-cards-v0.1.md` TC-06, TC-01, TC-04, TC-07, TC-08; `docs/protocols/human-timescales-commensurability-protocol-v0.1.md` (predecessor); `docs/protocols/human-timescales-reform-event-subtyping-protocol-v0.1.md` (TC-07, cross-card-coherence cross-checked); `docs/memos/defunct-archive-feasibility-memo-v0.1.md` (TC-08, R8 closure cross-card binding); `docs/memos/dissolution-cohort-anchor-house-feasibility-v0.1.md` (TC-08 anchor-house feasibility, R8 closure precondition); `meta/review-tasks/tc06-scout-review-v0.1.md` + `tc06-scout-review-response-v0.1.md` (RT-2026-001); `meta/review-tasks/tc06-guardian-review-v0.1.md` + `tc06-guardian-review-response-v0.1.md` (RT-2026-002); `meta/review-tasks/tc08-guardian-review-v0.1.md` + `tc08-guardian-review-response-v0.1.md` (RT-2026-004); `meta/horizon-signals.md` (SF-8, SF-10, R8 status); `data/m1-catholic-councils/schema.md` (administrative-time `straddles_admin_boundary` boolean to be added per §4.4); `data/t10-archive/schema.md` (per-institution `criterion_ref` field for institution-internal-time clock per §4.2).
