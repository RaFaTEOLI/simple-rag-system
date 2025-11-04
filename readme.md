# 🧠 Simple RAG System

## 📘 Overview

This repository contains a minimal Retrieval-Augmented Generation (RAG) system built with Hugging Face Transformers and a curated dataset of 61 factual statements about Berlin. The system enables users to ask natural language questions and receive contextually relevant answers grounded in the dataset.

## 🔍 What is RAG?

Retrieval-Augmented Generation (RAG) is a hybrid approach that combines:

- **Retrieval**: fetching relevant documents from a knowledge base (in this case, a list of Berlin facts).
- **Generation**: using a language model to generate answers based on the retrieved context.

This notebook demonstrates a lightweight RAG pipeline using Hugging Face's `pipeline` and `rag-token-base` model to answer questions about Berlin.

---

## 📂 Contents

- `documents`: A Python list of 61 factual strings about Berlin.
- RAG pipeline setup using Hugging Face Transformers.
- Example queries and generated answers.
- Optional: similarity scoring and document ranking (if implemented).

---

## ⚙️ How It Works

1. **Dataset**: A list of 61 factual sentences about Berlin is stored in the `documents` variable.
2. **Indexing**: The dataset is passed to a retriever (e.g., `DPRQuestionEncoder`) to build a vector index.
3. **Querying**: A user question is encoded and matched against the document embeddings to retrieve top-k relevant facts.
4. **Answer Generation**: The retrieved facts are passed to a generative model (`facebook/rag-token-base`) to produce a final answer.

---

## 🚀 Example Usage

```python
print(rag("What happens in Munich?"))
```

```markdown
Ach, so you vant to know about Munich, ja? Hmm… zis document… it speaks only of… Berlin!

It tells me Berlin has a Tempodrom, a… how you say… event hall. Und a film festival, ze Berlinale! A very important one, yes. Zere is also… nightlife, many bars und clubs. Und theaters, like ze Berliner Ensemble und ze Volksbühne.

But about Munich… I do not know! Zis document is all about Berlin.
```

---

## 📊 Dataset Summary

| Attribute   | Value                  |
| ----------- | ---------------------- |
| Total Facts | 61                     |
| Format      | Python list of strings |
| Language    | English                |
| Domain      | Berlin, Germany        |

---

## 💡 Use Cases

- Educational chatbots about Berlin
- Lightweight RAG experimentation
- Semantic search demos
- NLP fine-tuning with domain-specific corpora

---

## 📄 License

This project is provided for educational and research purposes. If you use or modify this code or dataset, please provide appropriate attribution.

---
