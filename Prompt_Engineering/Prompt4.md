# Advanced Prompt Techniques

## Introduction
- Basic prompt techniques har task ke liye sufficient nahi hote.
- Advanced techniques better reasoning aur accurate responses ke liye use ki jati hain.

---

# 1. Self-Consistency Prompting

## What is Self-Consistency?
- Chain-of-Thought (CoT) ka advanced version hai.
- AI ek hi reasoning path follow nahi karta.
- Multiple reasoning paths generate karta hai.
- Sabhi answers compare karke **most consistent/final answer** choose karta hai.

### How It Works

```text
Question
    ↓
Multiple Reasoning Paths
    ↓
Compare Results
    ↓
Most Consistent Answer
```

### Why Use It?
- Better accuracy
- Reduces reasoning mistakes
- Useful for logical & mathematical problems

### Best Use Cases
- Arithmetic problems
- Logical reasoning
- Complex decision making
- Common-sense reasoning

### Example

**Question**

```text
When I was 10, my sister was half my age.
Now I'm 40.
How old is my sister?
```

**Answer**

```text
When I was 10 → Sister was 5.

Age difference = 5 years.

Now I'm 40 → Sister = 35 years.
```

---

# Chain-of-Thought vs Self-Consistency

| Chain-of-Thought | Self-Consistency |
|------------------|------------------|
| One reasoning path | Multiple reasoning paths |
| Faster | More accurate |
| Higher chance of mistakes | Lower chance of mistakes |
| Good for simple reasoning | Best for complex reasoning |

---

# Key Takeaways

- Self-Consistency is an advanced version of CoT.
- Generates multiple reasoning paths before answering.
- Chooses the most consistent answer.
- Improves reasoning accuracy.
- Best for math, logic, and multi-step reasoning tasks.
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# 2. Tree of Thoughts (ToT) Prompting

<img width="786" height="755" alt="image" src="https://github.com/user-attachments/assets/e94036f2-09f1-44c0-9c70-fd9aadd550bc" />

## What is Tree of Thoughts (ToT)?
- Advanced reasoning technique based on **Chain-of-Thought (CoT)**.
- Instead of following **one reasoning path**, AI explores **multiple possible paths**.
- Best path is selected after evaluating different options.

### How It Works

```text
Question
    │
 ┌──┼──┐
Path1 Path2 Path3
 │      │      │
Evaluate All Paths
       │
Best Solution
```

### CoT vs ToT

| Chain-of-Thought (CoT) | Tree of Thoughts (ToT) |
|-------------------------|------------------------|
| Single reasoning path | Multiple reasoning paths |
| Sequential thinking | Tree-like branching |
| Faster | More accurate |
| Best for simple problems | Best for complex planning & reasoning |

---

## Advantages
- Explores multiple solutions.
- Better planning and decision making.
- AI can evaluate its own choices.
- Improves accuracy on difficult tasks.

---

## Best Use Cases
- Complex reasoning
- Planning tasks
- Strategy problems
- Creative writing
- Puzzle solving
- Mathematical reasoning

---

## Example: Game of 24

**Task:** Use four numbers and `+ - × ÷` to make **24**.

Input:
```text
4, 9, 10, 13
```

Possible Solution:
```text
(10 - 4) × (13 - 9) = 24
```

Instead of trying only one solution (CoT), **ToT explores multiple calculation paths and selects the correct one.**

---

## Key Takeaways

- ToT is an advanced version of CoT.
- Uses **tree-like branching** instead of a single reasoning path.
- Evaluates multiple possible solutions.
- Best for planning, puzzles, and complex reasoning tasks.
- Higher accuracy than CoT for difficult problems.
- --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# 3. Retrieval Augmented Generation (RAG)

## What is RAG?
- **RAG (Retrieval Augmented Generation)** is a technique where the LLM first **retrieves relevant information** from external sources and then generates the answer.
- Model **does not retrain** or change its weights.

  <img width="1240" height="461" alt="image" src="https://github.com/user-attachments/assets/de6eb368-04fd-49b2-96bc-d0c0c7323f4c" />


### How It Works

```text
User Query
      ↓
Retrieve Relevant Documents
      ↓
Provide Context to LLM
      ↓
Generate Accurate Answer
```
<img width="1466" height="846" alt="image" src="https://github.com/user-attachments/assets/bb732005-4cb9-4713-aae3-076069c62a10" />


---

## Data Sources
RAG can retrieve data from:
- Documents
- Databases
- APIs
- Knowledge Bases

---

## Advantages
- No need for Fine-Tuning
- Lower cost
- Uses latest information
- Reduces outdated responses
- Better domain-specific answers

---

## RAG vs Fine-Tuning

| RAG | Fine-Tuning |
|------|------------|
| Retrieves external data | Retrains the model |
| Model weights unchanged | Model weights updated |
| Low cost | Expensive |
| Uses latest information | Uses fixed training data |
| Easy to update | Requires retraining |

---

## Use Cases
- Company Chatbots
- Customer Support
- Enterprise Search
- Document Q&A
- Medical & Legal Assistants

---

## RAG Workflow

```text
Knowledge Base
      ↓
Retrieve Relevant Documents
      ↓
LLM + Retrieved Context
      ↓
Final Response
```

---

## Key Takeaways
- RAG = **Retrieve → Augment → Generate**
- Retrieves relevant information before answering.
- Doesn't modify model weights.
- More cost-effective than Fine-Tuning.
- Best for applications requiring up-to-date knowledge.
- --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# 4. Automatic Reasoning and Tool-use (ART)

## What is ART?
- **ART (Automatic Reasoning and Tool-use)** is an advanced prompting technique for **multi-step reasoning**.
- Builds on **Chain-of-Thought (CoT)**.
- Uses **few-shot examples + external tools** to solve complex tasks.
  <img width="736" height="665" alt="image" src="https://github.com/user-attachments/assets/96ed8279-4bf4-4a94-b4f6-838775503b5d" />


### How It Works

```text
Question
      ↓
Select Similar Examples
      ↓
Use External Tools
(Search, Code, etc.)
      ↓
Reason Step-by-Step
      ↓
Final Answer
```

---

## Features
- Uses task libraries with examples.
- Supports external tools (Search, Code, APIs).
- Better for unseen or complex tasks.
- Easy to update by modifying task libraries.

---

## Best Use Cases
- Multi-step reasoning
- Coding tasks
- Search-based questions
- Tool-assisted AI agents

---

# 5. ReAct Prompting (Reason + Act)

## What is ReAct?
- **ReAct = Reasoning + Acting**
- AI first **thinks (reasoning)** and then **uses external tools** to complete the task.

Unlike CoT, ReAct can access real-world information using tools.

---

## How It Works

```text
Question
      ↓
Thought
      ↓
Choose Tool
      ↓
Action
      ↓
Observation
      ↓
Repeat (if needed)
      ↓
Final Answer
```

---

## External Tools
- Calculator
- Search Engine
- SQL Database
- Wikipedia
- APIs

---

## Advantages
- More accurate answers
- Reduces hallucinations
- Can access updated information
- Suitable for real-world tasks

---

## Example

### Without Tool
```text
Question:
3.14^0.12345

LLM guesses the answer ❌
```

### With Calculator Tool
```text
Thought
↓
Use Calculator
↓
Correct Result
↓
Final Answer ✅
```

---

## Best Use Cases
- Mathematical calculations
- Database queries
- Information retrieval
- AI Agents
- Enterprise assistants

---

# ART vs ReAct

| ART | ReAct |
|------|--------|
| Multi-step reasoning | Reason + Action |
| Uses few-shot examples | Uses external tools dynamically |
| Tool-assisted reasoning | Tool-assisted execution |
| Good for complex workflows | Good for real-time tasks |

---

# Key Takeaways

- **ART** → Multi-step reasoning using examples + tools.
- **ReAct** → Combines reasoning with external actions.
- ReAct reduces hallucinations by using real-world tools.
- Both techniques improve accuracy for complex tasks.
