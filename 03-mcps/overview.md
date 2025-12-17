# Understanding MCPs

---

## What is MCP?

**Model Context Protocol (MCP)** is a standard that allows AI models like Claude to interact with external tools, services, and data sources.

---

## How MCPs Work

```
┌─────────────────┐
│     Claude      │
└────────┬────────┘
         │
    MCP Protocol
         │
┌────────▼────────┐
│   MCP Server    │
│  (Tool/Service) │
└─────────────────┘
```

1. Claude receives a request
2. Identifies relevant MCP tool
3. Sends structured request to MCP server
4. MCP server performs action
5. Returns results to Claude
6. Claude processes and responds

---

## Types of MCPs

### File System MCPs
- Google Drive
- Local files
- Dropbox

### API MCPs
- GitHub
- Slack
- External APIs

### Service MCPs
- VAPI (Voice)
- Databases
- Search engines

---

## Benefits

- **Extended Capabilities:** Do more than just chat
- **Real Data Access:** Work with actual files and services
- **Automation:** Perform actions automatically
- **Integration:** Connect your tools together

---

## Limitations

- Requires proper configuration
- Limited by MCP server capabilities
- Security considerations
- May have usage limits

---

*MCPs transform Claude from assistant to capable agent!*