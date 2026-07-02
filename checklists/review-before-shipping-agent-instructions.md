# Review Before Shipping Agent Instructions

Use this before publishing or merging changes to `AGENTS.md`, `CLAUDE.md`, `SKILL.md`, Cursor rules, or similar files.

## Final Read

- Read the file as if an agent will follow it literally.
- Remove jokes, lore, old debates, and vague slogans.
- Replace "always" and "never" with scoped rules unless the rule protects safety, data, secrets, or user intent.
- Make precedence explicit when multiple instruction sources exist.

## Currentness

- Commands match current config.
- Paths exist.
- Tool names are current.
- Runtime versions are current.
- Links work or are not required for the agent task.

## Scope Control

- The file does not ask agents to broaden every task.
- The file does not encourage unrelated lint cleanup.
- The file does not require full repo reading for small edits.
- The file does not duplicate skill bodies or external docs.

## Risk Areas

- Destructive commands require explicit user approval.
- Deployments require explicit user approval.
- Commits, force pushes, and history edits require explicit user approval unless the workflow clearly says otherwise.
- Secrets must not be written to tracked files.
- Tests must not be skipped, weakened, or deleted to create a false green state.

## Human Review

Ask a maintainer to review:

- Any command you could not run locally.
- Any rule that changes release or deployment behavior.
- Any instruction involving secrets, credentials, or production data.
- Any broad trigger added to a skill.
- Any generated instruction text.
