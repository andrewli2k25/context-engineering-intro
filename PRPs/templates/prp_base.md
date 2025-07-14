name: "Base PRP Template v2 - Context-Rich with Validation Loops"
description: |

## Purpose
Template optimized for AI agents to implement features with sufficient context and self-validation capabilities to achieve working code through iterative refinement.

## Core Principles
1. **Context is King**: Include ALL necessary documentation, examples, and caveats
2. **Validation Loops**: Provide executable tests/lints the AI can run and fix
3. **Information Dense**: Use keywords and patterns from the codebase
4. **Progressive Success**: Start simple, validate, then enhance
5. **Global rules**: Be sure to follow all rules in CLAUDE.md

---

## Goal
[What needs to be built - be specific about the end state and desires]

## Why
- [Business value and user impact]
- [Integration with existing features]
- [Problems this solves and for whom]

## What
[User-visible behavior and technical requirements]

### Success Criteria
- [ ] [Specific measurable outcomes]

## All Needed Context

### Documentation & References (list all context needed to implement the feature)
```yaml
# MUST READ - Include these in your context window
  - url: [Expo API docs URL]
  why: [Specific modules/methods you'll need]
  
- doc: [React Native documentation URL] 
  section: [Specific section about common pitfalls]
  why: [Key insight that prevents common errors]
  
- docfile: [PRPs/ai_docs/file.md]
  why: [docs that the user has pasted in to the project]

- expo: [Expo SDK documentation URL]
  why: [Specific module like Camera, Location, etc.]

- native: [Platform-specific considerations]
  why: [iOS-specific requirements]

```

### Current Codebase tree (run `tree` in the root of the project) to get an overview of the codebase
```bash

```

### Desired Codebase tree with files to be added and responsibility of file
```bash

```

### Known Gotchas of our codebase & Library Quirks
```javascript
# Example: Expo requires expo install for compatible versions
# Example: React Navigation requires specific stack setup
# Example: AsyncStorage has size limits and requires error handling
# Example: iOS requires specific permissions in app.json/app.config.js
# Example: Expo Go has limitations compared to development builds

```

## Implementation Blueprint

### Data models and structure

Create the core data models, we ensure type safety and consistency.
```javascript
Examples: 
  - State management schemas (Redux/Context)
 - API response types
 - Component prop types
 - Navigation param types
 - AsyncStorage data structures

```

### list of tasks to be completed to fullfill the PRP in the order they should be completed

```yaml
Task 1:
MODIFY src/navigation/AppNavigator.js:
  - FIND pattern: "const Stack = createStackNavigator()"
  - INJECT after existing screen definitions
  - PRESERVE existing navigation structure

CREATE src/screens/FeatureScreen.js:
  - MIRROR pattern from: src/screens/SimilarScreen.js
  - MODIFY component name and core logic
  - KEEP error handling pattern identical

...(...)

Task N:
...

```


### Per task pseudocode as needed added to each task
```python

// Task 1
// Pseudocode with CRITICAL details dont write entire code
const FeatureScreen = () => {
    // PATTERN: Always use custom hooks for complex logic (see src/hooks/)
    const { data, loading, error } = useFeature();
    
    // GOTCHA: Expo permissions must be requested before use
    const requestPermission = async () => {
        const { status } = await Location.requestForegroundPermissionsAsync();
        if (status !== 'granted') {
            // PATTERN: Use existing alert pattern
            showAlert('Permission denied');
            return;
        }
    };
    
    // PATTERN: Use existing loading/error states
    if (loading) return <LoadingSpinner />;
    if (error) return <ErrorMessage error={error} />;
    
    // CRITICAL: Always handle navigation params safely
    const handleNavigation = () => {
        navigation.navigate('NextScreen', { 
            param: data?.id || null // safe navigation
        });
    };
    
    return (
        <SafeAreaView style={styles.container}>
            {/* Component JSX */}
        </SafeAreaView>
    );
};
```

### Integration Points
```yaml
NAVIGATION:
  - add to: src/navigation/AppNavigator.js
  - pattern: "Stack.Screen name='Feature' component={FeatureScreen}"
  
STATE_MANAGEMENT:
  - add to: src/store/reducers/index.js (if Redux)
  - pattern: "combineReducers({ feature: featureReducer })"
  
PERMISSIONS:
  - add to: app.json
  - pattern: "permissions: ['android.permission.CAMERA']"
  
DEPENDENCIES:
  - add to: package.json
  - pattern: "expo install expo-camera expo-location"
```

## Validation Loop

### Level 1: Syntax & Style
```bash
# Run these FIRST - fix any errors before proceeding
npm run lint                     # ESLint checking
npm run type-check              # TypeScript checking (if used)
npx expo install --fix          # Fix dependency issues

# Expected: No errors. If errors, READ the error and fix.
```

### Level 2: Unit Tests each new feature/file/function use existing test patterns
```python
// CREATE __tests__/FeatureScreen.test.js with these test cases:
import { render, fireEvent } from '@testing-library/react-native';
import FeatureScreen from '../FeatureScreen';

describe('FeatureScreen', () => {
    test('renders correctly', () => {
        const { getByText } = render(<FeatureScreen />);
        expect(getByText('Feature Title')).toBeTruthy();
    });

    test('handles button press', () => {
        const { getByTestId } = render(<FeatureScreen />);
        fireEvent.press(getByTestId('feature-button'));
        // Assert expected behavior
    });

    test('displays loading state', () => {
        // Mock loading state
        const { getByTestId } = render(<FeatureScreen />);
        expect(getByTestId('loading-spinner')).toBeTruthy();
    });

    test('handles error state', () => {
        // Mock error state
        const { getByText } = render(<FeatureScreen />);
        expect(getByText('Error message')).toBeTruthy();
    });
});

```bash
# Run and iterate until passing:
npm test -- FeatureScreen.test.js
# If failing: Read error, understand root cause, fix code, re-run
```


## Final validation Checklist
- [ ] All tests pass: npm test
- [ ] No linting errors: npm run lint
- [ ] No type errors: npm run type-check
- [ ] Navigation flows work
- [ ] Permissions work successfully
- [ ] Error cases handled gracefully

---

## Anti-Patterns to Avoid
- ❌ Don't create new patterns when existing ones work
- ❌ Don't skip validation because "it should work"  
- ❌ Don't ignore failing tests - fix them    
- ❌ Don't use sync functions in async context
- ❌ Don't hardcode values that should be config
- ❌ Don't catch all exceptions - be specific
- ❌ Don't use React Native APIs directly when Expo equivalents exist
- ❌ Don't skip permission requests for sensitive features
- ❌ Don't ignore platform-specific differences (iOS vs Android)
- ❌ Don't use deprecated navigation patterns
- ❌ Don't hardcode dimensions - use responsive design
- ❌ Don't forget to handle offline states
- ❌ Don't use synchronous storage operations
- ❌ Don't ignore accessibility requirements
- ❌ Don't skip testing on both platforms
- ❌ Don't use console.log in production code
