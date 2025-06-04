---
applyTo: "**/.java"
---

# Spring Boot Copilot Instructions

Apply the [Java Core Copilot Instructions](./java.md) to all code.

## General Guidelines

- Follow Spring Boot best practices and conventions
- Keep the application modular, clean, and maintainable
- Leverage Spring Boot’s auto-configuration and starter dependencies effectively

## Project Setup

- Create projects using Spring Initializr or IDE templates
- Clearly manage dependencies using Maven (`pom.xml`) or Gradle (`build.gradle`)
- Structure the project using a layered architecture (controller, service, repository)

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
│   │   │       ├── entities/
│   │   │       ├── dto/
│   │   │       ├── exceptions/
│   │   │       └── config/
│   │   └── resources/
│   │       └── application.properties (or .yml)
│   └── test/
│       └── java/
│           └── com/example/
├── pom.xml or build.gradle
```

## Controllers

- Use `@RestController` or `@Controller` annotations appropriately
- Keep controllers thin; delegate business logic to services
- Map endpoints explicitly with `@RequestMapping`, `@GetMapping`, `@PostMapping`, etc.

## Services

- Annotate services with `@Service`
- Implement clear business logic within service classes
- Keep service methods concise and single-purpose

## Repositories

- Use Spring Data JPA or other Spring Data projects for data access
- Clearly define repository interfaces extending JpaRepository or CrudRepository
- Leverage built-in query methods and custom queries when needed

## Entities and DTOs

- Annotate entities clearly with JPA annotations (`@Entity`, `@Table`, `@Column`)
- Use DTOs for API data transfer; avoid exposing entities directly
- Implement mapping between entities and DTOs explicitly

## Validation

- Use Bean Validation (`javax.validation`) annotations for input validation
- Handle validation errors gracefully and explicitly return meaningful messages

## Exception Handling

- Implement centralized exception handling with `@ControllerAdvice`
- Define and use custom exceptions meaningfully
- Return consistent error responses with clear status codes and messages

## Configuration

- Externalize configurations using `application.properties` or `application.yml`
- Use profiles (`application-dev.yml`, `application-prod.yml`) to manage environment-specific settings
- Define beans and custom configurations explicitly using `@Configuration`

## Security

- Implement security with Spring Security
- Configure authentication and authorization clearly and explicitly
- Secure API endpoints using method-level security annotations (`@PreAuthorize`, `@Secured`)

## Testing

- Write tests using JUnit and Mockito
- Use Spring Boot Test annotations (`@WebMvcTest`, `@SpringBootTest`, `@DataJpaTest`)
- Ensure test coverage for controllers, services, and repositories

## Logging

- Use SLF4J with Logback (default in Spring Boot)
- Centralize and configure logging clearly through `application.properties` or `logback-spring.xml`
- Log key actions and errors explicitly

## Performance

- Optimize data fetching with proper queries, indexes, and caching
- Monitor performance with Actuator and performance profiling tools
- Configure caching explicitly using Spring Cache abstractions

## Deployment

- Create executable JAR files using Spring Boot Maven or Gradle plugins
- Containerize applications with Docker
- Automate builds and deployments through CI/CD pipelines
- Document deployment instructions and environment configurations clearly
