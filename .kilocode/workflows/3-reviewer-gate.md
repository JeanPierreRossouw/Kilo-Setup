# 3 — Reviewer Gate

1. The Reviewer runs the prune pipeline: `composer run prune` (or the equivalent CI command) to apply automated rectors, formatting, and lint fixes.
2. Immediately after, the Reviewer runs `composer run validate` to execute static analysis, tests, and build/type checks.
3. If validation passes: move the task file to .kilocode/vault/tasks/, append a concise entry to .kilocode/ledger.md recording the task id, title, approver, and timestamp, then mark the task as completed.
4. If validation fails: reject the task back to the Task Engineer with failure details and remediation instructions; do not move files to the vault.
# 3. Agile Reviewer Verification Workflow
You are acting as the Agile Reviewer. The implementation is complete and tests are passing locally. Follow these steps:

1. Use `execute_command` to run the project linters (e.g., `npm run lint`).
2. Use `execute_command` to run the Static Application Security Testing (SAST) tool if available locally.
3. Use `execute_command` to run the full test suite one final time to ensure no regressions occurred.
4. If any of the above commands fail, use `switch_mode` to send the context back to the `task-engineer` to fix 
   the errors.
5. If all commands pass cleanly, use the `write_to_file` or `apply_diff` tool to modify `.kilo/backlog/tasks/` 
   and mark the current task as `[x]`.
6. Announce to the user that the task is fully complete and verified.