# 5 — Refactor Pass

1. Before any refactor, run `composer run validate` to ensure a green baseline; do not refactor on a failing baseline.
2. Follow Laravel 12 architecture rules and module boundaries as defined by the Architect when performing refactors; prioritize readability, test coverage, and non-breaking changes.
3. Add or update tests to preserve behavior when refactoring; run the full test suite and static analysis before submitting changes for review.
4. Document the intent and scope of the refactor in the task file and obtain Architect approval for large-surface refactors.
