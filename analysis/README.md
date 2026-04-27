# Analysis

This directory holds analysis code: scripts and notebooks that operate on data in `../data/` and produce results consumed by documents in `../docs/` and entries in `../ledger/`.

## Structure

```
analysis/
├── README.md           (this file)
├── scripts/            (Python scripts, single-purpose, testable)
└── notebooks/          (Jupyter notebooks for exploration and reporting)
```

## Conventions

- **Language:** Python 3.11+ recommended. R or Julia permitted with declared environment.
- **Style:** PEP 8 for Python; type hints on public functions; docstrings on every public function.
- **Reproducibility:** seed declarations on stochastic computations; environment files (`requirements.txt`, `pyproject.toml`, or `environment.yml`) committed.
- **Determinism:** the `data/raw/ → data/processed/ → data/derived/` chain must be reproducible from committed scripts. If running a script does not reproduce the committed `processed/` or `derived/` files, the commit is incomplete.

## FAIR reminders

Code is part of FAIR data. Every analysis artefact must:

- [ ] Declare its inputs (paths in `../data/`).
- [ ] Declare its outputs (paths in `../data/processed/` or `../data/derived/`).
- [ ] Be runnable in isolation given declared inputs.
- [ ] Carry a header docstring describing purpose and provenance.
- [ ] Reference the task card it serves (TC-NN).

## Notebook discipline

- Notebooks should commit *with outputs stripped* unless an output is the deliverable. Use `nbstripout` or equivalent.
- Notebooks that ARE deliverables (reports, figures) commit with outputs included and are referenced from the deliverable they support.
- Long-running computations: cache intermediate results to `../data/derived/`; do not embed multi-hour computations inline in notebooks.

## License

All code in this directory is licensed under Apache-2.0 (see `../LICENSE.md`).

---

*v0.1 · 2026-04-27.*
