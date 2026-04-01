---
name: dependency-update-pip-group
description: Workflow command scaffold for dependency-update-pip-group in agent-chat.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /dependency-update-pip-group

Use this workflow when working on **dependency-update-pip-group** in `agent-chat`.

## Goal

Updates Python dependencies across multiple subprojects by modifying requirements.txt or pyproject.toml files, typically via automated tools like Dependabot.

## Common Files

- `**/requirements.txt`
- `**/pyproject.toml`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Identify outdated dependencies in each subproject.
- Update the relevant dependency version in requirements.txt or pyproject.toml.
- Repeat for each affected subproject/directory.
- Commit all updated files together.

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.