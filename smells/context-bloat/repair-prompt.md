# Repair Prompt: Context Bloat

Review the repository's agent instruction files, especially `AGENTS.md`, for context bloat.

Do not rewrite the project documentation. Make the smallest safe patch that turns the active instruction file into practical coding-agent guidance.

Please:

1. Identify stale history, duplicated docs, dead links, old setup commands, and narrative that agents should not act on.
2. Preserve current commands, safety constraints, project-specific conventions, and paths that help agents work.
3. Move or replace long background sections with short links to the right docs when those docs exist.
4. Remove conflicting old guidance instead of keeping it "for context."
5. Add a short precedence rule if nested instruction files or user task instructions may conflict.

After editing, summarize what was removed, what was preserved, how to verify the current commands, and what you intentionally left unchanged.
