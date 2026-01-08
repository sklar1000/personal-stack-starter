---
id: essay-personal-stack
type: essay
status: draft
created: 2025-12-28
updated: 2026-01-06
objective: pc-business
related:
  - "[[00_Operations/Personal-Stack-Guide|Personal-Stack-Guide]]"
  - "[[00_Operations/Personal-Stack-Spec|Personal-Stack-Spec]]"
  - "[[Personal-Stack-Explanations]]"
tags: [#writing, #personal-stack, #essay]
---

# The Personal Stack
*Building an AI-Native Operating System for Knowledge Work*

---

## Introduction

Every productivity system I've tried has failed the same way. Build something impressive, use it for three months, watch it rot. GTD, Notion, Roam, Tana—all of them. Either too simple for a real life, or so elaborate they become their own full-time job.

Then AI got good enough to actually help. Not a chatbot I paste things into, but something that knows my goals, my projects, and can read and write to my system directly. That changed everything. What if the system was designed for AI from the start?

So I built one. Obsidian for knowledge, Claude Code for intelligence, Git for version control. It loads my context when I start working. It maintains continuity across days. It automates the parts I used to forget. And it sticks—because the system does half the work.

This is how it works, why it works, and how to build your own.

---

## I. The Problem: Why Most Systems Fail

**The maintenance trap**
- Systems that create more work than they save
- Elaborate Notion setups that become full-time jobs
- The second-order cost of "staying organized"

**The AI disconnect**
- Powerful AI tools that don't know your context
- Starting every conversation from zero
- Copy-paste as integration strategy

**The knowledge-action gap**
- PKM for storage, task apps for doing, never connected
- Great notes that don't inform today's decisions
- "I know I wrote something about this..."

**What we actually need**
- An operating system, not another app
- Something that works as hard as you do
- Infrastructure for a life, not a weekend project

---

## II. The Insight: AI-Native Design

**The legacy problem**
- Most PKM systems were designed before AI
- Retrofitting AI onto existing systems is awkward
- Your beautiful prose notes are opaque to machines

**The design shift**
- What if we built for AI collaboration from the start?
- Structure for humans AND machines
- The AI as collaborator, not tool

**Three principles that change everything**
1. **Machine-readable by default** — Frontmatter, consistent patterns, explicit relationships
2. **Bidirectional AI** — Reads your context AND writes back to your system
3. **Explicit context boundaries** — Session start/end as first-class concepts

---

## III. The Architecture: Three Layers

The system has three layers, each handling a different job. The knowledge layer stores everything. The intelligence layer makes sense of it. The version layer tracks changes over time.

### A. The Knowledge Layer (Obsidian)

The foundation is an Obsidian vault, but not the usual kind. Every file has frontmatter—structured metadata at the top that both humans and machines can read. This isn't decorative. It's an API contract. When I write `next-action: "Draft Section III"` in a project's README, my AI can read that field and surface it during session start. When I set `location: focus`, the system knows this is my current priority.

The folder structure is PARA-inspired but adapted: Actions (projects with deadlines), Contexts (roles, people, domains), Knowledge (reference material that compounds), and Operations (system rules and templates). This isn't original—it's Tiago Forte's framework with modifications. What makes it different is that every structural choice was made with AI readability in mind.

Within the Knowledge layer, I maintain what I call "canons"—domain-specific knowledge bases that compound over time. My PC-Canon holds the methodology I teach. My NE-Canon holds everything related to the MBA course I teach at Rice. My Michael-Canon holds personal identity work—career artifacts, patterns I've noticed about myself, decisions and their outcomes. Each canon has its own ontology, its own artifacts, its own development history. They grow smarter as I use them.

Projects get special treatment. Every project has a README with machine-readable frontmatter: what objective it serves, what's the next action, where it sits in priority (Focus, Background, or Paused). Focus means I'm working on it this week—and I limit Focus to two projects at a time. This constraint is enforced by the system, not my willpower.

The other thing that makes this different: temporal depth. I have 10+ years of searchable history in this vault. Time isn't just when I captured something—it's an axis I can navigate. What was I working on in October 2023? What decisions did I make about this client relationship? Past patterns inform current choices.

### B. The Intelligence Layer (Claude Code)

The knowledge layer is inert without intelligence. That's where Claude Code comes in—not as a chatbot, but as a terminal-based AI that can read and write to my file system.

The magic is in "skills"—slash commands that automate workflows. `/start-session` loads my objectives, surfaces focus projects, shows recent commits, and tells me what to work on. `/end-session` documents what I accomplished, updates project status, and commits changes. `/add-task` captures tasks without breaking my flow. These aren't complicated—most are 50-100 lines of markdown instructions—but they eliminate the friction that kills systems.

I also have domain-specific skills. `/design-session` helps me plan a teaching session using pedagogical frameworks. `/map-curriculum` helps me architect learning sequences. `/thinking-partner` is for hard problems that need structured exploration. These emerged from repeated patterns—I noticed I was doing the same thing over and over, so I turned it into a skill.

The critical difference from normal AI use: this is bidirectional. The AI reads my objectives, my projects, my blockers. And it writes back—updating project status, creating artifacts, adding tasks to backlogs. My system and my AI share a common context. I'm not starting from zero every conversation.

### C. The Version Layer (Git/GitHub)

The third layer is version control. My vault lives in a git repository. Every change is tracked. Every session ends with a commit.

This gives me a work log I didn't have to write. What did I do on December 15th? Check the commits. What decisions did I make about the naming sprint? Search the history. It's not journaling—it's automatic documentation.

The version layer also connects my knowledge work to my code work. Code repositories have a PROJECT.md file that links back to the vault project. `/project-status` shows me repo-specific context. It's one system, not two separate worlds.

And yes, it's backup. The vault syncs to GitHub. If my laptop dies, I lose nothing. I can share canons with collaborators. I can recover from mistakes. Version control is table stakes for code—it should be table stakes for knowledge work too.

---

## IV. The Practice: A Day in the Stack

### Morning: Session Start

```
/start-session
```
- Objectives loaded (what you're building toward)
- Focus projects surfaced (what to work on this week)
- Background available (when energy/time allows)
- Recent commits visible (continuity with yesterday)
- Clear answer to "what should I work on?"

### Working: Context-Aware AI

- AI knows your current project, sprint tasks, blockers
- Can reference your frameworks and past work
- Suggests based on your patterns, not generic advice
- `/thinking-partner` when you're stuck

### Creating: Capture Without Breaking Flow

```
/add-task "investigate streaming issue in agent"
```
- Task goes to project backlog
- No context switch to task app
- Process later during review

### Evening: Session End

```
/end-session
```
- Documents what was accomplished
- Updates project README if significant
- Commits changes
- `next-action` updated for tomorrow

---

## V. The Philosophy: What Makes This Different

This isn't just a different set of tools. It's a different stance toward productivity systems—one that shifts several assumptions most people don't even notice they're making.

### Context as First-Class Citizen

Most tools treat context as an afterthought. You open your task manager, see a list of to-dos, and have to reconstruct why any of it matters. What project is this for? What was I thinking when I added this? What's the bigger picture?

In the Personal Stack, context loading is explicit infrastructure. When I run `/start-session`, the system doesn't just show me tasks—it shows me my three objectives, my focus projects, what I committed to this week, and what I did yesterday. The context is there before I have to ask for it.

This sounds small. It isn't. The cognitive cost of "where was I?" compounds across every session, every day. When the system maintains continuity, I can focus on the actual work instead of constantly rebuilding my mental model of what I'm doing and why.

### Whole-Life Integration

Most productivity systems draw a hard line: professional over here, personal over there. But that's not how a life actually works. My teaching informs my methodology. My methodology draws from my personal identity work. My identity work connects to how I've navigated my career.

The canon metaphor captures this. A canon isn't just a folder—it's what's true and lasting about a domain. My PC-Canon holds the methodology I'm developing. My Michael-Canon holds patterns I've noticed about myself, decisions I've made, artifacts from my career. These aren't separate—they're connected. When I teach frameworks, I draw from personal experience. When I do identity work, it shapes what I teach.

This is harder to build but more powerful in practice. A system that knows your whole context can make connections you'd miss. An AI that only sees your work tasks can't help you notice that you keep avoiding the same decision in different domains.

### Temporal Surfacing

History matters. Not in a nostalgic way—in a practical way. Patterns reveal themselves over time. Decisions have downstream consequences. Past versions of yourself made choices you've forgotten but still live with.

The Personal Stack makes time navigable. Weekly reviews, monthly objective checks, quarterly planning—these aren't bureaucracy, they're forcing functions. They make me look at what I said I'd do versus what I actually did. They surface patterns I'd otherwise miss.

There's something else here too. Your past self leaves notes for your future self. When I write progress notes on a project, I'm not just documenting—I'm communicating across time. Six months from now, I won't remember what I was thinking. But I'll be able to read what I wrote.

### Contemplative Practice Embedded

This is the part that sounds woo-woo but isn't. The system functions as a mirror.

Weekly reviews ask: what did I avoid? What kept recurring? What drained my energy versus gave it? Strategic blockers track decisions I've been discussing without deciding—13 touches on five blockers, average 68 days stuck. That's not a task list. That's a diagnosis.

Most productivity systems help you capture and organize. This one also helps you see yourself. Not through journaling (though you can)—through structure. The data tells a story if you're willing to look at it.

The system doesn't judge. It reflects. What you do with that reflection is up to you.

---

## VI. The Value: What Becomes Possible

**Reduced cognitive load**
- System tracks state; you don't have to
- No "where was I?" moments
- Context switching has lower cost

**Better decisions**
- Objectives visible during daily work
- Historical patterns inform current choices
- AI can connect dots you'd miss

**Knowledge compounding**
- Canons grow more valuable over time
- Student examples become case studies
- Frameworks evolve through use
- You get smarter, and so does your system

**Sustainable pace**
- Clear boundaries: Focus (max 2), Background, Paused
- System enforces "one thing at a time"
- Reviews catch drift before crisis
- Permission structure for saying no

---

## VII. The Key Design Principles (Reference)

1. **Machine-readable by default** — Frontmatter, consistent structure, explicit relationships
2. **Bidirectional AI** — Reads AND writes
3. **Session boundaries** — Explicit context loading/unloading
4. **Domains as canons** — Not just folders, but knowledge architectures
5. **Temporal depth** — History is searchable and valuable
6. **Composable skills** — Small, focused commands that combine
7. **Code and knowledge connected** — PROJECT.md → vault links

---

## VIII. Getting Started: Building Your Own

### The Minimum Viable Stack

**Week 1: Knowledge Layer**
- Obsidian vault with basic structure
- One `Objectives.md` file
- One project with README (frontmatter: `next-action`)
- Start using it before it's perfect

**Week 2: Intelligence Layer**
- Claude Code installed
- `/start-session` skill (even simple version)
- `/add-task` for quick capture
- Experience the context loading difference

**Week 3: Version Layer**
- Vault in git (private repo)
- `/commit` skill for smart commits
- PROJECT.md in any code repos, linked to vault

### Growing the System

- Add domain-specific canons as patterns emerge
- Create skills for workflows you repeat
- Connect code repos to vault projects
- Don't over-engineer; grow from use

### Common Pitfalls

- Building elaborate structure before you have patterns
- Too many focus projects (max 2, really)
- Skills that try to do too much
- Not doing the reviews (weekly, monthly)
- Treating it as finished (it evolves)

---

## IX. The Future: Where This Is Going

**Agents that execute**
- Multi-step workflows that run autonomously
- "Prepare my NE session for Tuesday" → research, draft, artifacts

**Voice integration**
- Capture while walking
- Review while commuting
- Dictation that understands your system

**Shared canons**
- Collaboration on methodology
- Team knowledge bases with same architecture
- Teaching materials that compound across instructors

**The Personal Stack as platform**
- Not just productivity, but life infrastructure
- Career navigation, relationship tracking, health
- AI that knows your whole context, not just work

---

## X. Conclusion: Your System Should Work as Hard as You Do

**This is not about productivity hacks**
- It's about building infrastructure for meaningful work
- The compound interest of good structure over decades
- A system that gets smarter as you use it

**AI is a partner, not a replacement**
- You still do the thinking
- The system handles the remembering and connecting
- More capacity for what matters

**Start small, grow from patterns**
- Don't build what you don't need yet
- Let friction reveal what to automate
- Trust that the structure will emerge

**Build your own operating system**
- This is my stack; yours will be different
- The principles transfer; the specifics are personal
- The best system is the one you actually use

---

## Appendix A: Starter Kit Files

For those building their own system, here are the operational files you'll want to create:

### Core System Files

| File | Purpose |
|------|---------|
| `Personal-Stack-Spec.md` | Technical reference for vault structure, layers, invariants |
| `Personal-Stack-Guide.md` | Practical workflow guide for daily use |
| `Objectives.md` | Quarterly goals with success criteria and blockers |
| `Weekly-Review-Protocol.md` | Structured process for weekly reviews |
| `Session-Boundaries.md` | What to load/unload at session start/end |

### AI Integration Files

| File | Purpose |
|------|---------|
| `CLAUDE.md` | Root-level instructions for AI (vault rules, patterns, context) |
| `AI-Operating-Policy.md` | Guidelines for AI behavior, what it can/can't do |
| `Skill-Backlog.md` | Ideas for new slash commands to build |
| `Prompt-Library.md` | Reusable prompts for common tasks |

### Project Templates

| File | Purpose |
|------|---------|
| `Templates/Project-README.md` | Standard project README with frontmatter schema |
| `Templates/Canon-README.md` | Standard canon structure (ontology, artifacts, development) |
| `Templates/Session-Notes.md` | Template for session documentation |

### Review & Maintenance

| File | Purpose |
|------|---------|
| `Monthly-Review-Protocol.md` | Process for monthly objectives review |
| `Quarterly-Review-Protocol.md` | Process for quarterly planning |
| `Vault-Health-Checks.md` | Periodic maintenance tasks (orphaned files, stale projects) |
| `Known-Issues.md` | Workarounds for tool limitations |

### Domain-Specific (examples)

| File | Purpose |
|------|---------|
| `[Domain]-Canon-Spec.md` | Technical spec for a domain canon (ontology, taxonomy) |
| `[Domain]-Workflow.md` | Domain-specific workflows and processes |
| `[Role]-Context.md` | Context file for a specific role or area |

---

## Appendix B: Sample Frontmatter Schemas

### Project README

```yaml
---
id: project-[name]-[date]
type: project
location: focus | background | paused
objective: [linked-objective-id]
next-action: "The ONE thing to do next"
horizon: 2025-Q1
created: 2025-01-01
updated: 2025-01-15
tags: [#project, #domain]
---
```

### Skill Definition

```markdown
# /skill-name

One-line description.

## Step 1: [Action]
[Instructions or bash commands]

## Step 2: [Action]
[Instructions]

## Output Format
[Template for consistent output]
```

### PROJECT.md (for code repos)

```markdown
# Project Name

vault-link: 01_Actions/1-Focus/Project-Name/README.md

## Current Sprint
[What you're working on]

## Next Actions
- [ ] Task 1
- [ ] Task 2

## Blockers
[What's in the way]
```
