# AGENTS.md

## Working Priority

1. Follow explicit user instructions for the current task.
2. Follow the closest nested `AGENTS.md` for files in its scope.
3. Follow this file for repository-wide defaults.
4. If a rule would change product behavior, expose secrets, delete data, or deploy software, ask first.

## Change Scope

- Make the smallest safe change that solves the task.
- Refactor nearby code only when it is required for correctness or keeps the change reviewable.
- Do not edit generated files unless the task is explicitly about generation or the checked-in generated output must be updated with source changes.

## Testing

- Run focused tests for narrow changes.
- Run broader tests when touching shared behavior, data models, routing, or build configuration.
- Update snapshots only after inspecting the changed UI or output and confirming the change is intended.

## UI Rules

- Use the design system for product UI.
- Use native controls only when they are already the local pattern or when the design system does not provide the needed control.
- Do not change product copy unless the task requires it or the existing copy is clearly broken.

## Deployment And Git

- Do not deploy from an agent session unless the user explicitly asks.
- Do not create commits unless the user explicitly asks.
