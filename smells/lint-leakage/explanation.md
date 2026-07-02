# Lint Leakage

## Smell

The instruction file copies linter rule catalogs, formatter trivia, and broad cleanup advice into active agent guidance. The file becomes a second, less accurate version of the tool config.

## Why it hurts coding agents

Agents do not need a copied list of lint rule codes to write or verify code. They need current commands and scope guidance. Lint leakage encourages broad mechanical churn, distracts from task behavior, and creates conflicts when the real lint config changes.

## Common symptoms

- Long lists of lint rule codes appear in `AGENTS.md`.
- The file explains tool behavior already encoded in config.
- Agents fix unrelated lint warnings while doing a narrow task.
- Formatter instructions conflict with the actual formatter config.
- Review diffs include large style-only changes outside the requested scope.

## What the fixed version changes

- Keeps current lint and format commands.
- Points to `pyproject.toml` as the source of truth.
- Adds scope guidance for lint cleanup.
- Removes copied rule catalogs.
- Warns against accepting unrelated formatter churn without inspection.

## How to review similar files

Keep commands and workflow rules. Delete copied linter documentation. If a rule is project-specific and not obvious from config, keep one sentence explaining why it matters. Otherwise link to the config and let the tool report exact violations.
