# Multi-Agent Programming Assistant (Agentic AI) Guide

This document explains the architecture and workflow of the Multi-Agent Programming Assistant, an AI system that automatically generates, improves, evaluates, and validates Python code using a collaborative multi-agent architecture.

The system is built using LangGraph, LangChain, and Llama3 via Ollama.

##1. Overview

The Multi-Agent Programming Assistant is an Agentic AI system where multiple specialized agents collaborate to solve programming problems.

Instead of relying on a single LLM response, the system:

Generates code

Improves and refactors it

Validates execution

Compares multiple solutions

Selects the best result

This multi-agent architecture improves reliability and correctness compared to traditional LLM-based coding assistants.

## Key Technologies

LangGraph → Agent workflow orchestration

LangChain → LLM agent tools and prompting

Ollama → Local LLM inference (Llama3)

Python Subprocess → Secure code execution

unittest → Automated validation


## 2. System Architecture (Agent Workflow)

The system functions as a state-driven multi-agent pipeline where different agents collaborate to complete the programming task.

Workflow

Generator Agent creates Python code.

Deliberative Fixer Agent improves or corrects the code.

Judge Agent evaluates both versions.

Execution Validator verifies correctness.

Final solution is returned to the user.

<img width="557" height="878" alt="Screenshot 2026-01-21 093249" src="https://github.com/user-attachments/assets/e49e8c8a-7c04-40be-af26-1d86982ba54d" />

## 3. Key Features
Multi-Agent Collaboration
Multiple AI agents collaborate instead of relying on a single LLM response.

Iterative Code Improvement
The system automatically improves generated code across iterations.

Execution Validation
Generated code is executed and verified before returning results.

Agentic AI Workflow
Uses LangGraph to orchestrate agent interactions.

Streaming Responses
Supports LLM streaming output for better responsiveness.

## 4.Example User Queries
The assistant can solve a variety of programming tasks.

Example Queries
Create a Python function to calculate factorial
Create a Python function to check if a number is prime
Write a Python program to sort a list using quicksort

## 5.. Safety Features
The system includes safeguards to ensure reliable execution.

Execution Isolation
Generated code is executed in an isolated process.

Error Handling
Runtime errors are captured and analyzed.

Iteration Limits
Maximum retry attempts prevent infinite loops.

Logging
Agent decisions and execution outputs are recorded.

