---
applyTo: "**/.go"
---

# Gin Copilot Instructions

Apply the [Go Copilot Instructions](./go.md) to all code.

## General Guidelines

- Follow Gin framework best practices and conventions
- Keep routing clear and organized
- Maintain efficient middleware and handlers

## Project Setup

- Initialize the project with `go mod init`
- Install Gin using `go get -u github.com/gin-gonic/gin`
- Structure code to separate routing, handlers, and services clearly

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

- `cmd/`: Application entry points (Gin engine initialization)
- `internal/`: Application-specific logic (handlers, services, repositories)
- `routes/`: Define routes and middleware
- `pkg/`: Reusable utilities

## Routing

- Define routes clearly with explicit HTTP methods (GET, POST, PUT, DELETE)
- Group related routes using `gin.RouterGroup`
- Implement route handlers concisely and delegate logic to services

## Middleware

- Use middleware for cross-cutting concerns (logging, authentication, CORS)
- Maintain middleware order explicitly
- Handle errors gracefully within middleware

## Handlers

- Keep handlers focused and concise
- Validate request inputs explicitly
- Delegate complex business logic to separate service layers
- Return consistent response structures (e.g., JSON responses with clear status)

## Error Handling

- Use Gin's built-in error handling (`c.Error()`)
- Centralize error response formatting
- Log detailed context about errors

## Data Validation

- Validate request payloads using binding tags (`binding:"required"`)
- Return clear validation error messages

## Logging

- Use structured logging libraries like `logrus` or `zap`
- Configure logging consistently across the app
- Log requests and errors explicitly

## Testing

- Write handler tests using Gin's test utilities
- Use `httptest` for integration tests
- Test middleware, handlers, and service logic separately

## Performance

- Optimize database queries and connection management
- Profile handlers and middleware for performance bottlenecks
- Use context management to handle request lifecycles efficiently

## Deployment

- Build deployable binaries explicitly (`go build`)
- Containerize applications with Docker
- Automate testing and deployments via CI/CD pipelines
