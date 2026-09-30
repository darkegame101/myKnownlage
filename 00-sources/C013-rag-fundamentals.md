# Course Summary: C013 — Tất tần tật về RAG cơ bản trong 20 phút

## Course Overview
- **Course ID**: C013
- **Provider**: Việt Nguyễn AI (YouTube)
- **Course Name**: Tất tần tật về RAG cơ bản trong 20 phút
- **URL**: [https://www.youtube.com/watch?v=NQOYXmZxqvI](https://www.youtube.com/watch?v=NQOYXmZxqvI)
- **Status**: Completed
- **Total Lectures**: 1 Video Lecture

## Topics Covered
1. **The Core Problem**: Why LLMs suffer from Hallucination (generating believable falsehoods) and lack access to private/real-time domain data.
2. **Definition of RAG (Retrieval-Augmented Generation)**: Architecture pattern separating knowledge storage from generative reasoning.
3. **Offline Ingestion Pipeline (Indexing)**:
   - Document Loading: Ingesting text, PDF, docs.
   - Chunking: Splitting large documents into semantically coherent chunks (chunk size & overlap trade-offs).
   - Embedding: Converting text chunks into high-dimensional numerical vectors using an embedding model.
   - Vector Storage: Indexing embeddings inside Vector Databases (Chroma, Qdrant, Pinecone).
4. **Online Query Pipeline (Retrieval & Generation)**:
   - Query Embedding: Transforming user input into a vector.
   - Semantic Search: Calculating vector distance (Cosine Similarity) to find top-k relevant chunks.
   - Prompt Augmentation: Injecting retrieved context chunks into the system/user prompt template.
   - LLM Generation: Model produces fact-grounded response citing source material.
5. **Key Trade-offs**: Chunk size selection, embedding model quality, retrieval latency, and context window limits.

## Topics Already Known Before Course
- Basic AI terminology and conversational LLM usage.

## New Knowledge Added
- Complete end-to-end RAG architecture and two-phase pipeline (Ingestion vs Retrieval).
- Chunking strategies and their impact on context coherence.
- Vector embeddings and vector similarity retrieval mechanisms.
- Augmentation technique for preventing hallucination.

## Knowledge Deepened
- Distinction between model training (expensive, static) vs dynamic context injection (cheap, instantaneous).

## Practical Skills Added
- Understanding the architectural blueprint of an enterprise RAG system.

## Remaining Gaps
- Hands-on coding of a RAG pipeline using Python (LangChain/LlamaIndex) or Java (Spring AI).
- Production vector database deployment and tuning (HNSW indexing, metadata filtering).
- RAG evaluation metrics (faithfulness, answer relevance using RAGAS).

## Resulting Skill Level
- **Theory**: 3/5
- **Practical**: 2/5
- **Troubleshooting**: 1/5
- **Design**: 2/5

## Recommended Follow-up
- Study advanced and Agentic RAG patterns (C014).
- Implement a practical RAG pipeline connecting Spring Boot or Python to a local vector store.
