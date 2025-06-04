---
applyTo: "**/.ts, **/.js, **/.html, **/.css, **/*.scss"
---

# Vue.js Coding Standards

Apply the [general coding guidelines](./js.md) to all code.

## General Standards

- Follow the General JavaScript Coding Standards for core coding practices, error handling, dependency management, code organization, logging, testing, documentation, security, and performance.

## Application Design

- Use Vue CLI, Vite, or Nuxt.js for scaffolding
- Use the Composition API with `<script setup>` (recommended for Vue 3)
- Organize code by feature or domain
- Use single-file components (SFCs) with `.vue` extension
- Prefer TypeScript for type safety (optional but recommended)
- Implement Vue Router for SPA navigation
- Use Vuex or Pinia for state management

## Folder Structure

- `src/components/`: Reusable UI components
- `src/views/`: Page-level components tied to routes
- `src/composables/`: Reusable logic using the Composition API
- `src/store/`: Vuex or Pinia stores
- `src/services/`: API calls and external logic
- `src/assets/`: Static files (images, fonts, icons)
- `src/styles/`: Global and base styles
- `src/router/`: Routing definitions
- `src/utils/`: Helper functions and utilities

## Component Practices

- Use `<script setup>` and Composition API in Vue 3 projects
- Keep components small and focused
- Use props for inputs and `emits` for events
- Destructure props in `<script setup>` scope
- Register and use components locally unless used app-wide
- Use `v-bind` and `v-on` shorthand (`:` and `@`)

## Styling

- Use scoped CSS in `.vue` files
- Use BEM naming for class selectors (optional)
- Define global styles in `src/styles/`
- Use CSS preprocessors like SCSS if needed
- Support responsive design with media queries or utility-first frameworks (e.g., Tailwind CSS)
- Ensure accessibility (ARIA attributes, semantic elements)

## Routing

- Use Vue Router for page navigation
- Define routes in a centralized `router/index.ts`
- Use lazy loading for route-based code splitting
- Use navigation guards for route protection

## State Management

- Use Pinia or Vuex for shared state
- Use the Composition API to create reactive state modules
- Keep state logic separated from components
- Persist state when needed using plugins (e.g., localStorage sync)

## Error Handling

- Use `try/catch` for async/await blocks
- Display user-friendly error messages in the UI
- Use global error boundaries or Vue error handlers
- Handle API errors in service layers or composables

## Performance

- Use `v-if` and `v-show` appropriately
- Use `key` in `v-for` loops
- Avoid large reactive objects when unnecessary
- Lazy-load heavy components using dynamic import
- Optimize image usage and component re-renders

## Testing

- Use Vitest or Jest for unit testing
- Use Vue Test Utils for component testing
- Mock API calls and store dependencies
- Test props, events, and lifecycle behavior
- Aim for coverage on shared logic and interactive components
