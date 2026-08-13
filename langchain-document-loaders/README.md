# LangChain Document Loaders

This folder contains my practice code for loading different types of documents using LangChain's document loaders. Each file shows a different way to load data so it can be used in LLM pipelines.

## What I Learned

LangChain has built-in loaders for almost every file type. You just point the loader to your file and call `.load()` — it returns a list of `Document` objects with `page_content` and `metadata`.

## Files

| File | What it does |
|------|-------------|
| `pdf_loader.py` | Loads a PDF file page by page using `PyPDFLoader` |
| `text_loader.py` | Loads a `.txt` file and uses a chain to summarize it |
| `csv_loader.py` | Loads a CSV file row by row using `CSVLoader` |
| `directory_loader.py` | Loads all PDFs from a folder using `DirectoryLoader` |
| `webbase_loader.py` | Scrapes a webpage and answers a question about it |

## Sample Data

- `dl-curriculum.pdf` — PDF used for `pdf_loader.py`
- `cricket.txt` — Text file (cricket poem) used for `text_loader.py`
- `Social_Network_Ads.csv` — CSV dataset used for `csv_loader.py`
- `books/` — Folder with a PDF book used for `directory_loader.py`

## Install

```bash
pip install langchain langchain-community langchain-openai pypdf python-dotenv
```

Make sure to add your `OPENAI_API_KEY` in a `.env` file for `text_loader.py` and `webbase_loader.py`.

## Quick Example

```python
from langchain_community.document_loaders import PyPDFLoader

loader = PyPDFLoader("dl-curriculum.pdf")
docs = loader.load()

print(f"Total pages: {len(docs)}")
print(docs[0].page_content)
```
