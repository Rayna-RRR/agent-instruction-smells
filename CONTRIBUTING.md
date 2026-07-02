# Contributing

This repository is a smell catalog, not a tool. Contributions should improve the examples, explanations, prompts, or review checklists without turning the project into a scanner, CLI, or generator.

## Contribution Rules

- Write in English.
- Use synthetic or heavily anonymized examples only.
- Do not paste real repository instructions, private policy text, client guidance, or internal tool docs without permission.
- Keep the tone practical and direct.
- Prefer one focused smell over a broad "misc cleanup" case.
- Keep examples readable without setup, dependencies, or generated assets.
- Do not add package dependencies.
- Do not add a CLI.

## New Smell Template

Create a folder under `smells/<smell-name>/` with:

```text
bad.AGENTS.md or bad.SKILL.md
fixed.AGENTS.md or fixed.SKILL.md
explanation.md
repair-prompt.md
```

Use `AGENTS.md` examples for repository-level instructions and `SKILL.md` examples for reusable skill instructions.

## Explanation Format

Every `explanation.md` must use these headings:

```markdown
# <Readable smell name>

## Smell

## Why it hurts coding agents

## Common symptoms

## What the fixed version changes

## How to review similar files
```

## Review Standard

Before opening a pull request, check that:

- The bad example is obviously flawed but still realistic.
- The fixed example preserves useful intent and repairs the same underlying artifact.
- The explanation teaches a reviewer what to look for next time.
- The repair prompt can be copied into Codex, Claude Code, or Cursor without editing.
- No file is empty.
- No generated dependency or build artifact was added.

## License

By contributing, you agree that your contribution will be licensed under the MIT License.
