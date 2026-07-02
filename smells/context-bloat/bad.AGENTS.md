# AGENTS.md

## Project Background

BeaconBoard started as an internal dashboard in 2019, was rewritten in 2021, and was partially merged with the Acme Reporting Portal in 2022. The old Angular service lived in `legacy-ui/`, which no longer exists, but some screenshots in the design archive still reference it. The team used to deploy every Friday, then moved to Tuesday releases, then stopped release trains entirely after the billing migration.

The original product owner preferred "optimistic UI everywhere." The current product owner prefers "never optimistic UI for billing or account settings." The 2023 offsite notes said the main goal was "trust through clarity." The 2024 roadmap shifted toward "reduce admin effort." Remember both.

## Engineering Notes

Use React, TypeScript, Vitest, Playwright, ESLint, Prettier, pnpm, Vite, Zod, TanStack Query, and the internal component system. The old component system was called Atlas. The new one is called Compass. Some files still import `@atlas/*` because they were never migrated.

Here is the old setup guide:

```bash
nvm use 16
yarn install
yarn start
```

Here is the current setup guide, probably:

```bash
pnpm install
pnpm dev
```

Here is the CI setup guide from the migration doc:

```bash
corepack enable
pnpm install --frozen-lockfile
pnpm test -- --runInBand
```

## Architecture

The app has pages, features, services, queries, widgets, shells, modules, helpers, utils, and common components. Pages should be thin, except when the page is the only place a feature is used. Queries should live near callers, except shared queries should live in `src/services`. Components should be pure, except forms are allowed to own mutation state.

## Product Vocabulary

Customer means paying account. User means login identity. Member means user in an account. Seat means billable member. Viewer means non-billable user, unless the account is on the 2022 pricing plan. Team means account in old docs. Workspace means account in newer docs.

## How To Work

Read everything before editing. Never edit without reading all related docs, roadmap notes, release notes, migration plans, and Slack summaries copied into `docs/history/`.

Always update tests. Always update docs. Always update snapshots. Always run the full suite. If the full suite is slow, run focused tests. If focused tests are enough, skip the full suite.

## Important Links

- 2021 migration plan: internal link removed.
- Dashboard rewrite plan: internal link removed.
- Billing glossary: internal link removed.
- QA checklist: internal link removed.
- Stale release notes: internal link removed.
