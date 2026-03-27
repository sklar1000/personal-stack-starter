# Track A: Just Exploring

**Time**: 15 minutes
**What you get**: A folder where Claude knows who you are and what you're working on.
**What you skip**: Git, project tracking, governance. You can add all of that later.

---

## Prerequisites

Complete [SETUP.md](SETUP.md) first (Claude Code installed + authenticated).

---

## Step 1: Create Your Folder (2 min)

Open your terminal:

```bash
mkdir my-stack
cd my-stack
```

That's your stack. One folder.

---

## Step 2: Create Your CLAUDE.md (10 min)

This is the file that tells Claude who you are. Create a file called `CLAUDE.md` in your folder and fill in the blanks:

```markdown
# CLAUDE.md

## About Me

I am a [YOUR ROLE] who works on [YOUR DOMAIN].
I care about [WHAT MATTERS TO YOU — 1-2 sentences].

## What I'm Working On

My current priority is [THE ONE THING].

## How I Work

- I prefer [DIRECT / DETAILED / CASUAL / FORMAL] communication
- [One thing Claude should always do — e.g., "Be concise" or "Challenge my assumptions"]
- [One thing Claude should never do — e.g., "Don't sugarcoat" or "Don't add emojis"]
```

**Don't overthink this.** Write what comes to mind. You'll edit it as you go — that's the whole point. Claude reads this file every time you start a conversation.

---

## Step 3: Start Talking (3 min)

```bash
claude
```

Try these:

- "Read my CLAUDE.md and tell me what you understand about me"
- "Help me think through [your current priority]"
- "What should I work on today?"

Notice the difference from a fresh Claude conversation — it already knows your context.

---

## That's It

You have a personal stack. One folder, one file, and an AI that remembers you.

### What to Do Next

**Use it for a week.** Just talk to Claude in this folder. Ask it to help you think, plan, draft, or organize. Save interesting outputs as markdown files in the same folder.

**When you're ready for more:**

Signs you've outgrown Track A:
- You wish Claude remembered what you did last session
- You have files piling up with no organization
- You keep re-explaining the same context
- You want to track tasks or projects

→ Move to [Track B: Ready to Build](TRACK-B-BUILD.md) for the full foundation.
→ Or jump straight to [Tier 2: Workflow](../02-workflow/UPGRADE.md) if Track B's basics feel obvious.
