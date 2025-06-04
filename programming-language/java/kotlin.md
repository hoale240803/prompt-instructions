General Java/Kotlin Coding Standards for Mobile
Code Practices

Use val (Kotlin) or final (Java) for immutable variables
Prefer concise syntax (e.g., Kotlin's type inference, Java's var in Java 10+)
Use descriptive names for classes, methods, and variables
Follow camelCase for variables and methods, PascalCase for classes
Keep methods small and focused on a single responsibility
Use null safety (Kotlin: ? and !!, Java: Optional or null checks)
Prefer functional programming constructs (e.g., Kotlin lambdas, Java streams)
Use modern language features (e.g., Kotlin coroutines, Java 17+ features)

Error Handling

Use try-catch for exception handling
Throw custom exceptions with meaningful messages
Validate inputs to prevent runtime errors
Handle nullability explicitly (Kotlin: safe calls, Java: Optional)

Dependency Management

Use Gradle for build and dependency management
Pin dependency versions in build.gradle
Group dependencies by purpose (e.g., implementation, testImplementation)
Regularly update dependencies for security and compatibility

Code Organization

Organize code by feature or module (e.g., feature/login, feature/payment)
Use packages to group related classes (e.g., com.example.model)
Keep configuration files (e.g., build.gradle, proguard-rules.pro) at project root
Use resource files for strings, dimensions, and assets

Logging

Use Android's Log class or a logging library (e.g., Timber for Kotlin)
Log errors with context (e.g., stack trace, user input)
Avoid logging sensitive data (e.g., user credentials)
Suppress debug logs in production builds

Testing

Write unit tests for business logic using JUnit or Kotest
Write UI tests using Espresso or UI Automator
Use Mockito or MockK for mocking dependencies
Aim for high test coverage (>80%) for critical paths

Documentation

Use KDoc (Kotlin) or Javadoc (Java) for public APIs
Maintain a README.md with setup and usage instructions
Document complex logic with inline comments
Include resource documentation (e.g., string names, layout purposes)

Security

Validate and sanitize user inputs
Encrypt sensitive data (e.g., using Android Keystore)
Use secure network protocols (e.g., HTTPS)
Implement permission checks for sensitive operations

Performance

Optimize resource usage (e.g., memory, CPU) for mobile constraints
Use lazy initialization for expensive resources
Implement caching for frequently accessed data
Minimize background processing to preserve battery
