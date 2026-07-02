# Skill Leakage

## Smell

The repository instruction file contains copied skill bodies, tool manuals, or generic agent workflows. It stops being repository guidance and becomes a pile of reusable skill text.

## Why it hurts coding agents

Skill leakage expands context without adding project-specific truth. It can also override better scoped skills, trigger expensive workflows for simple tasks, and make the repository file stale whenever the copied skill changes elsewhere.

## Common symptoms

- `AGENTS.md` includes long sections named after skills.
- Generic frontend, debugging, or review workflows dominate the file.
- The same skill text appears in multiple repositories.
- Agents run broad verification for tiny non-UI edits.
- Repository-specific rules are shorter than copied reusable guidance.

## What the fixed version changes

- Removes copied skill bodies.
- Keeps only repository-specific commands and rules.
- Describes when specialized guidance is relevant without embedding the whole skill.
- Reduces broad trigger language.
- Leaves reusable skill maintenance to the skill files.

## How to review similar files

Ask whether each section is true because of this repository or true for many repositories. If it is generic reusable behavior, it probably belongs in a skill, not `AGENTS.md`. Keep only local commands, boundaries, ownership notes, and repo-specific exceptions.
