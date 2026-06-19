Agentic Biotechnology RAG Chatbot
Overview

This project implements two Retrieval-Augmented Generation (RAG) chatbot workflows for answering biotechnology-related questions from PDF documents.

The system uses OpenAI models, vector embeddings, and FAISS-based semantic search to retrieve relevant information and generate context-aware responses.

The project demonstrates the evolution from a basic RAG agent to an advanced agentic RAG workflow with self-correction and query refinement capabilities.

Features
PDF document ingestion
Text chunking and preprocessing
OpenAI embeddings
FAISS vector database
Retrieval-Augmented Generation (RAG)
Agentic workflow orchestration
Query rewriting and retry mechanisms
Response grading and self-correction
Project Structure
1. Simple Agentic RAG

A lightweight workflow that decides whether retrieval is required before generating a response.

Workflow:

User Question
→ Decide Retrieval Needed?
→ Retrieve Documents (if required)
→ Generate Answer

This agent reduces unnecessary retrieval operations and demonstrates conditional routing within an agentic workflow.

2. Advanced Agentic RAG

A more sophisticated workflow that evaluates retrieval quality and iteratively improves responses.

Workflow:

User Question
→ Decide Retrieval Needed
→ Retrieve Documents
→ Grade Retrieved Context
→ Generate Answer
→ Grade Answer Quality
→ Retry Retrieval (if needed)
→ Rewrite Query (if needed)
→ Generate Improved Answer

This workflow enables:

Retrieval quality assessment
Query reformulation
Retry mechanisms
Improved answer accuracy
Self-correcting agent behavior

Technology Stack:

Python
OpenAI API
LangGraph
FAISS
Jupyter Notebook
dotenv
