# Programme workplan post-v0.3.0 — memo

*Endorsement Marker (provisional). Internal scoping work, not a Coastline. No external endorsement is asserted.*

**Date drafted:** 2026-04-29.
**Drafter:** Architect (programme-state synthesis after tier-5 ratification).
**Status:** DRAFT for Council orientation; not a binding plan.
**Source:** [0.3.0] Outstanding section (CHANGELOG); RT-2026-006 ratified; tier-6 triage memo; current TC-card status as of v0.3.0.

---

## §1. Purpose

After the v0.3.0 governance ratification, the programme has three distinct streams of pending work:

- **Governance follow-up** — RT-2026-007 lodgement and three minor non-blocking items.
- **Tier-6 substantive deliberation** — three methodological concerns now unblocked.
- **Critical-path empirical work** — TC-06 v0.2.1 → TC-01 sequence on the binding 2026-12-31 timeline; TC-04 on the binding 2027-06-30 timeline.

This memo organises the streams by horizon (immediate / near-term / medium-term) and notes their interactions. It does not propose a binding schedule; it proposes a sequencing recommendation for Council and Integrator scheduling decisions.

---

## §2. Immediate (next ~2 weeks, by ~2026-05-13)

### Governance follow-up

- **RT-2026-007 lodgement** (binding via Architect Q5(c) ruling). Two routed candidates:
  - Decision-register-citation verification — convention requiring that any cited Council decision number exists and binds what is claimed.
  - Cross-tracker linkage symmetry enforcement — audit mechanism for the §8 bidirectional cross-link discipline.
  - Architect drafts the brief; smell-test optional; issuance per standard RT pattern.

- **Q1 tracker-header housekeeping** — add entry-numbering convention to the four append-only tracker headers (`council-decisions.md`, `falsification-tracker.md`, `horizon-signals.md`, `stance-log.md`). Trivial patch; can be combined with RT-2026-007 work.

### TC-06 v0.2.1 closure

- **Era-band slope-floor derivation memo** (already drafted at `docs/memos/era-band-slope-floor-derivation-memo-v0.1.md`) — requires Guardian R8 review pass per the v0.2.1 binding. On Guardian ratification, TC-06 v0.2.1 protocol patch lands and TC-01 extraction is unblocked.

---

## §3. Near-term (next ~1 month)

### Tier-6 substantive deliberation (unblocked by tier-5 closure)

Per the tier-6 triage memo (`docs/memos/tier6-audit-concerns-triage-memo-v0.1.md`), three concerns require Council ruling on remedy mechanism. Suggested order per the triage memo's §5:

1. **Concern 3 (TC-05 dependency-scoping gap)** — cheap, prevents recurrence. Recommended option: combined (a)+(b) — pre-assignment dependency-scoping codified in CONVENTIONS.md (now feasible under the new §7 review-tasks framework) plus a one-time accessibility pass across all eleven TC cards.
2. **Concern 1 (Inverse-R4 fragility)** — gates TC-01. Currently being handled in part by the RT-2026-005 §3 inverse-R4 catch-all (Guardian R3+R4 review on TC-07 v0.1, awaiting response). Council should decide whether RT-2026-005's existing handling is sufficient or whether an Architect-led pre-extraction calibration memo is required before TC-01 extraction begins.
3. **Concern 2 (R8 / R3 status thinness)** — gates TC-09 ledger work; longer timeline. Council can defer pending TC-04 + TC-08 progress, OR commission a third paired-case feasibility check now (e.g., dissolved Buddhist monastic lineage) to thicken R3 mitigation.

### TC-07 RT-2026-005 response window

- Guardian R3+R4 ruling on TC-07 reform-event sub-typing protocol v0.1 still pending (issued 2026-04-28; standard response window ~1–2 weeks). Domain-consultant identification deferred per Architect refinement; provisional Guardian-only response expected first.

### TC-08 v0.2 drafting

- Author may proceed pending: (i) anchor-house feasibility resolution (Canterbury > Glastonbury per the dissolution-cohort feasibility memo); (ii) TC-04 stratum-comparability coordination per RT-2026-004 §3 design-coherence requirements.

### TC-11 v0.2.1 follow-ups

- Math / theoretical-physics cohort source (Architect Q-BF2 ratified follow-up).
- Inverse-citation sweeps for the four anchor articles.
- Broader non-English search round (German + French institutional-longevity literature).
- Hostile-to-thesis source band.

These are independent of the critical path; can be drafted in parallel with empirical TC work.

---

## §4. Medium-term (next ~3–6 months, through 2026-Q3)

### Critical-path empirical work

- **TC-01 (Catholic ecumenical councils M1 pilot)** — target **2026-12-31** (binding via FH-001). Gated by TC-06 v0.2.1 closure + TC-07 RT-2026-005 closure + Concern 1 resolution. Drafter assignment requires domain-consultant pairing (per Concern 3 codification, dependency-scoping verified before authorisation).

- **TC-02 (ICANN/IANA Sail) + TC-03 (Vatican II Sail)** — T4 kill-criterion candidates, parallel-run. Either survival = T4 retained; both fail = T4 dropped. Target Q3 2026 ideally. Drafter assignments pending.

- **TC-04 (T10 archive characterisation)** — target **2027-06-30** (binding via FH-002 / FH-003). 3+ institutions: IETF, W3C, ICANN. ~3–4 weeks focused work; drafter pairing required (Architect + Internet-governance consultant).

- **TC-05 (T2/SF-7 → L₅ mapping)** — currently BLOCKED (UW-direct custodian; GLHC dossier access required). Per Concern 3 resolution, dependency-scoping should formalise this BLOCKED state and surface re-assignment criteria.

### Other parallel work

- **TC-09 (Breakwater ledger entry)** — synthesis deliverable; depends on TC-01 + TC-04 + TC-05. Initial entry by Q4 2026 if TC-01 lands on time.

- **TC-10 (Harbour latency-tracking protocol)** — proposed, Integrator authorisation pending. Independent of critical path; can issue any time.

---

## §5. Deferred / non-blocking

- **CITATION.cff machine validation** (Q10.4) — schedule for any post-v0.3.0 patch release.
- **Apache-2.0 "(when added)" clarification** (Q9.2) — first time `analysis/` gains code, drafter clarifies the trigger condition in LICENSE.md.
- **Schema-language migration** (Architect Q6.2) — markdown+YAML acceptable floor; formal schema languages (JSON Schema, frictionless-data) preferred medium-term and required where schemas are referenced by code. Triggers on first TC-01 / TC-04 schema referenced by analysis code.

---

## §6. Sequencing recommendations

**Suggested order for the next two weeks:**

1. RT-2026-007 lodgement (governance follow-up; cheap; unblocks future audit cycle).
2. Q1 tracker-header housekeeping (combine with #1).
3. TC-06 v0.2.1 Guardian R8 review pass on the era-band slope-floor memo (unblocks TC-01).
4. Council deliberation on tier-6 Concern 3 (cheap; prevents Concern-3-class recurrence on TC-04 and TC-08 v0.2 drafter assignments).

**Suggested order for the next month:**

5. Guardian RT-2026-005 response (TC-07).
6. Council deliberation on tier-6 Concern 1 (gates TC-01).
7. Author TC-08 v0.2 drafting (after anchor-house resolution + TC-04 coordination).
8. Author TC-11 v0.2.1 follow-ups (parallel; independent).

**Critical-path forcing functions:**

- **2026-12-31** — TC-01 binding deadline. Working backwards: TC-01 needs ~2 weeks focused work + domain-consultant pairing + TC-06 v0.2.1 + TC-07 ratification + Concern 1 resolution. Latest possible TC-01 start: ~2026-12-15. Realistic target start with buffer: ~2026-11-15 (mid-November).

- **2027-06-30** — TC-04 binding deadline. Latest possible start: ~2027-06-01. Realistic target with buffer: ~2027-04-15.

These deadlines mean the gate-clearing work (tier-5 closed; tier-6 in progress; TC-06 v0.2.1; TC-07 ratification) is **on the critical path now**, not slack.

---

## §7. Out of scope

This memo does not address:

- Substantive empirical findings (none yet — pre-falsification phase).
- Hypotheses H₀ / H₁ / M-Conjecture themselves (claim-substance).
- The risk-register R1–R10 substantive evolution (downstream of TC-04 / TC-08 findings).
- Non-programme work (Open-Science Harbour ecosystem coordination).

---

## §8. Document control

- **v0.1** (DRAFT for Council orientation, 2026-04-29): Initial workplan synthesis after v0.3.0 ratification. Three streams (governance follow-up; tier-6 deliberation; critical-path empirical) organised by horizon (immediate / near-term / medium-term). Sequencing recommendations not binding.
- **Pending:** Council direction on tier-6 deliberation scheduling; Integrator decisions on TC-card drafter assignments; user direction on RT-2026-007 timing.
- **Linked:** `CHANGELOG.md` `[0.3.0]` Outstanding section; `meta/council-decisions.md` 2026-017 (RT-2026-006 ratification); `docs/memos/tier6-audit-concerns-triage-memo-v0.1.md` (tier-6 substantive concerns); `docs/memos/era-band-slope-floor-derivation-memo-v0.1.md` (TC-06 v0.2.1 binding follow-up); `docs/task-cards/human-timescales-task-cards-v0.2.md` (current TC-card statuses).

**Stance log.** Drafted Architect on programme-state synthesis. Not a binding plan; sequencing recommendations are open to Integrator override based on actual drafter availability and Council scheduling. No veto.

---

*Architect-stance workplan memo. ~1100 words. DRAFT for Council orientation.*
