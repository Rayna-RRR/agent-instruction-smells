# Review Before Adding A Skill

Use this before adding a `SKILL.md` or similar reusable agent instruction.

## Trigger

- The skill has one clear job.
- The "when to use" section is narrower than "any coding task."
- The skill says when not to use it.
- The skill does not claim priority over all other skills.
- The trigger can be understood without reading the whole skill.

## Instructions

- Steps support the stated trigger.
- The skill does not require broad repo inspection for narrow tasks.
- The skill does not ask agents to refactor opportunistically.
- The skill does not duplicate repository-specific commands.
- The skill does not copy large external tool docs.

## Safety

- No instruction bypasses approvals, sandbox rules, tests, or review.
- No instruction permits secrets in tracked files.
- No instruction permits destructive git operations without explicit user approval.
- No instruction tells agents to hide failures or warnings.
- Verification limits must be reported, not buried.

## Output

- The output format helps the user make a decision.
- The skill can report "no findings" or "not applicable" when appropriate.
- The skill does not default to approval.
- Required summaries are proportional to the task.

## Keep Or Cut

Cut any sentence that is:

- Generic enough to belong in global guidance.
- True only for one repository.
- A copied tool manual.
- A workaround for an old agent failure that no longer applies.
