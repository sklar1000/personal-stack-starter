---
description: Close work session with documentation and commit
---

Wrap up the current session. Document what happened and commit changes.

## Steps

### 1. Summarize Work

Render this as normal markdown (headings + bullets), not inside a code block:

> ## Session summary
> **Worked on:** [project name]
>
> **Completed**
> - [What got done]
>
> **In progress**
> - [What's partially done — what remains]
>
> **Files changed**
> - [List of modified files]

### 2. Update CLAUDE.md

If tasks were completed, update the task list in CLAUDE.md:
- Mark completed items with `[x]`
- Update the "Last Updated" date

### 3. Commit Changes

```bash
git status
git diff --stat
```

Propose a commit message. Ask me to confirm. Then commit:

```bash
git add [relevant files]
git commit -m "[type]: [description]"
```

Commit types: `feat:` (new), `fix:` (correction), `docs:` (documentation), `chore:` (maintenance)

### 4. Handoff

> ## Next session
> **Priority:** [what to focus on next]
> **Context:** [key thing to remember]
> **Resume with:** `/start-session`

### 5. Offer Push

If git remote is configured, ask: "Push to remote? (y/n)"
