---
applyTo: "**/.py"
---

# PyQt Copilot Instructions

Apply the [Python Coding Standards](./python.md) to all code.

## General Guidelines

- Follow PyQt best practices for GUI application development
- Ensure clear separation of UI components and business logic
- Maintain GUI responsiveness by using proper threading and signals/slots

## Project Setup

- Organize project to clearly separate UI, logic, and resources
- Manage dependencies with virtual environments (`venv`, `pipenv`, `poetry`)
- Document dependencies explicitly (`requirements.txt` or `pyproject.toml`)

## Folder Structure

```
project_root/
├── app/
│   ├── __init__.py
│   ├── ui/
│   │   ├── main_window.py
│   │   ├── dialogs.py
│   ├── logic/
│   │   ├── handlers.py
│   │   ├── validators.py
│   └── resources/
│       ├── images/
│       └── icons/
├── tests/
├── scripts/
├── requirements.txt
└── main.py
```

## Application Structure

- `ui/`: Contains PyQt UI components (main windows, dialogs, custom widgets)
- `logic/`: Application-specific logic and data processing
- `resources/`: Static resources like images and icons

## UI Design

- Use Qt Designer (`.ui` files) or programmatically define widgets
- Load `.ui` files using `uic.loadUi()` or `pyuic` generated Python classes
- Use standard Qt widgets (`QMainWindow`, `QWidget`, `QDialog`, etc.)
- Consistently apply layout managers (`QVBoxLayout`, `QHBoxLayout`, `QGridLayout`)

## Event Handling

- Clearly define signals and slots for event handling
- Keep event logic concise, delegating complex tasks to logic modules
- Explicitly connect signals to slots for readability

## Responsiveness

- Use `QThread` or `QRunnable` and `QThreadPool` for background tasks
- Emit signals to update UI safely from background threads

## Error Handling

- Gracefully handle exceptions with try-except blocks
- Display user-friendly error messages through message boxes (`QMessageBox`)
- Log detailed error information for debugging

## Validation

- Explicitly validate user input using custom validators or built-in PyQt validators
- Provide clear, immediate feedback on validation errors

## Styling

- Use Qt Style Sheets (QSS) for consistent and customizable styling
- Define common styles centrally and apply them consistently
- Avoid hardcoded styles directly within code; prefer external QSS files

## Testing

- Write unit tests for business logic using pytest or unittest
- Mock UI interactions and components where applicable
- Focus tests on logic, event handling, and validation routines

## Logging

- Use structured logging with Python's `logging` module
- Centralize logging configuration for consistency
- Avoid using print statements in production code

## Performance

- Optimize widget initialization and minimize unnecessary UI updates
- Profile and monitor performance-critical components
- Use resource-efficient widgets and avoid excessive nesting

## Distribution

- Package applications with tools like PyInstaller or cx_Freeze
- Ensure thorough testing of packaged executables
- Clearly document deployment steps and requirements
