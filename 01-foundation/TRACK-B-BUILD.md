# Track B: Ready to Build

**Time**: 30 minutes
**What you get**: A working system with project tracking, git history, session commands, and governance rules.
**Who this is for**: You already know you want this. You have a project. Let's go.

---

## Prerequisites

Complete [SETUP.md](SETUP.md) first (Claude Code + Git installed and authenticated).

---

## Step 1: Create Your Stack (2 min)

```bash
mkdir my-stack
cd my-stack
git init
```

You now have a folder with version control. Every change you make gets tracked.

---

## Step 2: Create Your CLAUDE.md (10 min)

Copy this template into a file called `CLAUDE.md` at your folder root. Fill in every `[BRACKET]`:

```markdown
# CLAUDE.md - My Personal Stack

Context for Claude when working in this folder.

---

## About Me

I am a [YOUR ROLE] who works on [YOUR DOMAIN].
I help [WHO] do [WHAT].

### Current Roles
- **[Role 1]**: [Brief description]
- **[Role 2]**: [Brief description — or delete this line if one role]

### How I Work
- I prefer [DIRECT / DETAILED / CASUAL / FORMAL] communication
- [What you value — e.g., "Evidence over opinion" or "Speed over polish"]
- [What to avoid — e.g., "Don't sugarcoat feedback" or "Skip the preamble"]

---

## What I'm Working On

### Active Project: [PROJECT NAME]

**Why**: [One sentence — why does this project exist?]
**Done when**: [What does completion look like?]

Current tasks:
- [ ] [Task 1]
- [ ] [Task 2]
- [ ] [Task 3]

---

## Rules for Claude

### Do
1. Read this file at the start of every session
2. Be direct — lead with the answer, not the reasoning
3. When I finish work, remind me to commit

### Don't
1. Don't create new folders without asking
2. Don't add features I didn't request
3. Don't sugarcoat — tell me what's wrong

---

## Slash Commands

| Command | Purpose |
|---------|---------|
| `/start-session` | Load context, show what to work on |
| `/end-session` | Document progress, commit changes |
| `/commit` | Smart git commit |
| `/add-task` | Add task to backlog |
| `/thinking-partner` | Explore a hard problem |

---

**Last Updated**: [TODAY'S DATE]
```

---

## Step 3: Set Up Commands (5 min)

Commands are instructions that Claude follows when you type `/command-name`. Create the folder and copy the starter commands:

```bash
mkdir -p .claude/commands
```

Copy each file from this repo's [`01-foundation/commands/`](commands/) folder into your `.claude/commands/` directory:

- `start-session.md` — loads your context at the start of each work session
- `end-session.md` — documents progress, commits, prepares handoff
- `commit.md` — creates clean git commits with good messages
- `add-task.md` — captures tasks without executing them
- `thinking-partner.md` — structured exploration for hard problems

---

## Step 4: Make Your First Commit (3 min)

```bash
claude
```

Inside Claude, type:

```
/commit
```

Claude will see your new files and propose a commit message. Approve it. You now have your first breadcrumb in git history.

---

## Step 5: Start Your First Session (5 min)

Still in Claude, type:

```
/start-session
```

Claude reads your CLAUDE.md, shows your project and tasks, and asks what to focus on. Tell it. Start working.

When you're done:

```
/end-session
```

Claude documents what you did, updates your tasks, commits your changes, and prepares a handoff for next time.

---

## Step 6: Push to GitHub (5 min, optional but recommended)

GitHub gives you a backup and a history you can browse from anywhere.

1. Create a new repository at [github.com/new](https://github.com/new) (private is fine)
2. Name it `my-stack` (or whatever you want)
3. Don't initialize with README (you already have files)

```bash
git remote add origin https://github.com/YOUR-USERNAME/my-stack.git
git push -u origin main
```

Now your stack is backed up and you can see your full history on GitHub.

---

## What You Have Now

- **CLAUDE.md** — Your AI knows who you are and what you're working on
- **5 commands** — Session management, task capture, thinking partnership
- **Git history** — Every session is a breadcrumb you can retrace
- **One project** — Tracked with tasks, not scattered across apps

---

## What to Do Next

**Use this for 2 weeks.** Run `/start-session` when you sit down. Run `/end-session` when you're done. Let the rhythm build.

**When you're ready for more**, you'll know — here are the signals:

→ [Tier 2: Workflow](../02-workflow/UPGRADE.md) — When sessions feel repetitive and you want more structure
→ [Tier 3: System](../03-system/UPGRADE.md) — When one project becomes three and you need architecture

**Don't add complexity before you need it.** The system grows with you.
