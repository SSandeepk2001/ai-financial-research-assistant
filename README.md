# AI Financial Research & Strategy Assistant

> A full-stack AI application for financial research, document question-answering, and context-aware report generation using **FastAPI, PostgreSQL, RAG architecture, and LLMs**.

## Overview

The **AI Financial Research & Strategy Assistant** is a portfolio-focused full-stack application designed to support financial research workflows through API-driven services, structured data storage, retrieval-augmented generation, and an interactive web interface.

The project demonstrates practical software-engineering capabilities across **backend development, REST APIs, databases, validation, exception handling, frontend integration, Git workflows, and AI/RAG architecture**.

## Key Features

- **FastAPI Backend** – REST APIs with request validation and exception handling
- **RAG Architecture** – Designed for grounded responses using retrieved financial context
- **PostgreSQL Database** – Persistent storage for documents and research-session metadata
- **LLM Integration** – Provider abstraction with support for an OpenAI-compatible API
- **Web Interface** – Responsive HTML, CSS, and JavaScript frontend
- **Docker Support** – Reproducible local development with Docker Compose
- **API Testing** – Pytest-based health/API test coverage
- **Modular Architecture** – Clear separation of API, services, data access, and presentation layers

## Architecture

mermaid
flowchart LR
    UI[Web UI<br/>HTML / CSS / JavaScript] --> API[FastAPI REST API]
    API --> RAG[RAG Service]
    RAG --> DB[(PostgreSQL)]
    RAG --> LLM[LLM Provider]
    API --> DOCS[Document Ingestion]
    DOCS --> DB


ai-financial-research-assistant/
│
├── app/
│   ├── main.py
│   ├── config.py
│   ├── db.py
│   ├── models.py
│   ├── schemas.py
│   │
│   ├── services/
│   │   ├── llm.py
│   │   └── rag.py
│   │
│   ├── static/
│   │   └── app.js
│   │
│   └── templates/
│       └── index.html
│
├── docs/
│   └── architecture.md
│
├── tests/
│   └── test_health.py
│
├── .env.example
├── .gitignore
├── Dockerfile
├── docker-compose.yml
├── requirements.txt
└── README.md

