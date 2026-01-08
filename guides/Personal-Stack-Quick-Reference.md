---
id: personal-stack-quick-reference
type: reference
status: draft
created: 2026-01-06
updated: 2026-01-06
tags: [#personal-stack, #reference, #cheatsheet]
---

# Personal Stack Quick Reference

One-page cheat sheet for daily use.

---

## Folder Structure

```
Personal-Stack/
├── 00_Inbox/        → Quick captures (48h max)
├── 00_Operations/   → System rules
├── 01_Actions/
│   ├── Focus/       → THIS WEEK (max 2)
│   ├── Background/  → When time allows
│   └── Paused/      → Blocked/waiting
├── 02_Contexts/     → Ongoing areas
├── 03_Knowledge/    → Reference
└── 04_Archive/      → Done (date-stamp)
```

---

## 5 Essential Commands

| Command | What It Does |
|---------|--------------|
| `/start-session` | Load context, show focus |
| `/end-session` | Document, commit, close |
| `/add-task [desc]` | Add to project backlog |
| `/commit` | Smart git commit |
| `/thinking-partner` | Explore hard problems |

---

## Daily Rhythm

**Start**: `/start-session`
- See objectives
- See focus projects
- Know what to work on

**During**: `/add-task` to capture
- Don't break flow
- Route to backlog

**End**: `/end-session`
- Document progress
- Update next-action
- Commit changes

---

## Weekly Review (15 min)

- [ ] Inbox at zero?
- [ ] Focus projects (max 2) correct?
- [ ] Anything to archive?
- [ ] Next-actions current?

---

## Anti-Clutter Rules

| Rule | What It Means |
|------|---------------|
| **Inbox Zero** | Process within 48 hours |
| **Rule of 3** | 3+ items before new folder |
| **Focus Limit** | Max 2 projects in Focus |
| **Archive Fast** | Done → Archive with date |

---

## Project README Keys

```yaml
---
next-action: "THE thing to do next"
---
```

**This field is critical.** AI reads it. Keep it current.

---

## When Stuck

1. `/thinking-partner` - Explore the problem
2. Check if it's actually the right problem
3. Break it into smaller pieces
4. Pick one piece and start

---

## Key Files

| File | Location |
|------|----------|
| CLAUDE.md | Vault root |
| Objectives.md | `01_Actions/` |
| Project READMEs | `01_Actions/[status]/[project]/` |
| Governance | `00_Operations/Governance-Rules.md` |

---

## Commit Types

- `feat:` new feature/content
- `fix:` correction
- `docs:` documentation
- `chore:` maintenance

---

*The best system is the one you actually use.*
