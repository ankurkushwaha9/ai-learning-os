# 💪 Discord Virtual Assistant - Coach Buddy

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Discord.py](https://img.shields.io/badge/Discord.py-2.0+-5865F2.svg)](https://discordpy.readthedocs.io/)
[![Groq](https://img.shields.io/badge/Groq-Llama_3.3-orange.svg)](https://groq.com/)
[![Status](https://img.shields.io/badge/Status-✅_Complete-brightgreen.svg)]()

---

## 📋 Project Overview

| Attribute | Details |
|-----------|---------|
| **Project Name** | Discord Virtual Assistant - Coach Buddy |
| **Category** | Medium Project |
| **Status** | ✅ Complete |
| **Duration** | 1 day |
| **Course** | MIT AAOT Module 3 Assignment |
| **Repository** | [GitHub](https://github.com/ankurkushwaha9/Discord-Virtual-Assistant) |

---

## 🎯 Problem Statement

Create a Discord bot that integrates with an AI service to provide intelligent, conversational responses to users within a Discord server.

---

## 💡 Solution

**Coach Buddy** - A motivational Discord bot powered by Groq AI (Llama 3.3 70B) that encourages users and helps them achieve their goals through supportive, AI-powered conversations.

---

## ✨ Features

| Feature | Description |
|---------|-------------|
| 🤖 **AI-Powered Responses** | Uses Groq's Llama 3.3 70B model for intelligent conversations |
| 💪 **Motivational Personality** | Custom system prompt creates an encouraging, coach-like persona |
| ⚡ **Fast Response** | Groq's optimized inference for quick replies |
| 🛠️ **Simple Commands** | Easy to use command structure |
| 🔒 **Secure** | Environment variables protect API keys |

---

## 🎮 Commands

| Command | Description |
|---------|-------------|
| `$hello` | Get a friendly greeting from Coach Buddy |
| `$coach [question]` | Ask Coach Buddy anything! |
| `$help` | Display available commands |

---

## 🔧 Tech Stack

| Technology | Purpose |
|------------|---------|
| Python 3.8+ | Core programming language |
| discord.py | Discord API wrapper |
| Groq API | AI inference (Llama 3.3 70B) |
| python-dotenv | Environment variable management |

---

## 🏗️ Architecture

```
┌─────────────────┐     ┌─────────────────┐     ┌─────────────────┐
│   Discord       │────▶│   Bot Server    │────▶│   Groq API      │
│   (User Input)  │     │   (Python)      │     │   (Llama 3.3)   │
└─────────────────┘     └─────────────────┘     └─────────────────┘
        │                       │                       │
        │                       ▼                       │
        │               ┌─────────────────┐             │
        │               │  Coach Buddy    │             │
        │               │  System Prompt  │             │
        │               └─────────────────┘             │
        │                       │                       │
        ◀───────────────────────┴───────────────────────┘
                    (AI Response)
```

---

## 📁 Project Structure

```
Discord-Virtual-Assistant/
├── discord-groq.py      # Main bot code with Coach Buddy personality
├── .env.example         # Template for environment variables
├── .env                 # Actual secrets (gitignored)
├── .gitignore           # Files to ignore in git
├── requirements.txt     # Python dependencies
└── README.md            # Documentation
```

---

## 🚀 Setup Steps

1. Clone the repository
2. Install dependencies: `pip install -r requirements.txt`
3. Create `.env` file with Discord TOKEN and GROQ_API_KEY
4. Run: `python discord-groq.py`

---

## 📸 Demo

### Bot Online
```
Coach Buddy is online! Logged in as Virtual Assistant#6147
Ready to motivate and assist!
----------------------------------------
```

### Sample Interaction
```
User: $hello
Coach Buddy: Hey there, champion! 💪 Coach Buddy here, ready to help you crush your goals!

User: $coach How can I stay motivated while studying?
Coach Buddy: I'm so proud of you for taking the first step towards your goals...
```

---

## 📚 Learning Outcomes

1. **Discord Bot Development** - Learned Discord.py library and event-driven architecture
2. **AI Integration** - Connected Groq API for LLM inference
3. **Environment Security** - Implemented secure credential management
4. **System Prompts** - Designed effective AI personality through prompting
5. **Python Async** - Used async/await patterns for Discord events

---

## 🙏 Credits

- Based on [AAOT Module 3 Demo](https://github.com/tobah59x/AAOT-Mod3-Demo) by Ali Tobah
- Original Discord bot template by [Dr. Abel Sanchez](https://github.com/abelsan/bot)
- MIT Professional Education: Agentic AI and Open Tools (AAOT) course

---

## 🔗 Links

- **Repository:** [GitHub](https://github.com/ankurkushwaha9/Discord-Virtual-Assistant)
- **Course:** MIT AAOT - Module 3

---

*Created by Ankur Kushwaha - December 2025*
