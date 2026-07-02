# Instruction Review Skill

## When to use

Use this skill when the user asks to review or improve `AGENTS.md`, `CLAUDE.md`, `SKILL.md`, Cursor rules, or another coding-agent instruction file.

Do not use this skill for ordinary application code reviews unless the instruction file itself is part of the change.

## Instructions

1. Identify the instruction file type and its intended scope.
2. Check for bloat, stale commands, conflicts, unsafe guidance, copied tool docs, and overbroad triggers.
3. Preserve project-specific commands, paths, conventions, and safety constraints.
4. Prefer small edits over rewrites.
5. Report anything that needs human review before publishing.

## Output

Summarize the smell found, the fix made or recommended, verification performed, and any remaining review items.
