---
applyTo: "**/.go"
---

# Fiber Copilot Instructions

Apply the [Go Copilot Instructions](./go.md) to all code.

## General Guidelines

- Follow Fiber framework best practices and conventions
- Keep routing organized, clear, and efficient
- Maintain clean middleware and handlers

## Project Setup

- Initialize project using `go mod init`
- Install Fiber with `go get github.com/gofiber/fiber/v2`
- Structure code to clearly separate routes, handlers, and services

## Folder Structure

```
project_root/
├── cmd/
│   └── app/
│       └── main.go
├── internal/
│   ├── handlers/
│   ├── services/
│   └── repositories/
├── routes/
│   └── routes.go
├── pkg/
│   └── utils/
├── configs/
├── tests/
└── go.mod
```

## Application Structure

- `cmd/`: Application entry points (Fiber app initialization)
- `internal/`: Core application logic (handlers, services, repositories)
- `routes/`: Define routes and middleware explicitly
- `pkg/`: Reusable utilities

## Routing

- Clearly define routes with explicit HTTP methods (GET, POST, PUT, DELETE)
- Use `fiber.Group` for route grouping
- Keep route handlers concise and delegate logic to service layers

## Middleware

- Use middleware for logging, authentication, recovery, and CORS
- Maintain explicit middleware order
- Handle errors gracefully within middleware

## Handlers

- Keep handlers simple and delegate complex logic to services
- Explicitly validate request inputs
- Ensure handlers return structured and consistent responses

## Error Handling

- Use Fiber's built-in error handling
- Standardize error response formats
- Log detailed error contexts

## Data Validation

- Validate inputs explicitly using validation libraries (e.g., `validator`)
- Clearly communicate validation errors to clients

## Logging

- Implement structured logging (using `logrus`, `zap`, or similar)
- Centralize logging configurations
- Log requests, responses, and errors explicitly

## Testing

- Write handler tests with Fiber's testing utilities and `httptest`
- Use table-driven tests for clarity
- Test middleware, handlers, and services independently

## Performance

- Optimize database access and queries
- Profile and optimize handlers and middleware
- Efficiently manage request lifecycles with contexts

## Deployment

- Build deployment-ready binaries explicitly with `go build`
- Containerize applications using Docker
- Automate deployments and tests using CI/CD pipelines
