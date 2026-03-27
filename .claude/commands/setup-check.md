---
description: Check if your personal stack is set up correctly
---

Verify my personal stack setup and tell me what's working and what's missing.

## Check these things

1. Does `CLAUDE.md` exist at the root? Read it.
2. Is git initialized? Run `git status`
3. Are there commands in `.claude/commands/`? List them.
4. Is there a folder structure? Run `ls`
5. Are there any project READMEs?

## Output format

```
SETUP CHECK
===========

CLAUDE.md:     [Found / Missing]
Git:           [Initialized / Not initialized]
Commands:      [N found: list them / None]
Structure:     [Folders found / Flat]
Projects:      [N projects / None]

MATURITY LEVEL: [1-3 based on what exists]

SUGGESTIONS:
- [What to add next, if anything]
```

Be encouraging. Tell me what's working, then what to add.
