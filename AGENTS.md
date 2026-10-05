# Finance Assistant

## Project context

- Personal financial management application.
- Telegram is the initial primary user interface.
- Architecture: feature-oriented modular monolith with a pragmatic layered architecture.
- Introduce AI features only after the core financial domain is working.

## Architecture and coding guidance

- Follow the detailed architecture guidance in [docs/engineering/architecture.md](docs/engineering/architecture.md).
- Follow the coding standards in [docs/engineering/coding-standards.md](docs/engineering/coding-standards.md).
- Agents implementing code must follow both documents.

## Definition of Done

- Follow the Definition of Done documented in [docs/engineering/definition-of-done.md](docs/engineering/definition-of-done.md).

## Technology baseline

- Python 3.13+ with FastAPI.
- Pydantic for validation.
- PostgreSQL with SQLAlchemy 2 for persistence.
- Alembic for database migrations.
- Pytest for tests.
- uv for package and project management.
- Ruff for linting and formatting.
- Pyright for static type checking.
- Docker and Docker Compose for infrastructure.
- GitHub Actions for CI/CD.

## Engineering principles

- Keep business logic outside FastAPI routers and external adapters, including Telegram.
- Never use `float` for monetary values. Use `Decimal` in Python and `NUMERIC` or `DECIMAL` in PostgreSQL.
- Keep modules cohesive and responsibilities separated.
- Prefer simple solutions over unnecessary abstractions.
- Do not introduce technologies, dependencies, architectural layers, or infrastructure without a concrete need.
- Application code uses type annotations. Test code should also be typed where practical without sacrificing readability.
- Add appropriate tests for new behavior.
- Never expose secrets or commit environment credentials.
- Do not modify unrelated code while implementing a task.

## AI-assisted development

This repository is a learning project for AI-assisted and agentic software engineering. The coding agent implements changes; architectural decisions remain subject to human review.

- Do not silently make significant architectural decisions.
- When requirements are ambiguous and the choice has meaningful architectural consequences, report the ambiguity rather than guessing.
- Before finishing an implementation task, summarize what changed, important decisions made, and validation performed.
