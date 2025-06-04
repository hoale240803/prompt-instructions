---
applyTo: "**/*.cs, **/*.xaml"
---

# .NET MAUI Coding Standards

Apply the [general coding guidelines](./csharp.md) to all code.

## General Standards

- Follow the General C# Coding Standards for core coding practices, error handling, dependency injection, data access, logging, testing, documentation, security, and performance.

## Application Design

- Use `dotnet new maui` as the base template
- Follow MVVM pattern: Models, Views, ViewModels
- Keep Views (XAML) focused on UI; move logic to ViewModels
- Define and inject interfaces for services
- Use commands for user interactions
- Implement navigation using Shell or a navigation service
- Design for cross-platform compatibility (iOS, Android, Windows, macOS)

## Folder Structure

- Models/: Domain models and entities
- ViewModels/: ViewModel classes
- Views/: XAML pages and controls
- Services/: Business logic and interfaces
- Repositories/: Data access logic and interfaces
- Common/: Shared utilities (e.g., converters, commands)
- Resources/: Static assets (images, fonts, styles)
- Configuration/: App settings and DI setup

## MVVM Practices

- Use ViewModels to manage view state and logic
- Bind XAML properties to ViewModel properties
- Use `ICommand` for event handling
- Avoid code-behind in XAML files
- Use data templates for dynamic UI
- Implement `INotifyPropertyChanged` for data binding

## UI and Styling

- Use XAML for UI design
- Define reusable styles in `Resources/Styles`
- Use platform-specific adjustments with `OnPlatform` and `OnIdiom`
- Ensure responsive design with layout controls
- Support light/dark themes
- Optimize for multiple form factors (phone, tablet, desktop)

## Platform-Specific Considerations

- Handle platform-specific services (e.g., permissions, notifications)
- Test on all target platforms (iOS, Android, Windows, macOS)

## Performance

- Use collection virtualization for large lists
- Optimize image loading and caching
