# Deploying a Simple GraphRAG Pipeline in Python

This project presents a streamlined implementation of a **Graph Retrieval-Augmented Generation (GraphRAG)** pipeline using Python. It is designed to construct knowledge graphs from text documents and use them to enhance the context-awareness of language models during response generation. The system integrates document parsing, chunking, semantic embeddings, and graph construction, and it provides an interactive interface for querying via Gradio.

## Project Objective

- Convert input text into a knowledge graph.
- Retrieve relevant information from the graph using semantic search.
- Use a fine-tuned language model to generate informed answers.
- Provide an easy-to-use interface for practical exploration and use.

## Model Used

The model used in this project is [`TinyLlama/TinyLlama-1.1B-Chat-v1.0`](https://huggingface.co/TinyLlama/TinyLlama-1.1B-Chat-v1.0), created by **Okon Prince**. This model is a small, efficient transformer-based language model designed for use on low-resource machines.

### Why TinyLlama?

- It is lightweight and can be run on CPUs or modest GPUs.
- Requires less memory and computation, enabling easier development and deployment.
- Suitable for fast experimentation and domain-specific fine-tuning.

### Domain Specialization

This model was trained using the `zeroshot/cybersecurity-corpus`, which makes it highly relevant for answering cybersecurity-related questions. The training goal was to make the model context-aware and capable of generating accurate responses in cybersecurity environments. This makes it ideal for enterprise systems, security analysts, and educational use cases within the cybersecurity domain.

## Dataset

This implementation is designed to work with any corpus of text documents, including `.txt` files. The documents are split into chunks, embedded, and used to build a semantic knowledge graph that enhances the model’s ability to retrieve and generate accurate information.

## Installation

To get started, install the required dependencies:

`pip install langchain openai gradio networkx sentence-transformers python-dotenv transformers accelerate tqdm matplotlib`

## Optional Dependencies

For additional functionality, install:

`pip install faiss-cpu`
`pip install huggingface_hub`

## API Key Configuration

If you are using OpenAI services for embeddings or language models, create a `.env` file in your project root directory with the following content:
`OPENAI_API_KEY=your_openai_api_key_here`

Make sure to load this environment variable before running the notebook. The `dotenv` package ensures secure access to API keys.

## How to Run

- Clone this repository or download the notebook.
- Install all dependencies listed above.
- Set up your `.env` file with API keys if applicable.
- Run the notebook step-by-step in a Jupyter environment.
- Launch the Gradio interface to interact with the GraphRAG system.

## Key Libraries and Tools

| Library/Tool             | Description                                                              |
|--------------------------|--------------------------------------------------------------------------|
| **LangChain**            | Framework for building LLM applications                                  |
| **OpenAI / HuggingFace** | For accessing and running LLMs and embeddings                            |
| **Sentence-Transformers**| Alternative to OpenAI embeddings for local use                           |
| **NetworkX**             | Graph construction and visualization                                     |
| **Gradio**               | Lightweight UI framework for ML apps                                     |
| **Transformers**         | For loading and using the TinyLlama model                                |
| **FAISS (optional)**     | Fast Approximate Nearest Neighbor search                                 |
| **dotenv**               | For securely loading API keys                                            |


## Model License

- **Model License**: Apache License 2.0  
- **Frameworks and Dependencies**: Open-source (MIT/BSD/Apache licenses)

Please ensure you comply with the individual licenses of all libraries and models used in this project.

## Possible Future Improvements

- Integrate an external graph database (e.g., Neo4j or Weaviate) for scalable knowledge graph management.
- Support additional file types such as PDF, Word, or HTML using parsers like PyMuPDF or BeautifulSoup.
- Add authentication and logging capabilities to the Gradio interface.
- Incorporate semantic reranking to improve retrieval relevance.
- Extend model functionality using fine-tuned adapters for other specialized domains.

## Author

**Okon Prince**  
Data Scientist and AI Researcher  
Developer; Simple Cyber-Security Query Assistant  
Specialized in AI applications for cybersecurity, environmental intelligence, and education.
