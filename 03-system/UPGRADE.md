# Tier 3: System

**You're ready for this when...**

- You have 3+ active projects and context-switching is painful
- You keep rebuilding the same frameworks for different contexts
- You want Claude to know your personality, values, and patterns — not just your projects
- You want automation: things that happen without you remembering to do them
- You've been using Tier 2 for a month and want more power

If you're here on day one, pause. Build the foundation first. This layer is powerful but it's overhead you don't need until you do.

---

## What Tier 3 Adds

| Capability | What It Does | Why It Matters |
|---|---|---|
| **Identity layer** | Your values, strengths, shadow patterns, working style | AI that adapts to YOU, not generic advice |
| **Multi-project structure** | 4-tier lifecycle: Focus / Background / Paused / Planning | Nothing falls through the cracks |
| **Knowledge canon** | Methodology separated from delivery | Build once, deploy many times |
| **Custom commands** | Build your own slash commands for repeated workflows | One word triggers complex processes |
| **Rules files** | Persistent behavioral rules for Claude | Consistency without re-explaining |

---

## The Identity Layer

This is where the system goes from useful to transformative. Write a file that tells Claude WHO YOU ARE — not just what you're working on.

Create `self/identity.md`:

```markdown
# Identity

## Core Profile
- **Type**: [Introvert/extrovert, analytical/creative, etc.]
- **Values**: [What you optimize for — autonomy? craft? speed? depth?]
- **Strengths**: [What you're genuinely good at]
- **Shadow patterns**: [Where you self-sabotage — be honest]

## Working Style
- [How you make decisions]
- [What drains your energy]
- [What gives you energy]
- [Your default failure mode under stress]

## Communication
- [How you want to be talked to]
- [What annoys you in collaboration]
- [What "good feedback" looks like to you]
```

Then add to your CLAUDE.md: `Read self/identity.md for my personality and working style.`

The more honest this file is, the better Claude gets. The shadow patterns are the most valuable part — they let Claude catch you when you're in a loop.

---

## Multi-Project Structure

Evolve your flat `01_Projects/` into a lifecycle:

```
01_Projects/
  Focus/          ← Max 3. Active daily work.
  Background/     ← Monitored, not daily. Work when time allows.
  Paused/         ← Explicitly parked. Not abandoned — parked.
  Planning/       ← Ideas. Unlimited. No commitment.
```

The constraint is the feature. You can only have 3 things in Focus. Moving something IN means something moves OUT.

Update `/start-session` to read Focus projects first, Background projects briefly, and ignore Paused/Planning.

---

## Knowledge Canon

If you teach, consult, write, or coach — you have a methodology. Stop rebuilding it for each engagement.

Create a `knowledge/` folder for reusable frameworks:

```
knowledge/
  my-framework.md       ← The canonical version
  my-process.md         ← Step-by-step how-to
  my-templates/         ← Reusable templates
```

**Canon rule**: The canonical version lives in `knowledge/`. Project-specific adaptations live in the project folder. Edit the canon, everything downstream updates.

---

## Custom Commands

You've been using the 5 starter commands. Now build your own.

A command is just a markdown file in `.claude/commands/` with instructions for Claude. Examples:

- `/weekly-review` — Check all projects, update priorities, archive stale items
- `/draft-email` — Write an email in your voice using your identity file
- `/prep-meeting` — Research a person, summarize context, suggest talking points

**How to create one**: Write what you'd normally say to Claude as step-by-step instructions. Save it as `.claude/commands/[name].md`. Now it's a one-word invocation.

---

## Rules Files

Rules are always-on instructions that Claude follows without being asked. Create `.claude/rules/` and add markdown files:

Example — `.claude/rules/writing-style.md`:
```markdown
# Writing Style

When writing for me:
- Be direct. Lead with the answer.
- No filler words or hedging.
- Short sentences. Active voice.
- If I'm wrong, say so.
```

Claude reads all rules files automatically. They persist across sessions without you mentioning them.

---

## What You Have Now

- **Identity layer** — Claude knows your personality, not just your projects
- **4-tier project lifecycle** — Focus, Background, Paused, Planning with enforced limits
- **Knowledge canon** — Methodology built once, deployed everywhere
- **Custom commands** — Repeating workflows reduced to one word
- **Rules** — Behavioral guardrails that persist automatically

---

## Beyond Tier 3

At this point, you're building a system that's uniquely yours. There's no Tier 4 guide — because from here, the system grows from your own friction. Every time something is annoying, you build a command. Every time Claude forgets something, you add a rule. Every time you repeat yourself, you create a template.

The system extends itself. That's the design.

**Resources for going deeper:**
- [Design Patterns](../reference/design-patterns.md) — 10 patterns that make the system work
- [Maturity Model](../reference/maturity-model.md) — Where you are and where you're going
