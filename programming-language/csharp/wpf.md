---
applyTo: "**"
---

# Project Coding Standards for WPF Desktop Application

## Application Design

- Use `dotnet new wpf` as the base template.
- Follow MVVM pattern:
  - Models for data.
  - Views for UI.
  - ViewModels for logic.
- Keep Views (XAML) focused on UI; move logic to ViewModels.
- Define and inject interfaces for services.
- Use commands for user interactions.
- Implement navigation using a navigation service.
- Design for modularity and reusability.

## Folder Structure

- **Models/**: Domain models and entities.
- **ViewModels/**: ViewModel classes.
- **Views/**: XAML views.
- **Services/**: Business logic and interfaces.
- **Repositories/**: Data access logic and interfaces.
- **Common/**: Shared utilities (e.g., converters, commands).
- **Assets/**: Static resources (images, styles).
- **Configuration/**: App settings and DI setup.

## Code Practices

- Use `async/await` for I/O-bound operations.
- Use `var` only when type is obvious.
- Use `nameof()` for property references.
- Use file-scoped namespaces.
- Minimize `using` statements.
- Handle nulls with `??` and `?.` operators.
- Prefer immutable properties and readonly fields.
- Implement `INotifyPropertyChanged` for data binding.

## MVVM Practices

- Use ViewModels to manage view state and logic.
- Bind XAML properties to ViewModel properties.
- Use `ICommand` for button/event handling.
- Avoid code-behind in XAML files.
- Use data templates for dynamic UI.

## Error Handling

- Implement centralized exception handling.
- Define custom exceptions (e.g., `DataAccessException`).
- Display user-friendly error messages via dialogs.
- Validate inputs in ViewModels.

## Dependency Injection

- Register services and repositories in DI container.
- Use appropriate DI lifetimes:
  - Singleton for services.
  - Transient for ViewModels.
- Use a DI framework (e.g., `Microsoft.Extensions.DependencyInjection`).

## Data Access

- Use repository pattern for data access.
- Use Entity Framework Core or SQLite for local storage.
- Implement data caching for performance.

## UI and Styling

- Use XAML for UI design.
- Define reusable styles and resources in `App.xaml`.
- Use data triggers and behaviors for dynamic UI.
- Ensure responsive design with layout controls.
- Support light/dark themes.

## Logging

- Use `ILogger` or a logging framework (e.g., Serilog).
- Log user actions and errors for debugging.

## Testing

- Write unit tests for ViewModels and services.
- Write integration tests for data access.
- Use `Moq` for mocking dependencies.
- Test UI interactions with UI automation frameworks.

## Documentation

- Use XML comments for public APIs and ViewModels.
- Document XAML bindings and styles.
- Maintain a project readme for setup instructions.

## Security

- Validate and sanitize user inputs.
- Encrypt sensitive data (e.g., user settings).
- Use secure storage for credentials.

## Performance

- Optimize data binding with lightweight models.
- Use virtualization for large lists.
- Implement lazy loading for resources.
- Minimize UI thread blocking.
