# AGENTS.md

## Project

Sample Python package used as a fixture for agent-instruction reviews.

## Commands

```bash
python -m pip install -e .
python -m pytest
python -m ruff check .
```

## Working Rules

- Keep examples small and readable.
- Do not add runtime dependencies to this fixture.
- Treat `pyproject.toml` as the source of truth for Python metadata and tool settings.
- If a command is not available locally, report that clearly instead of inventing a replacement.
