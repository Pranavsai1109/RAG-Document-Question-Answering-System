# RAG Document Question Answering System

## Overview

This project implements a simple Retrieval-Augmented Generation (RAG) pipeline that allows a user to ask questions about documents (such as PDFs). The system retrieves relevant parts of the document and sends them to a Large Language Model (LLM) to generate accurate answers.

The goal of this project is to build a beginner-friendly RAG system using modern Python AI tools.

## Features

* Load PDF documents
* Split documents into smaller chunks
* Convert text chunks into embeddings
* Store embeddings in a vector database
* Perform semantic search on documents
* Retrieve relevant context for answering questions

## Tech Stack

* Python
* LangChain
* FAISS vector database
* Sentence Transformers embeddings
* Gemini LLM
* UV package manager

## Project Structure

```
rag_project/
│
├── main.py
├── requirements.txt
├── data/
│   └── sample.pdf
│
├── vectorstore/
│
└── README.md
```

## Installation

1. Create a virtual environment

```
uv venv
```

2. Activate the environment

Windows:

```
.venv\Scripts\activate
```

3. Install dependencies

```
uv pip install -r requirements.txt
```

## Requirements

Example `requirements.txt`

```
langchain
langchain-community
langchain-google-genai
faiss-cpu
pypdf
python-dotenv
sentence-transformers
tiktoken
transformers
```

## Running the Project

Run the main script:

```
uv run main.py
```

## How the RAG Pipeline Works

1. Document Loading

   * PDFs are loaded from the `data/` folder.

2. Text Chunking

   * Documents are split into smaller pieces for better retrieval.

3. Embeddings

   * Each chunk is converted into a vector representation using a sentence transformer model.

4. Vector Database

   * Embeddings are stored in FAISS for fast similarity search.

5. Retrieval

   * When a user asks a question, the system finds the most relevant chunks.

6. LLM Generation

   * The retrieved context is sent to an LLM which generates the final answer.

## Example Workflow

User Question

↓

Convert Question to Embedding

↓

Search Similar Chunks in Vector Database

↓

Send Retrieved Context to LLM

↓

Generate Answer

## Future Improvements

* Add a chatbot interface
* Support multiple document formats
* Build a web interface
* Improve chunking strategies
* Add streaming responses

## Learning Goals

This project helps understand:

* RAG architecture
* Vector databases
* Embeddings
* LLM integration
* Document search systems

## License

This project is for educational and learning purposes.
