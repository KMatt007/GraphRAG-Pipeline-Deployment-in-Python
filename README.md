# GraphRAG Pipeline with Neo4j and Vector DB

A retrieval-augmented generation (RAG) system that combines the power of knowledge graphs (Neo4j) with vector similarity search to enhance information retrieval and question answering capabilities.

## Overview

This project implements a hybrid retrieval system that leverages:
- **Neo4j** for structured knowledge graph querying
- **Vector Database** (FAISS) for semantic similarity search
- **Hybrid Retrieval Pipeline** that combines both approaches for more comprehensive information retrieval

By combining graph-based querying with vector similarity search, this pipeline provides more contextually relevant and accurate results than using either approach alone.

## Features

- Document ingestion and processing pipeline
- Text chunking and embedding generation
- Knowledge graph construction from structured data
- Vector similarity search for semantic queries
- Graph traversal for relationship-based queries
- Hybrid retrieval combining both graph and vector-based results
- Simple query interface through Python scripts

## Installation

### Prerequisites

- Python 3.8+
- Neo4j Database (local or cloud instance)
- Git

### Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/graphrag-pipeline.git
   cd graphrag-pipeline
   ```
   
2. Create a virtual environment and install dependencies:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   pip install -r requirements.txt
   ```

3. Configure your Neo4j connection:
   ```bash
   Copy the .env.example file to .env
   Update the Neo4j connection details in the .env file
   ```
## Usage

### Data Ingestion
Process documents and build both vector embeddings and knowledge graph:
```bash
python ingest.py --data-dir /path/to/your/documents
```
## Querying the System
Run queries against the combined GraphRAG system:
```bash
python query.py --query "Your natural language query here"
```

## Advanced Usage
For more detailed control over the retrieval process:
```bash
python query.py --query "Your query" --graph-weight 0.7 --vector-weight 0.3 --top-k 5
```

##  Architecture
The system consists of three main components:

**1. Document Processor:** Handles document parsing, chunking, and preprocessing
**2. Vector Store:** Creates and stores embeddings using FAISS for semantic search
**3. Knowledge Graph:** Builds and queries a Neo4j graph database for structured information
**4. Hybrid Retriever:** Combines results from both retrieval methods

## Example Query Flow

1. User submits a question
2. Question is converted to embedding and relevant query patterns
3. Parallel retrieval from:

- Neo4j (structured data traversal)
- Vector DB (semantic similarity)


4. Results are combined, ranked and returned

## File Structure
├── README.md
├── requirements.txt
├── .env.example
├── src/
│   ├── __init__.py
│   ├── ingest.py           # Document ingestion pipeline
│   ├── query.py            # Query interface
│   ├── vector_store.py     # FAISS vector store implementation
│   ├── knowledge_graph.py  # Neo4j knowledge graph operations
│   ├── hybrid_retriever.py # Combined retrieval logic
│   └── utils.py            # Helper functions
├── examples/
│   ├── sample_query.py
│   └── batch_process.py
└── tests/
    ├── test_vector_store.py
    ├── test_knowledge_graph.py
    └── test_retrieval.py

## Configuration
Edit config.py to customize:

- Chunk size for text splitting
- Embedding model selection
- Neo4j connection parameters
- Retrieval weights and settings
    
## Author

**Okon Prince**  
*Data Scientist and AI Researcher  
Developer; Simple Cyber-Security Query Assistant  
Specialized in AI applications for cybersecurity, environmental intelligence, and education.*
