---
id: personal-stack-builders-guide
type: guide
status: draft
created: 2026-01-06
updated: 2026-01-06
objective: pc-business
related:
  - "[[Personal-Stack-Essay]]"
  - "[[Personal-Stack-One-Pager]]"
tags: [#writing, #personal-stack, #guide, #tutorial]
---

# Build Your Own Personal Stack

A 4-week guide to building an AI-native productivity system using Obsidian, Claude Code, and Git.

---

## Who This Is For

You're a knowledge worker—writing, teaching, consulting, building things. You've tried productivity systems before. They worked for a few months, then decayed. You want something that sticks.

This guide walks you through building a Personal Stack: a system where AI knows your context, your goals, and your projects. Not a chatbot you paste things into. A partner that can actually read and write to your files.

**Prerequisites:**
- Basic comfort with command line (or willingness to learn)
- Obsidian (free) installed
- Claude Code (requires Claude subscription)
- Git installed (for backup and history)

**Time commitment:** ~3-5 hours per week for 4 weeks

---

## The Four Phases

| Week | Focus | Outcome |
|------|-------|---------|
| 1 | Foundation | Folder structure + first Objectives file + git backup |
| 2 | AI Integration | CLAUDE.md + start-session + end-session commands |
| 3 | Workflow Commands | add-task, commit, thinking-partner |
| 4 | Governance | Anti-clutter rules + review rhythms |

After week 4, you'll have a functional system. It won't be fancy—it'll be usable. Fancy comes from patterns, and patterns emerge from use.

---

# Phase 1: Foundation (Week 1)

**Goal**: Create the folder structure, your first objectives file, and git backup.

## Step 1.1: Create Your Vault

1. Open Obsidian
2. Create new vault: `Personal-Stack` (or whatever name you want)
3. Choose a location you can access from terminal (avoid iCloud if possible for git)

## Step 1.2: Create the Folder Structure

Create these 6 folders inside your vault:

```
Personal-Stack/
├── 00_Inbox/           # Quick captures (process within 48 hours)
├── 00_Operations/      # System rules, templates, protocols
├── 01_Actions/         # Projects with deadlines
│   ├── Focus/          # This week's work (MAX 2 projects)
│   ├── Background/     # Touch when time/energy allows
│   └── Paused/         # Blocked or waiting
├── 02_Contexts/        # Ongoing roles, areas, people
├── 03_Knowledge/       # Reference material, frameworks
└── 04_Archive/         # Completed projects, cold storage
```

**Why this structure:**
- **Inbox**: Capture fast, route later. Never search here.
- **Operations**: How the system works. AI reads this.
- **Actions**: Projects with deadlines. Move between Focus/Background/Paused.
- **Contexts**: Ongoing responsibilities (not projects). Teaching, clients, etc.
- **Knowledge**: Reference that compounds. Your frameworks, notes, resources.
- **Archive**: Done projects. Date-stamp when archiving: `2026-01-Project-Name/`

## Step 1.3: Create Your First Objectives File

Create `01_Actions/Objectives.md`:

```markdown
---
type: objectives
updated: 2026-01-06
---

# Objectives

What you're building toward this quarter.

---

## Active Objectives (Max 3)

### 1. [Your First Objective]
- **Why**: [Why this matters]
- **Success looks like**: [Concrete outcome]
- **Projects**: [List related projects]

### 2. [Your Second Objective]
- **Why**: [Why this matters]
- **Success looks like**: [Concrete outcome]
- **Projects**: [List related projects]

---

## Review Questions

Monthly, ask:
- [ ] Are these still the right 2-3 objectives?
- [ ] Any objective resolved or stale?
- [ ] Should any project move between Focus/Background/Paused?
```

**Fill this in with your actual objectives.** Don't overthink—you can change them.

## Step 1.4: Create Your First Project

Create a folder for one active project:

```
01_Actions/Focus/My-First-Project/README.md
```

Project README template:

```markdown
---
type: project
next-action: "[THE thing to do next]"
created: 2026-01-06
updated: 2026-01-06
---

# My First Project

**Why**: [One sentence on why this matters]
**Done when**: [What does completion look like?]

---

## Active

Current sprint or focus:
- [ ] Task 1
- [ ] Task 2
- [ ] Task 3

---

## Backlog

Future tasks (add here, pull to Active when ready):
- [ ] Future task 1
- [ ] Future task 2

---

## Done

- [x] Completed task (2026-01-05)

---

## Notes

[Context, decisions, links]
```

**The critical field**: `next-action` in the metadata. This is THE thing to do next. Your AI will read this.

## Step 1.5: Initialize Git

Open terminal, navigate to your vault:

```bash
cd /path/to/your/Personal-Stack

# Initialize git
git init

# Create .gitignore
echo ".obsidian/workspace.json" >> .gitignore
echo ".DS_Store" >> .gitignore

# First commit
git add .
git commit -m "Initial vault setup"
```

Optional but recommended—create a private GitHub repo and push:

```bash
git remote add origin git@github.com:yourusername/personal-stack.git
git push -u origin main
```

## Phase 1 Checkpoint

You should now have:
- [ ] 6-folder structure in Obsidian
- [ ] `Objectives.md` with 1-2 real objectives
- [ ] One project folder with README (including `next-action`)
- [ ] Git initialized with first commit

**Test it**: Open your vault in Obsidian. Can you navigate to your project? Does the structure make sense?

---

# Phase 2: AI Integration (Week 2)

**Goal**: Connect Claude Code to your vault. Experience the context-loading difference.

## Step 2.1: Install Claude Code

Follow instructions at: https://claude.ai/claude-code

Once installed, you should be able to run `claude` from terminal.

## Step 2.2: Create CLAUDE.md

Create `CLAUDE.md` in your vault root (not in a folder):

```markdown
# CLAUDE.md - Personal Stack

Context for Claude when working in this vault.

---

## About Me

[2-3 sentences about who you are and what you do]

### Current Roles
- [Role 1]: [Brief description]
- [Role 2]: [Brief description]

### Working Style
- [How you like to work]
- [What you value in collaboration]

---

## Vault Structure

| Folder | Purpose |
|--------|---------|
| 00_Inbox/ | Quick captures, process within 48h |
| 00_Operations/ | System rules, templates |
| 01_Actions/ | Projects: Focus/, Background/, Paused/ |
| 02_Contexts/ | Ongoing roles and areas |
| 03_Knowledge/ | Reference material |
| 04_Archive/ | Completed work |

---

## Key Files

- **Objectives.md**: `01_Actions/Objectives.md` - Quarterly goals
- **Focus projects**: `01_Actions/Focus/*/README.md`
- **Background projects**: `01_Actions/Background/*/README.md`

---

## Rules for Claude

1. Read `next-action` from project READMEs to know what to surface
2. Max 2 Focus projects at a time
3. Don't create new folders without asking
4. Route quick captures to `00_Inbox/`
5. Commit changes at end of session

---

**Last Updated**: [DATE]
```

**Fill this in with your actual information.** The more context you give, the more useful AI becomes.

## Step 2.3: Create Your First Command

Commands live in `.claude/commands/` folder.

Create the folder structure:
```bash
mkdir -p .claude/commands
```

Create `.claude/commands/start-session.md`:

```markdown
---
description: Begin work session with context loading
---

## Session Startup

### Step 1: Get Date

```bash
date "+%A, %B %d, %Y"
```

### Step 2: Load Context

Read these files:
1. `01_Actions/Objectives.md` - Quarterly goals
2. `01_Actions/Focus/*/README.md` - Each Focus project
3. Git log - Last 3 commits

```bash
git log --oneline -3
```

### Step 3: Output

Format your response as:

```
SESSION READY
=============
[Day, Date]

OBJECTIVES:
1. [Objective 1]
2. [Objective 2]

FOCUS (this week):
  [Project 1]
  → Next: [next-action from frontmatter]

  [Project 2]
  → Next: [next-action from frontmatter]

BACKGROUND:
  [Project] → [next-action]

RECENT COMMITS:
  [commit 1]
  [commit 2]
  [commit 3]

---
What's the focus today?
```
```

## Step 2.4: Create End Session Command

Create `.claude/commands/end-session.md`:

```markdown
---
description: Close work session with documentation and git commit
---

## Session Shutdown

### Step 1: Summarize

Create brief summary:
```
SESSION SUMMARY
===============
Worked on: [project]

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

If significant progress, update the project's README.md:
- Move completed tasks to Done section
- Update `next-action` in frontmatter
- Add any notes

### Step 3: Git Status

```bash
git status
git diff --stat
```

### Step 4: Commit

Ask user to confirm, then:

```bash
git add .
git commit -m "[type]: [description]

[bullet points of what changed]

Generated with Claude Code"
```

Types: feat, fix, docs, chore

### Step 5: Handoff

```
NEXT SESSION
============
Priority: [next focus]
Context: [what to remember]

Resume with: /start-session
```
```

## Step 2.5: Test Your Setup

Open terminal in your vault:

```bash
cd /path/to/your/Personal-Stack
claude
```

Then type:
```
/start-session
```

Claude should read your Objectives.md, your Focus project, and show you a session summary.

**This is the magic moment.** The AI knows your context without you explaining it.

## Phase 2 Checkpoint

You should now have:
- [ ] Claude Code installed and working
- [ ] CLAUDE.md with your personal context
- [ ] `/start-session` command that loads context
- [ ] `/end-session` command that commits work

**Test it**: Run `/start-session`. Does it show your objectives and projects? Run `/end-session` after making a small change. Does it commit?

---

# Phase 3: Workflow Commands (Week 3)

**Goal**: Add commands for daily workflow—capturing tasks, committing changes, thinking through hard problems.

## Step 3.1: Add Task Command

Create `.claude/commands/add-task.md`:

```markdown
---
description: Add task to project backlog
---

## Add Task

When user runs `/add-task [description]`:

### 1. Identify Project

Look for keywords in the task:
- If mentions a project name → that project
- If unclear → ask which project

### 2. Add to Backlog

Open the project's README.md
Find the `## Backlog` section
Append:

```markdown
- [ ] [task description] (added [DATE])
```

### 3. Confirm

```
Added to [Project] backlog:
- [ ] [task description] (added [DATE])
```

DO NOT execute the task. Only add it to the file.
```

## Step 3.2: Commit Command

Create `.claude/commands/commit.md`:

```markdown
---
description: Smart git commit with auto-generated messages
---

## Commit

### 1. Check Status

```bash
git status
git diff --stat
```

### 2. If User Provided Message

Use their message directly:
```bash
git add .
git commit -m "[their message]"
```

### 3. If No Message

Generate based on changes:
- What files changed?
- What type of change? (feat/fix/docs/chore)

Propose message, ask for confirmation.

### 4. Commit Format

```
[type]: [short description]

[optional body]

Generated with Claude Code
```

### 5. After Commit

```
Committed: [hash] [message]
[N files changed]

Push to remote? (y/n)
```

### Rules
- Never force push
- Never skip hooks
- Warn if .env or credentials are staged
```

## Step 3.3: Thinking Partner Command

Create `.claude/commands/thinking-partner.md`:

```markdown
---
description: Structured exploration for hard problems
---

## Thinking Partner Mode

For deep exploration when you're stuck or need to think through something.

### Approach

- Challenge assumptions
- Offer alternative perspectives
- Ask probing questions
- Help synthesize insights

### Session Structure

1. **Topic**: What are we exploring?
2. **Current Thinking**: Where are you starting?
3. **Exploration**: Questions, alternatives, connections
4. **Synthesis**: What insights emerged?
5. **Next Actions**: What should you do with this?

### When to Use

- Stuck on a decision
- Need to generate alternatives
- Want to pressure-test an idea
- Feeling uncertain about direction

### My Role

I'll be a thinking partner, not just an answer machine:
- I'll push back on weak assumptions
- I'll offer frames you might not see
- I'll help you articulate what you're actually thinking

What do you want to think through?
```

## Step 3.4: Connect Code Repos (Optional)

If you have code projects, create a PROJECT.md in each repo that links to your vault:

```markdown
# Project Name

vault-link: 01_Actions/Focus/Project-Name/README.md

## Current Focus
[What you're working on]

## Next Actions
- [ ] Task 1
- [ ] Task 2
```

This connects your code work to your knowledge system.

## Phase 3 Checkpoint

You should now have:
- [ ] `/add-task` - captures tasks to project backlogs
- [ ] `/commit` - smart git commits
- [ ] `/thinking-partner` - structured exploration

**Test it**:
1. Run `/add-task Review Phase 3 checkpoint`
2. Check that it added to your project's backlog
3. Run `/commit` to commit the change
4. Run `/thinking-partner` and explore a real question you have

---

# Phase 4: Governance (Week 4)

**Goal**: Add rules that keep the system clean. Without governance, systems decay.

## Step 4.1: Create Governance Rules

Create `00_Operations/Governance-Rules.md`:

```markdown
---
type: governance
updated: 2026-01-06
---

# Governance Rules

Rules that keep the system healthy.

---

## Anti-Clutter Rules

### 1. Inbox Zero (48 hours)
Everything in `00_Inbox/` gets processed within 48 hours:
- Route to correct folder, OR
- Delete if not needed

If it's been in Inbox >48h, it's clutter.

### 2. Rule of 3
Only create a topic folder in `03_Knowledge/` when you have 3+ items on that topic.

Until then, keep items in `03_Knowledge/_Unsorted/`

### 3. Focus Limit
Maximum 2 projects in `01_Actions/Focus/` at any time.

If you want to add a third, something must move to Background or Paused first.

### 4. Archive Aggressively
When a project is done, move to `04_Archive/` with date:
```
04_Archive/2026-01-Project-Name/
```

Don't keep "finished" projects in Actions.

---

## Review Rhythms

### Daily
- Process Inbox (if anything there)
- Check Focus project next-actions

### Weekly (pick a day)
- [ ] Inbox at zero?
- [ ] Focus projects still right priorities?
- [ ] Any Background ready for Focus?
- [ ] Any completed work to archive?

### Monthly (first week)
- [ ] Review Objectives.md - still accurate?
- [ ] Check `03_Knowledge/_Unsorted/` - anything to organize?
- [ ] Archive stale projects

---

## File Naming

- Use `Title-Case-With-Hyphens.md`
- No spaces in filenames (use hyphens)
- Date prefix when relevant: `2026-01-06-Meeting-Notes.md`

---

## What Claude Should Enforce

1. Warn if Focus has >2 projects
2. Route captures to Inbox (not random folders)
3. Suggest archiving completed projects
4. Remind about weekly review

---

*These rules exist because systems decay. Governance prevents decay.*
```

## Step 4.2: Create Weekly Review Template

Create `00_Operations/Templates/Weekly-Review.md`:

```markdown
---
type: review
date: [DATE]
---

# Weekly Review - [DATE]

## What Happened This Week

### Completed
- [ ]
- [ ]
- [ ]

### Started
- [ ]
- [ ]

### Blocked
- [ ] [Thing] - blocked by [what]

---

## System Health

- [ ] Inbox at zero?
- [ ] Focus projects (max 2) correct?
- [ ] Any project ready to archive?
- [ ] `_Unsorted` folder checked?

---

## Next Week

### Focus
1. [Top priority]
2. [Second priority]

### If Time
- [Background item]
- [Background item]

---

## Notes

[Anything worth remembering]
```

## Step 4.3: Set Up Your First Review

1. Create `00_Operations/Reviews/` folder
2. Copy template to `00_Operations/Reviews/2026-01-06-week-review.md`
3. Fill it out for this week

## Step 4.4: Update CLAUDE.md

Add the governance rules to CLAUDE.md so AI knows to enforce them:

Add to your CLAUDE.md:

```markdown
## Governance Rules

- **Inbox Zero**: Process 00_Inbox/ within 48 hours
- **Rule of 3**: Only create topic folders with 3+ items
- **Focus Limit**: Max 2 projects in Focus at any time
- **Archive**: Move completed projects to 04_Archive/ with date

See: `00_Operations/Governance-Rules.md`
```

## Phase 4 Checkpoint

You should now have:
- [ ] `Governance-Rules.md` with anti-clutter rules
- [ ] `Weekly-Review.md` template
- [ ] First weekly review completed
- [ ] CLAUDE.md updated with governance reference

**Test it**: Run `/start-session`. Does Claude mention anything about your system health? Add a third project to Focus—does it warn you?

---

# You're Done (For Now)

You now have a functional Personal Stack:

**Structure:**
- 6 folders with clear purposes
- Objectives file
- Project READMEs with next-actions

**AI Integration:**
- CLAUDE.md with your context
- `/start-session` for context loading
- `/end-session` for clean shutdown
- `/add-task` for capture
- `/commit` for version control
- `/thinking-partner` for hard problems

**Governance:**
- Anti-clutter rules
- Weekly review rhythm
- Focus limits

---

## What's Next

**Don't add more complexity yet.** Use the system for 2-4 weeks. Notice friction. Then:

### Add commands when you repeat workflows
If you do the same thing 3+ times, make it a command.

### Add folders when you have content
Don't create structure for content you don't have yet. (Rule of 3)

### Grow canons from patterns
As you develop expertise in an area, it might become a "canon"—a structured knowledge base. But don't create canons preemptively.

### Connect more tools
Voice capture, calendar integration, other apps—add when you feel the need.

---

## Common Mistakes

1. **Building too much structure upfront** - Let it emerge from use
2. **More than 2 Focus projects** - The limit is real. Respect it.
3. **Not doing weekly reviews** - This is where systems die
4. **Treating Inbox as storage** - It's temporary. 48 hours max.
5. **Perfect over done** - A working system beats a beautiful unused one

---

## Resources

- **Starter templates**: `Personal-Stack-Starter-Kit/` folder
- **Quick reference**: `Personal-Stack-Quick-Reference.md`
- **Full essay**: `Personal-Stack-Essay.md`

---

The best system is the one you actually use. Start simple. Add when needed. Ship.
