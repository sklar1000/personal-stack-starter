# Tier 2: Workflow

**You're ready for this when...**

- You've run 10+ sessions and the rhythm feels natural
- You're losing track of tasks across sessions
- You wish Claude remembered what happened last time
- You have more than a handful of files and want organization
- You're ready to add a second project

If none of these are true yet, go back to using your foundation. Come back when they are.

---

## What Tier 2 Adds

| Capability | What It Does | Why It Matters |
|---|---|---|
| **Folder structure** | Organize files by what you DO with them | Stop losing things |
| **Project README** | Track tasks, decisions, and progress per project | Projects don't stall |
| **Governance rules** | Focus limits, inbox processing, archive triggers | System stays clean |
| **Frontmatter** | Metadata on files (type, date, version) | Files become searchable and sortable |
| **Session continuity** | Start/end sessions create a handoff trail | Never lose context between sessions |

---

## Step 1: Add Folder Structure (10 min)

Evolve your flat folder into an organized stack. Create these folders:

```bash
mkdir -p 00_Inbox 01_Projects 02_Reference 03_Archive
```

| Folder | What Goes Here | Rule |
|---|---|---|
| `00_Inbox/` | Quick captures, raw thoughts, voice memos | Process within 48 hours |
| `01_Projects/` | Active work, each project gets a subfolder | Max 3 active at a time |
| `02_Reference/` | Frameworks, templates, knowledge you reuse | Stuff you look up, not act on |
| `03_Archive/` | Completed or paused work | Date-prefix: `2026-03-Project-Name/` |

**Move your existing files** into the right folders. Don't reorganize everything — just the obvious ones. Claude can help: "Help me sort my files into the new folder structure."

Update your CLAUDE.md to document the new structure.

---

## Step 2: Add Project READMEs (10 min)

For each active project, create a `README.md` inside its folder:

```
01_Projects/
  my-project/
    README.md
    [other project files]
```

Project README template:

```markdown
# [Project Name]

**Why**: [One sentence — why does this project exist?]
**Done when**: [What does completion look like?]

---

## Active

- [ ] [Current task 1]
- [ ] [Current task 2]

## Backlog

- [ ] [Future task]

## Done

- [x] [Completed task] (2026-03-26)

## Notes

### Key Decisions
- [Decision]: [Why]

### Session Log
#### [DATE]
- Worked on: [what]
- Next: [what's next]
```

---

## Step 3: Add Governance Rules (5 min)

Add these rules to your CLAUDE.md (or create a separate `00_System/Governance-Rules.md`):

```markdown
## Governance

### Focus Limit
Max 3 active projects in 01_Projects/ at any time.
Adding a fourth means archiving or pausing one.

### Inbox Zero
Everything in 00_Inbox/ gets processed within 48 hours.
Process = move to the right folder or delete.

### Archive Aggressively
Done? Move to 03_Archive/YYYY-MM-Project-Name/.
Don't keep finished projects in 01_Projects/.
```

---

## Step 4: Add Frontmatter (5 min)

Start adding metadata to the top of important files:

```markdown
---
type: project
created: 2026-03-26
updated: 2026-03-26
---

# File Title

Content here...
```

You don't need to add frontmatter to every file. Start with project READMEs and anything you want to find later. Claude can help: "Add frontmatter to my project files."

---

## Step 5: Update Your CLAUDE.md (5 min)

Your CLAUDE.md should now reflect:
- The new folder structure
- Links to active project READMEs
- Governance rules
- Any new commands you've added

This is the most important file in your stack. Keep it current.

---

## What You Have Now

- **Organized files** — everything has a home based on what you DO with it
- **Project tracking** — tasks, decisions, and session logs per project
- **Governance** — focus limits and inbox processing keep it clean
- **Frontmatter** — files carry their own metadata
- **Session continuity** — `/start-session` and `/end-session` create handoff between sessions

---

## When You're Ready for More

→ [Tier 3: System](../03-system/UPGRADE.md) — When you're juggling 3+ projects and want automation, identity layers, and knowledge architecture.
