# Workflow: TDD Loop

1. **Feature Test**: Feature Engineer reads the backlog and writes Pest/Vitest E2E/Integration tests.
2. **Handoff**: Switch context to the `task-engineer`.
3. **Read Specs**: Task Engineer MUST read the new Feature Test.
4. **Unit Test**: Task Engineer writes an isolated, failing unit test.
5. **Implementation**: Task Engineer writes the minimal code required to pass the test.
6. **Validation**: Run tests locally. 
   - *CIRCUIT BREAKER*: If 3 consecutive failures occur, halt and ask for human help.
7. **Handoff**: If tests are green, switch context to the `agile-reviewer`.