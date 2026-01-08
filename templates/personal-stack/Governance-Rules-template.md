---
type: governance
updated: [DATE]
---

# Governance Rules

Rules that keep the system healthy. Without governance, systems decay.

---

## Anti-Clutter Rules

### 1. Inbox Zero (48 hours)

Everything in `00_Inbox/` gets processed within 48 hours:
- Route to correct folder, OR
- Delete if not needed

**If it's been in Inbox >48 hours, it's clutter.**

Processing options:
- Active project? → `01_Actions/[project]/`
- Ongoing responsibility? → `02_Contexts/`
- Reference material? → `03_Knowledge/`
- Not needed? → Delete

### 2. Rule of 3

Only create a new folder in `03_Knowledge/` when you have **3+ items** on that topic.

Until then, keep items in `03_Knowledge/_Unsorted/`

This prevents folder sprawl and premature organization.

### 3. Focus Limit (Max 2)

Maximum **2 projects** in `01_Actions/Focus/` at any time.

If you want to add a third:
- Move something to Background, OR
- Move something to Paused, OR
- Archive something that's done

**The limit is real. Respect it.**

### 4. Archive Aggressively

When a project is done, move it to Archive with a date prefix:
```
04_Archive/2026-01-Project-Name/
```

Don't keep "finished" projects in Actions. They create noise.

---

## Review Rhythms

### Daily (2 min)
- [ ] Anything in Inbox? Process or note for later.
- [ ] What's my Focus project next-action?

### Weekly (15 min) - Pick a day

- [ ] Inbox at zero?
- [ ] Focus projects (max 2) still the right priorities?
- [ ] Any Background project ready for Focus?
- [ ] Any completed projects to archive?
- [ ] Update `next-action` fields if stale

### Monthly (30 min) - First week

- [ ] Review `Objectives.md` - still accurate?
- [ ] Check `03_Knowledge/_Unsorted/` - anything to organize (Rule of 3)?
- [ ] Any objectives completed or stale?
- [ ] Archive anything that's been done >2 weeks

---

## File Naming

- Use `Title-Case-With-Hyphens.md`
- No spaces in filenames
- Date prefix when relevant: `2026-01-06-Meeting-Notes.md`
- Archive folders: `YYYY-MM-Project-Name/`

---

## What Claude Should Do

### Enforce
- Warn if Focus has >2 projects
- Route captures to Inbox (not random folders)
- Suggest archiving completed projects
- Read `next-action` from project READMEs

### Avoid
- Creating new top-level folders without asking
- Searching Inbox for reference (use Knowledge/Contexts)
- Adding tasks directly to Active (use Backlog first)

---

## System Health Indicators

**Healthy:**
- Inbox empty or <5 items
- 1-2 Focus projects
- `next-action` fields current
- Weekly review happening

**Unhealthy:**
- Inbox >10 items or >48h old
- 3+ Focus projects
- Stale `next-action` fields
- No review in 2+ weeks

---

*These rules exist because systems decay without maintenance. Governance prevents decay.*
