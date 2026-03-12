# Workflow: Plan Epic

1. **Draft Epic**: Agile Architect creates an Epic in `.kilocode/backlog/epics/` aligned to Laravel 12 modular monolith principles.
2. **Approval Gateway**: Architect MUST use `ask_followup_question` to get human approval for the Epic.
3. **Draft Stories**: Once approved, break the Epic down into Stories in `.kilocode/backlog/stories/`.
4. **JIT Breakdown**: Create Task markdown files in `.kilocode/backlog/tasks/` for the *first Story only*.
5. **Handoff**: Switch context to the `feature-engineer`.