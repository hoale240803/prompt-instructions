---
applyTo: "**/.py"
---

# FastAPI Copilot Instructions

Apply the [Python Coding Standards](./python.md) to all code.

## General Guidelines

- Follow FastAPI best practices and conventions.
- Leverage type annotations for automatic documentation and validation.
- Keep applications modular and structured.

## Project Setup

- Use standard project scaffolds (`cookiecutter-fastapi`) or manual setup.
- Manage dependencies with virtual environments (`venv`, `poetry`, or similar).
- Configure environment variables using `.env` and libraries like `python-dotenv`.

## Folder Structure

```
project_root/
├── app/
│   ├── __init__.py
│   ├── main.py
│   ├── api/
│   │   ├── v1/
│   │   │   ├── endpoints/
│   │   │   └── models/
│   ├── core/
│   │   ├── config.py
│   │   └── security.py
│   ├── db/
│   │   ├── base.py
│   │   └── session.py
│   └── schemas/
├── tests/
├── scripts/
├── requirements.txt
└── Dockerfile
```

## API Design

- Clearly define route prefixes and versioning (e.g., `/api/v1/...`).
- Use appropriate HTTP methods (`GET`, `POST`, `PUT`, `DELETE`).
- Leverage FastAPI dependency injection for shared logic.
- Use **Pydantic schemas** for request validation and response models.

## Routing and Endpoints

- Use FastAPI `APIRouter` for modular route management.
- Group related routes in separate files under `endpoints/`.
- Implement clear and concise route handlers.

## Data Models and Schemas

- Use **Pydantic** for request and response validation.
- Clearly separate **database models (ORM)** from Pydantic schemas.
- Define explicit validations and constraints.

## Database Management

- Use **SQLAlchemy** or **Tortoise ORM** for database interactions.
- Handle **database sessions** explicitly.
- Define migrations with **Alembic**.

## Dependency Injection

- Use FastAPI's **dependency injection system (`Depends()`)**.
- Clearly define and manage dependencies centrally.

## Error Handling

- Define consistent error responses using FastAPI's `HTTPException`.
- Implement **custom exception handlers** when needed.
- Log errors clearly with relevant context.

## Security

- Implement authentication (**JWT, OAuth2**).
- Define and enforce **authorization scopes and roles**.
- Validate and sanitize all inputs.

## Logging

- Use structured logging with Python's **logging module**.
- Centralize **logging configuration** and log levels.
- Avoid using `print()` statements in production.

## Testing

- Write tests using **pytest**.
- Use FastAPI's **TestClient** for endpoint testing.
- Mock **external dependencies** and databases.
- Ensure **good test coverage** for all critical logic.

## Performance

- Use **response caching** and proper database indexing.
- Optimize **query performance** and avoid **N+1 queries**.
- Profile and monitor **application performance** with tools.

## Deployment

- **Containerize applications** using Docker.
- Use **Uvicorn with Gunicorn** for deployment.
- Follow **FastAPI production deployment guidelines**.
- Set up **CI/CD pipelines** for automated deployment and testing.
