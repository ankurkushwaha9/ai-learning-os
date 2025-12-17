# Advanced Prompting Techniques

---

## 1. Chain-of-Thought (CoT)

Ask the AI to think step-by-step.

```
Solve this problem step by step:
[Problem]

Show your reasoning at each step before giving the final answer.
```

**When to use:** Complex reasoning, math, logic problems

---

## 2. Few-Shot Learning

Provide examples of desired input/output pairs.

```
Convert these sentences to formal tone:

Input: "Hey, can u help me out?"
Output: "Hello, would you be able to assist me?"

Input: "That's cool, thanks!"
Output: "That is wonderful, thank you."

Input: "gonna need that asap"
Output: [AI completes]
```

**When to use:** Specific formats, consistent style, pattern matching

---

## 3. Role Prompting

Assign a specific persona or expertise.

```
You are a senior software architect with 15 years of experience in distributed systems. Review this architecture proposal and provide feedback focusing on scalability and fault tolerance.
```

**When to use:** Expert advice, specific perspectives, specialized knowledge

---

## 4. Iterative Refinement

Build on previous outputs.

1. Get initial output
2. Ask for specific improvements
3. Request alternatives
4. Combine best elements

---

## 5. Constraint-Based Prompting

```
Write a product description with these constraints:
- Exactly 50 words
- Include 3 benefits
- End with a call-to-action
- Avoid superlatives
```

---

*Practice each technique to understand when it works best.*