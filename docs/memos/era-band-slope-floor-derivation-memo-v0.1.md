# Era-Band Slope-Floor Derivation — v0.2.1 Binding for TC-06 §5 Condition 5

**Version:** v0.1
**Stance:** Architect (drafting). Reviewer: Guardian R8-discipline (re-authorisation gate per RT-2026-002 Q1 ruling). Pending.
**Parent documents:** *Cross-Era Commensurability Protocol v0.2* §5 condition 5 (placeholder slopes 15% / 10% / 7% per century; v0.2.1 binding follow-up declared in §8 document control); *RT-2026-002 Guardian R8 review response* Q1 ruling (era-stratified three-band floor with pre-declared and locked band boundaries; band-specific slopes derived from L₅ scale with documentary-density covariate adjustment, drafter to compute and submit for Guardian ratification under v0.2 review).
**Feeds:** TC-06 v0.2.1 protocol patch (locks the derived band-specific slopes into §5 condition 5).
**Date:** 2026-04-28

---

## 0. Endorsement Marker (provisional)

Internal methodological memo. Not a Coastline. No external endorsement is asserted. The derivation below produces band-specific effect-size floors for TC-06 v0.2 §5 condition 5 from a defensible anchor-plus-covariate argument. The floors are *procedural thresholds*, not power calculations under specified noise distributions; their function is to set the operational definition of "stationary distribution" under the protocol, not to guarantee statistical power against a specific alternative hypothesis.

## 0a. Non-prescription clause (inherited)

Per `CONVENTIONS.md` §6 and scoping v0.2 §0a. Effect-size floors set methodological thresholds for what counts as "stationary" under the protocol; they do not endorse any institutional reform pace as correct, optimal, or politically legitimate. **A floor is not a target.**

---

## 1. Purpose

TC-06 v0.2 §5 condition 5 installed an era-stratified three-band floor for declaring stationarity, replacing v0.1's uniform 10%-per-century floor. The three bands are:

| Band | Years | Documentary regime | Provisional slope floor |
|---|---|---|---|
| B1 | 325–1100 | Internal records sparse; calendar dating relatively reliable | 15%/century |
| B2 | 1100–1800 | Papal succession well-documented and the construct under examination | 10%/century |
| B3 | 1800–1965 | Both channels well-documented | 7%/century |

The provisional values were placeholders pending Architect derivation. v0.2 document control declared this derivation a **v0.2.1 binding follow-up** to land *before* TC-01 extraction begins, with Guardian re-authorisation required under RT-2026-002 Q1.

This memo is the derivation. It produces:
- A defensible argument for the B2 anchor at 10%/century (the L₅-scale anchor, recovered from v0.1 with the era-band lens added).
- A documentary-density covariate adjustment that gives B1 and B3 their band-specific values relative to B2.
- A note on the realised n-per-band for the M1 Catholic-councils pilot, which determines whether each band's floor is operative or moot.
- Locked numbers for TC-06 v0.2.1 §5 condition 5.

---

## 2. The principle: effect-size floor as procedural threshold

The slope-floor's role under TC-06 §5 condition 5 is *procedural*, not power-analytic. It says:

> *A non-rejection of stationarity does not count as a stationarity claim if the smallest monotone trend the test was powered to detect at α = 0.05 (per condition 1 test family) exceeds the band-specific floor.*

In other words: if the test could only have detected a trend larger than X%/century, and the test does not reject stationarity, the verdict is **inconclusive** rather than **stationary**. The floor X is the threshold below which non-rejection is informative; above which non-rejection is power-limited.

Setting X is therefore a normative judgement about what counts as "informative" — small enough to constrain H₀, large enough to be achievable. The floor is set from two anchors:

- **L₅ scale anchor.** A meaningful trend is one that would compress (or expand) the inter-event interval by an L₅-relevant fraction per century.
- **Documentary-density adjustment.** Bands with sparse records have lower test power and tolerate higher floors; bands with dense records have higher power and require tighter floors.

The L₅ anchor sets the *standard* floor (used in B2). The covariate adjustment sets B1 and B3 relative to B2.

---

## 3. The L₅-scale anchor (B2 derivation)

L₅ in scoping v0.2 §3 is the legitimacy-transfer-generation timescale, ~25–40 years. Take L₅ = 30 years as the mid-range working value.

**Anchor argument.** A trend in inter-event intervals at slope s in log-units per century changes the interval by a factor of e^(s·t) over t centuries. For B2 (1100–1800, span Δt = 7 centuries), a slope of s = 0.10/century gives a cumulative factor of e^(0.10·7) ≈ 2.01 — the interval roughly doubles across the band.

**Why this is the right anchor.** The L₅ generation is the timescale on which institutional cohorts replace; the natural reference signal H₀ predicts is "no trend at the L₅ band." If interval lengths drift by a factor of ~2 across B2's 7-century span, that drift is **L₅-comparable**: the institutional reform-cycle is no longer stationary relative to the L₅ floor. A trend smaller than 10%/century may still be there, but the protocol does not claim the means to detect it as inconsistent with stationarity.

**Equivalent cumulative description.** A 10%/century slope across B2's 7 centuries = factor of 2.01 cumulative ≈ a doubling. Over 1 L₅ generation (3 centuries), it's a factor of 1.35 — about a third more interval length per generation. That is the B2 floor's qualitative meaning.

**B2 floor: 10%/century, retained as L₅-anchored standard.**

---

## 4. Documentary-density covariate (B1 and B3 adjustment)

The covariate adjustment relaxes B1's floor and tightens B3's floor relative to B2's standard, reflecting band-specific power asymmetry.

**Documentary-density definition.** For TC-01 Catholic-councils data: documentary density per band is estimated as (events per band) / (band span in centuries). For other archives (TC-04, TC-08), domain-specific density measures apply.

For TC-01:

| Band | Years | Span (centuries) | Events | Intervals (n) | Documentary density (events/century) |
|---|---|---|---|---|---|
| **B1** | 325–1100 | 7.75 | 8 | 7 | 1.03 |
| **B2** | 1100–1800 | 7.0 | 11 | 10 | 1.57 |
| **B3** | 1800–1965 | 1.65 | 2 | 1 | 1.21 |

**Adjustment rule.** Define ρ_band = documentary-density(band) / documentary-density(B2). Floor adjustment:

> floor_band = floor_B2 × √(ρ_B2 / ρ_band)

The square-root form reflects that test-statistic standard errors typically scale as 1/√n; a band with half the density therefore has √2 ≈ 1.41× higher MDE, motivating a √2-relaxed floor.

Applied to TC-01:
- ρ_B1 = 1.03 / 1.57 = 0.66 → floor_B1 = 10% × √(1/0.66) = 10% × 1.23 ≈ **12.3%/century**
- ρ_B2 = 1.0 → floor_B2 = **10%/century** (anchor)
- ρ_B3 = 1.21 / 1.57 = 0.77 → floor_B3 = 10% × √(1/0.77) ≈ **11.4%/century**

These are the *density-derived* floors. Note that B3's density-derived floor is *higher* than B2's, not lower as the v0.2 placeholder (7%/century) suggested. This is because B3 has only 2 events in the M1 pilot — the modern era's "high documentary density" applies to T10 / TC-04 archives, not to ecumenical councils, where the modern band is sparsely populated.

**Recommendation.** v0.2.1 protocol patch should adopt the *density-derived* floors above, replacing the v0.2 placeholder values that were heuristically anchored on a "modern era has more data" intuition that does not apply to the M1 pilot:

| Band | v0.2 placeholder | v0.2.1 derived | Δ |
|---|---|---|---|
| B1 | 15%/century | 12.3%/century | tighter |
| B2 | 10%/century | 10%/century | unchanged (anchor) |
| B3 | 7%/century | 11.4%/century | looser |

---

## 5. Realised n per band and operative-vs-moot floor distinction

Under TC-06 v0.2 §5 condition 4 three-tier power rule:

- **B1 (n=7)** sits in the **n<8 strict-concordance + inconclusive-default tier**. The floor is operatively *moot for stationarity claims* — verdicts default to inconclusive regardless of the floor — but the floor remains *informative for MDE reporting*: the analytic memo reports the smallest trend the test was powered to detect, and the floor anchors interpretation of that report.
- **B2 (n=10)** sits in the **8≤n<15 weak-concordance-permitted tier with mandatory MDE reporting**. The floor is **operative**: a non-rejection that crosses the floor is **inconclusive**, not **stationary**.
- **B3 (n=1)** sits **far below the n<8 tier**. The floor is **moot** for the M1 pilot; only one interval cannot support trend testing. The floor matters for TC-04 (T10 archives) where B3 has more events.

**Practical consequence.** The B2 floor (10%/century, anchor) is the only floor that operationally gates stationarity-vs-inconclusive in TC-01. B1's floor is informational; B3's floor is M1-moot but TC-04-relevant.

This is itself a finding: the v0.1 uniform 10%/century floor and the v0.2 era-stratified three-band floor differ operationally on the M1 pilot mostly via *condition 4* (the three-tier power rule pushing B1 and B3 to inconclusive default), not via *condition 5* (the floor itself). The era-stratification is methodologically necessary but operationally light-touch on the M1 pilot specifically.

---

## 6. Sensitivity analysis

How robust are the derived floors to assumptions?

### 6.1 If documentary-density estimates change

The √(ρ_B2 / ρ_band) form is mild: a 50% change in band density yields a √2 ≈ 1.41× change in floor. The derived floors are not knife-edge.

### 6.2 If L₅ scale ranges (25–40 yr) are used

L₅ doesn't enter the floor numerics directly; it enters via the "anchor reference signal" argument in §3. The 10% anchor would shift modestly under different L₅ assumptions but not dramatically — the L₅-comparable factor at 7 centuries is roughly 2× regardless of whether L₅ = 25 yr or 40 yr.

### 6.3 If band boundaries are revised

The era boundaries (325 / 1100 / 1800 / 1965) are pre-declared and locked per Guardian Q1 ruling. The ±25 yr boundary addendum (TC-06 v0.2 §4.3) handles edge cases. If Guardian re-authorises a band-boundary shift in a future revision, the floors recompute via the same density formula.

### 6.4 If TC-04's T10 institutions yield very different density patterns

For TC-04 (IETF / W3C / ICANN), B3 has the densest documentary record (modern technical-coordination archives). Per-institution density would be ρ_B3,TC04 ≫ ρ_B2,TC04, giving floor_B3,TC04 < floor_B2,TC04 — the v0.2 placeholder pattern (7%/century in modern band) is correct *for TC-04*, just not for TC-01. This argues for **per-archive density derivation**, with v0.2.1 locking *TC-01-specific* floors and TC-04 deriving its own at TC-04 design time.

---

## 7. Recommended floors for TC-06 v0.2.1 §5 condition 5

For the M1 Catholic-councils pilot (TC-01):

| Band | Years | Floor (slope of log-interval per century) | Operative status under §5 condition 4 |
|---|---|---|---|
| **B1** | 325–1100 | **12.3%/century** | Moot (n=7, strict + inconclusive default); informational for MDE reporting |
| **B2** | 1100–1800 | **10%/century** | **Operative** (n=10, weak-concordance tier) |
| **B3** | 1800–1965 | **11.4%/century** | Moot (n=1, no test possible) |

**Per-archive derivation principle.** TC-04 (T10 archives) and TC-08 (defunct-archive paired-case) compute their own band-specific floors via the same √(ρ_B2 / ρ_band) formula at extraction time, with archive-specific density values. v0.2.1 protocol patch should specify the *formula* as the binding rule, not just the M1-specific numbers.

**Pre-declaration and lock.** Per Guardian Q1 ruling, band boundaries (325 / 1100 / 1800 / 1965) and the slope-floor formula (√(ρ_B2 / ρ_band) with B2 = 10%/century anchor) are pre-declared and locked against post-hoc revision except by explicit Guardian re-authorisation. The M1-specific numerical values follow from the formula and the pre-declared B2 anchor.

---

## 8. Open questions

- **Q-SF1.** Whether the B3 v0.2.1-derived floor (11.4%/century) should be rounded to a clean 12% for protocol clarity, or retained at one-decimal precision. Drafter recommendation: round all to half-percent precision (B1 = 12.5%, B2 = 10%, B3 = 11.5%) for cleaner pre-declaration and lock.
- **Q-SF2.** Whether the documentary-density covariate should account for *dating precision* in addition to event count. Some B1 events have decade-precision dates only; some B3 events have day-precision. This precision asymmetry is currently absent from the density formula. Drafter recommendation: log as a Q-SF2.1 follow-up; not blocking for v0.2.1 commitment but worth investigating before TC-01 extraction begins.
- **Q-SF3.** Whether the per-archive derivation principle (§7) creates a motte-and-bailey rescue surface: an archive with thin density per band could rescue stationarity claims by relaxing its floor. **R4 audit:** Guardian invited to rule on whether the formula's per-archive computation requires a *minimum density floor* below which the band is hard-excluded from stationarity testing rather than relaxed-floor admitted. Drafter recommendation: yes — set ρ_band ≥ 0.5 × ρ_B2 as a minimum, below which the band is hard-excluded from stationarity claims regardless of the relaxed floor. This applies cleanly to TC-01 B1 (ρ = 0.66, above 0.5 threshold) but would have hard-excluded a hypothetical even-sparser band.
- **Q-SF4.** Whether Q-SF3's minimum-density floor interacts with TC-06 v0.2 §5 condition 4's three-tier power rule. Both impose lower bounds on what bands can produce stationarity claims; the interaction needs explicit protocol text. Drafter recommendation: require *both* (n ≥ 8 AND ρ_band ≥ 0.5 × ρ_B2) for stationarity-claim admissibility, not just one.
- **Q-SF5.** Whether the derived floors should be regenerated on each TC-01 extraction-pass iteration as new event counts firm up, or locked once at v0.2.1. Drafter recommendation: lock at v0.2.1 with re-authorisation gate via Guardian — predictable rules > moving targets, even if the latter is more "accurate."

---

## 9. Document control

- **v0.1** (2026-04-28): Initial derivation under Architect invocation, in response to TC-06 v0.2 §8 binding follow-up. Anchor argument (§3 L₅-scale anchor for B2 = 10%/century); documentary-density covariate (§4 √(ρ_B2 / ρ_band) formula for B1 and B3); realised-n analysis (§5 — B1 and B3 floors moot for M1 stationarity claims, B2 floor operative); sensitivity analysis (§6 — robustness checks); locked numbers for TC-06 v0.2.1 (§7 — 12.3% / 10% / 11.4% per century, with rounding option Q-SF1). Q-SF1–Q-SF5 logged for Guardian R8-discipline review pass before v0.2.1 lock.
- **v0.2 horizon (memo).** Guardian R8 review pass; resolution of Q-SF1–Q-SF5; possible TC-04 / TC-08 archive-specific density-derivation appendices.
- **TC-06 v0.2.1 protocol patch (downstream).** Once this memo's derivation is Guardian-ratified, draft TC-06 v0.2.1 incorporating: (a) the locked B2 anchor at 10%/century; (b) the per-archive √(ρ_B2 / ρ_band) formula as the binding rule; (c) the M1-specific numerical values for TC-01; (d) the minimum-density floor (Q-SF3) and its interaction with the three-tier power rule (Q-SF4) if Guardian ratifies.

**Stance log.** Drafted Architect, in response to RT-2026-002 Q1 Guardian ruling that band-specific slopes be derived from L₅ scale with documentary-density covariate adjustment. The L₅ anchor argument (§3) reads more weight off the *cumulative-factor-over-band-span* form than off the *per-century instantaneous slope* form; this is a deliberate choice — Architect contends that slope is a derivative quantity whose meaning comes from cumulative effect, and the cumulative effect reads more naturally against the L₅ scale. The √(ρ_B2 / ρ_band) covariate form is mild and standard; a stronger form (e.g., 1/ρ_band linear) would produce more aggressive band differentiation but at the cost of treating the floor numerics as a power calculation, which Architect declines to do because the floor is procedural-not-power-analytic per §2. Q-SF3 motte-and-bailey audit is the most consequential open question — Architect recommends a binding minimum-density floor for protocol-text clarity, but defers the binding decision to Guardian.

**Linked.** `docs/protocols/human-timescales-commensurability-protocol-v0.2.md` (TC-06 v0.2 §5 condition 5, target of v0.2.1 lock); `meta/review-tasks/tc06-guardian-review-response-v0.1.md` (RT-2026-002 Q1 ruling, source of the binding follow-up); `docs/scoping/human-timescales-scoping-v0.2.md` §3 L₅ definition; `data/m1-catholic-councils/schema.md` (event count and date precision per band, basis for §4 density values).
