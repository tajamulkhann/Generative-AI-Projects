# 🗂️ Multi-Document AI Chat Assistant

A generative-AI project focused on allowing users to chat interactively across a collection of documents—upload PDFs, DOCX, text files—and query them naturally using an LLM + RAG pipeline.

---

## 📌 Project Overview

This project builds a system where a user can upload multiple documents (e.g., reports, research papers, manuals), the system processes them (splits, embeds, indexes), and you can then ask natural-language questions— the assistant retrieves relevant context chunks and uses an LLM to answer. The goal is to create a conversational agent grounded in **multiple documents**, maintaining context over a conversation and enabling exploration of the document set.

---

## 🧰 Tech Stack

* **Language:** Python
* **Libraries:** `langchain` (or similar), `PyPDF2`/`pdfplumber`, `docx2txt`, a vector-store (e.g., FAISS, Chroma), `openai`/other LLM SDK
* **Environment:** Jupyter Notebook / Google Colab / Streamlit/Flask Web App

---

## 🔄 Workflow Summary

### 1. Document Ingestion & Pre-processing

* Upload a folder or set of documents (.pdf, .docx, .txt).
* Extract text, optionally metadata (title, author, date).
* Split text into chunks with overlap (e.g., 500 tokens/100 overlap) to preserve context.
* Embed each chunk (via embedding model) and add to vector store.

### 2. Indexing & Retrieval

* On user question, embed the query and fetch top-k similar chunks from vector store.
* Use those chunks as context for the LLM prompt.
* Maintain chat history so follow-up user queries can refer to previous interactions and context.

### 3. LLM Prompting & Chat Flow

* Construct a prompt including retrieved chunks, the user’s question, and optionally chat history.

  ```
  You are a knowledgeable assistant. Use the following document excerpts:
  [chunk 1] 
  [chunk 2] 
  ...
  Then answer the user’s question: {question}
  ```
* Send to LLM to generate an answer.
* Return answer to user; store interaction in chat history.

### 4. User Interface & Features

* Provide simple UI (Streamlit/Flask) where user can upload docs, type questions, and view chat.
* Show list of documents (metadata), option to add more documents dynamically.
* Optionally show which document chunks were used (transparency).
* Support conversation history: e.g., user asks “what about section 3?” after initial answer.

---

## 📁 Project Structure

```
Multi-Document-AI-Chat-Assistant/
│── docs/                  # Uploaded documents
│── data/                  # Processed chunks / embeddings
│── notebooks/
│   └── prototype.ipynb
│── src/
│   ├── ingest.py
│   ├── indexer.py
│   ├── chat_app.py
│   └── utils.py
│── requirements.txt
│── README.md
```

---

## 📈 Key Findings

* Splitting documents into manageable chunks + using embeddings + vector store allows scaling to **multiple** documents without overwhelming the LLM. (Similar techniques described in blog posts) ([Better Programming][1])
* Providing the correct document context significantly improves answer relevance and accuracy compared to naively sending all text.
* Maintaining conversational history helps the assistant handle follow-up questions and context referencing.
* User experience improves when the system shows which documents or chunks were used for the answer (increase trust).

---

## 🚀 Future Improvements

* Add support for **multi-modal** documents: images, tables, charts—allow visual context extraction.
* Improve UI: file browser, live chat, filtering by document.
* Add logging of user chat and document usage analytics (which docs are most queried).
* Deploy as web-service with authentication, upload quotas, and query quotas.
* Extend to **summary mode**: “Summarise all docs in 300 words” or “Compare section A of Doc1 with section B of Doc2”.

---

## 🧑‍💻 Author

**[Tajamul Khan](https://www.linkedin.com/in/tajamulkhann/) – Data Scientist & AI Engineer**

---

## Let's Connect <img src="https://github.com/JayantGoel001/JayantGoel001/blob/master/GIF/Handshake.gif" height="30px" style="max-width:100%;">

<div align="center">

<a href="https://www.linkedin.com/in/tajamulkhann/">
<img src="https://img.shields.io/badge/linkedin-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white">
</a>
<a href="https://www.instagram.com/tajamul.datascientist/" target="_blank">
<img src="https://img.shields.io/badge/Instagram-%23E4405F.svg?style=for-the-badge&logo=instagram&logoColor=white">
</a>
<a href="https://topmate.io/tajamulkhan" target="_blank">
<img src="https://img.shields.io/badge/Topmate-FF0000?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxMDAgMTAwIj48Y2lyY2xlIGN4PSI1MCIgY3k9IjUwIiByPSI0MCIgZmlsbD0id2hpdGUiLz48L3N2Zz4=&logoColor=white">
</a>
<a href="https://www.whatsapp.com/channel/0029VaYs05jJkK7JKCesw42f">
<img src="https://img.shields.io/badge/WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white">
</a>
<a href="https://t.me/tajamul_khan">
<img src="https://img.shields.io/badge/Telegram-26A5E4?style=for-the-badge&logo=telegram&logoColor=white">
</a>
<a href="https://substack.com/@tajamulkhan">
<img src="https://img.shields.io/badge/Substack-%23006f5c.svg?style=for-the-badge&logo=substack&logoColor=FF6719">
</a>
<a href="https://www.kaggle.com/tajamulkhan">
<img src="https://img.shields.io/badge/Kaggle-035a7d?style=for-the-badge&logo=kaggle&logoColor=white">
</a>
<a href="https://github.com/tajamulkhann">
<img src="https://img.shields.io/badge/Github-12100E?style=for-the-badge&logo=github&logoColor=white">
</a>
<a href="https://medium.com/@tajamulkhan">
<img src="https://img.shields.io/badge/Medium-12100E?style=for-the-badge&logo=medium&logoColor=white">
</a>
<a href="https://www.youtube.com">
<img src="https://img.shields.io/badge/YouTube-%23FF0000.svg?style=for-the-badge&logo=YouTube&logoColor=white">
</a>
</div>
