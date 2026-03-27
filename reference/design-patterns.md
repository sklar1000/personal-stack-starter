# 10 Design Patterns That Make It Work

These patterns emerged from 8,000+ files, 50+ commands, and a year of building a personal operating system with Claude Code. They're not rules — they're patterns that survived contact with reality.

You don't need all of these on day one. But when something isn't working, check this list. The fix is probably here.

---

## 1. Actionability-Based Organization

**Pattern**: Organize files by what you DO with them, not what they ARE about.

A file about marketing strategy doesn't go in a "Marketing" folder. It goes in `Projects/` if you're acting on it, `Reference/` if you're just storing it, or `Archive/` if you're done with it.

**Why it works**: You never ask "what folder has my stuff?" You ask "what am I working on?" The answer is always in Projects.

---

## 2. CLAUDE.md as Living Memory

**Pattern**: One file at the root of your folder that Claude reads every session. Contains: who you are, what you're working on, how you work, and what rules to follow.

**Why it works**: Instead of re-explaining yourself every conversation, you maintain one file. Edit it once, every future session benefits. It's external memory.

**Key insight**: This file should change often. If your CLAUDE.md hasn't changed in 2 weeks, it's not living — it's a gravestone.

---

## 3. Session Bracketing

**Pattern**: Explicit open and close rituals for every work session. `/start-session` loads context. `/end-session` documents outcomes and commits.

**Why it works**: You never lose context between sessions. The end-of-session handoff tells future-you exactly where to pick up. Git commits create a searchable trail of what happened when.

**The compounding effect**: After 20 sessions, you can trace the entire evolution of a project through commit history and session logs.

---

## 4. Focus Limits

**Pattern**: Hard cap on active projects (recommended: 3). Moving something in means something moves out. Enforced by the system, not by willpower.

**Why it works**: Unlimited work-in-progress is the #1 productivity killer. The constraint forces prioritization. You stop "working on everything" and start finishing things.

**The 4-tier lifecycle**: Focus (max 3, daily) / Background (monitored, weekly) / Paused (parked, monthly check) / Planning (unlimited ideas, zero commitment).

---

## 5. Commands Over Memory

**Pattern**: Any process you repeat more than twice becomes a slash command. One word triggers a multi-step workflow.

**Why it works**: You don't have to remember how to do things. The command encodes the process. It runs the same way every time, even when you're tired or distracted.

**How to build one**: Write what you'd tell Claude as step-by-step instructions. Save it as `.claude/commands/name.md`. Done.

---

## 6. Rules Over Repetition

**Pattern**: Behavioral rules go in `.claude/rules/` files. Claude follows them automatically without you mentioning them.

**Why it works**: Instead of saying "be concise" every session, you write it once as a rule. It persists forever. Rules accumulate — each one is a lesson learned, encoded.

**Examples**: Writing style, file naming conventions, what to never do, how to handle specific situations.

---

## 7. Canon vs. Delivery Separation

**Pattern**: Core methodology lives in one place (the canon). Every course, client engagement, essay, or workshop pulls from the canon. Edit the source, everything downstream updates.

**Why it works**: Knowledge compounds instead of getting rebuilt. Version your frameworks. A client gets "framework v1.2" — not a unique snowflake you built from scratch.

**When you need it**: When you catch yourself rebuilding the same framework for the third time.

---

## 8. The 48-Hour Inbox

**Pattern**: Everything captured goes to Inbox first. Nothing lives there longer than 48 hours. Process means route to the right folder or delete.

**Why it works**: Capture is fast (no decision about where it goes). Processing is a separate activity. The 48-hour rule prevents the inbox from becoming a junk drawer.

---

## 9. Archive as Memory, Not Deletion

**Pattern**: Completed projects go to Archive with a date prefix (`2026-03-Project-Name/`). They're searchable and retrievable but out of your active view.

**Why it works**: Nothing gets lost. But finished work stops competing for attention with active work. The archive IS your track record — browsing it shows you everything you've shipped.

---

## 10. The System Extends Itself

**Pattern**: When something is frustrating, don't work around it — build the fix. Every command, rule, and template started as friction. The system grows from use, not from planning.

**Why it works**: Systems built from real friction are always more useful than systems designed in advance. You solve the problems you actually have, not the problems you imagine having.

**The test**: If the system is the same after 30 days of use as it was on day one, something is wrong. It should be evolving.

---

## How to Use These Patterns

- **Day 1**: You need patterns 1, 2, 3. That's it.
- **Week 2**: Add patterns 4, 5, 8. Organization and workflow.
- **Month 2+**: Patterns 6, 7, 9, 10 as needed. The system tells you when.

Don't implement all 10 at once. That's over-engineering. Start with the minimum and let friction tell you what to add next.
