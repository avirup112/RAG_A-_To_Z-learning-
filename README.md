# RAG From Scratch

A simple implementation of Retrieval-Augmented Generation (RAG) built from scratch using Python, demonstrating the core concepts of document retrieval and response generation.

## Overview

This project implements a basic RAG system that:
1. Creates embeddings for documents using cosine similarity
2. Retrieves the most relevant document based on user queries
3. Generates responses using a local LLM (Llama2 via Ollama)

## Features

- **Document Corpus**: Pre-defined collection of activity suggestions
- **Cosine Similarity**: Custom implementation for document-query matching
- **Local LLM Integration**: Uses Ollama with Llama2 for response generation
- **Simple Retrieval**: Returns the most relevant document based on similarity scores

## Requirements

- Python 3.11+
- Jupyter Notebook
- Ollama with Llama2 model
- Required Python packages:
  - `requests`
  - `json`
  - `math`
  - `collections`

## Setup

1. **Install Ollama**: Download and install Ollama from [ollama.ai](https://ollama.ai)

2. **Pull Llama2 model**:
   ```bash
   ollama pull llama2
   ```

3. **Start Ollama server**:
   ```bash
   ollama serve
   ```

4. **Run the notebook**: Open `RAG_From Scratch.ipynb` in Jupyter

## How It Works

### 1. Document Preparation
The system starts with a corpus of activity suggestions:
- Walking in the park
- Museum visits
- Live music concerts
- Hiking adventures
- And more...

### 2. Embedding Creation
- Tokenizes documents and queries
- Creates word frequency counters
- Calculates cosine similarity between query and documents

### 3. Document Retrieval
- Compares user query against all documents
- Returns the document with highest similarity score

### 4. Response Generation
- Sends the retrieved document and user query to Llama2
- Generates a personalized recommendation

## Usage Example

```python
user_input = "Suggest some fun outdoor activities for the weekend."
relevant_document = return_response(user_input, corpus_of_documents)
# Returns: "Have a picnic with friends and share some laughs."
```

## Key Functions

- `cosine_similarity(query, document)`: Calculates similarity between query and document
- `return_response(query, corpus)`: Finds and returns the most relevant document
- LLM integration via Ollama API for final response generation

## Limitations

- Simple bag-of-words approach (no semantic understanding)
- Limited document corpus
- Basic similarity matching
- Requires local Ollama installation

## Future Improvements

- Implement proper vector embeddings (e.g., sentence transformers)
- Add more sophisticated retrieval methods
- Expand document corpus
- Implement chunking for larger documents
- Add evaluation metrics

## License

This project is for educational purposes, demonstrating RAG concepts from scratch.