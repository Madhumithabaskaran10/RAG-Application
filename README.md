# RAG Application — From Scratch
A hands-on project exploring the fundamentals of Retrieval-Augmented Generation (RAG) by building a document-based question answering pipeline and understanding how its components work together.

## Overview
Large Language Models (LLMs) can generate responses based on their learned knowledge, but they may lack access to private documents or up-to-date information. RAG addresses this limitation by retrieving relevant information from an external knowledge source and providing it as context to an LLM.
This project focuses on understanding the RAG workflow through practical experimentation, from document ingestion to answer generation.

## Architecture
The application follows three main stages:
### 1. Data Ingestion Pipeline
- Load and extract text from documents.
- Split text into manageable chunks with overlap.
- Generate embeddings for document chunks.
- Store embeddings, document content, and associated metadata in ChromaDB.
### 2. Retrieval Pipeline
- Accept a user query.
- Convert the query into an embedding.
- Retrieve relevant document chunks through vector similarity search.
- Use the retrieved content as context for answer generation.
### 3. Answer Generation
- Combine the user's query with the retrieved context.
- Send the context and prompt to an LLM through the Groq API.
- Generate a context-aware response.

## Key Concepts Explored
- Limitations of standalone LLMs and the purpose of RAG.
- Document loading, chunking, and chunk overlap.
- Text embeddings and semantic representations.
- Cosine similarity and vector similarity search.
- Vector storage and metadata in ChromaDB.
- Query embedding and relevant context retrieval.
- LLM integration using the Groq API.
- The end-to-end RAG pipeline.

## Technologies
- Python
- Jupyter Notebook
- LangChain
- ChromaDB
- Embedding models
- Groq API
- 
## Project Structure
```text
.
├── data/           # Source documents (where applicable)
├── notebook/       # Jupyter notebooks and experiments
├── .gitignore
├── .python-version
├── README.md
├── pyproject.toml
├── requirement.txt
└── uv.lock
```

## Learning Outcomes
This project strengthened my understanding of how document ingestion, vector embeddings, similarity-based retrieval, and LLM generation work together to build a RAG application.
