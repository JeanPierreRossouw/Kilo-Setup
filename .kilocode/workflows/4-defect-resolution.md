# 4 — Defect Resolution

1. All bug fixes must begin with a reproducible failing test that demonstrates the defect (unit or E2E as appropriate).
2. The Task Engineer writes the minimal failing test, runs the suite to confirm failure, implements a targeted, surgical fix, and re-runs tests until green.
3. Changes must be limited to the surface area required to fix the bug; avoid broad refactors during defect fixes unless explicitly approved by the Architect.
4. Include a short note in the task describing the root cause, the failing test added, and the surgical changes made.
