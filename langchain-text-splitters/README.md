# LangChain Text Splitters

Exploring different text splitting strategies in LangChain for chunking documents before feeding them into retrieval pipelines.

## 📁 Files

| File | Description |
|------|-------------|
| `length_based.py` | Splits text based on character count using `CharacterTextSplitter` |
| `text_structure_based.py` | Recursively splits text respecting natural structure using `RecursiveCharacterTextSplitter` |
| `markdown_splitting.py` | Splits Markdown documents intelligently using language-aware splitting |
| `python_code_splitting.py` | Splits Python code using language-aware recursive splitter |
| `semantic_meaning_based.py` | Splits text by semantic meaning using `SemanticChunker` with OpenAI embeddings |
| `dl-curriculum.pdf` | Sample PDF used for demonstrating PDF-based text splitting |

## 🔍 Text Splitting Strategies Covered

1. **Length-Based Splitting** – Simple character count-based chunking. Good baseline.
2. **Text Structure-Based Splitting** – Recursively splits on natural separators (paragraphs, sentences, words).
3. **Markdown Splitting** – Language-aware splitting tuned for Markdown structure.
4. **Code Splitting** – Splits source code (Python) respecting function/class boundaries.
5. **Semantic Splitting** – Uses embeddings to split at semantic breakpoints for more meaningful chunks.

## 🛠 Requirements

```bash
pip install langchain langchain-community langchain-experimental langchain-openai pypdf python-dotenv
```

## 💡 Notes

- For `semantic_meaning_based.py`, set your `OPENAI_API_KEY` in a `.env` file.
- `dl-curriculum.pdf` is the sample document used in `length_based.py`.
