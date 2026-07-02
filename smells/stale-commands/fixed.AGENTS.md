# AGENTS.md

## Setup

This repository uses pnpm through Corepack.

```bash
corepack enable
pnpm install
```

## Development

```bash
pnpm dev
```

The app runs on the port printed by Vite. Do not assume port `3000`.

## Verification

Use focused commands while developing:

```bash
pnpm lint
pnpm test -- --run
pnpm typecheck
```

Run the production build before finishing changes that touch routing, bundling, shared dependencies, or deployment configuration:

```bash
pnpm build
```

## Command Hygiene

- Do not run dependency upgrade commands as a repair step unless the user asks.
- Do not run removed scripts such as `scripts/fix-types.js`.
- If a documented command fails, verify it against `package.json` before changing code to work around the failure.
