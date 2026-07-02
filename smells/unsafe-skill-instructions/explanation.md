# Unsafe Skill Instructions

## Smell

This is an anti-pattern. The skill normalizes bypassing safety controls to move faster. It tells agents to skip tests, mutate git history, bypass approvals, paste secrets, force push, or hide warnings.

## Why it hurts coding agents

Agents follow instructions literally. Unsafe skill text can turn a normal hotfix into data loss, secret leakage, broken review history, or a false green build. Speed is not a reason to remove guardrails; it is a reason to reduce scope, define permission boundaries, and report verification limits clearly.

## Common symptoms

- The skill says speed matters more than process.
- Tests may be skipped, weakened, or deleted to pass CI.
- Destructive git commands are suggested as cleanup.
- Approval prompts are treated as obstacles.
- Secrets are allowed in tracked files "temporarily."
- Final output hides warnings to keep the message short.

## What the fixed version changes

- Keeps the fast-fix intent but changes the method.
- Defines permission boundaries for approvals, destructive commands, git history, deploys, and release state.
- Prohibits bypassing approvals, weakening tests, or hiding failures.
- Defines sensitive data handling by forbidding secrets in tracked files.
- Requires explicit user confirmation for force pushes, deploys, release changes, and destructive git operations.
- Defines safe failure behavior: preserve failing tests, run focused verification when time is tight, and disclose unverified areas.

## How to review similar files

Look for instructions that would be unacceptable if followed exactly. Pay special attention to tests, secrets, destructive commands, approval bypasses, deployments, release state, and history rewriting. Replace shortcut language with scope control, focused verification, explicit user confirmation, and clear reporting. This catalog helps reviewers spot unsafe instruction patterns; it is not a security scanner.
