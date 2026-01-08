---
description: Add task to project backlog
---

## Add Task to Backlog

Capture a task without executing it.

### When User Runs `/add-task [description]`

#### 1. Identify the Project

Look for keywords in the task description:
- If task mentions a known project name → use that project
- If unclear → ask which project

#### 2. Confirm

```
Detected: [Project Name]
Add to backlog? [Y/n/other project]
```

#### 3. Add to Project README

Open `01_Actions/[Focus|Background]/[Project]/README.md`

Find the `## Backlog` section

Append:
```markdown
- [ ] [task description] (added [DATE])
```

Get date with:
```bash
date +%Y-%m-%d
```

#### 4. Confirm

```
Added to [Project] backlog:
- [ ] [task description] (added 2026-01-06)

Location: Focus/[Project]/README.md
```

### Important

**DO NOT execute the task.** Only add it to the backlog file.

The task gets done later when pulled into Active.

### Examples

```
/add-task Review weekly metrics
→ Ask: "Which project?"
→ User: "Marketing"
→ Add to Marketing/README.md → Backlog
```

```
/add-task [Website] Fix mobile nav
→ Detect: Website project
→ Confirm: "Detected: Website. Add to backlog? [Y/n]"
→ Add to Website/README.md → Backlog
```

### If No Backlog Section

Create it before the final `---`:

```markdown
## Backlog

- [ ] [new task] (added [DATE])

---
```
