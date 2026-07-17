```markdown
# codex-plugin-cc Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns and conventions used in the `codex-plugin-cc` TypeScript repository. It covers file organization, code style, commit practices, and testing patterns to help you contribute consistently and efficiently.

## Coding Conventions

### File Naming
- Use **kebab-case** for all file names.
  - Example:  
    ```
    user-profile.ts
    plugin-manager.test.ts
    ```

### Import Style
- Use **relative imports** for modules within the codebase.
  - Example:
    ```typescript
    import { PluginManager } from './plugin-manager';
    ```

### Export Style
- Use **named exports** for all exported entities.
  - Example:
    ```typescript
    // plugin-manager.ts
    export function initializePlugin() { ... }
    export const PLUGIN_VERSION = '1.0.0';
    ```

### Commit Messages
- Follow **conventional commit** style.
- Use the `feat` prefix for new features.
  - Example:
    ```
    feat: add plugin initialization logic
    ```

## Workflows

### Creating a New Feature
**Trigger:** When you need to add a new feature or module  
**Command:** `/new-feature`

1. Create a new file using kebab-case (e.g., `feature-name.ts`).
2. Implement the feature using TypeScript.
3. Use relative imports for any dependencies.
4. Export your functions or constants using named exports.
5. Write corresponding tests in a file named `feature-name.test.ts`.
6. Commit your changes with a conventional commit message, prefixed with `feat`.

### Writing and Running Tests
**Trigger:** When you need to ensure code correctness  
**Command:** `/run-tests`

1. Write test files alongside your modules, using the pattern `*.test.ts`.
2. Use the project's preferred (unknown) testing framework.
3. Run the test suite using the appropriate command (see project documentation or package.json).

## Testing Patterns

- Test files are named using the pattern: `*.test.ts`
- Place test files next to the modules they test.
- Testing framework is not explicitly specified; check project documentation for details.
- Example test file:
  ```typescript
  // plugin-manager.test.ts
  import { initializePlugin } from './plugin-manager';

  describe('initializePlugin', () => {
    it('should initialize plugin correctly', () => {
      expect(initializePlugin()).toBeTruthy();
    });
  });
  ```

## Commands
| Command       | Purpose                                 |
|---------------|-----------------------------------------|
| /new-feature  | Scaffold a new feature/module           |
| /run-tests    | Run all test suites                     |
```
