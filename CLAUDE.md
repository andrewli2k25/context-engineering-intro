### 🔄 Project Awareness & Context
- **Always read `PLANNING.md`** at the start of a new conversation to understand the project's architecture, goals, style, and constraints.
- **Check `TASK.md`** before starting a new task. If the task isn’t listed, add it with a brief description and today's date.
- Use consistent naming conventions, file structure, and architecture patterns as described in PLANNING.md.
- Use npm or yarn for package management and running scripts, including for tests and development builds.


### 🧱 Code Structure & Modularity
- **Never create a file longer than 500 lines of code.** If a file approaches this limit, refactor by splitting it into modules or helper files.
-Organize code into clearly separated modules, grouped by feature or responsibility. For mobile apps this looks like:
  components/ - Reusable UI components
  screens/ - Screen-level components
  hooks/ - Custom React hooks for business logic
  services/ - API calls and external service integrations
  utils/ - Helper functions and utilities
  types/ - TypeScript type definitions
  context/ - React Context providers for state management
-Use clear, consistent imports (prefer relative imports within the same feature, absolute imports for shared utilities).
-Use expo-constants and expo-secure-store for environment variables and sensitive data storage.

Follow React Native and Expo project structure conventions:
 src/
├── components/
│   ├── common/
│   └── feature-specific/
├── screens/
├── navigation/
├── services/
├── hooks/
├── utils/
├── types/
└── context/



### 🧪 Testing & Reliability
Always create Jest unit tests for new features (components, hooks, services, utils).
After updating any logic, check whether existing unit tests need to be updated. If so, do it.
**Tests should live in a **__tests__/ folder or alongside components with .test.tsx suffix.
Include at least:
1 test for expected rendering/behavior
1 edge case (empty states, loading states)
1 failure case (error handling, network failures)
Use React Native Testing Library for component testing:
 typescript
import { render, fireEvent, waitFor } from '@testing-library/react-native';


Test React hooks with @testing-library/react-hooks when needed.
Mock external dependencies (AsyncStorage, API calls, navigation) using Jest mocks.
Run tests with: npm test or yarn test


### ✅ Task Completion
- **Mark completed tasks in `TASK.md`** immediately after finishing them.
- Add new sub-tasks or TODOs discovered during development to `TASK.md` under a “Discovered During Work” section.

### 📎 Style & Conventions
Use TypeScript as the primary language for type safety.
Follow ESLint and Prettier configurations, use strict TypeScript settings.
**Use **zod or built-in TypeScript types for data validation.
Use Expo Router for navigation and AsyncStorage for local data persistence if applicable.
Follow React Native and Expo naming conventions:
Components: PascalCase (e.g., UserProfile.tsx)
Hooks: camelCase starting with use (e.g., useUserData.ts)
Utils: camelCase (e.g., formatDate.ts)
Types: PascalCase with descriptive names (e.g., UserProfileProps)
Write JSDoc comments for every function using TypeScript-friendly format:
typescript
/**
 * Brief summary of what the function does.
 *
 * @param param1 - Description of the parameter
 * @param param2 - Description of the parameter
 * @returns Description of what is returned
 *
 * @example
 * ```typescript
 * const result = exampleFunction('input', 123);
 * ```
 */
function exampleFunction(param1: string, param2: number): ReturnType {
    // Implementation
}

Use consistent React patterns:
Functional components with hooks
Custom hooks for business logic
Context for global state management
Proper TypeScript interfaces for props
Follow Expo and React Native best practices:
Use StyleSheet.create() for styles
Handle platform differences with Platform.OS
Implement proper error boundaries
Handle loading and error states in components


### 📚 Documentation & Explainability
- **Update `README.md`** when new features are added, dependencies change, or setup steps are modified.
- **Comment non-obvious code** and ensure everything is understandable to a mid-level developer.
- When writing complex logic, **add an inline `# Reason:` comment** explaining the why, not just the what.

### 🧠 AI Behavior Rules
- **Never assume missing context. Ask questions if uncertain.**
- **Never hallucinate libraries or functions** – only use known, verified Python packages.
- **Always confirm file paths and module names** exist before referencing them in code or tests.
- **Never delete or overwrite existing code** unless explicitly instructed to or if part of a task from `TASK.md`.
