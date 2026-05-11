# Ecolab — RAG + Tool-calling Agent (Demo)

This project demonstrates a Retrieval-Augmented Generation (RAG) pipeline combined with tool calling for real-time API integration.  
It uses Azure OpenAI GPT-4.1, FAISS for retrieval, and the USGS Water Services API for validated answers on water streamflow.

## Features
- Retrieval-Augmented Generation (RAG) over PDF/TXT/MD documents.
- Semantic chunking + embeddings using ‘all-mpnet-base-v2’.
- Real-time USGS streamflow tool integration (`nwis/iv` endpoint).
- Chatbot UI built with Streamlit.
- Evaluation of chatbot responses with BERTScore (semantic similarity metric).

## Tech Stack
- Python 3.10+
- Azure OpenAI – for GPT-based generation.
- FAISS – for similarity search over embedded documents.
- Sentence-Transformers – for embeddings (`all-mpnet-base-v2`).
- Streamlit – for frontend UI.
- PyPDF2 – for PDF ingestion.
- BERTScore – for semantic evaluation.
- Requests – for API calls (USGS Water Services).

### Why These Choices?
- FAISS: Lightweight and fast similarity search for RAG.
- Azure OpenAI: Enterprise-grade security + GPT-4.1 for reasoning.
- BERTScore: Captures semantic similarity (better than ROUGE for meaning).
- Streamlit: Rapid prototyping and visualization.

---

## Setup Instructions

1. Load the Zip folder in VS code & create virtual environment
 python -m venv .venv
.venv\Scripts\activate   # (Windows)
source .venv/bin/activate  # (Linux/Mac)