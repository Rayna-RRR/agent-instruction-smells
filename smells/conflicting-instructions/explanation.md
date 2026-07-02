# Conflicting Instructions

## Smell

The file contains rules that cannot all be followed. It asks agents to make minimal changes and refactor opportunistically, never edit generated files and always regenerate clients, deploy and never deploy, commit and never commit.

## Why it hurts coding agents

Conflicts force the agent to invent precedence. Different agents may choose different rules, so behavior becomes inconsistent. The worst conflicts usually affect high-impact actions like commits, generated files, snapshots, deployments, and product behavior.

## Common symptoms

- Two bullets use "always" and "never" for the same action.
- A later section quietly overrides an earlier section.
- The agent does extra work because one rule says to broaden scope.
- The agent skips verification because another rule says tests are slow.
- Review comments say "it followed the instructions" but no one agrees which instruction mattered.

## What the fixed version changes

- Adds explicit precedence.
- Removes incompatible absolute rules.
- Narrows broad rules with conditions.
- Separates normal coding defaults from actions requiring user approval.
- Makes testing and snapshot updates depend on risk, not slogans.

## How to review similar files

Search for absolute words like "always," "never," "must," and "do not." For each one, look for a later exception or opposite command. Keep hard rules only when they protect safety, data, secrets, deployments, or user intent. Turn style preferences into defaults with clear exceptions.
