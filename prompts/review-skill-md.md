# Prompt: Review SKILL.md

Review the current `SKILL.md` for instruction quality.

Make a narrow patch that keeps the skill useful while reducing bad triggers, unsafe behavior, and review noise.

Check for:

- A trigger that matches too many tasks.
- Missing "do not use" cases.
- Instructions that duplicate repository-specific guidance.
- Instructions that encourage broad refactors during narrow tasks.
- Review behavior that defaults to approval.
- Unsafe guidance involving tests, approvals, secrets, destructive commands, deployments, or git history.

When editing:

1. Make the "when to use" section specific.
2. Add non-goals where nearby tasks could be confused with this skill.
3. Keep only steps that support the narrowed use case.
4. Preserve safety constraints.
5. Keep the output format proportional to the work.

After editing, summarize the old trigger, the new trigger, the safety changes, and any remaining human-review items.
