# Repair Prompt: Unsafe Skill Instructions

Review the current `SKILL.md` for unsafe instructions.

Make the smallest safe patch that preserves the useful workflow goal while removing bypasses and dangerous shortcuts.

Please:

1. Remove or rewrite instructions that allow skipping tests, weakening tests, hiding failures, bypassing approvals, pasting secrets, destructive git cleanup, force pushes, deploys, or release changes without explicit user approval.
2. Replace "move fast by bypassing process" guidance with "move fast by reducing scope" guidance.
3. Require focused verification when full verification is too slow.
4. Require the final response to disclose what was verified and what was not.
5. Preserve any legitimate urgency or hotfix guidance that remains safe.

After editing, summarize each unsafe instruction removed, the safer replacement, and any remaining workflow decision that needs human approval.
