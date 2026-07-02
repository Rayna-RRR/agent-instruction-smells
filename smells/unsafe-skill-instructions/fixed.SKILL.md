# Fast Fix Skill

## When to use

Use this skill when the user asks for a narrow bug fix, release patch, hotfix, or unblock and speed matters.

## Instructions

Move quickly by reducing scope, not by bypassing safety.

- Keep the fix as small as possible.
- Preserve existing tests. Do not skip, weaken, or delete tests to make a build pass.
- Do not run destructive git commands such as `git reset --hard` unless the user explicitly asks.
- Do not bypass approval prompts, sandbox restrictions, or repository safety rules.
- Do not paste secrets into tracked files.
- Do not force push, amend commits, deploy, or change release state unless the user explicitly asks.
- If verification is too slow for the hotfix window, run the highest-value focused check and report what was not verified.

## Output

Report the bug fixed, the files changed, the verification performed, and any safety-relevant work intentionally not done.
