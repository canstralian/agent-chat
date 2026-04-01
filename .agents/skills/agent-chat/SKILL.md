```markdown
# agent-chat Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill covers the core development patterns and workflows used in the `agent-chat` repository, a Python codebase built with the Flask framework. It documents the project's coding conventions, dependency update workflows, and testing patterns, providing practical examples and suggested commands to streamline contributions and maintenance.

## Coding Conventions

### File Naming
- **Style:** Snake case  
  **Example:**  
  ```
  chat_handler.py
  user_session_manager.py
  ```

### Import Style
- **Style:** Relative imports  
  **Example:**  
  ```python
  from .utils import format_message
  from ..models import ChatSession
  ```

### Export Style
- **Style:** Named exports (explicitly listing exported functions/classes)  
  **Example:**  
  ```python
  __all__ = ["ChatHandler", "UserSessionManager"]
  ```

### Commit Message Patterns
- **Type:** Freeform (no strict prefixes)
- **Average Length:** ~56 characters  
  **Example:**  
  ```
  Fix bug in chat session timeout logic
  Add support for user avatars in chat UI
  ```

## Workflows

### Dependency Update (Pip Group)
**Trigger:** When dependencies need to be updated for security, compatibility, or feature reasons across several Python submodules.  
**Command:** `/update-dependencies`

1. Identify outdated dependencies in each subproject.
2. Update the relevant dependency version in `requirements.txt` or `pyproject.toml`.
3. Repeat for each affected subproject/directory.
4. Commit all updated files together.

**Files involved:**  
- `**/requirements.txt`
- `**/pyproject.toml`

**Frequency:** ~2-3x/year

**Example:**
```bash
# Update dependencies in all subprojects
/update-dependencies
```

---

### Single Dependency Update (pyproject.toml)
**Trigger:** When a specific dependency (e.g., `llama-index`) needs to be bumped in one or more community submodules.  
**Command:** `/bump-dependency llama-index`

1. Identify the subprojects using the dependency.
2. Update the dependency version in `pyproject.toml` for each relevant subproject.
3. Commit all updated `pyproject.toml` files together.

**Files involved:**  
- `community/*/pyproject.toml`

**Frequency:** ~1x/quarter

**Example:**
```bash
# Bump llama-index in all relevant community subprojects
/bump-dependency llama-index
```

## Testing Patterns

- **Framework:** Unknown (not explicitly detected)
- **File Pattern:** Test files follow the `*.test.*` naming convention.  
  **Example:**  
  ```
  chat_handler.test.py
  utils.test.py
  ```

## Commands

| Command                    | Purpose                                                        |
|----------------------------|----------------------------------------------------------------|
| /update-dependencies       | Update all Python dependencies across subprojects               |
| /bump-dependency <package> | Bump a specific dependency (e.g., llama-index) in subprojects  |
```