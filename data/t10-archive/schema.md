# Schema — T10 Technical-Coordination Archive

**Format:** CSV (UTF-8, comma-delimited, RFC 4180).
**Filename (when populated):** `processed/t10-events.csv`
**Status:** Schema specification; data not yet collected.

## Column definitions

| Column | Type | Required | Description |
|---|---|---|---|
| `id` | string | yes | Stable identifier, e.g. `IETF-2018-LLC-formation`, `ICANN-2016-IANA-transition`. |
| `institution` | enum | yes | One of: `IETF`, `W3C`, `ICANN`, `IAU`, `IEEE`, `ISO`, `IEC`, `other` (declare in `notes`). |
| `event_layer` | enum | yes | `technical` or `governance`. Conflation forbidden. |
| `event_type` | enum | yes | For `technical`: `specification`, `recommendation`, `RFC`, `protocol-revision`, `other`. For `governance`: `charter-revision`, `mandate-change`, `sovereignty-transition`, `accountability-reform`, `restructuring`, `other`. |
| `event_name` | string | yes | Human-readable name. |
| `start_date` | ISO 8601 date | yes | When the event was initiated (proposal, draft, formal commencement). |
| `end_date` | ISO 8601 date | yes | When the event was completed (publication, ratification, contract expiry). |
| `lead_up_yr` | float | no | Years from earliest documented intent to `start_date`. Critical for governance-layer events. |
| `execution_yr` | float | derived | `end_date - start_date` in years. |
| `multi_domain_legitimacy` | enum | yes | `bounded-technical`, `partial-multi-domain`, `multi-domain`. Per QM1 criterion declared in `criterion_ref`. |
| `criterion_ref` | string | yes | Reference to the multi-domain-legitimacy criterion document used for assessment. |
| `external_stakeholders` | string | no | Stakeholder groups beyond the institution's core technical community. |
| `outcome_status` | enum | yes | `completed`, `partially-completed`, `failed`, `reversed`, `ongoing`. |
| `legitimacy_transfer_flag` | boolean | yes | Did this event involve transfer of authority to a new cohort or community? Critical for M-Conjecture testing. |
| `primary_source` | string | yes | Citation of primary archival source. |
| `secondary_source` | string | no | Additional sources. |
| `notes` | string | no | Free-text annotation. |
| `record_collector` | string | yes | ORCID or name. |
| `record_date` | ISO 8601 date | yes | When this record was added or last modified. |

## Controlled vocabularies

### `event_layer`

- `technical` — specification, protocol, recommendation, or operational decision within the institution's technical scope.
- `governance` — change in the institution's authority, structure, mandate, or accountability arrangements.

### `multi_domain_legitimacy`

- `bounded-technical` — authority is recognised only within the institution's technical scope.
- `partial-multi-domain` — authority extends beyond technical scope in some domains (e.g., commercial, civil-society) but not all.
- `multi-domain` — authority crosses spheres comparable to those covered by H₀ (legal, moral, economic, epistemic).

This classification is contested for some institutions (notably ICANN). The criterion used must be declared in `criterion_ref`.

### `outcome_status`

- `completed` — fully executed as planned.
- `partially-completed` — partially executed; remainder deferred or abandoned.
- `failed` — formally abandoned without execution.
- `reversed` — executed and subsequently undone.
- `ongoing` — initiated but not yet concluded as of `record_date`.

## Derived columns

`execution_yr = (end_date - start_date) / 365.25`. Where `start_date` and `end_date` are partial dates, derive with explicit precision and flag in `notes`.

## Predicted patterns under M-Conjecture

- For `event_layer = technical`: `execution_yr` should track communication-infrastructure availability over decades (not formally encoded, but observable across the dataset).
- For `event_layer = governance` with `legitimacy_transfer_flag = TRUE` and `multi_domain_legitimacy ≠ bounded-technical`: `lead_up_yr` should fall in the L₅ band (~25–40 years) or longer.
- A clean counter-example to M-Conjecture: a record with `event_layer = governance`, `legitimacy_transfer_flag = TRUE`, `multi_domain_legitimacy = multi-domain`, and `lead_up_yr` substantially below L₅.

## Validation

Validation script (to be added with TC-04 data) will check:
- All required columns non-null.
- `event_layer` and `event_type` consistent (technical types under technical layer, governance types under governance layer).
- Date consistency.
- `lead_up_yr` non-negative where supplied.

---

*v0.1 schema specification · 2026-04-27 · Stance: Architect (drafting). Reviewer: pending.*
