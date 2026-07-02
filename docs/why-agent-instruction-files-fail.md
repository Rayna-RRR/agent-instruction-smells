# Why Agent Instruction Files Fail

Agent instruction files fail when they stop being operational guidance and become a dumping ground for project memory. A coding agent reads them as active instructions. That means a stale note, a copied checklist, or a contradictory rule can change behavior in the next task.

The common failure is not that the file is badly written. It is that the file has no clear job.

## Helpful Instruction Files

Useful files answer questions an agent actually has while working:

- What is the project?
- Which commands are current?
- Which files or workflows are sensitive?
- What conventions should be followed?
- What should not be changed without explicit user approval?
- Where should the agent look for deeper context?

They do not try to reproduce the entire README, test strategy, style guide, design doc, and release process.

## Failure Modes

### Bloat

Long files hide the important rules. Agents still read the text, but every extra paragraph competes for attention with commands and constraints that matter.

### Staleness

Old commands are worse than missing commands. They send the agent into false failures, unnecessary debugging, or edits that compensate for the wrong thing.

### Conflict

Contradictory instructions force the agent to guess. If one section says "never edit generated files" and another says "regenerate snapshots directly," the agent has to choose a side.

### Leakage

Instruction files often absorb content from other places: linter docs, tool manuals, full skill bodies, old PR comments, or onboarding notes. The result is bigger but less useful.

### Unsafe Guidance

Some instructions normalize dangerous shortcuts: skipping tests, hiding failures, bypassing review, committing secrets, or using destructive commands without approval. These are not style issues. They are workflow hazards.

## The Repair Principle

Do not ask "Can this sentence be true?" Ask "Should an agent act on this sentence during a coding task?"

If the answer is no, remove it, link to it, or move it to human documentation.

Good agent instructions are small, current, scoped, and testable.
