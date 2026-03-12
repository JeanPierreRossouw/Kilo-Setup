# Workflow: Reviewer Gate

1. **Prune**: Agile Reviewer runs `composer run prune` (Rector/Lint/Format).
2. **Validate**: Run `composer run validate` (Tests/PHPStan/Build).
3. **Reject**: If validation fails or code is over-engineered (Complexity Gatekeeper), reject the task back to the `task-engineer`.
4. **Vault**: If validation is green, move the task file: `mv .kilocode/backlog/tasks/[file].md .kilocode/vault/tasks/`.
5. **Ledger**: Append a new table row to `.kilocode/ledger.md` documenting the vaulted task.
6. **Complete**: Announce success to the user.