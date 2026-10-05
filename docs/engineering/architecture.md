# Architecture

Finance Assistant uses a feature-oriented modular monolith with a pragmatic layered architecture. Features are organized into cohesive modules, while the application is deployed and operated as a single unit.

## Module responsibilities

The following are logical responsibilities that normally belong inside a module. They do not require specific directories, classes, or files.

- **Router:** transport concerns, such as receiving requests and returning responses. Routers do not contain business logic.
- **Service:** application and business orchestration.
- **Pydantic schemas:** validation and input/output contracts.
- **SQLAlchemy models:** persistence models.
- **Repository:** persistence operations and database queries, keeping persistence concerns out of services.

The physical structure of each module should remain as simple as its current requirements allow.

Business logic remains outside FastAPI routers and external adapters, including Telegram.

## Applying architectural principles

Apply SOLID and Clean Architecture principles pragmatically. Use them to keep responsibilities clear and dependencies understandable, without introducing abstractions that current requirements do not justify.
