# Repair Prompt: Conflicting Instructions

Review the repository's agent instruction files for conflicting instructions.

Make a narrow patch that resolves contradictions without changing the intended workflow more than necessary.

Please:

1. Find pairs of instructions that cannot both be followed.
2. Identify conflicts involving commits, deployments, generated files, snapshots, tests, product behavior, secrets, or destructive commands.
3. Replace conflicting absolute language with clear precedence and conditional rules.
4. Preserve real safety constraints.
5. Remove duplicate rules when one clearer rule is enough.

After editing, list the conflicts you resolved, the precedence rule you used, and any remaining decisions that need human review.
