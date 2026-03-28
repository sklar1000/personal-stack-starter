# Setup: Prerequisites and Installation

Everything you need before starting Track A or Track B.

---

## System Requirements

| Requirement | Details |
|---|---|
| **Operating System** | macOS 13+, Windows 10+, Ubuntu 20.04+, Debian 10+, Alpine 3.19+ |
| **RAM** | 4GB minimum |
| **Network** | Internet connection required |
| **Shell** | Terminal (Mac), PowerShell or CMD (Windows), Bash/Zsh (Linux) |
| **Git** | Required on Windows before installing. Recommended everywhere. |

**You do NOT need**: Python, Node.js, or any programming language runtime.

---

## Step 1: Install Claude Code

**Mac / Linux / WSL:**
```bash
curl -fsSL https://claude.ai/install.sh | bash
```

**Windows PowerShell:**
```powershell
irm https://claude.ai/install.ps1 | iex
```

**Windows CMD:**
```batch
curl -fsSL https://claude.ai/install.cmd -o install.cmd && install.cmd && del install.cmd
```

Claude Code auto-updates after installation. No maintenance needed.

---

## Step 2: Get a Claude Subscription

Claude Code requires a paid plan. Options:

| Plan | Cost | Best For |
|---|---|---|
| **Claude Pro** | $20/mo | Getting started, personal use |
| **Claude Max** | $100/mo | Heavy daily use, long sessions |
| **Claude Teams** | $30/user/mo | Team collaboration |
| **Claude Console** | Pay-per-use | Developers, API access (free $5 trial) |

Sign up at [claude.ai](https://claude.ai) if you don't have an account.

---

## Step 3: Install Git (Recommended)

Git tracks every change you make. It's your breadcrumb trail — you can see what you changed, when, and why. Even if you've never used Git before, install it now. Claude Code will help you use it.

**Mac:**
```bash
xcode-select --install
```
(Git comes with Xcode Command Line Tools)

**Windows:**
Download from [git-scm.com](https://git-scm.com/download/win) and run the installer. Use all defaults.

**Linux:**
```bash
sudo apt install git    # Ubuntu/Debian
sudo dnf install git    # Fedora
```

### Verify Installation

```bash
git --version
```

If you see a version number, you're good.

---

## Step 4: Authenticate

Open your terminal and run:

```bash
claude
```

A browser window opens. Log in with your Claude account. Done.

No API keys to paste. No config files to edit.

---

## Step 5: Install Obsidian (Optional)

Obsidian is a free markdown editor that gives you a visual interface for your stack. You don't need it — Claude Code and any text editor work fine. But if you want to browse your files with backlinks, graph views, and live preview, Obsidian is built for exactly this kind of folder.

**Why consider it**: Your stack is a folder of markdown files. Obsidian turns that folder into a connected knowledge base you can navigate visually — see how files link to each other, search across everything, and edit without touching the terminal.

**Download**: [obsidian.md](https://obsidian.md) — free for personal use.

After installing, open Obsidian and select "Open folder as vault" → point it at your stack folder (e.g., `my-stack/`). That's it. Obsidian reads the same files Claude Code does — no sync, no duplication.

**Recommended for**: Track B users who plan to add multiple projects or use Tier 2+ folder structures. Not needed for Track A.

---

## Troubleshooting

**"command not found: claude"**
→ Close and reopen your terminal, then try again. The installer updates your PATH.

**Browser doesn't open for auth**
→ Try `claude auth login` manually.

**Windows: "git is not recognized"**
→ Install Git for Windows first (Step 3 above), then reinstall Claude Code.

**"You've exceeded your usage limit"**
→ Your subscription tier has a usage cap. Wait for reset or upgrade your plan.

---

## Next Steps

You're set up. Pick your track:

- → [Track A: Just Exploring](TRACK-A-EXPLORE.md) — 15 minutes, see what this does
- → [Track B: Ready to Build](TRACK-B-BUILD.md) — 30 minutes, full working system
