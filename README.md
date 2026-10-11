# PDF-Based Retrieval-Augmented Generation (RAG) Chatbot
Developed by Pranavi

 A Retrieval-Augmented Generation chatbot that enables users to ask questions about large PDF documents and receive context-aware answers with source references.

The main problem I wanted to solve was the difficulty of manually searching lengthy documents containing hundreds of pages.

I designed the system using Python. First, I extracted text from PDFs using PyMuPDF and divided the extracted content into smaller, overlapping chunks. I then generated semantic embeddings using a Sentence Transformers model and stored the vectors in a FAISS index along with metadata such as page numbers.

When a user submits a question, the system converts the question into an embedding and retrieves the most relevant document chunks using similarity search. These chunks are passed to a Large Language Model through a carefully designed prompt to generate an answer grounded in the retrieved content.

I also designed the response pipeline to provide source references and indicate when the retrieved information is insufficient.

The main technologies used were Python, PyMuPDF, Sentence Transformers, FAISS, and an LLM API. A user interface can be built with Streamlit, while FastAPI can be used to expose the backend as a service.

This project demonstrates my understanding of document processing, semantic search, vector databases, prompt engineering, and LLM integration. The main benefit is that users can find information in lengthy documents more efficiently without reading every page manually.
