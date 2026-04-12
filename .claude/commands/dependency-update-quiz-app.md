---
name: dependency-update-quiz-app
description: Workflow command scaffold for dependency-update-quiz-app in ML-For-Beginners.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /dependency-update-quiz-app

Use this workflow when working on **dependency-update-quiz-app** in `ML-For-Beginners`.

## Goal

Keeps quiz-app dependencies up to date by bumping package versions.

## Common Files

- `quiz-app/package-lock.json`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Update quiz-app/package-lock.json with new dependency version
- Commit with message indicating which dependency was bumped
- Merge pull request for the dependency update

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.