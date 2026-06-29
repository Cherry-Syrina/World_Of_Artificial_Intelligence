# 1. Introduction to Prompt Engineering

## What is a Prompt?
- Prompt = Input/Instruction jo hum AI model ko dete hain.
- AI us prompt ke basis par response (output) generate karta hai.

**Example**
```text
Prompt:
Translate the following text from English to Spanish.
Hello, how are you today?

Output:
¿Hola, cómo estás hoy?
```

## What is Prompt Engineering?
Prompt Engineering = AI se better aur accurate output lene ke liye prompts ko design aur optimize karne ki technique.

## Why is it Important?
- Better quality responses milte hain.
- Complex tasks ko effectively solve kar sakte hain.
- AI ki limitations ko reduce karne me help karta hai.
- Different use cases ke liye prompts optimize kiye ja sakte hain.

## Key Takeaways
- Prompt = Instruction to AI.
- Output ki quality prompt par depend karti hai.
- Good prompts → Better AI responses.
- Prompt Engineering is an essential skill for working with Generative AI.


---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# 2. Basics of Foundation Models (FMs)

## What is Generative AI?
- Generative AI naya content create karta hai.
- Examples:
  - Text
  - Images
  - Videos
  - Music
  - Conversations

## What are Foundation Models (FMs)?
- Foundation Models (FMs) = Large pre-trained AI models.
- Huge amount of data par train hote hain.
- Self-supervised learning use karte hain.

## Why are FMs Special?
- Traditional ML models se kaafi bade hote hain.
- Deep Neural Networks use karte hain.
- Multiple tasks perform kar sakte hain bina alag model banaye.

## Common Use Cases
- Text Generation
- Text Summarization
- Question Answering
- Chatbots
- Information Extraction
- Image Generation

## Fine-Tuning
- FMs ko specific task ke liye customize (fine-tune) kiya ja sakta hai.

## Popular Foundation Models
- Amazon Titan
- Amazon Nova
- Meta Llama 2
- Anthropic Claude
- AI21 Jurassic-2 Ultra

## Key Takeaways
- Generative AI uses Foundation Models.
- FMs are large, pre-trained, and general-purpose.
- One FM can perform many different AI tasks.
- FMs can be fine-tuned for domain-specific applications.
- <img width="1175" height="587" alt="image" src="https://github.com/user-attachments/assets/2a23a22f-b941-4646-b717-dce14fee4f23" />
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# 3. Self-Supervised Learning

## What is Self-Supervised Learning?
- Labels manually dene ki zarurat nahi hoti.
- Model data se hi automatically labels generate karta hai.
- Isi technique se zyadatar Foundation Models pre-train hote hain.

## During Training
Model seekhta hai:
- Meaning of words
- Context
- Relationship between words

**Example:**
`drink` → Noun (beverage) ya Verb (consume liquid), context ke according.

---

# 4. RLHF (Reinforcement Learning from Human Feedback)

## What is RLHF?
- Humans AI ke outputs ko feedback dete hain.
- Model us feedback se apne responses improve karta hai.
- Goal: AI ko human preferences ke according align karna.

---

# 5. Fine-Tuning

## What is Fine-Tuning?
- Pre-trained model ko kisi specific task/domain ke liye train karna.
- Small & domain-specific dataset use hota hai.
- Model ki performance improve hoti hai.

## Types of Fine-Tuning

### 1. Instruction Fine-Tuning
- Model ko examples diye jate hain ki kisi instruction ka response kaise dena hai.
- Prompt Tuning bhi iska ek type hai.

### 2. RLHF
- Human feedback use karke model ko improve kiya jata hai.

## Example
Medical chatbot banane ke liye:
- Base Model → Pre-trained FM
- Fine-Tune → Medical journals & healthcare data

---

# 6. Prompt Engineering vs Fine-Tuning

| Prompt Engineering | Fine-Tuning |
|--------------------|------------|
| Sirf prompt change karte hain | Model ko retrain karte hain |
| Labeled data nahi chahiye | Labeled data chahiye |
| Fast & Low Cost | Slow & Expensive |
| No training infrastructure | Training infrastructure required |

## Key Takeaways
- Self-Supervised Learning → Automatic labels generate karta hai.
- RLHF → Human feedback se model improve hota hai.
- Fine-Tuning → Specific domain/task ke liye model customize karta hai.
- Prompt Engineering → Better output ke liye prompts optimize karta hai, bina model retrain kiye.
  -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  # 7. Types of Foundation Models (FMs)

## 1. Text-to-Text Models (LLMs)

### What are they?
- Text input lete hain aur text output generate karte hain.
- Large Language Models (LLMs) kehlate hain.
- Huge amount of text data par pre-trained hote hain.

### Use Cases
- Text Summarization
- Question Answering
- Information Extraction
- Content Writing (Blogs, Emails, Product Descriptions)
- Translation
- Chatbots
  <img width="657" height="452" alt="image" src="https://github.com/user-attachments/assets/8a1169b8-150d-4c21-aeac-8ab934babd5c" />


---

## 2. Text-to-Image Models

### What are they?
- Text prompt ko image me convert karte hain.
- User ke description ke according image generate karte hain.

### Use Cases
- AI Art
- Logo Design
- Posters
- Marketing Images
- Illustrations

### Popular Models
- DALL·E
- Imagen
- Stable Diffusion
- Midjourney
<img width="697" height="502" alt="image" src="https://github.com/user-attachments/assets/13509ea7-2abb-4e81-b9c5-73a4eea81d90" />

---

## Key Takeaways
- **Text → Text** = Generate text responses.
- **Text → Image** = Generate images from text prompts.
- Dono Foundation Models ke common applications hain.
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# 8. NLP (Natural Language Processing)

## What is NLP?
- NLP enables computers to understand, interpret, and generate human language.
- Used for analyzing text or speech.

### Common NLP Tasks
- Text Classification
- Sentiment Analysis
- Translation
- Chatbots
- Speech Recognition

> **Note:** Traditional NLP used preprocessing (tokenization, stemming, etc.), but modern LLMs can handle most of these automatically.

---

# 9. RNN (Recurrent Neural Network)

## What is RNN?
- Neural network designed for sequential data.
- Uses memory to remember previous inputs.

### Applications
- NLP
- Speech Recognition
- Machine Translation

### Limitations
- Slow to train
- Cannot process data in parallel
- Difficult to train on long sequences

---

# 10. Transformer Architecture

## What is a Transformer?
- Deep learning architecture used in modern LLMs.
- Processes all input tokens **simultaneously (parallel processing)**.

### Components
- **Encoder** → Converts input into embeddings.
- **Decoder** → Generates output from embeddings.

> Most modern LLMs mainly use the **Decoder**.

### Advantages
- Faster training
- Parallel processing
- Better performance on long text
- Foundation of modern LLMs (like ChatGPT)

---

# RNN vs Transformer

| RNN | Transformer |
|------|-------------|
| Sequential processing | Parallel processing |
| Slow training | Fast training |
| Uses memory | Uses Attention mechanism |
| Hard to scale | Easily scalable |
| Older architecture | Modern architecture |

## Key Takeaways
- NLP helps machines understand human language.
- RNN works well for sequential data but is slow.
- Transformers process data in parallel and power modern LLMs.
- Most current LLMs are based on the Transformer architecture.
- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# 11. Diffusion Model

## What is a Diffusion Model?
- Deep learning model used mainly for **AI image generation**.
- Works in **2 steps**:

### 1. Forward Diffusion
- Original image me gradually **noise** add kiya jata hai.
- End me image almost completely noisy ho jati hai.

### 2. Reverse Diffusion
- Model noise ko step-by-step remove karta hai.
- Final result → New image generate hoti hai.

> **U-Net** model noise ko predict aur remove karne me help karta hai.

## Key Takeaways
- Mainly used for **Text-to-Image generation**.
- Learns to convert noisy images into realistic images.

---

# 12. Large Language Models (LLMs)

## What are LLMs?
- LLMs are a subset of **Foundation Models (FMs)**.
- Trillions of words par train hote hain.
- Human-like text understand aur generate kar sakte hain.

## Capabilities
- Question Answering
- Text Summarization
- Content Writing
- Code Generation
- Recommendations
- Conversations

## Real-World Applications
- Marketing Content
- Legal Document Summary
- Financial Research
- Healthcare Assistance
- Software Development

## Key Takeaways
- Every LLM is a Foundation Model.
- Every Foundation Model is **not** necessarily an LLM.

---

# 13. Neural Network Layers in Transformers

## 1. Embedding Layer
- Text ko **vectors (embeddings)** me convert karta hai.
- Context aur meaning capture karta hai.

## 2. Feedforward Layer
- Embeddings ko process aur refine karta hai.
- Better understanding develop karta hai.

## 3. Attention Mechanism ⭐
- Sentence ke important words par focus karta hai.
- Context samajhne me help karta hai.
- Transformer ka sabse important component hai.

---

# LLM Processing Flow

```text
Input Text
      ↓
Embedding Layer
      ↓
Attention Mechanism
      ↓
Feedforward Layer
      ↓
Generated Output
```

## Key Takeaways
- **Embedding** → Text → Vectors
- **Attention** → Important words par focus
- **Feedforward** → Better understanding & output
- **Diffusion Models** → Image Generation
- **LLMs** → Text Understanding & Generation
