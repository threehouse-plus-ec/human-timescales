# Data

This directory holds empirical datasets for the programme. Data discipline follows FAIR principles (see `../FAIR.md`) with operational requirements declared below.

## Structure

Each dataset lives in its own subdirectory, named by the task card it serves (e.g., `m1-catholic-councils/` for TC-01). Each dataset directory contains:

```
dataset-name/
├── README.md          (purpose, source, coverage, limitations, licence)
├── schema.md          (column definitions, types, controlled vocabularies)
├── raw/               (primary archival extracts, untransformed)
├── processed/         (cleaned, normalised, ready for analysis)
└── derived/           (analytic products: aggregates, summaries — optional)
```

## FAIR discipline (per dataset)

Before any data commit, ensure:

- [ ] `README.md` is current and declares purpose, source, coverage period, collector, collection method, known limitations, licence.
- [ ] `schema.md` declares every column with type, units (where applicable), allowed values, and missingness handling.
- [ ] Tabular data is in CSV (UTF-8, comma-delimited, RFC 4180) or TSV with explicit declaration.
- [ ] Provenance is traceable: every record can be sourced back to a primary archive or the derivation script that produced it.
- [ ] Licence is declared in the dataset README.
- [ ] If derivative: derivation script committed to `../analysis/` and referenced in this dataset's README.

## State directories

- **`raw/`** — primary archival extracts. Untransformed. Read-only after commit.
- **`processed/`** — cleaned, normalised, schema-conforming. Ready for analysis. Reproducible from `raw/` via committed analysis scripts.
- **`derived/`** — analytic products (aggregates, computed statistics, summary tables). Reproducible from `processed/` via committed analysis scripts.

The `raw/ → processed/ → derived/` chain must be reproducible. If it is not, the commit is incomplete.

## Active datasets

| Dataset | Task card | Status |
|---|---|---|
| `m1-catholic-councils/` | TC-01 | placeholder; awaits TC-06/07 prerequisites |
| `t10-archive/` | TC-04 | placeholder |
| `defunct-archives/` | TC-08 | placeholder |

## Cross-era commensurability protocol

For datasets with cross-era temporal data (M1, T10), the commensurability protocol declared in TC-06 must be applied and noted in the dataset `README.md`. Without protocol declaration, downstream stationarity claims are invalidated.

## Survivorship-bias control

For long-archive datasets, the survivorship-bias control (TC-08) applies. Where applicable, dataset README must indicate whether defunct-institution data is included or whether the bias is acknowledged but uncorrected.

---

*v0.1 · 2026-04-27.*
