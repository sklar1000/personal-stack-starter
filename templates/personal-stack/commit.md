---
description: Smart git commit with auto-generated messages
---

## Commit

Create clean, consistent git commits.

### If User Provides Message

`/commit fix: typo in README`

Use their message directly:
```bash
git add .
git commit -m "fix: typo in README"
```

### If No Message Provided

`/commit`

#### 1. Check Status

```bash
git status
git diff --stat
```

#### 2. Analyze Changes

- What files changed?
- What type of change is this?

#### 3. Generate Message

Propose a commit message:

```
[type]: [short description]

- [specific change 1]
- [specific change 2]

Generated with Claude Code
```

Ask: "Commit with this message? [Y/edit/n]"

#### 4. Commit

```bash
git add .
git commit -m "$(cat <<'EOF'
[message here]
EOF
)"
```

#### 5. Confirm

```
Committed: [hash] [first line of message]
[N files changed]

Push to remote? (y/n)
```

### Commit Types

- `feat:` - new feature or content
- `fix:` - bug fix or correction
- `docs:` - documentation only
- `refactor:` - restructuring without behavior change
- `chore:` - maintenance, cleanup
- `style:` - formatting only

### Rules

- Never force push (`git push --force`)
- Never skip hooks (`--no-verify`)
- Warn if .env or credentials files are staged
- Match recent commit style in the repo

### Shortcuts

- `/commit wip` → "wip: work in progress"
- `/commit fix: [desc]` → Uses message directly
- `/commit` → Full analysis
