# AGENTS.md

## Current Commands

Use Python 3.12.

```bash
python -m pip install -e ".[dev]"
pytest
ruff check .
ruff format .
```

## Coding Guidance

- Follow the existing local style before introducing a new pattern.
- Keep lint fixes scoped to files relevant to the task unless the user asks for a broader cleanup.
- Do not churn unrelated files just to satisfy project-wide lint warnings.
- If `ruff format .` changes unrelated files, inspect the diff before keeping those changes.

## Where Lint Rules Live

Ruff configuration is in `pyproject.toml`. Treat that file as the source of truth for enabled rules and formatting settings.
