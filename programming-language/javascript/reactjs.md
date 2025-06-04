---
applyTo: "**/.ts, **/.js, **/.html, **/.css, **/*.scss"
---

# React.js Coding Standards

## General Standards

Apply the [General JavaScript Coding Standards](./js.md) to all code.

## Application Design

- Use `create-react-app` or Vite for scaffolding (prefer Vite for performance)
- Prefer functional components over class components
- Use TypeScript for type safety (recommended)
- Structure projects with separation of concerns: components, hooks, contexts, services
- Favor composition over inheritance

## Folder Structure

- `src/components/`: Reusable UI components
- `src/hooks/`: Custom React hooks
- `src/context/`: Global state providers
- `src/services/`: API calls and business logic
- `src/utils/`: Helper functions
- `src/assets/`: Static resources (images, fonts)
- `src/styles/`: Global and scoped CSS/SCSS files

## Component Practices

- Keep components small, focused, and reusable
- Use props and children for customization
- Destructure props in function parameters
- Use `React.memo`, `useMemo`, and `useCallback` for performance
- Co-locate styles and tests with components when practical

## Hooks

- Follow the Rules of Hooks (no conditional hooks, call from top level)
- Use built-in hooks (`useState`, `useEffect`, etc.) appropriately
- Use custom hooks for shared logic between components
- Name custom hooks with `use` prefix (e.g., `useAuth`)

## State Management

- Use `useState` for local UI state
- Use `useReducer` for complex or nested state
- Use Context API for shared state; avoid prop drilling
- Use state libraries (e.g., Redux, Zustand, Recoil) when global state becomes complex

## Styling

- Use CSS Modules or styled-components for scoped styles
- Define global styles in `index.css` or `App.css`
- Support responsive design via media queries or frameworks (e.g., Tailwind CSS)
- Ensure accessibility in all interactive components

## Routing

- Use `react-router-dom` for client-side routing
- Structure routes in a central place (e.g., `App.tsx` or `Routes.tsx`)
- Use `useNavigate` for programmatic navigation

## Error Handling

- Wrap critical UI areas with Error Boundaries
- Handle fetch/API errors in service layers
- Display fallback UI or error messages gracefully

## Performance

- Lazy load components with `React.lazy` and `Suspense`
- Use dynamic imports for heavy routes or features
- Debounce user input in search or filtering components
- Avoid unnecessary re-renders using `React.memo`, `useMemo`, `useCallback`

## Testing

- Use React Testing Library for rendering and interaction testing
- Use Jest for logic testing
- Mock APIs with MSW or custom mocks
- Test hooks using `@testing-library/react-hooks`
- Maintain high coverage for reusable components and hooks
