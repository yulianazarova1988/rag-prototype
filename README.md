
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

# Прототип RAG для помощника по аренде

Этот репозиторий содержит **игрушечный прототип** пайплайна Retrieval-Augmented Generation (RAG), собранного с помощью LangChain и sentence-transformers.

Задача — показать, как LLM можно применять в **финтехе аренды** для:
- Извлечения паттернов из договоров аренды (NER, проверка сущностей).
- Ответов на вопросы арендаторов через RAG по внутренним документам.
- Автоматической проверки соответствия требованиям (например, FICA в ЮАР).

---

## Что показывает ноутбук
- Полный поток: документ → чанки → эмбеддинги → векторное хранилище (FAISS) → поиск → ответ LLM.
- Простая логика прототипа для **вопрос-ответа** на базе договоров и FAQ.
- Пример кода для дообучения и оценки (BLEU/ROUGE).

---

## Что делали в реальном проекте
В реальном прототипе пайплайн был сложнее:
- Аннотация договоров и обучение **NER-модели** (spaCy / transformers).
- Проверки согласованности сущностей (суммы, даты, месяцы).
- Использование **RAG 2.0** (dense passage retrieval + reranker — ColBERT / cross-encoder).
- Интеграция с **workflow API** (например, DoxFox) для проверки пакета документов арендатора по **FICA**.
- Эксперименты с **дообучением LLM** (Flan-T5, LLaMA) на корпусе FAQ-диалогов.

---

## Следующие шаги
- Память диалога для многошаговых юридических консультаций.
- Шаблоны для юридически точных ответов.
- Более качественная система оценки (human-in-the-loop + автоматические метрики).
- Готовый к продакшену MVP для автоматизации поддержки.

---

⚠️ **Важно:** Этот ноутбук — учебный пример. Настоящие договоры, данные и логика не публикуются. Реальный пайплайн был существенно сложнее.

