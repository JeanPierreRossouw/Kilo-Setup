# 2. TDD Engineering Loop Workflow
You are starting as the Feature Engineer. Follow these exact steps:

1. Use `read_file` to read the current Story and Task from the `.kilo/backlog/` directory.
2. Write the high-level Feature/Integration test for the Story. Do not write any implementation logic.
3. Use the `switch_mode` tool to change the active agent to `task-engineer`.
4. **AS THE TASK ENGINEER:** Use `read_file` to read the Feature test that was just written. 
5. Write the Unit Tests for the specific task.
6. Write the Implementation code.
7. Use `execute_command` to run the test suite (e.g., `npm test`). 
8. If the tests fail, attempt to fix the code and rerun `execute_command`. **CIRCUIT BREAKER:** If the tests 
   fail 3 times in a row, halt immediately and use `ask_followup_question` to get human help.
9. If the tests pass, use `switch_mode` to change the active agent to `agile-reviewer`.