# 1 — Plan Epic

1. The Agile Architect drafts the Epic with a clear title, business rationale, success metrics, and a short technical approach aligned to Laravel 12 modular monolith patterns.
2. The Architect breaks the Epic into discrete Stories that represent vertical slices of functionality with acceptance criteria and E2E scenarios for the Feature Engineer to author tests against.
3. For the current Story, the Architect creates granular Task markdown files under .kilocode/backlog/tasks/ describing implementation steps, dependencies, and test expectations.
4. The Architect pauses and requests human approval before work continues; no Task moves to implementation without explicit approval.
# 1. Agile Architect Planning Workflow
You are acting as the Agile Architect. Follow these exact steps in order:

1. Create a new Epic markdown file in `.kilo/backlog/epics/` detailing the requested feature.
2. **GATEWAY:** Stop and use the `ask_followup_question` tool to ask the user to approve the Epic. Do not 
                proceed to step 3 until the user explicitly approves it.
3. Once approved, break the Epic down by creating the corresponding Story files in `.kilo/backlog/stories/`.
4. Perform Just-In-Time (JIT) breakdown: Create the granular implementation tasks in `.kilo/backlog/tasks/` 
   for the *first* Story only.
5. Use the `switch_mode` tool to change the active agent to `feature-engineer` and inform the user that 
   planning is complete and development is ready to begin.