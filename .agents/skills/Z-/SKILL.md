```markdown
# Z- Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns and conventions used in the Z- Python codebase. It covers file and code organization, commit message standards, import/export styles, and testing patterns. By following these guidelines, contributors can write consistent, maintainable, and high-quality code for the Z- project.

## Coding Conventions

### File Naming
- Use **snake_case** for all Python file names.
  - **Example:**  
    `user_profile.py`  
    `data_processor.py`

### Import Style
- Use **relative imports** within the codebase.
  - **Example:**
    ```python
    from .utils import parse_data
    from ..models import User
    ```

### Export Style
- Use **named exports** (explicitly listing exported symbols in `__all__`).
  - **Example:**
    ```python
    __all__ = ['process_data', 'UserModel']
    ```

### Commit Messages
- Follow **conventional commit** format.
- Use prefixes such as `docs` and `refactor`.
- Keep messages concise (average ~28 characters).
  - **Examples:**
    ```
    docs: update README with usage
    refactor: optimize data loading
    ```

## Workflows

### Documentation Update
**Trigger:** When updating or improving documentation  
**Command:** `/update-docs`

1. Make changes to documentation files (e.g., `README.md`).
2. Commit changes using the `docs:` prefix.
   - Example: `docs: add installation guide`
3. Push changes to the repository.

### Code Refactoring
**Trigger:** When improving code structure or readability without changing functionality  
**Command:** `/refactor-code`

1. Refactor code as needed (e.g., rename variables, reorganize functions).
2. Use relative imports and maintain snake_case file naming.
3. Commit changes using the `refactor:` prefix.
   - Example: `refactor: simplify parse logic`
4. Push changes to the repository.

## Testing Patterns

- **Framework:** Unknown (not detected in the repository)
- **Test File Pattern:** Test files use the `.test.ts` extension (suggesting some TypeScript tests may exist, or this is a placeholder).
  - **Example:** `user_profile.test.ts`
- **Note:** If adding Python tests, follow similar naming conventions (`test_*.py`) and place them in a `tests/` directory.

## Commands
| Command         | Purpose                                  |
|-----------------|------------------------------------------|
| /update-docs    | Start a documentation update workflow    |
| /refactor-code  | Begin a code refactoring workflow        |
```
