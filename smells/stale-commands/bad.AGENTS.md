# AGENTS.md

## Setup

Use Node 16 and Yarn Classic.

```bash
nvm use 16
yarn install
```

If dependencies fail, delete `node_modules` and run:

```bash
yarn upgrade --latest
```

## Development

```bash
yarn start
```

The app opens on `http://localhost:3000`.

## Tests

```bash
yarn test --watchAll=false
yarn lint
yarn typecheck
```

If `yarn typecheck` fails because of generated API files, run:

```bash
node scripts/fix-types.js
```

## Build

```bash
yarn build
```

## Notes

The repo is being migrated to pnpm soon. Until then, keep using Yarn.
