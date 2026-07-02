# agent-instruction-smells

Copyable bad-and-fixed examples for `AGENTS.md`, `CLAUDE.md`, `SKILL.md`, Cursor rules, and other coding-agent instruction files.

Most agent instructions fail in predictable ways: stale commands, copied tool docs, broad skill triggers, contradictory rules, context bloat, and unsafe shortcuts. This repo is a reusable smell catalog, not a linter, scanner, CLI, or generator.

Each smell includes a synthetic but realistic bad example, a safer fixed version, reviewer notes, and a repair prompt you can paste into Codex, Claude Code, Cursor, or another coding assistant.

## Safety And Example Scope

- Bad examples are anti-patterns. Do not copy or follow them as recommended instructions.
- Examples are synthetic or heavily anonymized. Do not paste private repository instructions into public examples.
- This repo is an educational and workflow-quality resource, not a security scanner, policy engine, or substitute for code review.

## What This Repo Provides

- Bad and fixed instruction-file examples for common failure modes.
- Explanations written for maintainers, not just tool authors.
- Repair prompts that turn vague cleanup work into a focused agent task.
- Checklists for reviewing instruction files before and after agent setup.
- Small fixtures you can use in docs, workshops, tests, or internal reviews.

## Who Should Use It

Use this repo if you:

- Maintain `AGENTS.md`, `CLAUDE.md`, `SKILL.md`, or coding-agent rules.
- Review pull requests that change agent instructions.
- Want a compact teaching corpus for team onboarding.
- Need examples of what "too much instruction" looks like.
- Suspect your agents are following old commands, broad triggers, or conflicting guidance.

## Smell Index

| Smell | File type | Risk | Use when | Action |
| --- | --- | --- | --- | --- |
| [Context bloat](smells/context-bloat/) | `AGENTS.md` | High | The file reads like a wiki dump instead of task guidance. | [Copy repair prompt](smells/context-bloat/repair-prompt.md) |
| [Conflicting instructions](smells/conflicting-instructions/) | `AGENTS.md` | High | Different sections tell agents to do incompatible things. | [Copy repair prompt](smells/conflicting-instructions/repair-prompt.md) |
| [Stale commands](smells/stale-commands/) | `AGENTS.md` | Medium | Setup, test, or deploy commands fail or reference removed tools. | [Copy repair prompt](smells/stale-commands/repair-prompt.md) |
| [Lint leakage](smells/lint-leakage/) | `AGENTS.md` | Medium | Linter or formatter trivia crowds out real workflow guidance. | [Copy repair prompt](smells/lint-leakage/repair-prompt.md) |
| [Skill leakage](smells/skill-leakage/) | `AGENTS.md` | Medium | Project instructions embed long skill bodies or copied tool docs. | [Copy repair prompt](smells/skill-leakage/repair-prompt.md) |
| [Overbroad skill trigger](smells/overbroad-skill-trigger/) | `SKILL.md` | High | A skill claims almost every task and steals context from better guidance. | [Copy repair prompt](smells/overbroad-skill-trigger/repair-prompt.md) |
| [Rubber-stamp reviewer](smells/rubber-stamp-reviewer/) | `SKILL.md` | High | Review instructions push approval instead of finding defects. | [Copy repair prompt](smells/rubber-stamp-reviewer/repair-prompt.md) |
| [Unsafe skill instructions](smells/unsafe-skill-instructions/) | `SKILL.md` | Critical | A skill asks agents to bypass approvals, secrets, tests, or safety checks. | [Copy repair prompt](smells/unsafe-skill-instructions/repair-prompt.md) |

## How To Use One Smell Case

1. Open a smell folder under `smells/`.
2. Read `bad.*.md` to recognize the failure mode.
3. Compare it with `fixed.*.md` to see the smaller, safer shape.
4. Read `explanation.md` for review heuristics.
5. Copy `repair-prompt.md` into your coding agent and point it at your own instruction file.

Example:

```text
smells/conflicting-instructions/
  bad.AGENTS.md
  fixed.AGENTS.md
  explanation.md
  repair-prompt.md
```

## How To Contribute A New Smell

Add one focused smell folder. Keep it small enough that a reader can understand it without running tools.

Each smell should include:

- A bad example that is synthetic but realistic.
- A fixed example that keeps useful intent and removes the failure mode.
- An `explanation.md` with these headings:
  - Smell
  - Why it hurts coding agents
  - Common symptoms
  - What the fixed version changes
  - How to review similar files
- A `repair-prompt.md` that is directly copy-pastable.

Good contributions make the smell sharper, not the repository larger for its own sake.
