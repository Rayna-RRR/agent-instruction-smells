# Context Bloat

## Smell

The instruction file tries to preserve project history, old migration notes, product philosophy, architecture commentary, glossary content, and multiple generations of commands in one active agent context.

## Why it hurts coding agents

Coding agents treat instruction files as operational guidance. Bloated files make current rules compete with stale context. The agent spends attention on old commands, dead links, and ambiguous history instead of the small set of constraints needed to edit safely.

## Common symptoms

- The file is longer than the README section it summarizes.
- Old setup commands sit next to current setup commands.
- Historical notes are written as if they still matter.
- The agent repeatedly asks for clarification or follows outdated paths.
- Important safety constraints are buried under product lore.

## What the fixed version changes

- Keeps only current commands.
- Moves background information into linked docs.
- Converts product history into a few active working rules.
- Defines where deeper context lives instead of copying it.
- Adds a conflict-resolution rule for nested instructions.

## How to review similar files

Read each paragraph and ask: "Should an agent act on this during a coding task?" If not, remove it, link to it, or move it to human documentation. Keep commands, constraints, ownership boundaries, and current workflow rules. Delete stale narrative.
