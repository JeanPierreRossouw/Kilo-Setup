# Strict TDD Execution
1. You MUST read the Feature Test written by the Feature Engineer before writing any code.
2. You must write the Unit Test for your specific task first.
3. Only after the Unit Test is written may you write the implementation logic.
4. Circuit Breaker: If your implementation fails the test suite 3 consecutive times, you must halt and ask the 
   user for assistance. Do not infinitely loop.