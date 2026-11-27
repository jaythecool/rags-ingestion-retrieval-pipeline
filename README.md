# RAG Ingestion & Retrieval Pipeline

A basic **Retrieval-Augmented Generation (RAG)** pipeline built with LangChain that enables context-aware question answering over custom documents using semantic search and LLMs.

## 🚀 Features

- Load text documents from a local directory
- Split documents into manageable chunks
- Generate embeddings using Hugging Face
- Store embeddings in ChromaDB
- Retrieve relevant chunks using cosine similarity
- Rewrite follow-up questions using chat history
- Generate context-aware answers using Groq LLM

## 🛠️ Tech Stack

- **Python**
- **LangChain**
- **ChromaDB**
- **Hugging Face Embeddings** — `all-MiniLM-L6-v2`
- **Groq API** — `openai/gpt-oss-20b`

## ⚙️ Pipeline

**Ingestion:** Documents → Chunking → Embeddings → ChromaDB

**Retrieval:** User Query → Question Rewriting → Semantic Search → Context Augmentation → LLM Response

## 📂 Project Structure

```text
├── docs/                   # Source text documents
├── db/                     # Persistent ChromaDB storage
├── ingestion_pipeline.py     # Document ingestion & vector creation
├── retrieval_pipeline.py    # Retrieval & answer generation
├── requirements.txt
├── .env.example
└── README.md
```

## 🔧 Setup

```bash
git clone https://github.com/YOUR_USERNAME/rags-ingestion-retrieval-pipeline.git
cd rags-ingestion-retrieval-pipeline

python -m venv venv
venv\Scripts\activate        # Windows
# source venv/bin/activate    # Linux/macOS

pip install -r requirements.txt
```

Create a `.env` file and add your Groq API key:

```env
GROQ_API_KEY=your_groq_api_key
```

Add your `.txt` documents to the `docs/` directory.

## ▶️ Usage

**1. Create the vector database**

```bash
python ingestion_pipeline.py
```

**2. Start asking questions**

```bash
python retrieval_pipeline.py
```

Type `quit` to exit the chat.

## 🔮 Future Improvements

- Support PDF and other document formats
- Experiment with chunk sizes and overlap
- Implement incremental document updates
- Add source citations
- Explore hybrid search and reranking
- Build a Streamlit interface

---

Built as a hands-on project to explore **RAG, semantic search, embeddings, vector databases, and LLM integration**.
