# VAPI MCP Setup Guide

> Connect Claude Desktop to VAPI for AI-powered voice calls and phone agents

**Status:** ✅ Active
**Added:** December 2025
**Difficulty:** Beginner-Friendly

---

## What This MCP Does

The VAPI MCP allows Claude Desktop to:
- Create and manage outbound phone calls
- Retrieve call details, transcripts, and outcomes
- List recent calls with filtering options
- Stop active calls
- List available AI assistants for calls

---

## Why You Need This

With VAPI MCP, you can tell Claude:
- "Call this phone number with my AI assistant"
- "Show me the transcript from my last call"
- "List all calls from today"
- "Stop the current active call"

Build voice AI agents without writing code!

---

## Prerequisites

Before starting, you need:
1. A VAPI account (sign up at [vapi.ai](https://vapi.ai))
2. Claude Desktop app installed (not the web version)
3. VAPI API Key
4. A configured phone number in VAPI (optional, for outbound calls)

---

## Step-by-Step Setup

### Step 1: Create VAPI Account

1. Go to [vapi.ai](https://vapi.ai)
2. Sign up for an account
3. Complete the onboarding process

### Step 2: Get Your VAPI API Key

1. Log into your VAPI dashboard
2. Go to **Settings** or **API Keys** section
3. Copy your API key
4. Save it somewhere safe

### Step 3: Get Your Phone Number ID (Optional)

If you want to make outbound calls:
1. In VAPI dashboard, go to **Phone Numbers**
2. Add a phone number or use an existing one
3. Copy the **Phone Number ID** (not the phone number itself)

### Step 4: Create the MCP Server Files

The VAPI MCP requires a custom setup. Here's how:

1. Create a folder for your MCP server:
   - Example: `D:\AI Study\MCP Server\vapi-mcp-server\`

2. Inside this folder, create a file called `start-vapi.bat` with:
```batch
@echo off
npx -y @vapi-ai/mcp-server
```

### Step 5: Configure Claude Desktop

1. Close Claude Desktop completely

2. Open the config file:
   - **Windows:** Press Win+R, type `%APPDATA%\Claude`, press Enter
   - **Mac:** Open Finder, press Cmd+Shift+G, type `~/Library/Application Support/Claude`

3. Open `claude_desktop_config.json`

4. Add this configuration:
```json
{
  "mcpServers": {
    "vapi": {
      "command": "D:\\YOUR_PATH\\vapi-mcp-server\\start-vapi.bat",
      "env": {
        "VAPI_API_KEY": "YOUR_VAPI_API_KEY_HERE",
        "VAPI_PHONE_NUMBER_ID": "YOUR_PHONE_NUMBER_ID_HERE"
      }
    }
  }
}
```

5. Replace:
   - `D:\\YOUR_PATH\\` with your actual folder path
   - `YOUR_VAPI_API_KEY_HERE` with your VAPI API key
   - `YOUR_PHONE_NUMBER_ID_HERE` with your phone number ID

6. Save the file

7. Restart Claude Desktop

### Step 6: Verify It Works

In Claude Desktop, ask:
"What MCPs do you have access to?"

You should see VAPI listed with its capabilities.

---

## Example Commands

Once set up, try these:

**List available assistants:**
"Show me my available VAPI assistants"

**Make a call:**
"Call +1234567890 using my customer service assistant"

**Check recent calls:**
"List my recent VAPI calls from today"

**Get call transcript:**
"Show me the transcript from my last call"

---

## Combining with GitHub MCP

You can have both MCPs active! Your config file should look like:
```json
{
  "mcpServers": {
    "vapi": {
      "command": "D:\\AI Study\\MCP Server\\vapi-mcp-server\\start-vapi.bat",
      "env": {
        "VAPI_API_KEY": "YOUR_VAPI_API_KEY",
        "VAPI_PHONE_NUMBER_ID": "YOUR_PHONE_NUMBER_ID"
      }
    },
    "github": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-github"],
      "env": {
        "GITHUB_PERSONAL_ACCESS_TOKEN": "YOUR_GITHUB_TOKEN"
      }
    }
  }
}
```

---

## Troubleshooting

| Problem | Solution |
|---------|----------|
| MCP not showing | Check JSON syntax, verify file paths |
| "Command not found" | Ensure Node.js is installed |
| API errors | Verify your VAPI API key is correct |
| Call fails | Check phone number ID and permissions |
| Path not found | Use double backslashes in Windows paths |

---

## Security Best Practices

⚠️ **Never share your actual API keys publicly!**

- Don't commit config files with real keys to GitHub
- Regenerate keys if accidentally exposed
- Use separate API keys for testing and production
- Monitor your VAPI usage for unexpected activity

---

## Use Cases

1. **Customer Service Bot:** Automate outbound follow-up calls
2. **Appointment Reminders:** Call customers about upcoming appointments
3. **Survey Calls:** Conduct automated phone surveys
4. **Lead Qualification:** AI-powered initial contact with leads

---

## Resources

- [VAPI Official Website](https://vapi.ai)
- [VAPI Documentation](https://docs.vapi.ai)
- [VAPI MCP Server](https://github.com/VapiAI/mcp-server)
- [Claude Desktop Download](https://claude.ai/download)

---

*Guide created by: Ankur Kushwaha*
*Part of my AI Learning Journey: [ai-learning-os](https://github.com/ankurkushwaha9/ai-learning-os)*
