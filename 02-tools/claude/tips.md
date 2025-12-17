# Claude Tips & Tricks

---

## 🎯 Getting Better Results

### 1. Use the Right Model
- **Opus:** Complex reasoning, nuanced tasks
- **Sonnet:** Balanced performance
- **Haiku:** Quick, simple tasks

### 2. Leverage Long Context
Claude can handle ~200K tokens. Use this for:
- Analyzing long documents
- Providing extensive context
- Processing multiple files

### 3. Ask for Explanations
```
"Explain your reasoning"
"Walk me through your thought process"
"Why did you choose this approach?"
```

---

## 💡 Power User Techniques

### XML Tags for Structure
```xml
<context>
Background information here
</context>

<task>
What you want done
</task>

<format>
How you want the output
</format>
```

### Multi-Step Tasks
Break complex tasks into steps and tackle sequentially.

### Artifacts for Code/Documents
Ask Claude to create artifacts for substantial outputs.

---

## 🔧 With MCPs

- Claude can access external tools
- Enable relevant MCPs for your workflow
- Combine multiple tools for complex tasks

---

## 🚫 What Doesn't Work Well

- Very recent events (use search)
- Precise calculations (use code execution)
- Real-time data (use appropriate MCPs)
- Tasks requiring actual memory between chats

---

*Experiment and find what works for your use cases!*