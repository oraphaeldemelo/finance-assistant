# Definition of Done — v1

## Requirements

- The task's acceptance criteria are satisfied.

## Architecture

- Changes follow the project's architecture guidelines.
- No unnecessary architectural abstractions were introduced.

## Code quality

- Changes follow the project's coding standards.

## Scope

- Changes remain focused on the task and reasonably reviewable.
- Unrelated refactors, cleanup, or improvements are not included.

## Static validation

- Ruff passes for the affected code.
- Pyright passes for the affected code.

## Tests

- Relevant existing tests pass.
- New or changed behavior has appropriate tests.

## Database

- When a change modifies the database schema, an appropriate Alembic migration is included.

## Documentation

- Documentation is updated when behavior, architecture, setup, or relevant interfaces change.

## Security

- No secrets, credentials, or sensitive configuration are committed.

## Validation failures

- If a required validation cannot be executed, it is explicitly reported and is not represented as passing.

## Agent completion

Before finishing, the coding agent reports:

- What changed.
- Why the chosen implementation was used.
- Relevant alternatives or trade-offs when a non-obvious implementation decision was made.
- Tests and validations performed.
- Any changes whose necessity is not obvious from the task.
- Known limitations or unresolved issues.

## Human review

- The resulting diff is reviewed and approved before the change is considered complete.
