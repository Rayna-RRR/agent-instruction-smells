# Repair Prompt: Lint Leakage

Review the repository's agent instruction files for lint leakage.

Make a narrow patch that keeps useful lint workflow guidance but removes copied linter documentation and broad cleanup pressure.

Please:

1. Remove long lists of lint rule codes, formatter trivia, and duplicated tool docs.
2. Keep verified lint, format, test, and typecheck commands.
3. Point agents to the real config file as the source of truth.
4. Add scope guidance so agents do not churn unrelated files during narrow tasks.
5. Preserve any genuinely project-specific style rule that is not obvious from the config.

After editing, summarize what tool documentation was removed, what commands remain, and how agents should handle unrelated lint failures.
