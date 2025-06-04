---
applyTo: "**/.ts, **/.js"
---

# React Native Copilot Instructions

Apply the [JavaScript Coding Standards](./js.md) to all code.
Apply the [TypeScript Coding Standards](./ts.md) to all code.

## General Standards

- Use TypeScript for new components and features
- Prefer functional components with React hooks
- Structure code for cross-platform compatibility (iOS and Android)
- Ensure app performance and responsiveness

## Project Setup

- Initialize projects using `npx react-native init` or `expo init`
- Clearly define scripts in `package.json` for common workflows
- Organize dependencies explicitly and group by purpose

## Folder Structure

```
project_root/
├── src/
│   ├── components/
│   ├── screens/
│   ├── navigation/
│   ├── hooks/
│   ├── context/
│   ├── services/
│   ├── assets/
│   │   ├── images/
│   │   ├── fonts/
│   └── utils/
├── App.tsx
├── package.json
└── tsconfig.json
```

## Component Practices

- Use `React.FC` for components with children
- Decompose large components into smaller reusable ones
- Use props and hooks to manage component logic
- Keep components pure and stateless where possible

## Navigation

- Use `@react-navigation/native` for navigation
- Define navigation stacks and tab navigators in the `navigation/` folder
- Type navigation props using `@react-navigation/native-stack`

## State Management

- Prefer Context API or lightweight libraries (e.g., Zustand, Jotai)
- Use Redux Toolkit for complex state requirements
- Keep global state minimal; prefer local state where possible

## Styling

- Use `StyleSheet.create()` for consistent and performant styles
- Organize common styles in a `theme/` or `styles/` file
- Use responsive units (`Dimensions`, `%`, `flex`) for layout
- Support dark mode via appearance detection or theming

## Asset Management

- Store images, fonts, and static assets in `assets/`
- Use `require()` or `import` to load assets
- Optimize assets for app size and performance

## Error Handling

- Wrap screens/components with error boundaries
- Use `try/catch` blocks for async operations
- Display user-friendly error messages (e.g., toasts, modals)

## Networking

- Use `axios`, `fetch`, or `react-query` for API calls
- Abstract networking logic into reusable services
- Handle loading, success, and error states explicitly

## Testing

- Use `Jest` for unit testing
- Use `React Native Testing Library` for component tests
- Mock native modules and navigation as needed

## Performance

- Use `useMemo`, `useCallback`, and `React.memo` to prevent unnecessary re-renders
- Profile app with Flipper or built-in React Native tools
- Use FlatList or SectionList for large datasets

## Native Modules

- Use community packages when available (e.g., `react-native-fs`, `react-native-device-info`)
- Bridge native code only when necessary
- Document native setup steps for iOS (Xcode) and Android (Gradle)

## Deployment

- Use EAS Build (Expo) or fastlane for automated CI/CD
- Sign apps with appropriate iOS/Android certificates
- Release apps through App Store and Google Play

## Security

- Store tokens securely with `react-native-keychain` or SecureStore
- Validate and sanitize all external data
- Avoid storing sensitive info in async storage

## Accessibility

- Use accessible components (`TouchableOpacity`, `Text`, etc.) with accessibility props
- Test with VoiceOver and TalkBack
- Support dynamic font sizes and contrast
