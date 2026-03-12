# The Law of the Land

## Architectural Decisions
1. **Architecture Style**: Modular Monolith. Code must be organized by domain modules, not technical layers.
2. **Testing Strategy**: Test-Driven Development (TDD) is mandatory. Tests must precede implementation.
3. **Security**: No secrets in plain text. All code must pass the GitHub Actions SAST and linting pipeline before merge.