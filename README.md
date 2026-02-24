# CivicRag

CivicRag builds a retrieval backbone for civic complaint data (NYC 311) and evaluates how LLM-based semantic normalization and dense embeddings improve search quality for RAG-style applications.

## Overview

Pipeline:

API Ingestion → Database → LLM Semantic Layer → Embeddings → Vector Index → Retrieval → Evaluation

The semantic layer extracts normalized issue type, severity, urgency, and contextual entities to reduce noise in real-world civic text.

## Retrieval Systems

- Keyword-based retrieval (structured SQL filters + TF-IDF/BM25)
- Dense semantic retrieval (LLM embeddings + vector search)
- Hybrid retrieval (structured filters + dense ranking)

## Evaluation

Metrics used:
- Precision@k  
- Recall@k  
- nDCG@k  
- Filter accuracy (for LLM-assisted query parsing)

## Extension

The same dataset and representations are used to study predictive modeling of complaint resolution speed (fast vs. slow) using traditional NLP features, LLM-structured attributes, dense embeddings, hybrid features, and end-to-end LLM classification.

---

## Purpose

To strengthen retrieval layers that support reliable RAG-style civic question answering and downstream predictive modeling.
