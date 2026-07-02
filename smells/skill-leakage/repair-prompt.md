# Repair Prompt: Skill Leakage

Review the repository's agent instruction files for skill leakage.

Make a small patch that removes copied reusable skill content from repository-level instructions while preserving local project guidance.

Please:

1. Identify sections that are generic skill bodies, tool manuals, or reusable workflows rather than repository-specific rules.
2. Remove copied skill content from `AGENTS.md` or equivalent repo instructions.
3. Keep local commands, file ownership notes, risk areas, and project-specific exceptions.
4. Replace long copied skill sections with short references to when specialized guidance is relevant.
5. Avoid creating new skill files unless the user explicitly asks.

After editing, summarize what generic skill content was removed, what local guidance remains, and whether any reusable skill should be reviewed separately.
