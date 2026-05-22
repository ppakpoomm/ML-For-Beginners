---
name: dependency-bump-quiz-app-workflow
description: Workflow command scaffold for dependency-bump-quiz-app-workflow in ML-For-Beginners.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /dependency-bump-quiz-app-workflow

Use this workflow when working on **dependency-bump-quiz-app-workflow** in `ML-For-Beginners`.

## Goal

Updates a development dependency in the quiz-app by bumping its version and updating the lockfile.

## Common Files

- `quiz-app/package-lock.json`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Update the dependency version in quiz-app/package-lock.json
- Commit and push the updated lockfile

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.