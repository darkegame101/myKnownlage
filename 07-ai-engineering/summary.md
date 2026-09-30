# Domain: AI Engineering & LLM Applications — Summary

## Current Level
- **Overall**: 2/5
- **Theory**: 3/5
- **Practical**: 2/5
- **Troubleshooting**: 1/5
- **Design**: 2/5
- **Confidence**: Medium
- **Evidence Status**: Partial (Conceptual architecture verified via C013 & C014; hands-on code project pending)

## What I Have Learned
- Foundations of Large Language Models (LLM), limitations of pre-trained static weights, knowledge cutoff, and the hallucination phenomenon.
- End-to-end Retrieval-Augmented Generation (RAG) architecture:
  - Ingestion (Indexing) Pipeline: Document parsing, chunking strategies, embedding generation, vector storage.
  - Retrieval & Generation Pipeline: Query vectorization, semantic similarity search (Cosine Similarity), prompt augmentation, fact-grounded response generation.
- Evolution of AI systems: Pure LLM $\rightarrow$ Standard (Naive) RAG $\rightarrow$ Advanced RAG $\rightarrow$ Agentic RAG.
- Architecture of Agentic RAG: Planning, iterative reasoning, self-reflection, dynamic query rewriting, and tool/function calling.

## Strong Areas
- Conceptual understanding of RAG pipeline stages and data flow.
- Understanding the root causes of hallucination and architectural mitigations.
- Comparing trade-offs between Pure LLMs, Naive RAG, and Agentic RAG for enterprise use cases.

## Weak Areas
- Hands-on coding of production RAG pipelines (Python LangChain/LlamaIndex or Java Spring AI).
- Production vector database deployment, indexing strategies (HNSW, IVFFlat), and metadata filtering.
- Automated evaluation metrics for RAG (RAGAS framework: faithfulness, answer relevancy, context precision).

## Missing Knowledge
- **Vector Databases in Production**: Deploying and configuring Qdrant, ChromaDB, Pinecone, or PostgreSQL with PGVector.
- **Framework Implementations**: Practical application development with LangChain, LangGraph, LlamaIndex, or Spring AI.
- **Advanced Retrieval**: Hybrid search (BM25 keyword + dense vector), Re-ranking (Cross-Encoders), contextual compression.
- **Tool Calling & Agent Workflows**: Implementing deterministic function calling and error-handling in agentic loops.

## Practical Gaps
- Theory Known: RAG pipeline architecture & Agentic RAG concepts = 3/5.
- Practical Known: Conceptual understanding = 2/5.
- Gap: Has not yet written code to parse documents, generate embeddings via API, query a vector store, and generate answers in a live application.

## Recommended Supplements
1. Build a prototype RAG CLI or web app in Java (using Spring AI + Ollama/Gemini) or Python.
2. Practice chunking documents and inspecting embeddings inside a local vector database (e.g. ChromaDB).
3. Implement a simple tool-calling agent that queries an external API.

## Readiness for Next Topics
- **RAG & LLM Concepts**: **READY (3/5 Theory)**
- **RAG Hands-on Application Development**: **PARTIALLY READY (2/5)** — Requires hands-on project to achieve full practical mastery (Level 4/5).
