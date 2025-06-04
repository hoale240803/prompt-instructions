---
applyTo: "**/.go"
---

# Go Copilot Instructions

Apply standard Go best practices to all code.

## General Guidelines

- Follow Go conventions and idiomatic patterns
- Maintain clarity, simplicity, and efficiency in your code
- Use explicit and descriptive naming

## Project Setup

- Initialize projects with `go mod init`
- Manage dependencies using Go Modules (`go.mod`, `go.sum`)
- Structure code logically and modularly

## Folder Structure

```
project_root/
├── cmd/
│   └── app/
│       └── main.go
├── pkg/
│   ├── handlers/
│   ├── services/
│   └── utils/
├── internal/
│   ├── models/
│   └── repositories/
├── api/
│   ├── v1/
│   └── routes/
├── configs/
├── scripts/
├── tests/
└── go.mod
```

## Application Structure

- `cmd/`: Application entry points
- `pkg/`: Library code reusable across projects
- `internal/`: Application-specific packages
- `api/`: API definitions and routing
- `configs/`: Configuration files and loading logic

## Code Practices

- Follow standard Go formatting (`gofmt` or `goimports`)
- Handle errors explicitly; never ignore error returns
- Keep functions short and focused; avoid deeply nested code

## Naming Conventions

- Use PascalCase for exported names (functions, types, constants)
- Use camelCase for unexported names (variables, internal functions)
- Use short, meaningful names (e.g., `id`, `err`, `ctx`)

## Error Handling

- Always check returned errors explicitly
- Return descriptive error messages using `fmt.Errorf`
- Log errors with sufficient context

## Concurrency

- Use goroutines for concurrency
- Ensure safe concurrent access using mutexes, channels, or atomic operations
- Avoid leaking goroutines; use contexts to manage lifecycles

## Testing

- Write unit tests using Go's built-in testing framework
- Place tests in files ending with `_test.go`
- Use table-driven tests for clarity and coverage
- Measure test coverage regularly

## Logging

- Use structured logging libraries (e.g., `logrus`, `zap`)
- Centralize logging configuration
- Log errors, warnings, and critical information explicitly

## Performance

- Profile and optimize critical code paths
- Avoid unnecessary allocations and copying
- Use efficient data structures appropriate for the task

## Documentation

- Write concise and clear doc comments on exported functions and types
- Document module-level packages with appropriate package-level comments

## Deployment

- Build binaries explicitly with `go build`
- Containerize applications using Docker for consistency
- Implement automated testing and deployment via CI/CD
