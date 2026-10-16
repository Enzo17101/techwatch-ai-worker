# TechWatch AI - Worker Service

A specialized Python microservice designed for content extraction, document enrichment, and asynchronous Retrieval-Augmented Generation (RAG) tasks within the TechWatch AI distributed architecture.

## Overview

This worker processes technological watch feeds by:
- Scraping and cleaning article payloads from web sources.
- Interfacing with local LLMs and vectorization engines (Ollama) to compute embeddings.
- Storing and querying vector representations using PostgreSQL (`pgvector`).
- Serving semantic search queries via FastAPI endpoints.

## Architecture & Tech Stack

- **Framework:** FastAPI
- **Data & Vector Store:** SQLAlchemy, PostgreSQL (`pgvector`)
- **Extraction:** Trafilatura, BeautifulSoup4
- **Testing:** Pytest, Pytest-Asyncio, Respx

## Project Structure

├── app/
│   ├── api/          # Router endpoints
│   ├── core/         # Configuration & Database setup
│   ├── models/       # SQLAlchemy models
│   ├── schemas/      # Pydantic validation models
│   └── services/     # Business logic, scraping, and RAG services
├── tests/            # Isolated test suites and mocks
├── requirements.txt  # Python dependencies
├── run.bat           # Run uvicorn server
└── README.md