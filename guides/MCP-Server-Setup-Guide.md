# MCP Server Setup Guide

How to extend Claude Code with MCP (Model Context Protocol) servers for additional capabilities.

---

## What Are MCP Servers?

MCP servers give Claude Code access to external tools and data sources. Instead of copy-pasting information, Claude can directly:

- Search Google Drive
- Query databases
- Fetch web pages
- Access APIs
- Read from external services

Think of them as plugins that expand what Claude can do.

---

## When You Need MCP Servers

**You probably need MCP servers if:**
- Your vault references files in Google Drive
- You want Claude to search the web
- You need access to external APIs (GitHub, Notion, etc.)
- You want library documentation lookup

**You probably don't need them if:**
- Your vault is self-contained
- You're just starting out
- You prefer to copy-paste when needed

**Recommendation**: Start without MCP servers. Add them when you feel the friction.

---

## Setting Up MCP Servers

### Step 1: Locate Your Config File

Claude Code stores MCP configuration in:
```
~/.claude/settings.json
```

Or project-specific:
```
/path/to/your/vault/.claude/settings.json
```

### Step 2: Add MCP Server Configuration

Edit the settings file to add servers:

```json
{
  "mcpServers": {
    "server-name": {
      "command": "command-to-run",
      "args": ["arg1", "arg2"],
      "env": {
        "API_KEY": "your-key-here"
      }
    }
  }
}
```

### Step 3: Restart Claude Code

After changing settings, restart Claude Code for changes to take effect.

---

## Common MCP Servers

### Google Drive

Access files stored in Google Drive (useful if your vault syncs there).

**Setup:**
```json
{
  "mcpServers": {
    "gdrive": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-gdrive"]
    }
  }
}
```

**First run**: Will prompt for Google OAuth authorization.

**What it enables:**
- `mcp__gdrive__search` - Search files by name
- Reading Google Docs, Sheets, etc.

---

### Web Fetch

Fetch and analyze web pages.

**Setup:**
```json
{
  "mcpServers": {
    "fetch": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-fetch"]
    }
  }
}
```

**What it enables:**
- Fetching URLs and extracting content
- Analyzing web pages
- Following redirects

---

### Context7 (Library Documentation)

Get up-to-date documentation for programming libraries.

**Setup:**
```json
{
  "mcpServers": {
    "context7": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-context7"]
    }
  }
}
```

**What it enables:**
- `mcp__context7__resolve-library-id` - Find library IDs
- `mcp__context7__query-docs` - Query documentation

**Usage**: Ask Claude "How do I use [library]? use context7"

---

### GitHub

Access GitHub repositories, issues, PRs.

**Setup:**
```json
{
  "mcpServers": {
    "github": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-github"],
      "env": {
        "GITHUB_TOKEN": "your-github-token"
      }
    }
  }
}
```

**Get a token**: GitHub → Settings → Developer settings → Personal access tokens

---

### Filesystem (Extended Access)

Give Claude access to directories outside the current working directory.

**Setup:**
```json
{
  "mcpServers": {
    "filesystem": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-filesystem", "/path/to/allow"]
    }
  }
}
```

---

## Full Example Configuration

A typical setup for Personal Stack users:

```json
{
  "mcpServers": {
    "gdrive": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-gdrive"]
    },
    "context7": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-context7"]
    }
  }
}
```

---

## Verifying MCP Servers

After setup, verify servers are working:

1. Start Claude Code
2. Type `/mcp` or ask "What MCP servers are available?"
3. Claude should list connected servers

If a server isn't showing:
- Check the settings.json syntax (valid JSON?)
- Check the command path (is npx available?)
- Check environment variables (API keys set?)
- Restart Claude Code

---

## Troubleshooting

### "Server not found"
- Verify the package name is correct
- Try running the command manually in terminal
- Check npm/npx is installed

### "Authentication failed"
- Check API keys in env section
- Regenerate tokens if expired
- Verify OAuth flow completed (for Google)

### "Permission denied"
- Check file paths are accessible
- Verify Claude Code has necessary permissions
- Try with absolute paths

### Server crashes
- Check logs: `~/.claude/logs/`
- Try updating the MCP package: `npm update -g @anthropic/mcp-[name]`

---

## Security Considerations

**Be careful with:**
- API keys in settings.json (don't commit to public repos)
- Filesystem access (limit to specific directories)
- OAuth tokens (revoke if compromised)

**Best practices:**
- Use environment variables for sensitive keys
- Limit filesystem access to what's needed
- Review MCP server permissions before installing

---

## Building Custom MCP Servers

For advanced users, you can build custom MCP servers:

1. Use the MCP SDK
2. Define tools your server provides
3. Handle requests from Claude

**Resources:**
- [MCP Documentation](https://docs.anthropic.com/mcp)
- [MCP SDK on GitHub](https://github.com/anthropics/mcp)

---

## Recommended Setup for Personal Stack

**Minimum (most users):**
- Google Drive (if vault is there)
- Context7 (if you code)

**Extended:**
- Add GitHub if you work with repos
- Add web fetch for research tasks

**Start simple. Add servers when you feel the friction.**

---

*MCP servers extend Claude's reach. Use them to reduce copy-paste friction.*
