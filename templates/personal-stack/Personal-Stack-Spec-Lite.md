# Personal Stack Spec (Lite)

Technical reference for how the system works. Keep this in `00_Operations/`.

---

## The Six Layers

| Layer | Folder | Purpose | Retention |
|-------|--------|---------|-----------|
| **Inbox** | `00_Inbox/` | Quick captures | 48h max |
| **Operations** | `00_Operations/` | System rules, templates | Permanent |
| **Actions** | `01_Actions/` | Projects with deadlines | Until done |
| **Contexts** | `02_Contexts/` | Ongoing roles, areas | Long-lived |
| **Knowledge** | `03_Knowledge/` | Reference, frameworks | Permanent |
| **Archive** | `04_Archive/` | Completed work | Cold storage |

---

## Layer Rules (Invariants)

### 00_Inbox
- **Purpose**: Temporary landing zone
- **Rule**: Process within 48 hours
- **Never**: Search here for reference
- **Never**: Let items age past 48h

### 00_Operations
- **Purpose**: How the system works
- **Contains**: CLAUDE.md, specs, templates, protocols
- **Rule**: AI reads this to understand system rules

### 01_Actions
- **Purpose**: Time-bound work with deadlines
- **Structure**:
  ```
  01_Actions/
  ├── Focus/      # This week (MAX 2)
  ├── Background/ # When time allows
  ├── Paused/     # Blocked, known resume trigger
  └── Objectives.md
  ```
- **Rule**: Max 2 projects in Focus at any time
- **Rule**: Every project has README with `next-action` field

### 02_Contexts
- **Purpose**: Ongoing responsibilities (not projects)
- **Examples**: Teaching, Clients, Writing, Health
- **Rule**: Changes slowly—if it has a deadline, it's a project

### 03_Knowledge
- **Purpose**: Reference material that compounds
- **Structure**:
  ```
  03_Knowledge/
  ├── [Domain]-Canon/  # Governed knowledge (advanced)
  ├── Topics/          # General reference
  └── _Unsorted/       # New items (Rule of 3)
  ```
- **Rule of 3**: Only create topic folder when you have 3+ items

### 04_Archive
- **Purpose**: Completed projects, cold storage
- **Format**: `04_Archive/YYYY-MM-Project-Name/`
- **Rule**: Date-stamp when archiving
- **Rule**: Don't assume archived content is current

---

## Routing Decision Tree

When processing Inbox, ask:

```
Is this temporary or durable?
├─ Temporary → Delete or complete now
└─ Durable → Continue...

Does it have a deadline?
├─ Yes → 01_Actions/[project]/
└─ No → Continue...

Is it an ongoing responsibility?
├─ Yes → 02_Contexts/[area]/
└─ No → Continue...

Is it reference/knowledge?
├─ Yes → 03_Knowledge/ (Topics/_Unsorted first)
└─ No → Delete or rethink
```

---

## Project README Standard

Every project in `01_Actions/` needs a README.md:

```yaml
---
type: project
next-action: "THE one thing to do next"
created: YYYY-MM-DD
updated: YYYY-MM-DD
---

# Project Name

**Why**: [One sentence]
**Done when**: [Completion criteria]

## Active
- [ ] Current task 1
- [ ] Current task 2

## Backlog
- [ ] Future task

## Done
- [x] Completed task (date)
```

**Critical field**: `next-action` — AI reads this to know what to surface.

---

## Anti-Clutter Rules

| Rule | What It Means |
|------|---------------|
| **Inbox Zero** | Nothing in Inbox older than 48h |
| **Rule of 3** | 3+ items before creating a folder |
| **Focus Limit** | Max 2 projects in Focus |
| **Archive Fast** | Done → Archive with date |

---

## AI Integration Points

### CLAUDE.md (vault root)
AI reads this for:
- Who you are
- Your objectives
- Vault structure
- Rules to follow

### Project READMEs
AI reads `next-action` field to know priorities.

### Commands (`.claude/commands/`)
Slash commands that automate workflows:
- `/start-session` — Load context
- `/end-session` — Document and commit
- `/add-task` — Capture to backlog

---

## File Naming

- **Standard**: `Title-Case-With-Hyphens.md`
- **No spaces**: Use hyphens
- **Dates when relevant**: `YYYY-MM-DD-Name.md`
- **Archive folders**: `YYYY-MM-Project-Name/`

---

## What AI Should Enforce

**Do**:
- Read `next-action` from project READMEs
- Warn if Focus has >2 projects
- Route captures to Inbox
- Suggest archiving completed projects

**Don't**:
- Create top-level folders without asking
- Search Inbox for reference
- Execute tasks from `/add-task` (only add them)

---

*This spec defines how the system works. Respect the invariants.*
