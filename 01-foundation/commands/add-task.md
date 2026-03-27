---
description: Add task to backlog without executing it
---

Capture a task. Don't execute it.

## When I say `/add-task [description]`

1. Find the right place to add it (CLAUDE.md task list, or a project README if one exists)
2. Confirm: "Add to [location]? [Y/n]"
3. Append to the task list:
```markdown
- [ ] [task description] (added [DATE])
```

## Important

**DO NOT execute the task.** Only record it.

The task gets done later when I'm ready to work on it.

## Examples

```
/add-task Write the project proposal
→ Added to CLAUDE.md tasks:
  - [ ] Write the project proposal (added 2026-03-26)
```
