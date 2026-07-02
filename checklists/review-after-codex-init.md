# Review After Codex Init

Use this after creating or regenerating a repository-level instruction file.

## Scope

- Confirm the file is repository guidance, not a copied README.
- Confirm it does not claim to be a linter, scanner, or policy engine.
- Confirm nested instruction files are mentioned only if they exist.

## Current Commands

- Setup command is current.
- Dev command is current.
- Test command is current.
- Lint or format command is current.
- Build command is current, if the project has one.
- Commands match project config and CI.
- No old package manager or deleted script is mentioned.

## Agent Usefulness

- The file tells agents where important code lives.
- The file names areas that need extra caution.
- The file explains what not to change without explicit approval.
- The file gives useful verification guidance without demanding full-suite work for every small edit.
- The file is short enough to scan.

## Smells To Check

- Context bloat.
- Conflicting instructions.
- Stale commands.
- Lint leakage.
- Skill leakage.
- Unsafe shortcuts.

## Publish Decision

Before shipping, a maintainer should be able to answer:

- What should an agent do differently because this file exists?
- Which commands did we verify?
- Which instructions are project-specific rather than generic?
- What did we intentionally leave out?
