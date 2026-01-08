---
description: Close work session with documentation and git commit
---

## Session Shutdown

Document progress, commit changes, prepare for next session.

### Step 1: Summarize Work

```
SESSION SUMMARY
===============
Worked on: [project name]

COMPLETED:
- [Task 1]
- [Task 2]

IN PROGRESS:
- [Partial task] - [what remains]

FILES CHANGED:
- [File 1]
- [File 2]
```

### Step 2: Update Project README

For the project(s) worked on:
1. Move completed tasks to `## Done` section
2. Update `next-action` in frontmatter
3. Add notes if needed

### Step 3: Check Git Status

```bash
git status
git diff --stat
```

### Step 4: Commit Changes

Ask user to confirm, then:

```bash
git add .
git commit -m "[type]: [description]

- [what changed]
- [what changed]

Generated with Claude Code"
```

**Commit types:**
- `feat:` - new feature or content
- `fix:` - bug fix or correction
- `docs:` - documentation
- `chore:` - maintenance, cleanup

### Step 5: Next Session Handoff

```
NEXT SESSION
============
Priority: [what to focus on]
Context: [key thing to remember]

Resume with: /start-session
```

### Step 6: Offer Push

Ask: "Push to remote? (y/n)"

### Quick Version

For short sessions, just:
1. Brief summary
2. Update next-action
3. Commit
4. Done
