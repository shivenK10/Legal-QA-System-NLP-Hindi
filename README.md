# Legal QA Chatbot for Indian Constitution & IPC (Hindi)

A prototype Retrieval-Augmented Generation (RAG) chatbot that answers questions about the Indian Constitution and Indian Penal Code (IPC) in Hindi. It ingests born-digital Hindi texts, splits them into chunks, embeds them with a multilingual MiniLM, indexes with FAISS, and uses an instruction-tuned MT0-small model to generate concise, citation-backed answers in Hindi.

## Features

- 🔍 **Semantic Search** over Hindi Constitution & IPC texts  
- 🤖 **RAG Pipeline** using FAISS + instruction-tuned MT0-small  
- 📝 **Answers in Hindi** with chunk-level citations  
- 🚀 **Lightweight & Fast** on CPU/MPS/GPU  

## Dataset

- **Constitution of India (Hindi PDF)**  
- **Indian Penal Code (Hindi PDF)**  
- Text extracted via OCR and stored as `.txt` files  
- Source PDFs downloaded from:
  - https://legislative.gov.in/constitution-of-india/  
  - https://vault.drishtijudiciary.com/.../IPC.pdf

## Models

1. **Embedding:** `sentence-transformers/paraphrase-multilingual-MiniLM-L12-v2`  
2. **Generation:** `bigscience/mt0-small` (instruction-tuned, multilingual)

# Install dependencies
pip install pdf2image pytesseract pdfplumber langchain-community transformers torch faiss-cpu sentence-transformers