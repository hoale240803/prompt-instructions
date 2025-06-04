---
applyTo: "**"
---

# Project Coding Standards for ASP.NET Core Microservice with Domain-Driven Design (DDD)

## Application Design

- Use `dotnet new webapi` as the base for each microservice.
- Follow Domain-Driven Design (DDD) principles:
  - Entities, Aggregates, Value Objects.
- Define bounded contexts for each microservice.
- Keep controllers thin; move logic to application services.
- Use interfaces for services and repositories.
- Apply `[ApiController]` for automatic model binding.
- Group related endpoints by bounded context.
- Use RESTful or event-driven communication:
  - HTTP, gRPC, or message queues.

## Folder Structure

- **Domain/**: Core entities, aggregates, value objects, domain events.
- **Application/**: Application services, DTOs, commands, queries.
- **Infrastructure/**: Repositories, EF Core configurations, external integrations.
- **API/**: Controllers, middleware, API configurations.
- **Common/**: Shared utilities (e.g., AutoMapper profiles, exceptions).
- **Tests/**: Unit and integration tests.

## Code Practices

- Use `async/await` for I/O-bound operations.
- Return `ActionResult<T>` with proper status codes.
- Use `var` only when type is obvious.
- Use `nameof()` for parameter references.
- Use file-scoped namespaces.
- Minimize `using` statements.
- Handle nulls with `??` and `?.` operators.
- Prefer immutable properties and readonly fields.

## Domain-Driven Design

- Define aggregates with a single root entity.
- Use value objects for immutable, identity-less types.
- Implement domain events for cross-aggregate communication.
- Enforce invariants within aggregates.
- Use specifications for complex query logic.

## Application Layer

- Use MediatR for CQRS (commands and queries).
- Define command/query handlers for application logic.
- Use DTOs for input/output data transfer.
- Implement business rules in application services.

## Error Handling

- Implement centralized exception handling with middleware.
- Define custom domain exceptions (e.g., `DomainValidationException`).
- Validate inputs with FluentValidation or data annotations.
- Return consistent error responses (e.g., Problem Details).

## Dependency Injection

- Register services, repositories, and handlers in `Program.cs`.
- Use appropriate DI lifetimes:
  - Scoped for handlers.
  - Transient for lightweight objects.

## Data Access

- Use repository pattern for data access within Infrastructure.
- Use Entity Framework Core for persistence.
- Define EF configurations in Infrastructure layer.
- Use in-memory databases for testing.

## Messaging and Communication

- Use message queues (e.g., RabbitMQ, Kafka) for inter-service communication.
- Implement event publishing/subscription for domain events.
- Use HTTP/gRPC for synchronous communication.

## Logging

- Use `ILogger` for structured logging.
- Log domain events and critical operations.

## Testing

- Write unit tests for domain logic and application services.
- Write integration tests for controllers and repositories.
- Use `Moq` for mocking dependencies.
- Test domain invariants and event handling.

## Documentation

- Enable Swagger for API documentation.
- Use XML comments for controllers and DTOs.
- Document domain models and business rules.

## Security

- Implement authentication (e.g., JWT, OAuth) and `[Authorize]`.
- Validate and sanitize inputs.
- Configure CORS for inter-service communication.
- Use API gateways for centralized security.

## Performance

- Use response caching for read-heavy endpoints.
- Implement pagination for large datasets.
- Optimize database queries with projections.
- Use asynchronous messaging for scalability.
