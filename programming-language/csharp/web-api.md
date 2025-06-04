---
applyTo: "**/*.cs"
---

# Project Coding Standards for ASP.NET Core Web API

## API Design

- Use `dotnet new webapi` as the base template
- Keep controllers thin; move logic to services
- Define and inject interfaces for all services
- Apply `[ApiController]` for automatic model binding
- Group related endpoints in dedicated controllers
- Follow RESTful conventions (nouns, HTTP methods, status codes)
- Implement API versioning (e.g., `api/v1/products`)

## Folder Structure

- Controllers/: API controllers
- Models/: Domain models
  - DTOs/: Data Transfer Objects
- Services/: Business logic and interfaces
- Repositories/: Data access logic and interfaces
- Configuration/: DI setup and configurations
- Middleware/: Custom middleware
- Exceptions/: Custom exception types
- Utilities/: Helper classes (e.g., AutoMapper profiles)

```
MyApiProject/
├── Controllers/
│   ├── ProductsController.cs
│   ├── OrdersController.cs
├── Models/
│   ├── Product.cs
│   ├── DTOs/
│   │   ├── ProductDto.cs
│   │   ├── CreateProductDto.cs
├── Services/
│   ├── IProductService.cs
│   ├── ProductService.cs
├── Repositories/
│   ├── IProductRepository.cs
│   ├── ProductRepository.cs
├── Configuration/
│   ├── ServiceCollectionExtensions.cs
├── Middleware/
│   ├── ExceptionMiddleware.cs
├── Exceptions/
│   ├── NotFoundException.cs
├── Utilities/
│   ├── MappingProfile.cs
├── appsettings.json
├── Program.cs
```

## Code Practices

- Use `async/await` for I/O and API methods
- Return `ActionResult<T>` with proper status codes
- Use `var` only when type is obvious
- Use `nameof()` for parameter references
- Use file-scoped namespaces
- Minimize `using` statements
- Handle nulls with `??` and `?.` operators
- Prefer immutable properties and readonly fields

## Error Handling

- Implement centralized exception handling with middleware
- Define custom exceptions (e.g., `NotFoundException`)
- Validate inputs with data annotations and `ModelState`

## Dependency Injection

- Register services and repositories in `Program.cs`
- Use appropriate DI lifetimes (Scoped, Singleton, Transient)

## Data Access

- Use repository pattern for data access
- Use Entity Framework Core for database interactions

## DTOs and Mapping

- Define DTOs for API contracts
- Use AutoMapper for entity-DTO mapping
  Configure AutoMapper in Program.cs

## Logging

- Use ILogger for structured logging

## Testing

- Write unit tests for services and repositories
- Write integration tests for controllers
- Use Moq for mocking dependencies

## Documentation

- Enable Swagger with `Swashbuckle.AspNetCore` or ``Scalar.AspNetCore`
- Use XML comments for controllers and DTOs

## Security

- Implement authentication (e.g., JWT) and `[Authorize]`
- Validate and sanitize inputs
- Configure CORS for cross-domain access

## Performance

- Use response caching for read-heavy endpoints
- Implement pagination for large datasets
