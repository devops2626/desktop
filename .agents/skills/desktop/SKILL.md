```markdown
# desktop Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches you the core development patterns and conventions used in the `desktop` TypeScript codebase. You'll learn about file naming, import/export styles, commit patterns, and how to write and run tests. While no specific frameworks or automated workflows were detected, this guide will help you maintain consistency and quality in your contributions.

## Coding Conventions

### File Naming
- Use **camelCase** for file names.
  - Example: `userProfile.ts`, `mainWindow.test.ts`

### Import Style
- Use **relative imports** for modules.
  - Example:
    ```typescript
    import { fetchData } from './apiUtils';
    ```

### Export Style
- Use **named exports** for functions, constants, and classes.
  - Example:
    ```typescript
    // In userProfile.ts
    export function getUserProfile(id: string) { ... }
    export const DEFAULT_AVATAR = 'default.png';
    ```

### Commit Patterns
- Commit messages are **freeform** and typically around 63 characters.
- No strict prefixing, but keep messages concise and descriptive.
  - Example:  
    ```
    Fix window resize issue on macOS
    ```

## Workflows

### Adding a New Module
**Trigger:** When you need to add a new feature or utility.
**Command:** `/add-module`

1. Create a new file using camelCase, e.g., `featureName.ts`.
2. Implement your logic using named exports.
3. Use relative imports to include dependencies.
4. Write corresponding tests in a file named `featureName.test.ts`.
5. Commit your changes with a clear, concise message.

### Writing and Running Tests
**Trigger:** When you add or update code that requires testing.
**Command:** `/run-tests`

1. Create a test file with the pattern `*.test.ts` (e.g., `apiUtils.test.ts`).
2. Write your tests using the project's preferred (unknown) testing framework.
3. Run tests using the project's test runner (check project docs or package.json for scripts).
4. Ensure all tests pass before committing.

## Testing Patterns

- Test files follow the `*.test.*` naming pattern.
  - Example: `mainWindow.test.ts`
- The specific testing framework is not detected; check project documentation or `package.json` for details.
- Place tests alongside or near the modules they test.
- Example test file structure:
  ```typescript
  // mainWindow.test.ts
  import { openMainWindow } from './mainWindow';

  describe('openMainWindow', () => {
    it('should open the main window', () => {
      // test implementation
    });
  });
  ```

## Commands
| Command      | Purpose                                   |
|--------------|-------------------------------------------|
| /add-module  | Scaffold a new module with tests          |
| /run-tests   | Run all test suites in the codebase       |
```
