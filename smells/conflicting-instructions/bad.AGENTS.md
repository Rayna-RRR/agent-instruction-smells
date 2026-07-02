# AGENTS.md

## General Rules

- Always make the smallest possible change.
- Always refactor nearby code while you are there.
- Never touch generated files.
- Regenerate API clients after every backend-related change.
- Never ask the user for clarification.
- Ask before changing product behavior.
- Commit after every successful edit.
- Do not create commits unless the user explicitly asks.

## Testing

- Run the full test suite before finishing.
- Avoid running slow tests unless the user asks.
- Update snapshots whenever they fail.
- Never update snapshots without inspecting the UI.

## UI Rules

- Use the design system for all UI.
- Plain HTML controls are preferred because they are easier to debug.
- Do not add new copy without product approval.
- Improve unclear copy opportunistically.

## Deployment

- If the build passes, deploy to staging.
- Never deploy from an agent session.

## If Something Is Confusing

Use your best judgment and keep moving.
