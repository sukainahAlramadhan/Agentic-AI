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
