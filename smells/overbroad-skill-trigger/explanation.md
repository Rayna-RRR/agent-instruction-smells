# Overbroad Skill Trigger

## Smell

The skill claims nearly every task. It tells agents to use it before other skills and starts a broad workflow regardless of the user's actual request.

## Why it hurts coding agents

Skills are supposed to add specialized guidance at the right time. An overbroad trigger steals context from more relevant instructions, increases work for simple tasks, and makes agents over-edit. It also makes skill routing unpredictable because the skill matches almost everything.

## Common symptoms

- The "when to use" section lists most software tasks.
- The skill says to use it before other skills.
- The instructions require reading the whole repo for narrow edits.
- The skill tells agents to refactor or add tests opportunistically.
- The output format is heavy even for small tasks.

## What the fixed version changes

- Keeps the same general coding-assistant purpose but narrows activation to scoped repository work.
- Defines when not to use the skill so it does not capture audits, deployments, dependency work, or open-ended planning.
- Replaces whole-repo reading and opportunistic refactoring with evidence-based scope expansion.
- Separates implementation tasks from review-only tasks.
- Keeps the output contract proportional to the requested work and verification performed.

## How to review similar files

Read only the trigger section first. If the skill would activate for routine unrelated tasks, it is too broad. A useful skill should be easy to not use. Add explicit "do not use" cases, remove language that ranks the skill above better scoped guidance, and make the fixed version repair the same underlying artifact rather than changing the subject.
