# Bengali LLaMA Repo Chatbot

A minimal Retrieval-Augmented Generation (RAG)-style chatbot that answers questions about the GitHub repository:

> **Fine-Tuning LLaMA 3.1-8B for Bengali Empathetic Dialogue**  
> (`ratulsaha2021/Fine-Tuning-LLaMA-3.1-8B-for-Bengali-Empathetic-Dialogue`)

The app uses **SentenceTransformers** embeddings, a **FAISS** vector store, and a **Streamlit** chat interface to search the repo’s documentation and return short answers. [web:22][web:101]

---

## Features

- Indexes `.md` and `.txt` files inside the fine-tuning repo.
- Splits files into overlapping chunks for better retrieval.
- Uses `sentence-transformers/all-MiniLM-L6-v2` to embed chunks and queries. [web:56]
- Stores embeddings in a FAISS vector index for fast similarity search. [web:68]
- Simple Streamlit chat UI (`st.chat_input` and `st.chat_message`) for Q&A. [web:93]

---

## Project structure

```text
bengali-llama-repo-chatbot/
│
├── app.py             # Streamlit chat app
├── build_index.py     # Loads repo files and builds FAISS index
├── requirements.txt   # Python dependencies
└── README.md          # Project description
