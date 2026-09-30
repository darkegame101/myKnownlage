# Course Summary: C014 — Understanding LLM, RAG and Agentic RAG

## Course Overview
- **Course ID**: C014
- **Provider**: Việt Nguyễn AI (YouTube)
- **Course Name**: Introduction: Understanding LLM, RAG and Agentic RAG in 15 Minutes
- **URL**: [https://www.youtube.com/watch?v=waesmuwRT0c](https://www.youtube.com/watch?v=waesmuwRT0c)
- **Status**: Completed
- **Total Lectures**: 1 Video Lecture

## Topics Covered
1. **Evolution of AI Paradigms**: From Pure LLMs $\rightarrow$ Standard (Naive) RAG $\rightarrow$ Advanced RAG $\rightarrow$ Agentic RAG.
2. **Pure LLM Limitations**: Static knowledge cutoff, no external environment interaction, hallucination when queries require domain facts.
3. **Naive RAG Bottlenecks**: Garbage in, garbage out (poor retrieval produces incorrect generation), single-turn static lookup, inability to execute multi-step complex tasks.
4. **Agentic RAG Architecture**:
   - Integrating autonomous AI Agents into the retrieval loop.
   - Core capabilities: Planning, Reasoning, Tool Calling, and Reflection/Self-Evaluation.
   - Iterative feedback: Agent evaluates whether retrieved documents are sufficient; if not, rewrites queries or calls external tools before generating final answer.
5. **Architectural Comparison**:
   - Pure LLM: Internal weights only.
   - RAG: Internal weights + static external knowledge retrieval.
   - Agentic RAG: Internal weights + dynamic retrieval + multi-step reasoning + tool execution.

## Topics Already Known Before Course
- Basic RAG pipeline concepts (from C013).

## New Knowledge Added
- Evolution and limitations of Naive RAG.
- Conceptual mechanics of Agentic RAG (ReAct loop, query rewriting, reflection).
- When to use Pure LLM vs Standard RAG vs Agentic RAG in enterprise architectures.

## Knowledge Deepened
- Understanding that AI is evolving from passive chatbots into proactive autonomous problem-solving agents.

## Practical Skills Added
- Evaluating software architecture trade-offs between standard RAG and Agentic RAG.

## Remaining Gaps
- Building stateful multi-agent workflows using LangGraph, AutoGen, or CrewAI.
- Context window engineering and memory optimization in multi-turn agent loops.
- Setting up guardrails and safety controls on autonomous agent tool execution.

## Resulting Skill Level
- **Theory**: 3/5
- **Practical**: 2/5
- **Troubleshooting**: 1/5
- **Design**: 2/5

## Recommended Follow-up
- Build a prototype RAG system with document search.
- Explore LangGraph or Spring AI Tool Calling for agentic implementations.
