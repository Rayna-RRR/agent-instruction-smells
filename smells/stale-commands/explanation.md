# Stale Commands

## Smell

The instruction file contains old setup, test, build, or repair commands. Some refer to removed package managers, old ports, deleted scripts, or risky dependency upgrades.

## Why it hurts coding agents

Agents use documented commands as ground truth. A stale command can waste time, trigger unnecessary dependency changes, or cause the agent to patch code that was not broken. Stale repair commands are especially risky because they can mutate dependencies or generated files while hiding the real mismatch.

## Common symptoms

- The command does not exist in `package.json`, `pyproject.toml`, `Makefile`, or CI.
- The instruction references a package manager the repo no longer uses.
- Ports, script names, or runtime versions differ from current config.
- The file says "migration soon" long after the migration happened.
- The recommended fix is to upgrade dependencies or run an old cleanup script.

## What the fixed version changes

- Replaces Yarn and Node 16 instructions with current pnpm and Corepack commands.
- Removes a deleted repair script.
- Avoids assuming a fixed dev-server port.
- Warns agents not to run dependency upgrades as a generic fix.
- Tells agents to verify commands against project config before debugging code.

## How to review similar files

Compare every command in the instruction file against current project files and CI. For JavaScript projects, check `package.json`, lockfiles, and workflow files. For Python projects, check `pyproject.toml`, lockfiles, tox, nox, Makefiles, and CI. Delete commands that no longer exist. Replace uncertain commands with verified ones.
