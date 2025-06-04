---
applyTo: "**/.py"
---

# Tkinter Copilot Instructions

Apply the [Python Coding Standards](./python.md) to all code.

## General Guidelines

- Follow Tkinter best practices for GUI applications
- Keep GUI responsive by avoiding blocking operations in the main thread
- Clearly separate UI logic from business logic

## Project Setup

- Structure your project to clearly separate UI and logic
- Use virtual environments (`venv`, `pipenv`, or similar) for dependency management
- Document dependencies clearly (`requirements.txt` or `pyproject.toml`)

## Folder Structure

```
project_root/
├── app/
│   ├── __init__.py
│   ├── gui/
│   │   ├── main_window.py
│   │   ├── dialogs.py
│   ├── logic/
│   │   ├── handlers.py
│   │   ├── validators.py
│   └── assets/
│       ├── images/
│       └── icons/
├── tests/
├── scripts/
├── requirements.txt
└── main.py
```

## Application Structure

- `gui/`: Contains all Tkinter UI components (windows, dialogs, widgets)
- `logic/`: Business logic separated from UI components
- `assets/`: Static resources (images, icons)

## UI Design

- Use `Tkinter` widget classes (`Frame`, `Button`, `Entry`, `Label`, etc.)
- Maintain clear and consistent layout using geometry managers (`pack`, `grid`, `place`)
- Organize widgets logically and clearly name variables

## Event Handling

- Clearly define event handlers and callbacks separately from widget initialization
- Keep event handling logic concise and delegate complex logic to separate modules
- Bind events explicitly to widgets

## Responsiveness

- Use threading or asynchronous techniques for long-running tasks to prevent UI freezing
- Regularly update the UI status to inform users about ongoing operations

## Error Handling

- Catch and handle exceptions gracefully
- Show meaningful error messages to users
- Log errors with detailed context

## Validation

- Validate user input explicitly
- Provide clear feedback on invalid inputs

## Styling

- Use consistent styles across the application
- Define common styles centrally (e.g., fonts, colors)
- Avoid hardcoded styling; prefer style configuration objects or classes

## Testing

- Write unit tests for business logic
- Mock GUI components when necessary for testing
- Focus tests on logic and event handling

## Logging

- Implement structured logging using Python’s built-in `logging` module
- Configure logging formats and levels centrally
- Avoid using print statements in the final application

## Performance

- Optimize UI loading and rendering
- Avoid frequent and unnecessary redraws
- Profile performance-critical operations

## Distribution

- Package applications using tools like PyInstaller for distribution
- Test packaged applications thoroughly
- Document deployment and installation instructions clearly
