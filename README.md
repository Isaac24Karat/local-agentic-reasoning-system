# Local Agentic Reasoning System (LARS)

![Status](https://img.shields.io/badge/status-active-brightgreen)
![Built With](https://img.shields.io/badge/built%20with-n8n%20%7C%20Offline%20Fallback%20%7C%20LangChain-blue)
![AI Agents](https://img.shields.io/badge/agents-Local%20Retriever%20%7C%20Supervisor-purple)
![License](https://img.shields.io/badge/license-MIT-lightgrey)
![Last Update](https://img.shields.io/github/last-commit/Isaac24Karat/local-agentic-reasoning-system)


> **Project Pitch:**  
> I built a local-first, agentic RAG system that processes complex user queries by reasoning, researching, and validating across multiple specialized agents.  
> Instead of simple retrieval, the system splits questions into sub-tasks, routes each sub-question to a domain expert, verifies the outputs with a Supervisor Agent, and synthesizes a complete, high-quality final answer.

---

## System Diagram

![Local Agentic RAG System Diagram](local-agentic-rag-system-diagram.png)

---

## What It Does
- Receives complex natural language questions
- Breaks down questions into sub-tasks using smart parsing
- Routes each sub-task to specialized domain agents
- Each agent retrieves and reasons about its specific topic
- A Supervisor Agent validates, merges, and finalizes the structured answer
- All data processing happens **locally** to protect privacy and improve speed
🧠 Supports multi-turn reasoning
📄 Handles structured and unstructured document input
🔒 Local-first processing, no cloud required


---

## Technologies Used
- n8n (workflow orchestration)
- Local LLM connections (Ollama / Custom LLM base URLs)
- Local vector search (PGVector, PostgreSQL)
- Metadata-based agent routing
- Multi-agent reasoning flow design
- RAG (Retrieval-Augmented Generation) strategies with local knowledge bases

---

## Files
- **local_agentic_rag_system_customized.json** — The customized n8n workflow
- **local-agentic-rag-system-diagram.png** — Visual system flow diagram

---

## Why This Matters
LARS demonstrates how AI systems can move beyond simple lookup responses — building **local-first**, **secure**, **multi-agent reasoning systems** that adapt to complex real-world user queries.  
This is a blueprint for real-world, scalable AI deployment in enterprises where data privacy, modularity, and flexibility are critical.

---

## Offline Fallback System

If the online document retrieval API fails (due to a timeout or outage), the system activates a local fallback node.  
This ensures the user still receives a valid response using cached knowledge.  
Merged results are then passed forward to the Supervisor Agent for further processing.


![Local Agentic RAG System Diagram](local-agentic-reasoning-diagram-v2.png)

---

## Future Work

- Add offline query fallback mode using cached vector store
- Fine-tune local LLMs for internal domain queries
- Create continuous learning pipeline to improve local knowledge base
- Log failed queries to detect scope gaps in local sources

---
*Demo built for AI Agent Implementation Manager portfolio presentation.*
