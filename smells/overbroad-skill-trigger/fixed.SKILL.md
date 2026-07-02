# Targeted Coding Skill

## When to use

Use this skill only for a clearly scoped repository task, such as a small implementation, focused bug fix, narrow refactor, related test or docs update, or review of a specific diff.

Do not use this skill for broad architecture research, whole-repo cleanup, dependency upgrades, deployment or release tasks, security audits, open-ended planning, or work covered by a more specific skill.

## Instructions

1. Restate the task boundary before expanding scope.
2. Inspect the relevant files, callers, and project commands; expand only when evidence shows the task depends on it.
3. Reuse existing project patterns and make the smallest safe change.
4. Do not refactor, rename, add tests, or update docs opportunistically unless the task or risk requires it.
5. If the task is review-only, do not edit files; report findings with evidence.
6. Run verification that matches the changed surface or review scope.
7. Ask before destructive git operations, deployments, release changes, secrets handling, or product behavior changes.

## Output

For implementation tasks, summarize the files changed, why the change was necessary, verification performed, and what was intentionally not changed.

For review tasks, list findings by severity, then open questions, verification notes, and a short summary.
