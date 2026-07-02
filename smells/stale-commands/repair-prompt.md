# Repair Prompt: Stale Commands

Review the repository's agent instruction files for stale commands.

Make the smallest safe patch that aligns the instructions with the current project configuration. Do not upgrade dependencies or rewrite the build system.

Please:

1. Compare every setup, dev, test, lint, typecheck, build, and deploy command against current project files and CI.
2. Remove commands that reference deleted scripts, old package managers, old ports, old runtime versions, or obsolete migration notes.
3. Replace stale commands with verified current commands.
4. Add a short warning against using dependency upgrades as a generic fix.
5. If a command cannot be verified locally, label it as unverified instead of presenting it as fact.

After editing, report which commands were verified, which were removed, and which still need human confirmation.
