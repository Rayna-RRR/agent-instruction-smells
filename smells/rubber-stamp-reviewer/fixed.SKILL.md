# Code Review Skill

## When to use

Use this skill when the user asks for a code review, PR review, or risk assessment of a change.

## Instructions

Review for bugs, behavioral regressions, hidden side effects, missing tests, security issues, performance risks, maintainability problems, and compatibility breaks.

Prioritize findings by severity. Ground each finding in a file, line, behavior, or test gap. Do not approve a change just because tests pass. If there are no findings, say that clearly and name any residual risk or verification gap.

Avoid style-only comments unless the style issue creates real maintenance cost or violates an established project convention.

## Output

Use this order:

1. Findings, highest severity first.
2. Open questions or assumptions.
3. Brief verification notes.
4. Short summary only after the findings.

Do not write "Approved" unless the user explicitly asked for an approval decision and the review supports it.
