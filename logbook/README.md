# Logbook

Dated research logbook. Append-only, chronological, cross-referenced.

## Purpose

The logbook captures:

- Daily or weekly research activities and decisions.
- Stance invocations during the session.
- Open questions raised and resolved.
- Artifacts touched (created, edited, reviewed).
- Council interactions and deliberations.
- Cross-references to parent documents and task cards.

The logbook is **not** a substitute for:
- Substantive deliverables (those live in `../docs/`, `../analysis/`, `../data/`, `../ledger/`).
- Decision records (those live in `../meta/council-decisions.md`).
- Stance audit (that lives in `../meta/stance-log.md`, populated from logbook entries).

## Structure

```
logbook/
├── README.md            (this file)
├── _template.md         (template for new entries)
├── 2026-04/
│   └── 2026-04-27.md    (initial entry)
├── 2026-05/             (future entries)
└── _archive/            (archived old entries; rarely used in active programme)
```

Entries are organised by year-month directories. Filename is ISO date: `YYYY-MM-DD.md`.

## Discipline

- **Append-only.** Entries are not edited after the day they describe, except for typo corrections.
- **Cross-reference.** Every artifact touched is referenced by relative path.
- **Stance.** Every entry declares the stance(s) under which work was performed.
- **Open-question discipline.** Open questions raised should appear in subsequent entries when resolved or carried forward, with explicit closure notes.

## Granularity

Daily entries are the default for active research periods. Weekly summary entries are acceptable when the day-by-day record would be repetitive (e.g., a long focused-drafting period).

## FAIR reminders

Logbook entries:

- [ ] Date is in ISO 8601 format in both filename and content.
- [ ] Stance is declared.
- [ ] Cross-references use relative paths.
- [ ] Updates to artifacts are reflected in the artifact's own document control section, not just the logbook.

## Template

See `_template.md` for the entry template.

---

*v0.1 · 2026-04-27.*
