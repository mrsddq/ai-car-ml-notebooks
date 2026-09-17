# AI Car ML Notebooks: Engineering Runbook

This repository is a learning archive. See the [README](../README.md) for its
structure and [review path](REVIEW_PATH.md) before selecting an experiment.

## Verify notebook structure

Use an isolated Python 3.11 environment from the repository root:

```bash
python -m venv .venv
source .venv/bin/activate
python -m pip install 'nbformat>=5.10,<6'
python scripts/check_notebooks.py
```

On Windows PowerShell, activate the environment with
`.venv\Scripts\Activate.ps1` instead of the `source` command.

The checker validates notebook JSON and schemas, excludes historical checkpoint
duplicates, and reports saved error outputs. It does not execute cells, download
datasets, train models or establish prediction accuracy. Historical outputs are
preserved; a schema pass does not mean every exercise runs successfully.

## Reproduce an experiment

Inspect the chosen notebook's imports, dataset paths and course instructions
before installing its dependencies. There is no single verified execution
environment for the whole archive. Run the selected notebook from top to bottom
in a separate environment and record package versions, dataset provenance,
random seeds, train/test split and fresh results in the
[experiment log](experiment-log.md). Do not describe saved historical results as
a new benchmark run.

Preserve course attribution and lesson context. Review `git diff --check` and
`git status --short` before committing, and exclude credentials, environments,
caches and newly downloaded datasets from commits.
