# 🤖 Lyzr Customer Support Multi-Agent System

[![Lyzr Studio](https://img.shields.io/badge/Lyzr-Agent_Studio-blue.svg)](https://studio.lyzr.ai/)
[![OpenAI](https://img.shields.io/badge/OpenAI-GPT--4o--mini-412991.svg)](https://openai.com/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)
[![Status](https://img.shields.io/badge/Status-✅_Complete-brightgreen.svg)]()

---

## 📋 Project Overview

| Attribute | Details |
|-----------|---------|
| **Project Name** | Lyzr Customer Support Multi-Agent System |
| **Category** | Medium Project |
| **Status** | ✅ Complete |
| **Duration** | 2-3 days |
| **Repository** | [GitHub](https://github.com/ankurkushwaha9/lyzr-customer-support-agents) |

---

## 🎯 Problem Statement

Create a production-ready multi-agent customer support system that can intelligently route and handle diverse customer inquiries including product questions, refund policies, and order tracking.

---

## 💡 Solution

A hierarchical multi-agent architecture using **Lyzr Agent Studio** with:
- **Manager Agent** (Orchestrator) - Routes queries to specialized sub-agents
- **Product Availability Advisor** - Handles product inquiries
- **Refunds & Returns Policy Assistant** - Provides policy guidance
- **Return & Refund Status Reporter** - Tracks refund status

---

## ✨ Features

| Feature | Description |
|---------|-------------|
| 🎯 **Intent Classification** | Automatically classifies customer intent (product_info, refund_policy, tracking) |
| 🔄 **Multi-Agent Orchestration** | Manager agent delegates to specialized sub-agents |
| 📚 **Knowledge Base Integration** | Each agent has dedicated knowledge base for accurate responses |
| 🚀 **Escalation Handling** | Routes complex queries for human intervention |
| 🔒 **Security First** | No API keys in code, placeholder-based configuration |

---

## 🏗️ Architecture

```
┌─────────────────────────────────────────────────────────────────┐
│                     CUSTOMER QUERY                              │
└─────────────────────────────┬───────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────────┐
│              CUSTOMER SUPPORT MANAGER AGENT                     │
│  • Triages incoming requests                                    │
│  • Classifies intent                                            │
│  • Delegates to appropriate sub-agent(s)                        │
└───────┬─────────────────────┬─────────────────────┬─────────────┘
        │                     │                     │
        ▼                     ▼                     ▼
┌───────────────────┐ ┌───────────────────┐ ┌───────────────────┐
│   PRODUCT         │ │    REFUNDS        │ │   REFUND          │
│ AVAILABILITY      │ │   & RETURNS       │ │   STATUS          │
│   ADVISOR         │ │    POLICY         │ │   REPORTER        │
└───────────────────┘ └───────────────────┘ └───────────────────┘
```

---

## 🔧 Tech Stack

| Technology | Purpose |
|------------|---------|
| Lyzr Agent Studio | Multi-agent orchestration platform |
| GPT-4o-mini | LLM for agent reasoning |
| JSON Configuration | Agent definitions |
| Knowledge Bases | Domain-specific information storage |

---

## 📁 Project Structure

```
lyzr-customer-support-agents/
├── README.md
├── LICENSE                 # MIT License
├── CONTRIBUTING.md         # Contribution guidelines
├── CODE_OF_CONDUCT.md      # Community standards
├── SECURITY.md             # Security policy
├── agents/
│   ├── manager/
│   │   └── customer_support_manager.json
│   └── sub-agents/
│       ├── product_availability_advisor.json
│       ├── refunds_returns_policy_assistant.json
│       └── return_refund_status_reporter.json
├── docs/
│   ├── architecture.md
│   └── setup-guide.md
└── .gitignore
```

---

## 🚀 Setup Steps

1. Clone the repository
2. Create a Lyzr Studio account
3. Import agent JSON configurations
4. Set up Knowledge Bases for each sub-agent
5. Link sub-agents to Manager Agent
6. Configure API keys in Lyzr Studio (not in code)

---

## 📚 Learning Outcomes

1. **Multi-Agent Architecture** - Learned hierarchical agent design patterns
2. **Intent Classification** - Implemented smart query routing
3. **Lyzr Agent Studio** - Mastered no-code/low-code agent platform
4. **Knowledge Base Design** - Created domain-specific data stores
5. **Open Source Best Practices** - Implemented LICENSE, CONTRIBUTING, CODE_OF_CONDUCT, SECURITY files

---

## 🌟 Open Source Compliance

This project follows open source best practices with:
- ✅ MIT License
- ✅ Contributing Guidelines
- ✅ Code of Conduct (Contributor Covenant 2.1)
- ✅ Security Policy
- ✅ Comprehensive Documentation

---

## 🔗 Links

- **Repository:** [GitHub](https://github.com/ankurkushwaha9/lyzr-customer-support-agents)
- **Lyzr Studio:** [studio.lyzr.ai](https://studio.lyzr.ai/)
- **Architecture Docs:** [architecture.md](https://github.com/ankurkushwaha9/lyzr-customer-support-agents/blob/main/docs/architecture.md)
- **Setup Guide:** [setup-guide.md](https://github.com/ankurkushwaha9/lyzr-customer-support-agents/blob/main/docs/setup-guide.md)

---

*Created by Ankur Kushwaha - January 2026*
