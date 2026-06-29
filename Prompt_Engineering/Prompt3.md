# Basic Prompt Techniques

## What are Prompt Techniques?
- Different ways of writing prompts to get better responses from AI.
- Choosing the right technique depends on the task.

---

# 1. Zero-Shot Prompting
<img width="642" height="427" alt="image" src="https://github.com/user-attachments/assets/b9488f2f-8d2c-478a-a544-7557bedbb7d8" />


## Definition
- AI ko **sirf task** diya jata hai.
- **No examples** are provided.

### Best For
- Simple tasks
- Modern LLMs (ChatGPT, Claude, Gemini, etc.)

### Example

```text
Prompt:
Classify the sentiment:
"I love this phone."

Output:
Positive
```

### Tips
- Works better with large LLMs.
- Clear instructions improve results.

---

# 2. Few-Shot Prompting
<img width="652" height="412" alt="image" src="https://github.com/user-attachments/assets/d17cc8f7-1516-4e6a-a70d-ea07b418fdd9" />


## Definition
- AI ko task ke **2–5 examples** diye jate hain.
- Model examples dekhkar same pattern follow karta hai.

### Best For
- Classification
- Structured outputs
- Consistent formatting

### Example

```text
Positive → "Great product"

Negative → "Worst experience"

"This movie is amazing"

Output:
Positive
```

### Advantages
- Better accuracy
- Consistent responses
- Useful for complex tasks

---

# Zero-Shot vs Few-Shot

| Zero-Shot | Few-Shot |
|------------|----------|
| No examples | Examples provided |
| Faster | More accurate |
| Good for simple tasks | Better for complex tasks |

---

# 3. Chain-of-Thought (CoT) Prompting
<img width="617" height="391" alt="image" src="https://github.com/user-attachments/assets/9107b94d-10d1-497c-afef-76d4d815ac67" />


## Definition
- AI ko **step-by-step reasoning** karne ke liye guide karna.
- Complex problems solve karne ke liye use hota hai.

### Common Phrase

```text
Think step by step.
```

### Best For
- Math
- Logical reasoning
- Multi-step problems
- Decision making

### Example

```text
Question:
Which vehicle requires a larger down payment?

Think step by step.
```

AI pehle calculation karega, fir final answer dega.

---

# CoT + Zero-Shot

- No examples
- Sirf **"Think step by step"** add karte hain.

Example

```text
Solve this math problem.

Think step by step.
```

---

# CoT + Few-Shot

- Examples bhi dete hain.
- Saath me **Think step by step** bhi likhte hain.

Ye sabse powerful combinations me se ek hai.

---

# Which Technique to Use?

| Task | Best Technique |
|------|----------------|
| Simple Q&A | Zero-Shot |
| Classification | Few-Shot |
| Complex Reasoning | Chain-of-Thought |
| Multi-step Problems | CoT + Few-Shot |

---

# Key Takeaways

- **Zero-Shot** → No examples.
- **Few-Shot** → Few examples provided.
- **Chain-of-Thought (CoT)** → AI reasons step by step.
- **CoT + Few-Shot** → Best for difficult reasoning tasks.
- "Think step by step" is a common trigger for CoT prompting.
