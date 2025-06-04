---
applyTo: "**/.ts, **/.js, **/.html, **/.css, **/*.scss"
---

# Angular Coding Standards

Apply the [general coding guidelines](./js.md) to all code.

## General Standards

- Follow the General JavaScript Coding Standards for core coding practices, error handling, dependency management, code organization, logging, testing, documentation, security, and performance.

## Application Design

- Use the Angular CLI (`ng new`) for scaffolding projects
- Use TypeScript for all development
- Follow the component-based architecture pattern
- Use services for business logic and dependency injection
- Keep components declarative and focused on UI
- Structure apps using modules for feature separation
- Use Angular Routing for SPA navigation

## Folder Structure

- `src/app/`: Root application folder
- `src/app/components/`: Reusable UI components
- `src/app/pages/`: Page-level components tied to routes
- `src/app/services/`: Injectable services
- `src/app/models/`: Interface and class definitions
- `src/app/guards/`: Route guards
- `src/app/interceptors/`: HTTP interceptors
- `src/app/shared/`: Shared modules, pipes, and directives
- `src/assets/`: Static files (e.g., images, icons)
- `src/environments/`: Environment-specific config

## Component Practices

- Use Angular CLI (`ng generate component`) to generate components
- Use `@Input()` and `@Output()` for parent-child communication
- Keep component classes minimal; delegate logic to services
- Follow naming conventions (`kebab-case` for selectors, `PascalCase` for files)
- Use `OnPush` change detection strategy for performance
- Separate template logic from business logic

## Templates and Styling

- Use inline templates/styles only for small or utility components
- Use component-scoped styles (default behavior)
- Use CSS/SCSS modules for reusable styles
- Avoid deep CSS selectors; prefer component encapsulation
- Follow BEM naming convention for class names (optional)
- Ensure accessibility (ARIA attributes, semantic HTML)

## Services and Dependency Injection

- Use `@Injectable()` for all services
- Register services in appropriate modules or `providedIn: 'root'`
- Keep services stateless where possible

## Routing

- Define routes in `app-routing.module.ts` or feature modules
- Use lazy loading for feature modules
- Use guards for authentication and authorization logic

## State Management

- Use `@ngrx/store`, `NgRx Signals`, or services for state management
- Minimize component state; use observables or async pipe for binding
- Use effects for side effects and API interactions

## Forms

- Prefer reactive forms for complex validations
- Use `FormGroup`, `FormControl`, and custom validators
- Avoid logic in templates; keep it in the component class

## Error Handling

- Use `HttpInterceptor` for centralized HTTP error handling
- Display user-friendly messages via toast/snackbar components
- Use try/catch or RxJS `catchError` for observable streams

## Performance

- Use `OnPush` change detection and trackBy with `*ngFor`
- Use lazy loading and preload strategies for routes
- Avoid memory leaks with proper `unsubscribe` logic
- Optimize image loading and bundle sizes

## Testing

- Use Jasmine and Karma for unit testing
- Test services, components, and pipes
- Use Angular TestBed for configuring test environments
- Use spies or mocks for service dependencies
- Maintain high coverage for core logic and shared components
