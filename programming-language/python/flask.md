---
applyTo: "**/.py"
---

# Flask Copilot Instructions

Apply the [Python Coding Standards](./python.md) to all code.

## General Guidelines

- Follow Flask best practices and conventions.
- Keep applications modular and lightweight.
- Adhere to explicit over implicit coding practices.

## Project Setup

- Scaffold projects using standard templates or `cookiecutter-flask`.
- Manage dependencies with virtual environments (`venv`) and requirements files (`requirements.txt` or `pyproject.toml`).
- Use `.env` files for environment configurations (with `python-dotenv`).

## Folder Structure

```
project_root/
├── app/
│   ├── __init__.py
│   ├── routes.py
│   ├── models.py
│   ├── templates/
│   └── static/
├── tests/
├── scripts/
├── config.py
├── requirements.txt
└── run.py
```

## Application Structure

- `app/__init__.py`: Application initialization and configurations.
- `app/routes.py`: Route handlers and view logic.
- `app/models.py`: Database models (use SQLAlchemy or similar).
- `app/templates/`: HTML templates.
- `app/static/`: CSS, JavaScript, images.

## Routing and Views

- Define routes clearly with meaningful URL paths.
- Keep view functions concise and delegate complex logic to separate functions or services.
- Use route decorators (`@app.route`) explicitly.
- Implement RESTful routes appropriately (`GET`, `POST`, `PUT`, `DELETE`).

## Templates

- Use **Jinja2** templating engine effectively.
- Extend base templates (`base.html`) for consistency.
- Keep logic in templates minimal; use filters and context processors appropriately.

## Database Management

- Use **Flask-SQLAlchemy** or similar ORM.
- Define explicit models with validations and constraints.
- Handle database migrations with **Flask-Migrate**.
- Avoid raw SQL queries; prefer ORM queries.

## Forms

- Use **Flask-WTF** for form handling and CSRF protection.
- Validate forms explicitly and handle errors gracefully.
- Access form data via `form.data` or `form.validate_on_submit()`.

## Error Handling

- Implement error handlers (`@app.errorhandler`).
- Return meaningful error responses with appropriate status codes.
- Log errors with detailed context for debugging.

## Security

- Enable **CSRF protection** and secure cookies.
- Sanitize all user inputs to prevent injections.
- Handle sessions and authentication securely.
- Avoid exposing sensitive data in logs or error responses.

## Testing

- Write tests with **Pytest** or **unittest**.
- Use **test clients** for route testing.
- Mock database interactions and external services.
- Maintain good test coverage, especially for core logic.

## Logging

- Use Python’s built-in `logging` module.
- Configure logging formats and levels centrally.
- Avoid print statements in production code.

## Performance

- Implement caching for frequently accessed data.
- Optimize database queries and indexing.
- Profile critical paths and bottlenecks.

## Deployment

- Use **Gunicorn, uWSGI**, or similar WSGI servers.
- Follow **Flask's deployment guidelines**.
- Implement **CI/CD** for automated testing and deployment.
- Properly configure **static file handling** in production.
