# AGENTS.md

## Project Scope

BeaconBoard is a React and TypeScript admin dashboard for account, billing, and reporting workflows.

## Current Commands

```bash
pnpm install
pnpm dev
pnpm test
pnpm lint
```

Use focused test commands when changing a narrow area. Run the broader suite when touching shared state, billing behavior, account permissions, or routing.

## Working Rules

- Prefer existing Compass components before creating new UI primitives.
- Keep pages thin when a feature already has a `src/features/<name>/` module.
- Do not use optimistic UI for billing, account settings, permissions, or destructive actions.
- Treat `customer`, `account`, and `workspace` as the same product entity in old docs; use `account` in new code.
- Do not edit generated files unless the task is explicitly about regeneration.

## Where To Look

- `src/features/` for feature-owned UI, queries, and tests.
- `src/services/` for shared API clients and cross-feature queries.
- `docs/billing-glossary.md` for billing vocabulary.
- `docs/testing.md` for full test strategy.

## If Instructions Conflict

Follow this file first, then the closest nested `AGENTS.md`, then task-specific user instructions. Ask the user only when the conflict changes product behavior or could cause data loss.
