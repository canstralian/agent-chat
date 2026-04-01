---
name: single-dependency-update-pyproject-toml
description: Workflow command scaffold for single-dependency-update-pyproject-toml in agent-chat.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /single-dependency-update-pyproject-toml

Use this workflow when working on **single-dependency-update-pyproject-toml** in `agent-chat`.

## Goal

Updates a single dependency (such as aiohttp or llama-index) in one or more community subprojects by changing the pyproject.toml file(s).

## Common Files

- `community/*/pyproject.toml`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Identify the subprojects using the dependency.
- Update the dependency version in pyproject.toml for each relevant subproject.
- Commit all updated pyproject.toml files together.

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.