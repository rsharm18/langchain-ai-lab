# AI-Powered HR Assistant (RAG-based Chatbot)

## Overview
This project is an AI-powered HR assistant that allows users to query company HR policies using natural language. It leverages Retrieval-Augmented Generation (RAG) to provide accurate, context-aware responses from internal documents.

## DEMO
![Demo](https://github.com/rsharm18/langchain-ai-lab/blob/main/RAG-based%20enterprise%20assistant/PDFFile_RAG_DEMO.gif)

## Features
- 📄 PDF document ingestion (HR policy)
- ✂️ Intelligent text chunking
- 🔍 Semantic search using vector embeddings
- 🧠 Context-aware answer generation using LLM
- 💬 Interactive chat interface using Gradio

## Architecture

1. **Document Loading**
   - PDF loaded using PyPDFLoader

2. **Text Splitting**
   - RecursiveCharacterTextSplitter (chunk size: 512, overlap: 64)

3. **Embeddings**
   - Model: `sentence-transformers/all-mpnet-base-v2`

4. **Vector Store**
   - FAISS for similarity search

5. **Retriever**
   - Retrieves relevant chunks based on query

6. **LLM Integration**
   - Groq LLM via LangChain

7. **UI**
   - Gradio-based chat interface

## Tech Stack
- LangChain
- HuggingFace Embeddings
- FAISS
- Groq LLM
- Gradio

## How It Works

1. User submits a question
2. Query is converted into embeddings
3. Relevant document chunks are retrieved
4. Retrieved context + question is sent to LLM
5. LLM generates a final answer

## Example Query
What are line managers' responsibilities?


## Setup

```bash
pip install gradio langchain langchain-core langchain-community \
langchain-text-splitters langchain-huggingface faiss-cpu \
transformers accelerate bitsandbytes
```

## Limitations
1. No persistent vector storage
2. Limited prompt engineering
3. Basic UI
4. No evaluation metrics

## Future Improvements

1. Add persistent FAISS index
2. Improve prompt templates
3. Introduce streaming responses
4. Add multi-document support
5. Deploy via FastAPI + frontend UI
6. Add observability and logging

## Use Cases
1. HR policy assistant
2. Internal knowledge base chatbot
3. Enterprise document search
   
## Author
Ravi Kumar Sharma

Built as a proof-of-concept for RAG-based enterprise assistants.
