# ⚖️ DPDP Legal Assistant • RAG-Powered AI Chatbot
[Link to the website](https://lovable.dev/projects/7c22fcef-7c42-4197-8ebc-2f343f559a48)

> An AI-powered legal assistant that answers questions about India's **Digital Personal Data Protection (DPDP) Act 2023**, built using Retrieval-Augmented Generation (RAG) with production-grade monitoring.

---

## 🧠 What Problem Does This Solve?

The DPDP Act 2023 is India's first comprehensive data privacy law — but it's dense, technical, and hard to navigate for founders, startups, and professionals.

This assistant lets anyone ask plain-English (or Hinglish) questions about the Act and get accurate, grounded answers instantly — without reading 50 pages of legal text.

---

## 🏗️ Architecture

```
User Query
    ↓
Dify RAG Pipeline
    ↓
Jina AI Embeddings  →  Vector Store (Retrieval)
    ↓
Groq (Llama-3.1-8b-instant)  →  Answer Generation
    ↓
Langfuse (Production Monitoring)
    ↓
Response to User
```

---

## 🛠️ Tech Stack

| Layer | Tool |
|---|---|
| RAG Framework | Dify |
| Embeddings | Jina AI |
| LLM | Groq — Llama-3.1-8b-instant |
| Frontend | Lovable |
| Monitoring | Langfuse |
| Knowledge Base | DPDP Act 2023 (official PDF) |

---

## 📊 Evaluation Results

Built a custom **50-question evaluation dataset** to measure RAG accuracy.

| Metric | Score |
|---|---|
| Overall Accuracy | **8.5 / 10** |
| Evaluation Method | Manual + LLM-as-judge |
| Dataset Size | 50 questions |
| Question Types | Factual, Definitional, Penalty-based, Comparative |

---

## 📡 Production Monitoring (Langfuse)

Integrated Langfuse for real-time observability across all queries.

| Metric | Value |
|---|---|
| Total Traces Tracked | 31 |
| P50 Latency | 0.82s |
| P90 Latency | 1.16s |
| P95 Latency | 1.64s |
| P99 Latency | 2.73s |
| Total Cost (31 queries) | $0.002189 |
| Cost per Query | ~$0.00007 |

> 💡 **Key Insight:** 31 queries processed at a total cost of less than ₹0.20 — making this solution extremely cost-efficient for legal Q&A at scale.

---

## 💬 Sample Questions It Can Answer

- What is the DPDP Act 2023 and why was it introduced?
- Who is considered a Data Fiduciary?
- What are the rights of a Data Principal?
- What is the maximum penalty for a data breach?
- How does DPDP Act differ from GDPR?
- Can a minor's data be collected under the DPDP Act?
- What is the role of the Data Protection Board of India?

---

## 🔍 What I Learned

- How to build and tune a RAG pipeline for domain-specific legal content
- Importance of chunking strategy for dense legal documents
- How to design and run a 50-question evaluation dataset to measure RAG quality
- How to integrate production monitoring (Langfuse) to track latency, cost, and usage
- Real-world cost analysis of LLM-powered applications

---


*If this project was helpful or interesting, feel free to ⭐ the repo!*