---
applyTo: "**/*.py"
---

# Python Coding Standards

- Follow PEP 8 for formatting and PEP 257 for docstrings
- Use snake_case for variables, functions, and methods
- Use PascalCase for class names
- Use ALL_CAPS for constants
- Prefer explicit over implicit code

## Application Design

- Organize code using packages and modules
- Separate business logic, configuration, and entry points
- Use virtual environments (venv, pipenv, poetry) for dependency management
- Use `.env` files for environment configuration (with `python-dotenv` or similar)

## Folder Structure

- `src/`: Application logic
- `src/module/`: Feature or domain-specific modules
- `tests/`: Unit and integration tests
- `config/`: Configuration files and environment loaders
- `scripts/`: Utility scripts or CLI tools

## Function & Class Practices

- Keep functions small and focused
- Use type hints for function signatures and class attributes
- Use docstrings for public functions, classes, and modules
- Prefer dataclasses for simple data structures
- Use `@staticmethod` or `@classmethod` where appropriate

## Error Handling

- Use try/except for error handling
- Catch specific exceptions; avoid broad `except:` blocks
- Log errors with context instead of silently passing
- Raise exceptions with meaningful messages

## Logging

- Use the built-in `logging` module
- Configure log levels and formats in a central location
- Avoid print statements in production code

## Testing

- Use `pytest` or `unittest` for testing
- Follow the Arrange-Act-Assert pattern
- Mock external services and I/O
- Maintain good test coverage for critical logic

## Code Quality

- Use linters like `flake8`, `pylint`, or `ruff`
- Use formatters like `black`
- Use type checkers like `mypy`
- Document with docstrings and `mkdocs` or `sphinx` if needed

## Security

- Validate and sanitize all inputs
- Avoid hardcoded secrets; load from environment or vault
- Regularly update dependencies and audit them with `pip-audit`

## Performance

- Avoid unnecessary loops and object creation
- Profile and optimize critical code paths using `cProfile` or `line_profiler`
- Use generators and comprehensions where appropriate
