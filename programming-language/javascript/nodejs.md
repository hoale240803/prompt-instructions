---
applyTo: "**"
---

# General Node.js Coding Standards

Apply the [general coding guidelines](./js.md) to all code.

## Code Practices

- Use `const` for variables that won't be reassigned; use `let` for variables that will.
- Prefer arrow functions (`=>`) for concise function expressions.
- Use `async/await` for asynchronous operations; avoid callback hell.
- Use strict equality (`===`) for comparisons.
- Avoid global variables; use modules for encapsulation.
- Use ES modules (`import/export`) over CommonJS.
- Follow `camelCase` for variable and function names.
- Use descriptive names for variables, functions, and files.
- Keep functions small and focused on a single task.

## Error Handling

- Use `try/catch` for synchronous and async error handling.
- Handle promise rejections with `.catch()` or `try/catch` in async functions.
- Throw custom errors with meaningful messages.
- Validate inputs to prevent runtime errors.

## Dependency Management

- Use `npm` or `Yarn` for package management.
- Pin dependency versions in `package.json`.
- Group dependencies by purpose (e.g., production, dev).
- Regularly update dependencies to address security vulnerabilities.

## Code Organization

- Organize code into modules by feature or responsibility.
- Use a consistent folder structure (e.g., `src/`, `lib/`, `utils/`).
- Keep configuration files (e.g., `.eslintrc`, `package.json`) at project root.
- Use environment variables for configuration (e.g., via `dotenv`).

## Logging

- Use a logging library (e.g., `Winston`, `Bunyan`) for structured logging.
- Log errors with sufficient context (e.g., stack trace, request data).
- Suppress `console.log` in production; use for debugging only.

## Testing

- Write unit tests for core logic using `Jest`, `Mocha`, or `Vitest`.
- Write integration tests for critical paths.
- Use mocking libraries (e.g., `Jest`, `Sinon`) for dependencies.
- Aim for high test coverage (`>80%`).

## Documentation

- Use `JSDoc` for function and module documentation.
- Maintain a `README.md` with setup, usage, and API instructions.
- Document complex logic with inline comments.

## Security

- Validate and sanitize all user inputs.
- Avoid `eval` and similar unsafe functions.
- Use `HTTPS` for network requests.
- Implement rate limiting and request validation.
- Use secure headers (e.g., `Helmet` for Express).

## Performance

- Optimize I/O operations with async patterns.
- Use caching (e.g., `Redis`) for frequently accessed data.
- Minimize bundle size for client-side assets.
- Profile performance with tools like `clinic.js`.

---

This Markdown format keeps it clean and structured for easy readability and use. Let me know if you need modifications or enhancements! 🚀
