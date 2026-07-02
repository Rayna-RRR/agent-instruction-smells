# Smell Taxonomy

This taxonomy groups instruction-file smells by the way they degrade agent work.

## 1. Context Quality Smells

These make the agent carry too much or the wrong kind of context.

- Context bloat
- Skill leakage
- Lint leakage

Primary repair: compress the file around task-relevant rules, current commands, and links to deeper docs.

## 2. Instruction Reliability Smells

These make the agent follow guidance that is wrong or ambiguous.

- Stale commands
- Conflicting instructions

Primary repair: verify commands, remove obsolete sections, and make precedence explicit.

## 3. Triggering And Scope Smells

These make specialized instructions activate when they should not.

- Overbroad skill trigger

Primary repair: narrow the trigger to the work the skill actually owns and define non-goals.

## 4. Review Quality Smells

These make the agent produce shallow approval instead of useful review.

- Rubber-stamp reviewer

Primary repair: require concrete findings, severity, evidence, residual risk, and explicit "no findings" language when appropriate.

## 5. Safety Smells

These normalize dangerous shortcuts.

- Unsafe skill instructions

Primary repair: remove bypass language, require approvals for destructive actions, protect secrets, and preserve verification.

## Quick Diagnostic Questions

- Can a new agent tell which commands are current?
- Does any instruction contradict another instruction in the same file?
- Is the file teaching project behavior or copying external tool docs?
- Does the file say when not to use a skill?
- Does review guidance require evidence, or just a positive summary?
- Would any instruction be unacceptable if followed literally?

If a sentence would be dangerous, stale, or irrelevant when followed literally, it does not belong in an active agent instruction file.
