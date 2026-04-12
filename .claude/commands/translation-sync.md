---
name: translation-sync
description: Workflow command scaffold for translation-sync in ML-For-Beginners.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /translation-sync

Use this workflow when working on **translation-sync** in `ML-For-Beginners`.

## Goal

Synchronizes translations and translated images with the latest source changes.

## Common Files

- `translations/*/.co-op-translator.json`
- `translations/*/README.md`
- `translations/*/*/README.md`
- `translations/*/*/assignment.md`
- `translations/*/*/notebook.ipynb`
- `translated_images/*/*`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Update translations/<lang>/.co-op-translator.json
- Update translations/<lang>/README.md and lesson files
- Update translated_images/<lang>/* if needed
- Commit with message indicating translation sync and chunk info
- Merge pull request for translation sync

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.