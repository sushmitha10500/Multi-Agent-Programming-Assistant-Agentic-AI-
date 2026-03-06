# Multi-Agent Programming Assistant (Agentic AI)

An AI-powered programming assistant built using **LangGraph, LangChain, and Llama3 (Ollama)** that generates, evaluates, and improves Python code using a **multi-agent architecture**.

The system follows an **agentic design pattern** where multiple AI agents collaborate to generate, analyze, and validate Python code automatically.

---

# Overview

This project demonstrates how **multiple AI agents can collaborate in a structured workflow** to solve programming tasks.

Instead of relying on a single LLM response, the system introduces specialized agents that:

- Generate code
- Improve the generated code
- Evaluate which version performs better
- Verify execution before returning the final solution

The workflow is orchestrated using **LangGraph**, enabling a structured agent pipeline.

---

# Architecture

The system uses **three specialized agents**:

### 1. Code Generator Agent
Responsible for generating Python code for a given task using a **ReAct reasoning pattern**.

Responsibilities:
- Understand user requirements
- Generate Python code
- Provide structured reasoning before output

---

### 2. Deliberative Fixer Agent
Improves and refactors the generated code.

Responsibilities:
- Analyze execution results
- Fix logical errors
- Improve code structure and readability

---

### 3. Judge Agent
Evaluates both code versions and decides which one performs better.

Responsibilities:
- Execute both versions of the code
- Compare outputs
- Select the best solution

---

# Workflow

The application follows the workflow below:

User Task
↓
Generator Agent
↓
Deliberative Fixer Agent
↓
Judge Agent
↓
Execution Verification
↓
Final Code Output



If the generated solution fails, the system automatically retries for up to **three iterations**.

---

# Key Features

- Multi-agent architecture using **LangGraph**
- Code generation using **LLM agents**
- Automatic code debugging and improvement
- Execution validation before returning results
- Iterative improvement loop
- Streaming LLM response output
- Built-in unit tests for validation

---

# Tech Stack

Programming Language
- Python

LLM & AI Frameworks
- LangChain
- LangGraph

LLM Model
- Llama3 (via Ollama)

Other Libraries
- unittest
- typing
- subprocess
- contextlib

---
# Example query
What should I code? Anything

Create a Python function to calculate factorial

Create a Python function to check if a number is prime

