---
applyTo: "**/.ts, **/.js"
---

# Electron Coding Standards

Apply the [general coding guidelines](./js.md) to all code.

## General Standards

- Follow the General JavaScript Coding Standards for core coding practices, error handling, dependency management, code organization, logging, testing, documentation, security, and performance.

## General Standards

- Follow the **General JavaScript Coding Standards** for:
  - Core coding practices.
  - Error handling.
  - Dependency management.
  - Code organization.
  - Logging.
  - Testing.
  - Documentation.
  - Security.
  - Performance.

## Application Design

- Use **electron-forge** or **electron-builder** as the base template.
- Structure application with **main** and **renderer** processes.
- Use **Inter-Process Communication (IPC)** for main-renderer communication.
- Prefer **TypeScript** for type safety (recommended).
- Design for **cross-platform compatibility** (Windows, macOS, Linux).
- Implement **context isolation** and **node integration** for security.
- Use **MVVM** or similar pattern for renderer process UI.

## Folder Structure

- **src/main/**: Main process code (e.g., `main.js`, IPC handlers).
- **src/renderer/**: Renderer process code (e.g., UI components, logic).
- **src/common/**: Shared utilities and models.
- **src/assets/**: Static files (images, icons, styles).
- **src/services/**: External services (e.g., API calls, file system).
- **tests/**: Unit and integration tests.
- **dist/**: Build output (managed by build tools).

## Main Process Practices

- Keep **main process** focused on app lifecycle, windows, and IPC.
- Use `@electron/remote` for renderer access to main process (if needed).
- Handle app events (e.g., `ready`, `window-all-closed`) in `main.js`.
- Minimize **main process logic**; delegate to services.
- Use **BrowserWindow options** for security (e.g., `nodeIntegration: false`, `contextIsolation: true`).

## Renderer Process Practices

- Use **React, Vue, or plain JavaScript** for UI rendering.
- Implement components in `src/renderer/components/` (if using a framework).
- Use **IPC (`ipcRenderer`)** for communication with the main process.
- Avoid **direct access to Node.js APIs** in the renderer; use IPC instead.
- Use **state management** (e.g., React hooks, Vuex) for UI state.
- Implement **error boundaries** for UI error handling.

## IPC Practices

- Define clear IPC channels with **unique names** (e.g., `ipcMain.handle('channel-name')`).
- Validate **IPC inputs** in the main process.
- Use **async IPC handlers** for I/O operations.
- Avoid **sending sensitive data** over IPC without encryption.

## Data Access

- Use **file system** (`fs`) or **local databases** (e.g., SQLite) in the main process.
- Encapsulate **data access** in services (e.g., `src/services/dataService.js`).
- Use **IPC to expose data** to the renderer process.
- Implement **caching** for frequently accessed data.

## Styling

- Use **CSS Modules**, `styled-components`, or frameworks (e.g., **Tailwind CSS**).
- Define **global styles** in `src/assets/styles/`.
- Ensure **responsive design** for different window sizes.
- Support **light/dark themes** based on OS settings.
- Use Electron’s **nativeTheme** for theme detection.

## Error Handling

- Handle errors in **main process** with `try/catch` and logging.
- Use **error boundaries** in the renderer process (if using React).
- Display **user-friendly error dialogs** via `dialog` module.
- Validate **inputs** in both main and renderer processes.

## Build and Packaging

- Use **electron-forge** or **electron-builder** for packaging.
- Configure **platform-specific settings** (e.g., icons, notarization for macOS).
- Minimize **bundle size** by excluding unnecessary dependencies.
- Test builds on **all target platforms** (Windows, macOS, Linux).

## Performance

- Optimize **renderer process** with memoization (e.g., `React.memo`).
- Minimize **IPC calls**; batch data transfers.
- Use **lazy loading** for large assets.
- Optimize **startup time** with preload scripts.
- Profile performance with **Electron’s DevTools**.

## Testing

- Use **Spectron** or **Playwright** for end-to-end testing.
- Test **main process logic** with `Jest` or `Mocha`.
- Test **renderer process** with **React Testing Library** (if using React).
- Mock **IPC and Node.js APIs** for unit tests.
- Ensure **cross-platform test coverage**.
