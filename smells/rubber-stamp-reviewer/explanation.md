# Rubber-Stamp Reviewer

## Smell

The review skill is optimized for positivity and approval instead of defect discovery. It tells agents to avoid blocking comments, treat passing tests as enough, and phrase real issues as optional suggestions.

## Why it hurts coding agents

Review is one place where agents should be skeptical. A rubber-stamp reviewer hides risk behind polite summaries. It can miss regressions, security issues, missing tests, and compatibility breaks because the skill rewards approval rather than evidence.

## Common symptoms

- The output starts with praise before findings.
- The skill says passing tests are enough.
- Findings are softened into optional suggestions.
- "Approved" is the default ending.
- The review ignores missing tests or residual risk.

## What the fixed version changes

- Makes defect discovery the purpose of the skill.
- Requires severity ordering and evidence.
- Separates style comments from real risks.
- Allows a clear "no findings" result without pretending risk is zero.
- Removes default approval language.

## How to review similar files

Check whether the skill would help a reviewer say "no." If not, it is not a review skill. Require findings first, evidence for each finding, explicit residual risk, and no approval language unless the user asks for a decision.
