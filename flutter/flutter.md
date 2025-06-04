---
applyTo: "**/*.dart"
---

# Swift iOS Copilot Instructions

## Project Setup

- Use Xcode project or Swift Package Manager
- Follow Apple's Human Interface Guidelines
- Target appropriate iOS versions with deployment settings

## Architecture

- Use MVVM or VIPER pattern for scalable apps
- Keep `ViewController` lightweight; move logic to `ViewModel` or `Interactor`
- Use `Coordinator` pattern to manage navigation flows if applicable

## Folder Structure

# Flutter Coding Standards

## General Standards

- Follow the **General Java/Kotlin Coding Standards for Mobile** for:
  - Core error handling.
  - Dependency management.
  - Code organization.
  - Logging and testing.
  - Documentation and security.
  - Performance optimization.
- Adapt Java/Kotlin practices to Dart where applicable.

## Application Design

- Use `flutter create` as the base template.
- Follow **MVVM** or **BLoC pattern** for separation of concerns.
- Keep widgets **lightweight**; move logic to ViewModels or BLoC.
- Use **Flutter's widget tree** for UI composition.
- Design for **cross-platform compatibility** (iOS, Android, web, desktop if needed).
- Leverage **Flutter packages** (e.g., `provider`, `flutter_bloc`) for state management.
- Support **multiple screen sizes** and orientations.

## Folder Structure

- **lib/src/features/**: Feature-based folders (e.g., `login`, `products`).
- **lib/src/models/**: Data models.
- **lib/src/screens/**: Screen-level widgets.
- **lib/src/widgets/**: Reusable widget components.
- **lib/src/services/**: Business logic and API services.
- **lib/src/utils/**: Utility functions and helpers.
- **assets/**: Static assets (images, fonts).
- **test/**: Unit and widget tests.
- **integration_test/**: Integration tests.

## Code Practices

- Use **const constructors** for widgets to improve performance.
- Prefer **stateless widgets** over stateful widgets when possible.
- Use **final** for immutable variables.
- Follow **Dart naming conventions**:
  - `camelCase` for variables/functions.
  - `PascalCase` for classes.
- Use **null safety** (`?`, `!`) for safe variable handling.
- Keep widget `build()` methods **clean and focused**.
- Use `async/await` for asynchronous operations (e.g., API calls).

## Widget Practices

- Build UI with **Flutter widgets** or custom widgets.
- Use **BuildContext** appropriately in widget trees.
- Implement **responsive layouts** with `MediaQuery` and `LayoutBuilder`.
- Use **InheritedWidget** or providers for state sharing.
- Avoid **deep widget trees**; refactor into smaller widgets.
- Use **const** for static widgets to reduce rebuilds.

## State Management

- Use `provider`, `flutter_bloc`, or `riverpod` for state management.
- Keep state **localized** to relevant widgets.
- Use **streams** or reactive programming for complex state (e.g., BLoC).
- Implement **state restoration** for critical UI states.

## Data Access

- Use `http` or `dio` for network requests.
- Encapsulate data access in **services** or **repositories**.
- Use **sqflite** or **hive** for local storage.
- Implement **offline-first strategies** with caching.
- Use `json_serializable` for JSON parsing.

## UI and Styling

- Use **Material** or **Cupertino design** for platform-specific UI.
- Define themes in **lib/src/themes/**.
- Support **light/dark modes** with `ThemeMode`.
- Use **asset images** with proper resolution variants.
- Ensure **accessibility** (e.g., semantics, touch targets).
- Optimize animations with **AnimatedBuilder** or **AnimatedWidget**.

## Platform-Specific Considerations

- Handle **platform-specific features** (e.g., permissions, notifications) with packages (e.g., `permission_handler`).
- Use **Platform checks** for conditional platform logic.
- Test on **iOS and Android devices/emulators**.

## Performance

- Use **const widgets** to minimize rebuilds.
- Optimize **image loading** with `cached_network_image`.
- Implement **list virtualization** with `ListView.builder`.
- Profile with **Flutter DevTools** for performance issues.
- Minimize **unnecessary widget rebuilds**.

## Testing

- Write **widget tests** using `flutter_test`.
- Test **business logic** with unit tests.
- Use **mockito** or **mocktail** for mocking dependencies.
- Write **integration tests** for critical user flows.
- Test on **multiple platforms** (iOS, Android).

---

This Markdown format ensures a structured approach to Flutter development. Let me know if you'd like refinements! 🚀
