# Workflow: Refactor Pass

1. **Baseline Validation**: Run `composer run validate` to ensure a green baseline before starting any refactoring.
2. **Refactor**: Refactor the code for Native-First and KISS compliance *without* changing any external behavior.
3. **Re-Validate**: Run `composer run validate` again.
4. **Handoff**: Switch context to the `agile-reviewer` for final validation.