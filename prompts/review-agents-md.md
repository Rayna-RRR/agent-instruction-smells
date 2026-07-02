# Prompt: Review AGENTS.md

Review the repository's `AGENTS.md` and any nested agent instruction files.

Do not rewrite the whole file unless it is necessary. Make the smallest safe patch that improves usefulness for coding agents.

Check for:

- Context bloat.
- Conflicting instructions.
- Stale setup, test, lint, build, or deploy commands.
- Lint or formatter documentation copied into the instruction file.
- Skill bodies or tool manuals pasted into repository guidance.
- Unsafe instructions involving tests, secrets, git history, destructive commands, approvals, deployments, or releases.

When editing:

1. Preserve repository-specific commands, paths, conventions, and risk areas.
2. Remove stale, generic, duplicated, or contradictory guidance.
3. Add precedence rules only if multiple instruction sources can conflict.
4. Keep the file readable and short.
5. Do not create a CLI, generator, dependency, or new instruction framework.

After editing, summarize what changed, why it was necessary, how to verify the current commands, and what was intentionally not changed.
