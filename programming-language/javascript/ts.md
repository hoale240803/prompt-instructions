---
applyTo: "**/*.ts"
---

# TypeScript Coding Standards

## General Standards

- Follow the **General Node.js Coding Standards** for:
  - Core coding practices.
  - Error handling.
  - Dependency management.
  - Code organization.
  - Logging.
  - Testing.
  - Documentation.
  - Security.
  - Performance.

## Identifiers

- Use **UpperCamelCase** for:
  - Classes, interfaces, types, enums, decorators, and type parameters.
- Use **lowerCamelCase** for:
  - Variables, parameters, functions, methods, properties, and module aliases.
- Use **CONSTANT_CASE** for:
  - Global constant values, including enum values.
- Avoid **private identifiers** (`#ident`).
- Treat abbreviations as whole words (e.g., `loadHttpUrl`, not `loadHTTPURL`).
- Avoid using `$` in identifiers unless required by third-party frameworks.
- Type parameters may use a **single uppercase character** (e.g., `T`) or **UpperCamelCase**.
- Test method names may use `_` separators (e.g., `testX_whenY_doesZ()`).
- Do **not** use `_` as a prefix or suffix in identifiers.

## Code Practices

- Use `const` for immutable variables; use `let` for mutable ones.
- Prefer **arrow functions** (`=>`) for concise function expressions.
- Use `async/await` for asynchronous operations.
- Use strict equality (`===`) for comparisons.
- Avoid global variables; encapsulate logic in modules.
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

- Use a logging library (e.g., `Winston`, `Pino`) for structured logging.
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
- Use secure headers (e.g., `Helmet` for Express`).

## Performance

- Optimize I/O operations with async patterns.
- Use caching (e.g., `Redis`) for frequently accessed data.
- Minimize bundle size for client-side assets.
- Profile performance with tools like `clinic.js`.
