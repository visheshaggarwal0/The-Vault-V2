```markdown
# The-Vault-V2 Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill provides guidance on contributing to the The-Vault-V2 TypeScript codebase. It covers code style conventions, file organization, and common workflows such as updating image assets in the main HTML file. Whether you're adding new features, fixing bugs, or updating assets, following these patterns will help maintain consistency and quality across the project.

## Coding Conventions

### File Naming
- Use **camelCase** for file names.
  - Example: `gameLogic.ts`, `userProfile.ts`

### Import Style
- Use **relative imports** for referencing modules.
  - Example:
    ```typescript
    import { getUserData } from './userData';
    ```

### Export Style
- Use **named exports** for functions, types, and constants.
  - Example:
    ```typescript
    // In gameLogic.ts
    export function startGame() { /* ... */ }
    export const MAX_SCORE = 100;
    ```

### Commit Messages
- Freeform style, no enforced prefixes.
- Average commit message length: ~28 characters.

## Workflows

### Update Index HTML with Image Assets
**Trigger:** When someone adds or updates game images and needs them displayed on the main page.  
**Command:** `/add-image-to-index`

1. **Add or update image files** in the `images/` directory.
   - Example: Place `newGameImage.jpg` in `images/`.
2. **Edit `index.html`** to reference the new or updated images.
   - Example:
     ```html
     <img src="images/newGameImage.jpg" alt="New Game">
     ```
3. **Commit your changes** with a descriptive message.
4. **Push to the repository** and verify that the images appear correctly on the main page.

## Testing Patterns

- **Test files** follow the `*.test.*` naming pattern.
  - Example: `gameLogic.test.ts`
- **Testing framework** is not explicitly defined; check existing test files for conventions.
- Place test files alongside the modules they test or in a dedicated test directory.

## Commands

| Command               | Purpose                                                        |
|-----------------------|----------------------------------------------------------------|
| /add-image-to-index   | Synchronize image assets and update `index.html` with new images |

```