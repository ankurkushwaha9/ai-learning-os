# How LLMs Work

> A practical understanding for AI builders

---

## The Big Picture

Large Language Models (LLMs) like Claude, GPT, etc. are trained to predict the next word (token) in a sequence. Through training on massive amounts of text, they learn:

- Language patterns and grammar
- Facts and knowledge
- Reasoning patterns
- Different writing styles

---

## Key Concepts

### 1. Token Prediction

At their core, LLMs predict: "Given all the text so far, what's the most likely next token?"

This simple mechanism, at scale, produces remarkably coherent outputs.

### 2. Context Window

Models can only "see" a limited amount of text at once:

| Model | Context Window |
|-------|---------------|
| Claude 3 | 200K tokens |
| GPT-4 | 128K tokens |

**Implication:** Long conversations may lose early context.

### 3. Temperature

- **Low (0-0.3):** Focused, deterministic responses
- **Medium (0.4-0.7):** Balanced creativity
- **High (0.8-1.0+):** More random, creative

### 4. Training Data Cutoff

Models are trained on data up to a certain date. They don't know about events after their cutoff.

---

## Implications for Prompting

1. **Be explicit** - The model continues patterns, so set them clearly
2. **Provide context** - More relevant context = better outputs
3. **Verify facts** - Models can hallucinate, especially about recent events
4. **Iterate** - First output isn't always best

---

*You don't need to understand the math, but knowing these concepts helps!*