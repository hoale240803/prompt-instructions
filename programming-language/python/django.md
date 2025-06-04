---
applyTo: "**/.py"
---

# Django Copilot Instructions

Apply the [Python Coding Standards](./python.md) to all code.

## General Guidelines

- Use Django's built-in functionality and conventions.
- Keep apps focused, modular, and reusable.
- Follow Django best practices and DRY principles (Don't Repeat Yourself).

## Project Setup

- Start projects with `django-admin startproject` and apps with `python manage.py startapp`.
- Use virtual environments and manage dependencies with `requirements.txt` or `pyproject.toml`.
- Use `.env` files for configuration and environment variables (with `django-environ` or similar).

## Folder Structure

- **project_root/**
  - `manage.py`
  - **project/** (settings and configuration)
  - **apps/** (all Django apps)
  - **templates/** (shared templates)
  - **static/** (CSS, JS, images)
  - **media/** (user-uploaded content)

## Apps Structure

Each app should contain:

- `models.py`: Database models.
- `views.py`: Views handling requests.
- `urls.py`: URL routing for the app.
- `forms.py`: Form definitions and validation logic.
- `admin.py`: Django admin configuration.
- `tests/`: Unit and integration tests.
- `templates/app_name/`: HTML templates specific to the app.

## Models

- Define explicit model fields with appropriate validation and constraints.
- Use meaningful model names and verbose names.
- Implement `__str__` method for readable representations.
- Define model methods for reusable queries or business logic.

## Views

- Prefer class-based views (`ListView`, `DetailView`, etc.).
- Keep views concise by delegating complex logic to models or services.
- Use decorators (`@login_required`, `@permission_required`) for authentication and authorization.

## Templates

- Use Django's built-in template language.
- Extend base templates (`base.html`) for consistent layouts.
- Use template tags and filters appropriately.
- Keep templates clean and free of heavy logic.

## URL Routing

- Define URL patterns clearly and consistently.
- Use named URL patterns for reverse lookups.
- Group related URLs with `include()`.

## Forms

- Use Django forms or ModelForms for data validation and processing.
- Include form validation and handle errors gracefully.
- Avoid direct access to `request.POST`; use `form.cleaned_data`.

## Security

- Use Django's security features (CSRF protection, session management, secure cookies).
- Sanitize user inputs to avoid injection attacks.
- Configure permissions and user access control explicitly.
- Never expose sensitive data or debugging info in production.

## Database

- Use Django ORM effectively for queries and transactions.
- Optimize queries with `select_related` and `prefetch_related`.
- Create and manage migrations regularly.

## Testing

- Write tests using Django's built-in test framework.
- Test views, models, and forms thoroughly.
- Use fixtures or factory libraries (like `Factory Boy`) for test data.

## Performance

- Cache frequently accessed data.
- Optimize database interactions.
- Profile critical paths using tools like `Django Debug Toolbar`.

## Deployment

- Follow Django's deployment checklist.
- Configure static files handling and media serving properly.
- Use **gunicorn**, **uWSGI**, or similar for production deployments.
- Implement CI/CD for automated testing and deployment.
