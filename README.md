# 📄 Chat With PDF

An AI-powered PDF question-answering chatbot built using **Retrieval-Augmented Generation (RAG)**.

The application allows users to upload a PDF and ask natural-language questions about its content. Instead of sending the entire document to the language model, the application retrieves the most relevant sections of the PDF and uses them as context to generate accurate, context-aware responses.

## 🚀 Features

- 📄 Upload PDF documents
- 🔍 Extract and split PDF content into chunks
- 🧠 Generate embeddings for document chunks
- 🗃️ Store and search document embeddings using ChromaDB
- 🔎 Retrieve relevant information using semantic similarity search
- 🤖 Generate answers using Google's Gemini API
- 💬 Ask multiple questions about the uploaded document
- 🌐 Simple and interactive Streamlit interface

## 🛠️ Tech Stack

- **Python**
- **Streamlit** – Web interface
- **LangChain** – RAG pipeline and document processing
- **Google Gemini** – Large Language Model
- **ChromaDB** – Vector database
- **PyPDF** – PDF text extraction

## 🧠 How It Works

The application follows a Retrieval-Augmented Generation (RAG) pipeline:

```text
             PDF Upload
                  ↓
          Extract PDF Text
                  ↓
          Split into Chunks
                  ↓
        Generate Embeddings
                  ↓
       Store in ChromaDB
                  ↓
          User asks a question
                  ↓
       Semantic Similarity Search
                  ↓
       Retrieve relevant chunks
                  ↓
       Send context to Gemini
                  ↓
          Generate Answer

## 🚀 How to Run Locally
```bash
pip install -r requirements.txt
streamlit run chat_with_pdf.py
```

## 🔑 Setup
Add your OpenAI API key in `.streamlit/secrets.toml`:
```toml
OPENAI_API_KEY = "your-key-here"
```

## 💡 How It Works
1. PDF is loaded and split into chunks
2. Chunks are embedded and stored in ChromaDB
3. Your question is matched to relevant chunks
4. OpenAI generates an answer based on those chunks# Chat-With-Pdf
An AI-powered chatbot that lets you upload a pdf and ask questions about it using RAG
