# RAG using LangChain & LangGraph

Hands-on implementation of Retrieval-Augmented Generation (RAG) covering document processing, text splitting, embeddings, vector databases, retrieval strategies, and LLM-based question answering.

## 📂 Modules

| Folder | Description |
|--------|-------------|
| [`langchain-text-splitters/`](./langchain-text-splitters/) | Different text splitting strategies — length-based, structure-based, markdown, code, and semantic |

## 🔧 Tech Stack

- **LangChain** – Core framework for building LLM applications
- **LangGraph** – For stateful, graph-based LLM workflows
- **ChromaDB** – Vector database for document retrieval
- **OpenAI / HuggingFace** – Embedding and LLM backends

## 🚀 Getting Started

```bash
pip install langchain langchain-community langchain-experimental langchain-openai chromadb python-dotenv
```

Set up your `.env` file with API keys (e.g., `OPENAI_API_KEY`).
