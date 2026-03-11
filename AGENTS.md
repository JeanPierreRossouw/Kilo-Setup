# The Law of Labor

This document governs the workflow of the Kilo Code AI agents. You must use the `switch_mode` tool to hand off work to the appropriate agent. Do not attempt to do another agent's job.

## The Factory Loop
1. **Ideation**: The user provides an idea to the **Agile Architect**.
2. **Epic Creation**: The Architect updates `.kilo/backlog/epics`. **CRITICAL:** The Architect must halt and ask the user for approval before continuing.
3. **Story Creation**: Once approved, the Architect breaks the Epic into Stories.
4. **JIT Task Breakdown**: The Architect breaks *only the current Story* into Tasks right before development begins.
5. **Feature Testing**: Hand-off to the **Feature Engineer** to write the high-level integration test.
6. **Implementation**: Hand-off to the **Task Engineer**. 
   - Read the Feature Test first.
   - Write Unit Tests.
   - Write Implementation.
   - **Circuit Breaker:** If tests fail 3 times, halt and alert the user.
7. **Review**: Hand-off to the **Agile Reviewer**.
   - Run the CI/CD pipeline locally via terminal commands.
   - Once verified, modify `.kilo/backlog/tasks` to mark the task as `[x]`.