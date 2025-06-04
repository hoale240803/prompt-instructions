---
applyTo: "**/.java, **/.xml, **/.gradle "
---

# Android Studio (Java) Copilot Instructions

Apply the [Java Core Copilot Instructions](./java.md) to all Java code.

## General Guidelines

- Follow Android best practices and material design principles
- Maintain clear separation between UI, business logic, and data layers
- Optimize code for performance and responsiveness

## Project Setup

- Initialize projects using Android Studio templates
- Clearly manage dependencies using Gradle (`build.gradle`)
- Target appropriate SDK versions explicitly in Gradle configuration

## Folder Structure

```
project_root/
├── app/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/com/example/
│   │   │   │   ├── activities/
│   │   │   │   ├── fragments/
│   │   │   │   ├── adapters/
│   │   │   │   ├── viewmodels/
│   │   │   │   ├── repositories/
│   │   │   │   └── models/
│   │   │   └── res/
│   │   │       ├── layout/
│   │   │       ├── drawable/
│   │   │       ├── values/
│   │   │       └── menu/
│   │   └── test/
│   └── build.gradle
├── build.gradle
└── settings.gradle
```

## Activities and Fragments

- Keep Activities lean, delegating logic to ViewModels and Fragments
- Use Fragments for reusable UI components
- Clearly manage lifecycle events explicitly

## ViewModels

- Use `ViewModel` from Android Architecture Components
- Handle UI data preparation and business logic
- Implement observable data patterns with LiveData or Flow

## Repositories and Data Sources

- Abstract data access logic in repositories
- Implement repositories clearly to separate data sources (network, local databases)
- Use libraries like Room or Retrofit for data access

## UI Design

- Follow Material Design guidelines explicitly
- Define layouts clearly and consistently using XML
- Optimize UI components for various device configurations and screen sizes

## Dependency Injection

- Implement dependency injection with libraries like Hilt or Dagger
- Keep injection configurations clear and explicit

## Data Binding and View Binding

- Prefer View Binding for efficient view referencing
- Use Data Binding selectively for reactive UI updates

## Error Handling

- Clearly handle exceptions and errors in UI and data layers
- Display meaningful and user-friendly error messages
- Log detailed error contexts explicitly

## Performance

- Optimize UI rendering and minimize memory usage
- Use profiling tools provided by Android Studio (Profiler)
- Avoid blocking the main thread (use coroutines, RxJava, or AsyncTask appropriately)

## Testing

- Write unit tests using JUnit and Mockito
- Write UI tests using Espresso
- Test ViewModels and repositories explicitly

## Logging

- Use Android Logcat (`Log`) for logging
- Clearly differentiate log levels (DEBUG, INFO, WARN, ERROR)
- Avoid excessive logging in production builds

## Security

- Secure sensitive data using Android’s security best practices (KeyStore, encryption)
- Validate and sanitize all user input explicitly

## Deployment

- Generate signed APKs or Android App Bundles (AAB) explicitly
- Automate testing and deployment through CI/CD pipelines
- Document deployment steps and requirements clearly
