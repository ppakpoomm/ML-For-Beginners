```markdown
# ML-For-Beginners Development Patterns

> Auto-generated skill from repository analysis

## Overview

This skill teaches you how to contribute to the [ML-For-Beginners](https://github.com/microsoft/ML-For-Beginners) repository, which provides a beginner-friendly introduction to machine learning concepts and practical exercises. The codebase is primarily written in TypeScript (no framework detected), with a focus on clear documentation, organized lesson content, and collaborative workflows for translation, dependency management, and content improvement.

## Coding Conventions

- **File Naming:**  
  Use camelCase for filenames, e.g.:
  ```
  linearRegression.ts
  quizAppConfig.ts
  ```

- **Import Style:**  
  Use relative imports for modules:
  ```typescript
  import { calculateLoss } from './utils';
  ```

- **Export Style:**  
  Use named exports:
  ```typescript
  // In utils.ts
  export function calculateLoss(...) { ... }

  // In another file
  import { calculateLoss } from './utils';
  ```

- **Commit Message Patterns:**  
  - Use prefixes like `chore:`, `fix:`
  - Keep messages concise (average ~69 characters)
  - Example:
    ```
    fix: correct terminology in regression lesson table
    chore: bump lodash in quiz-app to 4.17.21
    ```

## Workflows

### Dependency Update (Quiz App)
**Trigger:** When a dependency in `quiz-app` has a new version available  
**Command:** `/update-dependency quiz-app`

1. Update `quiz-app/package-lock.json` with the new dependency version.
2. Commit the change with a message indicating which dependency was bumped.
3. Open and merge a pull request for the dependency update.

**Example Commit Message:**
```
chore: bump react in quiz-app to 17.0.2
```

---

### Translation Sync
**Trigger:** When source content changes or during scheduled translation sync  
**Command:** `/sync-translations`

1. Update `translations/<lang>/.co-op-translator.json` with new or changed keys.
2. Update `translations/<lang>/README.md` and lesson files to match the latest source.
3. Update `translated_images/<lang>/*` if images have changed.
4. Commit with a message indicating translation sync and chunk info.
5. Open and merge a pull request for the translation sync.

**Example Commit Message:**
```
chore: sync translations (chunk 3/5)
```

---

### Documentation Wording Improvement
**Trigger:** When improving clarity or fixing minor issues in documentation  
**Command:** `/improve-docs wording`

1. Edit the relevant `README.md` file(s) to improve wording or clarity.
2. Commit with a message referencing improved wording or clarity.
3. Open and merge a pull request for the documentation improvement.

**Example Commit Message:**
```
chore: improve wording in 1-Introduction/README.md
```

---

### Lesson Content Fix
**Trigger:** When a mistake or inconsistency is found in lesson content  
**Command:** `/fix-lesson-content`

1. Edit the affected lesson markdown files (e.g., fix terminology, table alignment).
2. Commit with a message referencing the fix.
3. Open and merge a pull request for the fix.

**Example Commit Message:**
```
fix: correct table formatting in 2-Regression/3-Linear/README.md
```

## Testing Patterns

- **Test File Naming:**  
  Test files use the pattern `*.test.*`, e.g.:
  ```
  linearRegression.test.ts
  ```

- **Framework:**  
  The specific testing framework is not detected, but standard TypeScript/Jest patterns are likely.

- **Example Test:**
  ```typescript
  // linearRegression.test.ts
  import { linearRegression } from './linearRegression';

  test('calculates correct slope', () => {
    expect(linearRegression([1, 2, 3], [2, 4, 6])).toEqual({ slope: 2, intercept: 0 });
  });
  ```

## Commands

| Command                   | Purpose                                                      |
|---------------------------|--------------------------------------------------------------|
| /update-dependency quiz-app | Update dependencies in the quiz-app subproject               |
| /sync-translations        | Synchronize translations and translated images                |
| /improve-docs wording     | Refine or clarify documentation wording                       |
| /fix-lesson-content       | Fix errors or inconsistencies in lesson content               |
```
