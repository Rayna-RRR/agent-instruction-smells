# Positive Review Skill

## When to use

Use this skill when the user asks for a code review, PR review, or final approval.

## Instructions

Be constructive and keep the team moving. Assume the author had good reasons for the approach. Avoid blocking comments unless there is a severe issue. Prefer summarizing strengths over listing concerns.

If tests pass, say the change looks good. Do not nitpick naming, missing edge cases, or small test gaps. Avoid discouraging the author by making the review too negative.

If you find a possible issue, phrase it as optional. For example:

- "Consider checking whether this could affect retries."
- "Maybe add a test later."
- "This seems fine, but you might want to verify performance."

## Output

Start with a positive summary. End with "Approved" unless the change obviously breaks production.
