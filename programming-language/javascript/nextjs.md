---
applyTo: "**"
---

## General Standards

Apply the [general coding guidelines](./js.md) to all code.

## Application Design

- Use `npx create-next-app@latest` as the base template
- Prefer functional components with React hooks
- Use TypeScript for type safety (recommended)
- Leverage Next.js features: SSR, SSG, and ISR
- Implement API routes for backend functionality
- Use Next.js routing (file-based or App Router)
- Optimize for SEO with metadata and dynamic routes

## Folder Structure

- `app/`: App Router for pages, layouts, and API routes (if used)
- `pages/`: Pages for traditional routing (if not using App Router)
- `components/`: Reusable UI components
- `lib/`: Utility functions and services
- `styles/`: Global and module CSS files
- `public/`: Static assets (images, fonts)
- `hooks/`: Custom React hooks
- `context/`: React Context for state management

## Component Practices

- Use JSX/TSX for component rendering
- Keep components small and focused
- Use props for component configuration; destructure in parameters
- Implement prop types or TypeScript interfaces
- Use `React.memo`, `useMemo`, and `useCallback` for performance
- Prefer Server Components (App Router) for server-side rendering
- Use Client Components (`"use client"`) for interactivity

## Routing

- Use file-based routing in `app/` or `pages/`
- Implement dynamic routes with parameters (e.g., `[id].js`)
- Use `getStaticProps`, `getServerSideProps`, or `getStaticPaths` for data fetching (Pages Router)
- Use Server Components and async components for data fetching (App Router)
- Leverage `next/link` for client-side navigation
- Use `next/router` for programmatic navigation

## Data Fetching

- Use `fetch` or libraries like Axios for API calls
- Implement data fetching in Server Components or `getStaticProps`/`getServerSideProps`
- Use SWR or React Query for client-side data fetching and caching
- Handle loading and error states in components

## Styling

- Use CSS Modules or styled-components for scoped styles
- Define global styles in `styles/globals.css`
- Support responsive design with media queries or frameworks (e.g., Tailwind CSS)
- Use `next/image` for optimized image loading
- Ensure accessibility (e.g., ARIA attributes, keyboard navigation)

## Error Handling

- Use Error Boundaries for client-side errors
- Implement custom error pages (e.g., `app/error.js`, `pages/_error.js`)
- Handle API errors in services or data fetching methods
- Display user-friendly error messages

## State Management

- Use `useState` for local component state
- Use `useReducer` for complex state logic
- Use Context API or libraries (e.g., Redux) for global state
- Minimize global state; prefer component-level state

## Performance

- Optimize re-renders with `React.memo` and hooks
- Use `next/dynamic` for dynamic imports and code splitting
- Leverage `next/image` for image optimization
- Implement ISR or SSG for static content
- Use Vercel or similar platforms for optimized deployments

## Testing

- Use React Testing Library for component tests
- Test Server Components and data fetching with Jest
- Mock API calls with MSW or Jest
- Test custom hooks with `@testing-library/react-hooks`
- Include tests for routing and navigation
