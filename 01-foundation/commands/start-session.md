---
description: Begin work session with context loading
---

Load my context and show what to work on.

## Steps

1. Get today's date
2. Read `CLAUDE.md` for objectives and project context
3. Find any project README files and read their current tasks
4. Check recent git commits (if git is initialized)

```bash
git log --oneline -3 2>/dev/null || echo "No git history yet"
```

## Output Format

Render this as normal markdown, not inside a code block:

> ## Session ready — [Day], [Date]
>
> **Working on:** [Project Name]
> → Next: [most important task from CLAUDE.md or project README]
>
> **Recent:** [last 3 commits, if any]
>
> ---
> What's the focus today?

## After Startup

Wait for my response, then help me work on whatever I choose.
