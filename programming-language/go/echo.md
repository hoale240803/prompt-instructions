---
applyTo: "**/.go"
---

# Echo Copilot Instructions

Apply the [Go Copilot Instructions](./go.md) to all code.

## General Guidelines

- Follow Echo framework best practices and conventions
- Maintain clear and structured routing
- Implement efficient middleware and handlers

## Project Setup

- Initialize project with `go mod init`
- Install Echo using `go get github.com/labstack/echo/v4`
- Structure the project to separate routes, handlers, and business logic clearly

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

- `cmd/`: Application entry point and Echo initialization
- `internal/`: Core logic, handlers, services, repositories
- `routes/`: Explicit route definitions and middleware
- `pkg/`: Common utilities and reusable code

## Routing

- Clearly define routes using explicit HTTP methods (`GET`, `POST`, `PUT`, `DELETE`)
- Group related routes using Echo’s `Group` functionality
- Delegate route logic to dedicated handlers

## Middleware

- Implement middleware for logging, recovery, authentication, and CORS
- Explicitly maintain middleware execution order
- Ensure middleware handles errors gracefully

## Handlers

- Keep handlers concise and clear
- Explicitly validate request data
- Delegate complex logic to separate service modules
- Provide structured and consistent JSON responses

## Error Handling

- Use Echo’s built-in HTTP error handling (`echo.NewHTTPError`)
- Standardize error responses consistently
- Log detailed context around errors

## Data Validation

- Validate inputs explicitly using validation libraries (`validator`)
- Provide clear validation error messages to clients

## Logging

- Implement structured logging using libraries such as `logrus` or `zap`
- Centralize and standardize logging configuration
- Explicitly log incoming requests, responses, and errors

## Testing

- Write tests using Echo’s testing utilities along with `httptest`
- Follow a table-driven approach for clarity and maintainability
- Independently test handlers, middleware, and services

## Performance

- Optimize database interactions and queries
- Profile handlers and middleware to identify bottlenecks
- Manage request lifecycles efficiently using contexts

## Deployment

- Build binaries explicitly (`go build`)
- Containerize applications using Docker
- Automate deployments and tests through CI/CD pipelines
