# Personal Stack Starter

Build an AI-native productivity system using Obsidian, Claude Code, and Git.

## What Is This?

A **Personal Stack** is a knowledge system designed for AI collaboration from the start. Instead of bolting AI onto existing tools, you build a system where:

- AI knows your context, goals, and projects
- Session start loads everything you need
- Session end documents and commits your work
- Knowledge compounds over time

This repo contains guides and templates to build your own.

## Who Is This For?

- Knowledge workers (writing, teaching, consulting, building)
- People who've tried productivity systems and watched them decay
- People who want AI that actually knows what they're working on

## What's Included

### Guides

| Guide | Description |
|-------|-------------|
| [Personal Stack Essay](guides/Personal-Stack-Essay.md) | The philosophy: why this approach works |
| [One-Pager](guides/Personal-Stack-One-Pager.md) | Plain-language explainer (2 min read) |
| [Builder's Guide](guides/Personal-Stack-Builders-Guide.md) | 4-week step-by-step setup |
| [Quick Reference](guides/Personal-Stack-Quick-Reference.md) | One-page cheat sheet |
| [Canon Builder's Guide](guides/Canon-Builders-Guide.md) | Advanced: building governed knowledge systems |

### Starter Templates

**Basic Stack** (`templates/personal-stack/`):
- CLAUDE.md template
- Objectives template
- Project README template
- 5 slash command templates
- Governance rules

**Canon Kit** (`templates/canon/`):
- Canon README template
- Ontology template
- Framework template
- Governance template
- Example template

## Quick Start

### Option A: Copy Templates Manually

1. Read the [Builder's Guide](guides/Personal-Stack-Builders-Guide.md)
2. Create your Obsidian vault
3. Copy templates from `templates/personal-stack/` as needed

### Option B: Clone and Customize

```bash
git clone https://github.com/sklar1000/personal-stack-starter.git
cd personal-stack-starter

# Copy templates to your vault
cp -r templates/personal-stack/* /path/to/your/vault/
```

## The 4-Week Build

| Week | Focus | Outcome |
|------|-------|---------|
| 1 | Foundation | Folder structure + Objectives + Git |
| 2 | AI Integration | CLAUDE.md + start/end session commands |
| 3 | Workflow | add-task, commit, thinking-partner |
| 4 | Governance | Anti-clutter rules + review rhythms |

## Core Concepts

### Folder Structure

```
Your-Vault/
├── 00_Inbox/           # Quick captures (48h max)
├── 00_Operations/      # System rules
├── 01_Actions/         # Projects
│   ├── Focus/          # THIS WEEK (max 2)
│   ├── Background/     # When time allows
│   └── Paused/         # Blocked/waiting
├── 02_Contexts/        # Ongoing areas
├── 03_Knowledge/       # Reference + Canons
└── 04_Archive/         # Done (date-stamped)
```

### Essential Commands

| Command | Purpose |
|---------|---------|
| `/start-session` | Load context, show focus |
| `/end-session` | Document, commit, close |
| `/add-task` | Capture to backlog |
| `/commit` | Smart git commit |
| `/thinking-partner` | Explore hard problems |

### Anti-Clutter Rules

- **Inbox Zero**: Process within 48 hours
- **Rule of 3**: 3+ items before creating a folder
- **Focus Limit**: Max 2 projects in Focus
- **Archive Fast**: Done → Archive with date

## Advanced: Building Canons

Once your basic stack is working, you can add **Canons**—governed knowledge systems for domains where you need:

- Shared vocabulary (ontology)
- Proven frameworks
- Status gates (draft → candidate → stable)
- Change governance

See the [Canon Builder's Guide](guides/Canon-Builders-Guide.md).

## Technology Stack

**Required:**
- [Obsidian](https://obsidian.md/) (free)
- [Claude Code](https://claude.ai/claude-code) (requires Claude subscription)
- Git

**Optional:**
- GitHub (backup + sharing)
- tmux (session management)

## License

MIT - Use freely, attribution appreciated.

## Contributing

This is a personal methodology, but improvements welcome:
- Bug fixes in templates
- Clarifications in guides
- Typo fixes

## Related

- [Personal Cartography](https://michaelsklar.ai) - The methodology this system supports
- [Claude Code Documentation](https://docs.anthropic.com/claude-code)

---

*The best system is the one you actually use. Start simple. Add when needed.*
