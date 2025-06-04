---
applyTo: "**"
---

# NestJS Coding Standards

Apply the [general coding guidelines](./js.md) to all code.

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

## Application Design

- Use `nest new` as the base template.
- Follow **modular architecture** with modules, controllers, and services.
- Use **TypeScript** for type safety.
- Keep controllers **thin**; move logic to services.
- Use **dependency injection** for services and providers.
- Implement **RESTful APIs** or **GraphQL** based on project needs.
- Support **API versioning** (e.g., `@nestjs/versioning`).

## Folder Structure

- **src/modules/**: Feature-based modules (e.g., `products/`, `users/`).
- **src/modules/\*/controllers/**: Controller classes.
- **src/modules/\*/services/**: Business logic.
- **src/modules/\*/entities/**: Data models or entities.
- **src/common/**: Shared utilities, decorators, and pipes.
- **src/config/**: Configuration files.
- **src/middleware/**: Custom middleware.

## Module and Component Practices

- Define **one module per feature** (e.g., `ProductsModule`).
- Use `@Controller` and `@Injectable` decorators.
- Use **DTOs** for input/output validation with `class-validator`.
- Implement **pipes** for request validation.
- Use `@nestjs/config` for environment variables.
- Group routes by resource with **proper HTTP methods**.

## Data Access

- Use `@nestjs/typeorm`, `@nestjs/sequelize`, or similar for ORM integration.
- Encapsulate **data access** in repositories or services.
- Use **entities** for database schema definition.
- Implement **migrations** for database changes.

## Error Handling

- Use **NestJS built-in exception filters**.
- Define **custom exceptions** with `@nestjs/common`.
- Return **consistent error responses** (e.g., HTTP Problem Details).
- Use **global pipes** for validation.

## Performance

- Use `@nestjs/cqrs` for complex command/query patterns.
- Implement **caching** with `@nestjs/cache-manager`.
- Optimize **database queries** with proper indexing.
- Use **pagination** for large datasets.

---

This Markdown file ensures clarity, structure, and best practices for NestJS development. Let me know if you'd like any refinements! 🚀
