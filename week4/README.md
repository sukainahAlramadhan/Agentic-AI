# Week 4
# Week 4 – Task-Oriented Agent Workflow

## Overview

This notebook demonstrates how to build a **task-oriented AI agent** using LangChain. The agent can break down complex tasks, use external tools, combine retrieved information with calculations, and determine when a task is completed.

## Topics Covered

- Task-oriented agents
- Task decomposition
- Tool usage and tool chaining
- Web search and information retrieval
- Mathematical calculations
- ReAct agent workflow
- Autonomy control and safety
- Research and analysis workflows

## Tools Used

The agent is equipped with two main tools:

1. **Web Search** – retrieves real-world information using DuckDuckGo.
2. **Math Calculator** – performs calculations on retrieved data.

## Agent Architecture

The notebook uses:

- **LangChain**
- **OpenAI GPT-4o-mini**
- **ReAct Agent**
- **AgentExecutor**
- **DuckDuckGo Search**

The general workflow is:

```text
User Task
   ↓
Task Decomposition
   ↓
Web Search
   ↓
Information Retrieval
   ↓
Math Calculation
   ↓
Tool Chaining
   ↓
Final Answer



# Week 4 – LangChain_wikipedia.ipynb

# Overview
This notebook demonstrates how to build a Retrieval-Augmented Generation (RAG) agent using LangChain. The agent retrieves structured and unstructured data, performs hybrid searches across vector and lexical stores, leverages live web search when necessary, and maintains conversational context across user interactions.

# Topics Covered
* Document ingestion and chunking
* Hybrid search (vector embeddings + keyword search)
* Cache-backed embeddings for performance optimization
* Agentic tool integration (retriever tools & external web search)
* ReAct agent workflow and execution
* Session-based conversational memory

# Tools Used
* **Restaurant / Avengers Document Retriever** – searches and extracts information from local vector stores (**FAISS**) and keyword indices (**BM25**).
* **Tavily Web Search** – retrieves real-time, external web information when local knowledge is insufficient.

# Agent Architecture
The workflow follows a hybrid retrieval and reasoning pipeline:

User Query
   ↓
Agent Executor (ReAct Framework)
   ↓
Decision Point (Choose Tool)
   ├── Ensemble Retriever (FAISS + BM25)
   └── Tavily Web Search Tool
   ↓
Context & Search Results
   ↓
RunnableWithMessageHistory (Memory Persistence)
   ↓
Final Response
