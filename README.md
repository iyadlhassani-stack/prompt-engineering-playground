# Prompt Engineering Playground

## 🎯 Project Objective

This project explores the behavior of a **Large Language Model (LLM) used on its own**, without Retrieval-Augmented Generation (RAG), external databases, or paid APIs.

The goal is **not** to build a production-ready tool, but to **understand the fundamental limitations of standalone LLMs**, especially:
- instruction following,
- format compliance,
- response stability,
- hallucinations,
- and the real impact of prompt design.

---

## 🧠 Why this project?

Before using advanced architectures such as **RAG**, it is important to understand **how a language model behaves without any external context**.

This project acts as a **learning baseline** to:
- observe how an LLM responds to different prompts,
- see why prompt engineering alone is not sufficient,
- better understand why RAG-based systems are needed.

---

## ⚙️ Tech Stack

- Python  
- Google Colab  
- Hugging Face Transformers  
- Model: `google/flan-t5-base`  
- PyTorch  

👉 No heavy local models  
👉 No paid APIs  
👉 Intentionally simple setup  

---

## 🧪 Experiments Overview

The notebook includes several prompt experiments:

1. Simple and vague prompts  
2. Role-based prompts (e.g. *"You are an expert..."*)  
3. Explicit constraints (format, refusal, "I don't know")  
4. Strict output formats (bullet points, structured outputs)  

Each experiment focuses on observing:
- whether the model follows instructions,
- whether responses vary with prompt changes,
- how often the model generalizes or hallucinates.

---

## 🔍 Key Observations

- The model almost always produces an answer, even when the question is ambiguous.
- Different prompts can result in **exactly the same output**.
- Formatting instructions are **not guaranteed** unless strongly enforced.
- With `temperature = 0`, responses are stable but often overly simplistic.
- The model does not verify truth — it generates what is **statistically plausible**.

👉 A prompt acts as a **fragile interface**, not as executable logic.

---

## 🔁 Difference Compared to a RAG-Based Approach

### Without RAG (this project)
- The model answers using only its internal knowledge.
- It may hallucinate or oversimplify.
- There is no way to inspect or verify sources.
- "I don't know" behavior is unreliable.

### With RAG
- The model answers **based on retrieved documents**.
- Responses change depending on the data.
- Sources can be inspected.
- Refusal becomes logical (no relevant context → no answer).

👉 This project demonstrates **why RAG is necessary**, not just convenient.

---

## 📂 Repository Structure

prompt-engineering-playground/
│
├── 01_basic_prompting.ipynb
├── requirements.txt
└── README.md

---

## 🧭 Conclusion

This project is a **deliberately simple first step** toward understanding how language models actually behave.

By clearly exposing the limitations of standalone LLMs, it provides a solid foundation for moving toward **RAG-based systems** with real understanding rather than treating them as black boxes.
