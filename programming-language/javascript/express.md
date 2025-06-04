---
applyTo: "**"
---

# Express.js Coding Standards

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

- Use **Express.js** for lightweight, RESTful APIs.
- Structure application with **middleware, routes, and controllers**.
- Keep routes focused on **HTTP handling**; move logic to services.
- Use middleware for cross-cutting concerns (e.g., authentication, logging).
- Implement **RESTful conventions** (noun-based routes, HTTP methods, status codes).
- Support **API versioning** (e.g., `/api/v1/products`).

## Folder Structure

- **src/routes/**: Route definitions.
- **src/controllers/**: Request handling logic.
- **src/services/**: Business logic.
- **src/middleware/**: Custom middleware.
- **src/models/**: Data models (if not using an ORM).
- **src/utils/**: Utility functions.
- **src/config/**: Configuration files (e.g., database, environment).

## Route and Controller Practices

- Define routes in **separate files** by resource (e.g., `productRoutes.js`).
- Use controllers to handle **route logic**.
- Return **consistent HTTP status codes** (e.g., `200`, `201`, `404`, `400`).
- Use **async handlers** with `express-async-handler` for error handling.
- Validate request data with **libraries like `express-validator`**.

## Middleware

- Use middleware for **authentication, logging, and error handling**.
- Implement **custom middleware** for reusable logic.
- Use `express.json()` and `express.urlencoded()` for request parsing.
- Apply **Helmet** for security headers.

## Data Access

- Use an **ORM** (e.g., `Sequelize`, `TypeORM`) or query builder (e.g., `Knex`).
- Encapsulate **data access** in services or repositories.
- Use **connection pooling** for database performance.

## Performance

- Use **compression middleware** (e.g., `compression`).
- Implement **pagination** for large datasets.
- Cache responses with **apicache or Redis**.
