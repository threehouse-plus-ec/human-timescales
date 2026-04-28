# Horizon-Signal Register

Scout-flagged horizon signals across the programme. Append-only with status updates appended (entries themselves are not modified except for typo corrections).

Distinct from `falsification-tracker.md` (formal claim handles, FH-NNN) and from the `docs/scoping/*` risk register (R1–R10). This file tracks **horizon signals** — Scout-stance early-warning flags that have not been promoted to risk-register entries or formal falsification handles, plus risk-register status updates that emerge from review passes.

Format:
- **Signal ID.** SF-NNN.
- **Issued.** Date.
- **Issuer.** Stance and source artifact.
- **Statement.** What the signal says.
- **Target deliverable.** Where the signal bites.
- **Status.** LIVE / PROMOTED-TO-RISK / PROMOTED-TO-FH / CLOSED.
- **Resolution.** Filled in when status changes.

---

## SF-7

- **Issued:** Pre-2026-04-27 (existing; carried forward in scoping v0.2 §2 T2).
- **Issuer:** Scout, GLHC dossier work.
- **Statement:** Custodial-attenuation envelope of ~2–3 generations across multiple creative traditions in the GLHC dossier.
- **Target deliverable:** TC-05 (T2 / SF-7 → L₅ mapping).
- **Status:** LIVE.
- **Resolution:** *(pending TC-05 — drafter is UW-direct custodian; held until UW-direct drafting.)*

## SF-8

- **Issued:** 2026-04-28.
- **Issuer:** Scout, response to RT-2026-001 (`meta/review-tasks/tc06-scout-review-response-v0.1.md`).
- **Statement:** *Coverage-correction divergence artifact.* If TC-01 applies coverage correction differently per channel (e.g., documentary-density proxies for calendar time, succession-completeness proxies for institution-internal time), channel divergence under TC-06 dual measurement may be artifactual rather than substantive.
- **Target deliverable:** TC-01 coverage-correction methodology; TC-06 v0.2 revision (require coverage-correction methods declared channel-explicit; add `coverage-artifact` as a divergence-cause tag in TC-06 §4.4).
- **Status:** LIVE.
- **Resolution:** *(pending TC-06 v0.2 revision pass.)*

- **Update issued:** 2026-04-28 (later same day).
- **Source:** Guardian response to RT-2026-002 (Q3 ruling).
- **Update text:** SF-8's prescription to add `coverage-artifact` as a §4.4 divergence-cause tag is **ratified** by Guardian Q3 ruling and lands in the expanded six-tag set for TC-06 v0.2 (`tenure-trend`, `succession-contested`, `coverage-gap`, `coverage-artifact`, `R8-residual-confirmed`, `none-identified`). SF-8 status remains LIVE pending TC-06 v0.2 drafting; the channel-explicit coverage-correction declaration is also ratified for v0.2 inclusion.

## SF-9

- **Issued:** 2026-04-28.
- **Issuer:** Scout, response to RT-2026-001.
- **Statement:** *Multi-tagging era-heterogeneity inflation.* Modern councils (Trent, Vatican I, Vatican II) have richer documentary records than early-medieval ones. Strict multi-tagging under TC-07 will therefore produce higher multi-tag rates in recent eras, creating era-correlated sub-type stratification that looks like temporal trend but is source-heterogeneity bias.
- **Target deliverable:** TC-07 inter-coder reliability sampling (require era-stratified calibration samples, not only sub-type-stratified); TC-07 v0.2 revision.
- **Status:** LIVE.
- **Resolution:** *(pending TC-07 v0.2 revision pass and the calibration pilot per TC-07 §7.)*

## SF-10

- **Issued:** 2026-04-28.
- **Issuer:** Guardian, response to RT-2026-002 (`meta/review-tasks/tc06-guardian-review-response-v0.1.md`).
- **Statement:** *Boundary-condition fragility.* Era-band boundaries (Q1: 1100, 1800), n-tier cut-offs (Q2(b): 8, 15), and sample-size cut-offs (Q5: 30) introduce step-function discontinuities under the TC-06 v0.2 design. An analyst whose sample is n = 14 vs n = 15 picks different concordance rules; an interval at year 1099 vs year 1101 picks different effect-size floors and channel-dominance presumptions. This is a generic R8/R4 rescue surface where verdicts can flip across the cut-off without methodologically defensible reason.
- **Target deliverable:** TC-06 v0.2 §5 (procedural mitigation drafted into the conditions, not appended): Q1 boundary addendum (verdicts within ±25 yr of a band boundary reported under both adjacent rules); Q2(b) tier-overlap reporting; Q5 written-deviation requirement.
- **Status:** PROCEDURALLY-MITIGATED-IN-V0.2-DESIGN; LIVE pending v0.2 ratification.
- **Resolution:** *(pending TC-06 v0.2 drafting and downstream verification that the mitigations are load-bearing in TC-01 / TC-04 / TC-08 use.)*

---

## Risk-register status updates

Substantive updates to risk-register entries (R1–R10 in scoping v0.2 §9) that emerge from review passes and require findable trail before scoping-document revision incorporates them.

### R8 — Temporal parallax

- **Update issued:** 2026-04-28.
- **Source:** Scout response to RT-2026-001 (R8 closure call).
- **Update text:** R8 status is **procedurally-managed-but-live**. Dual measurement under TC-06 v0.1 does not close R8; it converts R8 from an unexamined assumption into an empirically reportable quantity, which is a methodological advance, but the temporal-parallax risk itself remains active wherever channels diverge. R8 closes only when stable cross-channel calibration is demonstrated across at least two distinct institutional forms — i.e., post-TC-04. Until then, every stationarity claim issued under TC-06 carries a live R8 residual that must be declared in the claim's annotation.
- **Binding effect:** v0.3 of the scoping document must update §9 R8 to reflect this status; intermediate deliverables (TC-09, ledger-drafts) must annotate the R8 residual on every stationarity claim.

- **Update issued:** 2026-04-28 (later same day; Guardian ruling on RT-2026-002 Q4 supersedes the Scout closure-call on closure scope only, leaves the procedurally-managed-but-live status intact).
- **Source:** Guardian response to RT-2026-002 (`meta/review-tasks/tc06-guardian-review-response-v0.1.md`), Q4 ruling.
- **Update text:** R8 closure now requires *both* TC-04 (cross-institution portability) *and* TC-08 (defunct-archive paired-case for survivor-vs-defunct robustness), plus satisfaction of three Guardian-pre-declared thresholds: (i) per-interval channel-ratio bound — variation by no more than a factor of 2 from the cross-case median across all paired intervals in TC-04 and TC-08; (ii) no tag-cluster dominance — neither `tenure-trend` nor `R8-residual-confirmed` modal in any TC-04 case or in the TC-08 paired-case set; (iii) cross-form coverage — at least one TC-04 case and at least one TC-08 case characterised without invoking the Q2(b) lower-tier weak-concordance regime as the modal verdict-issuance pathway. On satisfaction, R8 status moves to **closed-conditional-on-thresholds**, with the three thresholds themselves subject to Guardian re-authorisation if any TC-04 or TC-08 finding exposes their fragility.
- **Binding effect:** TC-06 v0.2 §6 must encode the three thresholds. The pre-staged TC-08 Guardian R3 brief (provisional RT-2026-004) §1 must be revised pre-issuance to reflect that TC-08 is gating to R8 closure as well as R3 closure. v0.3 of the scoping document carries the closure-conditional status forward in §9 R8.

---

*Append below this line. Update statuses with new dated entries below the original entry, not by editing the original.*
