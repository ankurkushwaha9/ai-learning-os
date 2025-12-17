# GitHub MCP Setup Guide

> Connect Claude Desktop to GitHub for seamless repository management

**Status:** ✅ Active
**Added:** December 2025
**Difficulty:** Beginner-Friendly

---

## What This MCP Does

The GitHub MCP allows Claude Desktop to:
- Create and manage repositories
- Create, update, and delete files
- Push code directly to GitHub
- Manage branches and commits
- Create and manage issues
- Handle pull requests
- Search code and users

---

## Why You Need This

Instead of manually copying code and uploading to GitHub, you can simply tell Claude:
- "Create a new repository called my-project"
- "Push this code to my repo"
- "Create a new file in my repository"

Claude handles everything directly!

---

## Prerequisites

Before starting, you need:
1. A GitHub account (free at github.com)
2. Claude Desktop app installed (not the web version)
3. Node.js installed on your computer

---

## Step-by-Step Setup

### Step 1: Create GitHub Account

If you don't have one:
1. Go to [github.com](https://github.com)
2. Click "Sign Up"
3. Follow the registration process

### Step 2: Generate Personal Access Token

1. Go to: https://github.com/settings/tokens
2. Click "Generate new token" dropdown
3. Select "Generate new token (classic)"
4. Enter your password if asked

**Configure the token:**
- **Note:** Claude Desktop GitHub Access
- **Expiration:** 90 days (or your preference)
- **Scopes:** Check these boxes:
  - ☑️ repo (all sub-items)
  - ☑️ workflow

5. Click "Generate token"
6. **COPY THE TOKEN IMMEDIATELY** (starts with `ghp_`)
7. Save it somewhere safe - GitHub won't show it again!

### Step 3: Install Node.js (if not installed)

1. Open Command Prompt (Windows) or Terminal (Mac)
2. Type: `node --version`
3. If you see an error:
   - Go to [nodejs.org](https://nodejs.org)
   - Download the LTS version
   - Run the installer with default settings
   - Restart your computer

### Step 4: Configure Claude Desktop

1. Close Claude Desktop completely

2. Open the config file:
   - **Windows:** Press Win+R, type `%APPDATA%\Claude`, press Enter
   - **Mac:** Open Finder, press Cmd+Shift+G, type `~/Library/Application Support/Claude`

3. Open `claude_desktop_config.json` (create it if it doesn't exist)

4. Add this configuration:
```json
{
  "mcpServers": {
    "github": {
      "command": "npx",
      "args": [
        "-y",
        "@modelcontextprotocol/server-github"
      ],
      "env": {
        "GITHUB_PERSONAL_ACCESS_TOKEN": "YOUR_TOKEN_HERE"
      }
    }
  }
}
```

5. Replace `YOUR_TOKEN_HERE` with your actual token (keep the quotes)

6. Save the file

7. Restart Claude Desktop

### Step 5: Verify It Works

In Claude Desktop, ask:
"What MCPs do you have access to?"

You should see GitHub listed with its capabilities.

---

## Example Commands

Once set up, try these:

**Create a repository:**
"Create a new public repository called test-project with description 'My test project'"

**Create a file:**
"Create a README.md file in my test-project repository"

**Push code:**
"Add this Python code to my repository as main.py: [your code]"

---

## Adding Multiple MCPs

If you have other MCPs (like VAPI), your config file should look like:
```json
{
  "mcpServers": {
    "github": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-github"],
      "env": {
        "GITHUB_PERSONAL_ACCESS_TOKEN": "YOUR_TOKEN_HERE"
      }
    },
    "other-mcp": {
      "command": "...",
      "env": {
        "API_KEY": "..."
      }
    }
  }
}
```

---

## Troubleshooting

| Problem | Solution |
|---------|----------|
| MCP not showing | Check JSON syntax, restart Claude Desktop |
| "Command not found" | Install Node.js and restart computer |
| Auth errors | Generate a new token, update config |
| Permission denied | Check token has correct scopes |

---

## Security Best Practices

⚠️ **Never share your actual token publicly!**

- Don't commit your config file to GitHub
- Regenerate token if accidentally exposed
- Use minimum required scopes
- Set token expiration dates

---

## Resources

- [GitHub MCP Official Repo](https://github.com/modelcontextprotocol/servers)
- [GitHub Token Documentation](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token)
- [Claude Desktop Download](https://claude.ai/download)

---

*Guide created by: Ankur Kushwaha*
*Part of my AI Learning Journey: [ai-learning-os](https://github.com/ankurkushwaha9/ai-learning-os)*
