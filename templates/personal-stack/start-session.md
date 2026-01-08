---
description: Begin work session with context loading
---

## Session Startup

Load context and show what to work on.

### Step 1: Get Date

```bash
date "+%A, %B %d, %Y"
```

### Step 2: Load Context

Read these files:
1. `01_Actions/Objectives.md` - Quarterly goals
2. `01_Actions/Focus/*/README.md` - Each Focus project (read `next-action` from frontmatter)
3. `01_Actions/Background/*/README.md` - Just the `next-action` field
4. Recent git commits

```bash
git log --oneline -3
```

### Step 3: Output Format

```
SESSION READY
=============
[Day], [Month] [Date], [Year]

OBJECTIVES:
1. [Objective 1]
2. [Objective 2]

FOCUS (this week):
  [Project 1]
  → Next: [next-action from frontmatter]

  [Project 2]
  → Next: [next-action from frontmatter]

BACKGROUND (when time):
  [Project] → [next-action]
  [Project] → [next-action]

RECENT:
  [commit 1]
  [commit 2]
  [commit 3]

---
What's the focus today?
```

### When to Use

- Start of work session
- After a break
- When you need to remember context

### After Startup

Common follow-ups:
- "Let's work on [project]"
- "Show me [project] details"
- "Add task: [description]"
