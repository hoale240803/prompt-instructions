---
applyTo: "**/*.swift"
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

```
project_root/
├── Models/
├── Views/
├── ViewModels/
├── Controllers/
├── Coordinators/
├── Resources/
│ ├── Assets.xcassets
│ ├── Localizable.strings
│ └── Info.plist
├── Extensions/
└── Utilities/
```

## UI Development

- Prefer Storyboards or SwiftUI depending on project strategy
- Use Auto Layout or SwiftUI layout modifiers for responsiveness
- Avoid hardcoding sizes or colors; use constants or system styles

## State Management

- Use `@State`, `@Published`, or Combine for reactive UI
- Avoid force-unwrapping optionals (`!`) in UI logic

## Dependency Injection

- Use protocols for abstraction and inject dependencies via initializers or service locators
- Use third-party DI libraries (e.g., Swinject) only when needed

## Error Handling

- Use Swift's `do-catch` blocks for error-prone operations
- Define custom `Error` types for domain-specific errors
- Display user-friendly messages for failures (e.g., alerts)

## Networking

- Use `URLSession`, `Alamofire`, or Combine-based networking
- Create a networking layer for reusable API handling
- Always handle retries, timeouts, and parsing gracefully

## Testing

- Write unit tests with XCTest
- Use mocks or fakes for service and network dependencies
- Include UI tests for user flows using XCUITest

## Performance

- Profile the app with Instruments for memory and CPU usage
- Avoid blocking main thread with long-running tasks
- Cache expensive computations or images where needed

## Accessibility

- Add accessibility labels to all UI components
- Support dynamic type and VoiceOver

## Security

- Store sensitive data in Keychain
- Avoid logging personal or sensitive information
- Validate and sanitize all external inputs

## Release and Deployment

- Sign apps with proper provisioning profiles
- Configure build settings for Debug and Release
- Upload builds through TestFlight or App Store Connect
