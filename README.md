# RAG Chatbot for PDF Question Answering

This project implements a **Retrieval-Augmented Generation (RAG) Chatbot** designed to interact with PDF documents. By combining **retrieval-based methods** with **generative language models**, the chatbot answers questions about the content of uploaded PDF files in a detailed and context-aware manner.

---

## Features

- **PDF Content Extraction**: Reads and processes PDF files, splitting them into meaningful chunks for efficient retrieval.
- **Vector-Based Retrieval**: Uses embeddings to build a vector store for semantic search.
- **Generative QA**: Combines context retrieval with the power of `google/flan-t5-large` for in-depth responses.
- **Customizable Parameters**: Adjustable chunk sizes, overlap, and retrieval settings.
- **Interactive Chat**: Engage with the system in real-time to ask questions about the uploaded PDF.

---

## Architecture

The chatbot leverages the RAG (Retrieval-Augmented Generation) architecture:
1. **Document Loading**: Extracts content from PDFs using `PyPDFLoader`.
2. **Text Chunking**: Splits the document into chunks using `RecursiveCharacterTextSplitter` for context continuity.
3. **Embedding Generation**: Converts chunks into vector embeddings using `sentence-transformers/all-MiniLM-L6-v2`.
4. **Vector Search**: Stores embeddings in Chroma for fast semantic retrieval.
5. **Generative QA**: Combines retrieved context with the `google/flan-t5-large` model to generate detailed answers.

---

## Requirements

- Python 3.8+
- A CUDA-capable GPU (optional, for faster processing)

### Install Dependencies

Run the following command to install the required libraries:

pip install transformers langchain chromadb sentence-transformers torch
