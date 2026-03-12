# Strict TDD Execution

1. **Read Feature Tests**: You MUST read the Feature Test written by the Feature Engineer before writing any code.
2. **Write Unit Test**: Write the isolated Unit Test for your specific task FIRST.
3. **Implement**: Only after the Unit Test is written and failing may you write the minimal implementation logic to pass it.
4. **Circuit Breaker**: If your implementation fails the test suite 3 consecutive times, halt immediately and ask the user for assistance. Do not infinitely loop.