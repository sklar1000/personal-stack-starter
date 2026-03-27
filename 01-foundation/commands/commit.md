---
description: Smart git commit with auto-generated message
---

Create a clean git commit.

## If I provide a message

`/commit fix: typo in README`

Use my message directly:
```bash
git add .
git commit -m "fix: typo in README"
```

## If no message provided

1. Check what changed:
```bash
git status
git diff --stat
```

2. Analyze the changes and propose a commit message:
```
[type]: [short description]

- [specific change 1]
- [specific change 2]
```

3. Ask: "Commit with this message? [Y/edit/n]"

4. On confirmation, commit.

## Commit Types

- `feat:` — new feature or content
- `fix:` — bug fix or correction
- `docs:` — documentation only
- `chore:` — maintenance, cleanup
- `refactor:` — restructuring

## Rules

- Never force push
- Warn if .env or credential files are staged
- After commit, offer to push if remote is configured
