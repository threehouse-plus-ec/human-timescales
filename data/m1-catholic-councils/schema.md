# Schema — M1 Catholic Ecumenical Councils

**Format:** CSV (UTF-8, comma-delimited, RFC 4180).
**Filename (when populated):** `processed/catholic-councils.csv`
**Status:** Schema specification; data not yet collected.

## Column definitions

| Column | Type | Required | Description |
|---|---|---|---|
| `id` | integer | yes | Sequential integer (1 = Nicaea I, ..., 21 = Vatican II). |
| `name` | string | yes | Canonical name in English (e.g., "Council of Nicaea I"). |
| `latin_name` | string | no | Latin name where canonically used. |
| `start_date` | ISO 8601 date | yes | Council opening date. Format: `YYYY-MM-DD`. Where day or month uncertain, use `YYYY-MM-XX` or `YYYY-XX-XX` and declare in `date_uncertainty`. |
| `end_date` | ISO 8601 date | yes | Council closing date. Same format conventions. |
| `start_julian` | boolean | yes | TRUE if start_date is in Julian calendar; FALSE if Gregorian (proleptic where pre-1582). |
| `date_uncertainty` | string | no | Free-text annotation of date imprecision or contested dating. |
| `location` | string | yes | City of convening (modern English name). |
| `subtype_doctrinal` | boolean | yes | Council addressed doctrinal questions (creeds, dogma, theological clarification). Per TC-07 protocol. |
| `subtype_structural` | boolean | yes | Council addressed structural questions (governance, hierarchy, jurisdiction). Per TC-07 protocol. |
| `subtype_disciplinary` | boolean | yes | Council addressed disciplinary questions (clerical conduct, sacramental practice, lay obligations). Per TC-07 protocol. |
| `subtype_notes` | string | no | Free-text annotation on sub-typing ambiguity. |
| `recognised_catholic` | boolean | yes | Recognised as ecumenical by the Catholic Church (TRUE for all 21 canonical events). |
| `recognised_orthodox` | boolean | yes | Recognised as ecumenical by the Eastern Orthodox tradition. |
| `recognised_status_notes` | string | no | Annotations on contested status (e.g., Pisa 1409, Constantinople IV). |
| `external_shock_tag` | enum | no | Predominant external context. Allowed values: `none`, `political-reform`, `theological-controversy`, `schism`, `reformation`, `modernity`, `war`, `migration`, `other`. |
| `external_shock_notes` | string | no | Free-text annotation. |
| `interval_to_previous_yr` | float | derived | Years from previous council's `end_date` to this council's `start_date`. NULL for id=1. |
| `commensurability_protocol` | string | yes | Declared protocol per TC-06. Values: `calendar-julian`, `calendar-gregorian-proleptic`, `internal-time`, `dual`. |
| `primary_source` | string | yes | Citation of primary source for dates and status. |
| `secondary_source` | string | no | Additional sources where primary insufficient. |
| `record_collector` | string | yes | ORCID or name of data collector. |
| `record_date` | ISO 8601 date | yes | Date this record was added or last modified. |

## Controlled vocabularies

### `external_shock_tag`

- `none` — no identifiable external precipitating context.
- `political-reform` — convened in response to political reorganisation (e.g., imperial succession).
- `theological-controversy` — convened to resolve a doctrinal dispute already in progress.
- `schism` — convened in response to or aftermath of ecclesial schism.
- `reformation` — convened in response to the Protestant Reformation.
- `modernity` — convened in response to modernist intellectual or social challenges.
- `war` — convened in immediate aftermath of major war.
- `migration` — convened in response to demographic shift.
- `other` — annotate in `external_shock_notes`.

### `commensurability_protocol`

Declared per TC-06. The value chosen affects how `interval_to_previous_yr` is computed and interpreted. See `../../docs/task-cards/human-timescales-task-cards-v0.1.md` (TC-06).

## Derived columns

`interval_to_previous_yr` is derived; its computation depends on `commensurability_protocol`. The derivation script lives in `../../analysis/scripts/` (to be added by TC-01 drafter).

## Missingness

Required columns must be non-null. Optional columns may be empty (empty string for strings, empty for floats). NULL handling is via empty string or `NaN` per CSV convention; declared explicitly in derived columns where applicable.

## Validation

A validation script (to be added with TC-01 data) will check:
- All required columns non-null.
- Sub-type booleans: at least one TRUE per record (every council does at least one kind of work).
- Date consistency: `start_date <= end_date`.
- Interval consistency: `interval_to_previous_yr >= 0` for id ≥ 2.

---

*v0.1 schema specification · 2026-04-27 · Stance: Architect (drafting). Reviewer: pending.*
