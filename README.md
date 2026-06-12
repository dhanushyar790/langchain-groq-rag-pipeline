# RAG Question Answering using LangChain, FAISS and Groq

A simple Retrieval-Augmented Generation (RAG) application that loads text documents, creates vector embeddings, stores them in FAISS, retrieves relevant context, and generates answers using the Groq LLM.

## Features

- Load text documents
- Split documents into chunks
- Generate embeddings using Hugging Face
- Store embeddings in FAISS vector database
- Retrieve relevant context
- Answer questions using Groq LLM
- Simple and lightweight implementation

## Project Structure

```text
RAG-Question-Answering/
│
├── notes.txt
├── rag.py
├── requirements.txt
├── .gitignore
└── README.md
```

## Installation

### Clone the Repository

```bash
git clone https://github.com/your-username/RAG-Question-Answering.git
cd RAG-Question-Answering
```

### Create a Virtual Environment

```bash
python -m venv venv
```

Activate the environment:

Windows

```bash
venv\Scripts\activate
```

Linux / macOS

```bash
source venv/bin/activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

## Required Packages

```txt
langchain
langchain-core
langchain-community
langchain-text-splitters
langchain-huggingface
langchain-groq
faiss-cpu
sentence-transformers
```

## Environment Variables

Create a `.env` file in the project root.

```env
GROQ_API_KEY=your_groq_api_key
```

## Dataset

Place your text file inside the project directory.

Example:

```text
notes.txt
```

The application will load this file and use it as the knowledge base for answering questions.

## Workflow

```text
Text File
    ↓
Document Loader
    ↓
Text Splitter
    ↓
Hugging Face Embeddings
    ↓
FAISS Vector Store
    ↓
Retriever
    ↓
Groq LLM
    ↓
Generated Answer
```

## Running the Project

```bash
python rag.py
```

Example:

```python
response = qa_chain.invoke("Give the important points")
print(response)
```

## Technologies Used

- Python
- LangChain
- FAISS
- Hugging Face Embeddings
- Groq
- Llama 3.3 70B Versatile

## Example Use Cases

- Personal Notes Question Answering
- Knowledge Base Search
- Document Retrieval
- Study Material Assistant
- Internal Documentation Search

## Future Improvements

- PDF support
- Multiple document support
- Conversational memory
- Web interface using Streamlit
- Advanced retrieval techniques
- Hybrid search

## Author

Dhanushya R

## License

This project is licensed under the MIT License.
