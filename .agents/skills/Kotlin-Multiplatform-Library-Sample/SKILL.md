```markdown
# Kotlin-Multiplatform-Library-Sample Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches best practices for contributing to the `Kotlin-Multiplatform-Library-Sample` repository, a TypeScript codebase with a focus on modular, maintainable code. You'll learn the project's coding conventions, commit patterns, file organization, and how to write and run tests. While no automated workflows are detected, this guide suggests command patterns for common tasks.

## Coding Conventions

### File Naming
- Use **camelCase** for file names.
  - Example: `myLibraryModule.ts`

### Import Style
- Use **relative imports** for modules within the project.
  - Example:
    ```typescript
    import { myFunction } from './utils';
    ```

### Export Style
- Use **named exports** to expose functions, types, or constants.
  - Example:
    ```typescript
    export function myFunction() { ... }
    export const MY_CONSTANT = 42;
    ```

### Commit Messages
- Follow **conventional commit** style.
- Use the `chore` prefix for maintenance commits.
  - Example: `chore: update dependencies`

## Workflows

### Code Contribution
**Trigger:** When adding new features or fixing bugs  
**Command:** `/contribute`

1. Create a new branch for your changes.
2. Write code following the coding conventions above.
3. Add or update tests as needed.
4. Commit changes using the conventional commit format.
5. Open a pull request for review.

### Dependency Maintenance
**Trigger:** When updating project dependencies  
**Command:** `/update-deps`

1. Update dependencies in the relevant configuration files.
2. Test the project to ensure compatibility.
3. Commit with a message like `chore: update dependencies`.
4. Push changes and open a pull request.

## Testing Patterns

- Test files follow the `*.test.*` naming pattern.
  - Example: `myLibraryModule.test.ts`
- The specific testing framework is not detected; refer to existing test files for structure.
- Place test files alongside or near the modules they test.

**Example Test File:**
```typescript
// myLibraryModule.test.ts
import { myFunction } from './myLibraryModule';

describe('myFunction', () => {
  it('should return expected result', () => {
    expect(myFunction()).toBe('expected');
  });
});
```

## Commands
| Command         | Purpose                                 |
|-----------------|-----------------------------------------|
| /contribute     | Start the code contribution workflow     |
| /update-deps    | Update dependencies and test changes     |
```
