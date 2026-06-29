# Domain-Specific Prompt Engineering

## What is Domain-Specific Prompt Engineering?
- Har industry (domain) ke liye prompts ko customize karna.
- Different domains ki terminology, rules aur requirements ko dhyan me rakhkar prompt likhna.
- Generic prompts ki jagah domain-specific prompts better aur accurate results dete hain.

---

# Domain Adaptation Principles

## 1. Contextual Specificity
- Prompt me proper background/context do.
- Domain clear mention karo.

### Example
❌ Explain diabetes.

✅ Explain diabetes in **human medicine** for MBBS students.

---

## 2. Terminology Precision
- Domain ke technical terms sahi use karo.
- Ambiguous words avoid karo.

### Example
Finance me:
- ROI
- EBITDA
- CAGR

Healthcare me:
- Diagnosis
- Prognosis
- Symptoms

---

## 3. Regulatory & Ethical Awareness
- Domain ke rules aur ethics follow karo.

Examples:
- Healthcare → HIPAA, Patient Privacy
- Finance → Regulatory Compliance
- Legal → Laws & Jurisdiction

---

## 4. Output Formatting
- Output domain ke standard format me mangna.

Examples:
- Medical Report
- Legal Document
- Financial Report
- Case Summary

---

# Healthcare Prompt Engineering

## Focus Areas
- Patient Confidentiality
- Medical Accuracy
- Safety & Compliance

### Applications
- Patient Summary
- Medical Report Analysis
- Treatment Recommendations
- Clinical Documentation

### Best Practice
- Medical terminology use karo.
- Patient data private rakho.
- Professional medical format follow karo.

---

# Finance Prompt Engineering

## Focus Areas
- Numerical Accuracy
- Financial Terminology
- Regulatory Compliance

### Applications
- Financial Analysis
- Fraud Detection
- Customer Support
- Investment Reports

### Best Practice
- Correct financial terms use karo.
- Time-sensitive data ko accurately process karo.
- Financial regulations follow karo.

---

# Legal Prompt Engineering

## Focus Areas
- Legal Accuracy
- Proper Citations
- Jurisdiction-specific Rules

### Applications
- Legal Document Analysis
- Case Law Research
- Contract Review
- Compliance Checking

### Best Practice
- Correct legal terminology use karo.
- Proper citation format follow karo.
- Applicable jurisdiction mention karo.

---

# Domain Comparison

| Domain | Main Focus |
|---------|------------|
| Healthcare | Patient Privacy, Medical Accuracy |
| Finance | Numerical Accuracy, Compliance |
| Legal | Legal Precision, Citations |

---

# Best Practices

- Domain-specific context do.
- Correct terminology use karo.
- Regulations & ethics follow karo.
- Expected output format mention karo.
- Generic prompts avoid karo.

---

# Key Takeaways

- Har domain ke prompts alag hote hain.
- Context + Technical Terms + Regulations = Better Output.
- Domain-specific prompting Healthcare, Finance aur Legal jaise industries me bahut important hai.
- -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# Model-Specific Prompt Techniques

## What are Model-Specific Prompt Techniques?
- Har LLM ka apna prompt format aur best practices hote hain.
- Ek hi prompt sab models par same result nahi deta.
- Isliye har model ke according prompts optimize karne chahiye.

---

# Popular Models

| Model | Best For |
|--------|----------|
| Amazon Titan | General-purpose tasks |
| Amazon Nova | Text, Image & Video understanding |
| Anthropic Claude | Chat, Coding, Summarization |
| AI21 Jurassic-2 | Zero-shot & Few-shot prompting |

---

# Important Prompt Parameters

| Parameter | Purpose |
|-----------|---------|
| **Temperature** | Creativity vs Accuracy |
| **Top_p** | Diversity of responses |
| **Top_k** | Selects top probable words |
| **Max Tokens** | Maximum output length |
| **Min Tokens** | Minimum output length |
| **Stop Sequences** | Stops generation at specific text |
| **Frequency Penalty** | Reduces repeated words |
| **Presence Penalty** | Encourages new topics |
| **Count Penalty** | Controls repeated token usage |

### Memory Trick

```text
Low Temperature
↓
More Accurate

High Temperature
↓
More Creative
```

---

# Amazon Titan Best Practices

- Clear & simple instructions do.
- Context add karo.
- Output format specify karo.
- Sentence/Bullet count mention karo.
- Default response define kar sakte ho.
- Role-based prompting use karo.
- Code generation support karta hai.
- API me `\n` (new line) use karna helpful hota hai.

### Example

```text
Summarize this article in 3 bullet points.
```

---

# Amazon Nova Best Practices

## Best Practices
- Clear & specific prompts likho.
- Context pehle do.
- Output format define karo.
- Prompt ko sections me divide karo.
- Few-shot examples use karo.
- RAG support ke liye trusted reference text do.
- Long documents ke liye context pehle aur instructions baad me likho.

## Features
- Supports Text
- Images
- Videos
- Long Context Window
- System Prompt

---

# System Role (Amazon Nova)

System Prompt AI ka permanent behavior define karta hai.

Examples:
- Act as a Doctor.
- Act as a Teacher.
- Respond only in JSON.
- Always answer politely.

> **System Prompt > User Prompt** (Higher Priority)

---

# Anthropic Claude Best Practices

- Use **Human** and **Assistant** tags.
- Detailed instructions do.
- XML tags use kar sakte ho.
- Output length specify karo.
- Complex task ko small parts me divide karo.
- "Think step by step" reasoning improve karta hai.

### Example

```text
Human:
Summarize this article.

Assistant:
```

---

# AI21 Jurassic-2 Best Practices

- Zero-shot prompts par achha perform karta hai.
- Few-shot bhi support karta hai.
- Output length specify karo.
- Ambiguous prompts avoid karo.
- Extra context do.
- Long documents me instructions end me likho.

---

# Parameter Guide

| Task | Temperature |
|------|-------------|
| Facts | 0.0 – 0.3 |
| Coding | 0.1 – 0.3 |
| Summarization | 0.2 – 0.5 |
| Creative Writing | 0.7 – 1.0 |

---

# Model Comparison

| Model | Speciality |
|--------|------------|
| Amazon Titan | General-purpose prompts |
| Amazon Nova | Multimodal + Long Context |
| Claude | Chat, Reasoning, XML |
| Jurassic-2 | Zero-shot & Few-shot |

---

# Key Takeaways

- Har model ki prompting strategy alag hoti hai.
- Prompt parameters output ko control karte hain.
- **Temperature** sabse important parameter hai.
- Amazon Nova me **System Prompt** bahut powerful hota hai.
- Claude detailed prompts aur XML tags ke saath best perform karta hai.
- Jurassic-2 zero-shot prompting ke liye optimize hai.
