---
name: sync-translations-workflow
description: Workflow command scaffold for sync-translations-workflow in ML-For-Beginners.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /sync-translations-workflow

Use this workflow when working on **sync-translations-workflow** in `ML-For-Beginners`.

## Goal

Keeps translation files up to date with the latest source changes across multiple languages.

## Common Files

- `translations/*/.co-op-translator.json`
- `translations/*/1-Introduction/4-techniques-of-ML/README.md`
- `translations/*/2-Regression/3-Linear/README.md`
- `translations/*/2-Regression/3-Linear/solution/notebook.ipynb`
- `translations/*/4-Classification/3-Classifiers-2/solution/notebook.ipynb`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Update .co-op-translator.json for each affected language
- Update README.md files for each affected lesson in each language
- Update solution/notebook.ipynb files for each affected lesson in each language

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.