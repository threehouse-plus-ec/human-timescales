# Defunct-Institution Archives

**Task card:** TC-08 (Survivorship-bias control).
**Parent:** scoping v0.2 §5 M1 (Scout signal 2 / R3).
**Status:** Placeholder. Pending TC-08 feasibility check.

## Purpose

To address the survivorship-bias risk (R3) in the M1 pilot: long-archive datasets like Catholic ecumenical councils consist precisely of institutions that survived. If failed institutions had systematically shorter reform cycles (oscillated to death), observed survivor-stationarity is a selection effect, not evidence for H₀.

This directory will hold reform-cycle data reconstructed from at least one defunct institutional archive, sufficient for null-model comparison against the M1 pilot.

## Candidate archives

- **Knights Templar** (1119–1312). Extensive documentary trace including the 1312 papal bull *Vox in excelso* dissolving the order. Caveat: dissolution circumstances (papal suppression, political motive) may not represent generic dynamics.
- Dissolved monastic orders with extant cartularies.
- Failed corporations with documented restructuring histories before dissolution.

## Output

TC-08 deliverable is a feasibility memo (not yet a populated dataset). On positive feasibility, this directory will hold:

- `README.md` (revised, post-feasibility)
- `schema.md` (cohort-replacement events for the chosen defunct institution)
- `raw/`, `processed/`

On negative feasibility, this directory will hold the feasibility memo as the deliverable, with explicit acknowledgement that R3 is named but not corrected.

## FAIR discipline

Per `../README.md`. Defunct-archive data are particularly subject to documentary-survival asymmetry; provenance discipline is critical and must be flagged in any final dataset README.

---

*v0.1 placeholder · 2026-04-27.*
