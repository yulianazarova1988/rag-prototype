
# RAG Prototype for Rental Deposit Assistant

This repository contains a **toy prototype** of a Retrieval-Augmented Generation (RAG) pipeline, built with LangChain and sentence-transformers embeddings.

The goal was to explore how Large Language Models (LLMs) can be used in the **fintech rental space** to:
- Extract patterns from rental agreements (NER, entity validation).
- Answer tenants' FAQ using RAG over internal documents.
- Automate compliance checks (e.g., FICA requirements in South Africa).

---

## What this notebook shows
- End-to-end flow: document → chunking → embeddings → vector store (FAISS) → retrieval → LLM response.
- Simple prototype logic for **question answering** over contracts and FAQs.
- Example code for fine-tuning and evaluation (BLEU/ROUGE).

---

## What we actually built in production prototype
In the real project, the pipeline was more advanced:
- Annotated contracts and trained a proper **NER model** (spaCy / transformers).
- Applied **entity consistency checks** (amounts, dates, months).
- Used **RAG 2.0** (dense passage retrieval + reranker such as ColBERT / cross-encoder).
- Integrated with **workflow APIs** (e.g., DoxFox) to check completeness of tenants’ documents under **FICA regulations**.
- Experimented with **fine-tuning LLMs** (Flan-T5, LLaMA) on internal FAQ dialogues.

---

## Next steps (future iterations)
- Conversational memory for multi-turn legal Q&A.
- Templates for legally precise answers.
- Better evaluation pipeline (human-in-the-loop + automatic metrics).
- Deployable MVP for legal support automation.

---

⚠️ **Note:** This notebook is illustrative. It omits real contracts, sensitive data, and production logic. The real implementation was more complex and cannot be published here.
