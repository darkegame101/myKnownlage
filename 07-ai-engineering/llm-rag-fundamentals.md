# LLM, RAG Pipelines & Agentic RAG Architecture

## Status
- **Overall Level**: 2/5
- **Theory**: 3/5
- **Practical**: 2/5
- **Troubleshooting**: 1/5
- **Design**: 2/5
- **Confidence**: Medium

## What I Have Learned
- **Large Language Model (LLM) Fundamentals**:
  - Nature of LLM as next-token prediction engine trained on vast public datasets.
  - Inherent limitations: Knowledge cutoff, absence of private/real-time domain data, and hallucination (confidently asserting false facts).
- **RAG (Retrieval-Augmented Generation) Architecture**:
  - Paradigm: Separating long-term parametric memory (LLM weights) from dynamic non-parametric memory (external retrieval index).
  - Two decoupled pipelines:
    1. **Ingestion / Indexing Pipeline**:
       - Document Loading: Ingesting raw unstructured documents (PDF, Markdown, HTML).
       - Chunking: Breaking text into manageable segments (evaluating chunk size vs context preservation, chunk overlap).
       - Vector Embeddings: Transforming text chunks into high-dimensional numerical vectors using an embedding model.
       - Vector Store: Indexing vector embeddings and metadata in vector databases (Chroma, Qdrant, Pinecone, PGVector).
    2. **Retrieval & Generation Pipeline**:
       - Query Vectorization: Generating embedding vector for user query.
       - Similarity Search: Calculating vector distance (Cosine Similarity, Euclidean Distance) to retrieve top-k nearest semantic chunks.
       - Prompt Augmentation: Assembling context window with retrieved chunks and user question into an augmented prompt.
       - Response Generation: LLM synthesizes a grounded answer citing source documents.
- **Evolution of AI Paradigms**:
  - **Pure LLM**: Static internal knowledge only $\rightarrow$ prone to hallucination for private data.
  - **Naive RAG**: Static single-step retrieval $\rightarrow$ vulnerable to bad retrieval producing bad answers (Garbage In, Garbage Out).
  - **Advanced RAG**: Pre-retrieval (query rewriting, routing) + Post-retrieval (re-ranking, filtering).
  - **Agentic RAG**: Integrating autonomous agent loops (Planning $\rightarrow$ Multi-step Retrieval $\rightarrow$ Reflection / Evaluation $\rightarrow$ Tool Calling $\rightarrow$ Synthesis).

## What I Understand
- Why fine-tuning a model is rarely the right solution for enterprise knowledge bases (fine-tuning is expensive, slow to update, and teaches style rather than reliable factual retrieval; RAG is cheap, updates in seconds, and provides verifiable source citations).
- The mathematical intuition behind Embeddings: text with similar semantic meaning occupies nearby positions in vector space, allowing semantic search beyond literal keyword matching.
- The fundamental bottleneck of Naive RAG: if the retrieval step fetches irrelevant chunks, the LLM either hallucinates or fails to answer; Agentic RAG resolves this by allowing the agent to evaluate retrieved content and perform follow-up queries.

## What I Can Do
- Explain the end-to-end data flow of an enterprise RAG system without confusing ingestion and query phases.
- Articulate the role of Chunking, Embeddings, Vector Stores, and Prompt Augmentation.
- Compare architectural trade-offs between Pure LLM, Naive RAG, and Agentic RAG.
- Design high-level system architecture diagrams for RAG-powered applications.

## What I Cannot Yet Do
- Build a production-ready RAG application using Python (LangChain/LlamaIndex) or Java (Spring AI).
- Implement advanced chunking strategies (semantic chunking, parent-document retrieval).
- Implement re-ranking (Cross-Encoders) and hybrid search (BM25 + Dense vector search).
- Build stateful multi-agent workflows using LangGraph or AutoGen.
- Evaluate RAG pipeline quality using automated benchmarks (RAGAS, TruLens).

## Sources & Knowledge Traceability

**Knowledge $\rightarrow$ Source Mapping**:
- **SRC-013** — Tất tần tật về RAG cơ bản trong 20 phút (Việt Nguyễn AI) | URL: https://www.youtube.com/watch?v=NQOYXmZxqvI
  - Evidence Record: [`00-sources/C013-rag-fundamentals.md`](../00-sources/C013-rag-fundamentals.md)
- **SRC-014** — Introduction: Understanding LLM, RAG and Agentic RAG in 15 Minutes (Việt Nguyễn AI) | URL: https://www.youtube.com/watch?v=waesmuwRT0c
  - Evidence Record: [`00-sources/C014-llm-rag-agentic.md`](../00-sources/C014-llm-rag-agentic.md)

Master Sources Catalog: [`00-sources/learning-sources.md`](../00-sources/learning-sources.md)

## Weaknesses
- Knowledge is currently theoretical and conceptual; lacks concrete repository commit evidence for practical code implementation.
- Untested in handling noisy documents (tables, images, corrupted PDFs) during chunking.

## Missing Knowledge
- **Vector Database Hands-on**: Direct configuration of ChromaDB, Qdrant, or PGVector.
- **SDK Implementation**: Implementing RAG with Spring AI (Java) or LangChain (Python).
- **Evaluation & Guardrails**: Hallucination detection, prompt injection defense, latency optimization.

## Recommended Supplements
1. Implement a simple RAG pipeline in Java using Spring AI with Ollama and a vector store.
2. Experiment with chunk size variations (256 vs 512 vs 1024 tokens) to observe retrieval quality changes.
