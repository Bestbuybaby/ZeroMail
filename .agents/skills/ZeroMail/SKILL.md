```markdown
# ZeroMail Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches you the core development patterns and conventions used in the ZeroMail TypeScript codebase. You'll learn how to structure files, write imports/exports, follow commit message standards, and write tests in a way that matches the project's established style.

## Coding Conventions

### File Naming
- Use **camelCase** for file names.
  - Example: `emailParser.ts`, `userSettings.ts`

### Import Style
- Use **relative imports** for modules within the project.
  - Example:
    ```typescript
    import { sendMail } from './mailer';
    import { parseEmail } from '../utils/emailParser';
    ```

### Export Style
- Use **named exports** rather than default exports.
  - Example:
    ```typescript
    // mailer.ts
    export function sendMail() { /* ... */ }
    export function queueMail() { /* ... */ }
    ```

### Commit Messages
- Follow **conventional commit** format.
- Use the `chore` prefix for maintenance commits.
- Keep commit messages concise (average 74 characters).
  - Example:
    ```
    chore: update dependencies to latest versions
    ```

## Workflows

### Making a Code Change
**Trigger:** When you need to add or update functionality.
**Command:** `/make-change`

1. Create or update files using camelCase naming.
2. Use relative imports for any internal modules.
3. Export functions or variables using named exports.
4. Write or update corresponding tests in `*.test.*` files.
5. Commit your changes using the conventional commit format (e.g., `chore: ...`).

### Running Tests
**Trigger:** Before pushing changes or verifying functionality.
**Command:** `/run-tests`

1. Locate test files matching the `*.test.*` pattern.
2. Run the test suite using the project's test runner (framework not specified; check project docs or scripts).
3. Review test results and fix any failing tests.

## Testing Patterns

- Test files are named using the `*.test.*` pattern (e.g., `mailer.test.ts`).
- The specific testing framework is not detected; refer to project documentation or look for test scripts in `package.json`.
- Place tests alongside or near the modules they test for clarity and maintainability.

## Commands
| Command        | Purpose                                      |
|----------------|----------------------------------------------|
| /make-change   | Guide for making a code change               |
| /run-tests     | Steps to run the test suite                  |
```