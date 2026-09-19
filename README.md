# AI Car ML Notebooks

Machine learning notebook archive for introductory AI car concepts, Python fundamentals, and applied ML experiments.

This repository is kept as a learning archive, but it is structured so the work can be reviewed and extended without guessing where things belong.

## Structure

```text
Introduction to Python and Machine Learning/
docs/
  experiment-log.md
  notebook-review-checklist.md
```

## How to Use

1. Create a virtual environment.
2. Open the notebooks in VS Code or JupyterLab.
3. Run notebooks from top to bottom.
4. Record findings in `docs/experiment-log.md`.

## Learning Goals

- Python data handling
- exploratory data analysis
- model training basics
- model evaluation
- reproducible notebook habits

## Status

Learning archive with reproducibility docs. For polished ML project templates, use `python-ml-project-template`.

Use [docs/REVIEW_PATH.md](docs/REVIEW_PATH.md) to rerun the notebooks and decide whether one experiment deserves extraction.
## Lightweight verification

From the repository root, use an isolated Python 3.11 environment:

```bash
python -m venv .venv
source .venv/bin/activate  # Windows PowerShell: .venv\Scripts\Activate.ps1
python -m pip install 'nbformat>=5.10,<6'
python scripts/check_notebooks.py
```

CI checks that notebook JSON and notebook schemas are readable; it does not execute cells, train models, download datasets, or establish model accuracy. Historical checkpoint duplicates are excluded. Saved error outputs are reported rather than silently erased: some exercises intentionally demonstrate errors, and others still need repair. Existing outputs are historical, not fresh experiment results.

To run an experiment, inspect its imports, dataset paths, and course instructions first; then use a separate environment and record package versions, random seeds, train/test split, and fresh results. There is no single verified environment for every notebook in this archive.
