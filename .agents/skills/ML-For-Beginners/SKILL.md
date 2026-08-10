```markdown
# ML-For-Beginners Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill outlines the development patterns and workflows used in the **ML-For-Beginners** repository, a TypeScript-based educational resource for learning machine learning concepts. The repository emphasizes clear code structure, consistent naming conventions, and streamlined workflows for translation synchronization and dependency management.

## Coding Conventions

### File Naming
- **PascalCase** is used for file names.
  - Example: `LinearRegression.ts`, `QuizApp.ts`

### Import Style
- **Relative imports** are used throughout the codebase.
  - Example:
    ```typescript
    import { LinearRegression } from './LinearRegression';
    ```

### Export Style
- **Named exports** are preferred.
  - Example:
    ```typescript
    export function trainModel(data: DataSet) { ... }
    export const MODEL_VERSION = '1.0.0';
    ```

### Commit Patterns
- **Conventional commits** are used, with prefixes such as `chore`.
  - Example:
    ```
    chore: update dependencies in quiz-app
    ```

## Workflows

### Sync Translations Workflow
**Trigger:** When source content changes and translations need to be updated to match.  
**Command:** `/sync-translations`

1. Update `.co-op-translator.json` for each affected language.
2. Update `README.md` files for each affected lesson in each language.
3. Update `solution/notebook.ipynb` files for each affected lesson in each language.

**Files Involved:**
- `translations/*/.co-op-translator.json`
- `translations/*/1-Introduction/4-techniques-of-ML/README.md`
- `translations/*/2-Regression/3-Linear/README.md`
- `translations/*/2-Regression/3-Linear/solution/notebook.ipynb`
- `translations/*/4-Classification/3-Classifiers-2/solution/notebook.ipynb`

**Frequency:** ~2-4x/month

#### Example
To synchronize translations after updating lesson content:
```sh
/sync-translations
```

---

### Dependency Bump Quiz-App Workflow
**Trigger:** When a new version of a dev dependency is released and dependabot or a maintainer initiates an update.  
**Command:** `/bump-dep quiz-app <package> <version>`

1. Update the dependency version in `quiz-app/package-lock.json`.
2. Commit and push the updated lockfile.

**Files Involved:**
- `quiz-app/package-lock.json`

**Frequency:** ~2x/month

#### Example
To bump the `typescript` version in the quiz-app:
```sh
/bump-dep quiz-app typescript 4.9.5
```

---

## Testing Patterns

- **Test Framework:** Unknown (not detected).
- **Test File Pattern:** Files follow the `*.test.*` naming convention.
  - Example: `LinearRegression.test.ts`
- **Test Placement:** Test files are located alongside the code they test or in dedicated test directories.

## Commands

| Command                                 | Purpose                                                    |
|------------------------------------------|------------------------------------------------------------|
| /sync-translations                       | Synchronize translation files with the latest source changes|
| /bump-dep quiz-app <package> <version>   | Bump a dev dependency in the quiz-app and update lockfile  |
```