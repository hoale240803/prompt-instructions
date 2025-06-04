---
applyTo: "**/.java"
---

# Java Core Copilot Instructions

## General Guidelines

- Follow Java coding conventions and best practices
- Maintain clear, readable, and maintainable code
- Adhere to SOLID principles and design patterns appropriately

## Project Setup

- Structure projects using Maven or Gradle for dependency management
- Define clear project modules/packages for logical separation
- Manage dependencies explicitly through `pom.xml` (Maven) or `build.gradle` (Gradle)

## Folder Structure

```
project_root/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com/example/
│   │   │       ├── controllers/
│   │   │       ├── services/
│   │   │       ├── repositories/
│   │   │       ├── models/
│   │   │       └── utils/
│   │   └── resources/
│   └── test/
│       └── java/
│           └── com/example/
├── pom.xml (Maven)
├── build.gradle (Gradle)
```

## Naming Conventions

- Use PascalCase for class names (e.g., `UserService`)
- Use camelCase for methods and variables (e.g., `calculateTotal`)
- Constants should use ALL_CAPS with underscores (e.g., `MAX_LIMIT`)
- Package names should be lowercase and meaningful

## Coding Practices

- Use proper encapsulation (private fields, getters/setters)
- Avoid deep nesting; use early returns and guard clauses
- Keep methods small, single-purpose, and concise
- Document public methods and classes clearly with Javadoc

## Error Handling

- Use try-catch blocks appropriately; avoid catching generic exceptions
- Define and use meaningful custom exceptions
- Log exceptions explicitly with detailed context

## Collections and Streams

- Prefer streams for complex data transformations
- Choose appropriate collection types (`List`, `Set`, `Map`) based on requirements
- Optimize use of streams for readability and performance

## Concurrency

- Use thread-safe collections and concurrency utilities
- Clearly manage thread lifecycle and use synchronization appropriately
- Leverage Executors and CompletableFuture for asynchronous operations

## Testing

- Write unit tests using JUnit or TestNG
- Mock dependencies with Mockito or similar libraries
- Keep tests isolated, repeatable, and fast
- Aim for high test coverage on critical components

## Logging

- Use structured logging libraries such as Log4j, SLF4J, or Logback
- Centralize logging configuration and use different log levels clearly
- Avoid System.out.println statements in production code

## Performance

- Optimize critical paths and minimize object creation
- Profile performance with tools like VisualVM or JProfiler
- Regularly monitor and address performance bottlenecks

## Documentation

- Use Javadoc to document public APIs clearly
- Include meaningful explanations of parameters, return values, and exceptions
- Document module and package responsibilities explicitly

## Deployment

- Package applications clearly with JAR/WAR files
- Automate builds and deployments using CI/CD pipelines
- Document deployment instructions and environment configurations explicitly
