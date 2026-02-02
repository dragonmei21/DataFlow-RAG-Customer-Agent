# DataFlow Customer Service RAG Agent

A RAG (Retrieval-Augmented Generation) system that provides intelligent customer support by searching enterprise documents and generating contextual responses.

## Overview

Built for DataFlow Enterprise (fictional SaaS company) to automate customer service responses across 4 departments and 18+ documents.

## Pipeline

1. **Document Loading** - Load docs from multiple formats (markdown, CSV, JSON, txt)
2. **Text Chunking** - Split into 1000-char chunks with 200 overlap
3. **Vector Embeddings** - Convert to 384-dim vectors using HuggingFace `all-MiniLM-L6-v2`
4. **RAG Agent** - Query with LLM (Ollama/OpenAI) + semantic search via FAISS

## Tech Stack

- LangChain (orchestration)
- FAISS (vector database)
- HuggingFace (embeddings)
- Ollama / OpenAI (LLM)

## Results

- 75%+ retrieval accuracy
- Sub-3s response times
- ~$25K estimated annual savings vs manual support

## Setup

```bash
pip install langchain langchain-huggingface faiss-cpu sentence-transformers

# For local LLM
ollama pull llama3.2
ollama serve
```
