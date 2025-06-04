---
applyTo: "**/*.cs"
---

# Project Coding Standards for ASP.NET Core MVC

## Application Design

- Use `dotnet new mvc` as the base template.
- Keep controllers thin; move logic to services.
- Define and inject interfaces for all services.
- Use `[Controller]` and `[Route]` attributes for routing.
- Group related actions in dedicated controllers.
- Follow MVC pattern:
  - Models for data.
  - Views for UI.
  - Controllers for logic.
- Implement URL-friendly routing (e.g., `/products/details/{id}`).

## Folder Structure

- **Controllers/**: MVC controllers.
- **Models/**: Domain models.
- **DTOs/**: Data Transfer Objects.
- **Services/**: Business logic and interfaces.
- **Repositories/**: Data access logic and interfaces.
- **Views/**: Razor views organized by controller.
- **wwwroot/**: Static files (CSS, JS, images).
- **Configuration/**: DI setup and configurations.
- **Middleware/**: Custom middleware.
- **Exceptions/**: Custom exception types.
- **Utilities/**: Helper classes (e.g., AutoMapper profiles).

## Code Practices

- Use `async/await` for I/O-bound operations.
- Return `IActionResult` with appropriate status codes.
- Use `var` only when type is obvious.
- Use `nameof()` for parameter references.
- Use file-scoped namespaces.
- Minimize `using` statements.
- Handle nulls with `??` and `?.` operators.
- Prefer immutable properties and readonly fields.

## View Practices

- Use Razor syntax for views.
- Leverage ViewModels for view-specific data.
- Use partial views for reusable UI components.
- Implement layouts for consistent UI.
- Use Tag Helpers over HTML Helpers.

## Error Handling

- Implement centralized exception handling with middleware.
- Define custom exceptions (e.g., `NotFoundException`).
- Validate inputs with data annotations and `ModelState`.
- Use custom error views (e.g., `Error.cshtml`).

## Dependency Injection

- Register services and repositories in `Program.cs`.
- Use appropriate DI lifetimes (Scoped, Singleton, Transient).

## Data Access

- Use repository pattern for data access.
- Use Entity Framework Core for database interactions.

## DTOs and Mapping

- Define DTOs for API and view data transfer.
- Use AutoMapper for entity-DTO/ViewModel mapping.
- Configure AutoMapper in `Program.cs`.

## Logging

- Use `ILogger` for structured logging.

## Testing

- Write unit tests for services and repositories.
- Write integration tests for controllers and views.
- Use `Moq` for mocking dependencies.

## Documentation

- Enable Swagger for API endpoints (if combined with Web API).
- Use XML comments for controllers and models.
- Document view logic with comments in Razor files.

## Security

- Implement authentication (e.g., ASP.NET Core Identity) and `[Authorize]`.
- Validate and sanitize inputs.
- Configure CORS if needed.
- Use HTTPS redirection.
- Implement CSRF protection with `[ValidateAntiForgeryToken]`.

## Performance

- Use response caching for static content.
- Implement pagination for large datasets.
- Optimize view rendering with ViewComponents.
