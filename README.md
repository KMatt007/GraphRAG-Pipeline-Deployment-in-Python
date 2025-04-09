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


## Author

**Okon Prince**  
*Data Scientist and AI Researcher  
Developer; Simple Cyber-Security Query Assistant  
Specialized in AI applications for cybersecurity, environmental intelligence, and education.*
