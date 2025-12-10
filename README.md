# Containerized RAG Architecture with BGE Embeddings and Qdrant

A scalable and efficient Retrieval-Augmented Generation (RAG) system containerized using Docker, leveraging BGE (BAAI General Embedding) models for document embeddings and Qdrant as a vector database for efficient similarity search.

## 🌟 Features

- **Document Processing**: Extract text from PDF documents with support for chunking large documents
- **Semantic Search**: Advanced vector similarity search using BGE embeddings
- **Containerized Architecture**: Easy deployment with Docker and Docker Compose
- **RESTful API**: FastAPI backend for document upload and querying
- **Streaming Responses**: Real-time streaming of query results
- **Document Management**: Upload, list, and delete documents through the API
- **Scalable**: Built to handle large document collections efficiently

## 🛠️ Tech Stack

- **Backend**: FastAPI
- **Vector Database**: Qdrant
- **Embeddings**: BGE (BAAI General Embedding) via Sentence Transformers
- **Frontend**: Streamlit-based web interface
- **Containerization**: Docker & Docker Compose
- **Document Processing**: PyPDF2, LangChain

## 🚀 Quick Start

### Prerequisites

- Docker
- Docker Compose
- Python 3.8+

### Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd "A Containerized RAG Architecture for Efficient Document Retrieval using BGE Embledings and Qdrant"
   ```

2. Build and start the services:
   ```bash
   docker-compose up --build
   ```

3. Access the web interface at `http://localhost:8501`

## 🧩 Project Structure

```
.
├── app.py              # FastAPI application with RAG endpoints
├── ui.py               # Streamlit web interface
├── Dockerfile          # Docker configuration for the application
├── docker-compose.yml  # Service definitions for the full stack
├── requirements.txt    # Python dependencies
└── ollama/             # Configuration for local LLM (if used)
```

## 📚 API Endpoints

- `POST /upload`: Upload a PDF document
- `POST /query`: Query the RAG system
- `GET /files`: List all uploaded files
- `DELETE /files`: Delete specific files

## 🤖 Using the RAG System

1. **Upload Documents**: Use the web interface or send a POST request to `/upload` with a PDF file
2. **Query the System**: Ask questions in natural language through the web interface or API
3. **Manage Documents**: View and delete uploaded documents as needed

## 🔧 Configuration

Configuration can be done through environment variables in the `docker-compose.yml` file:

- `QDRANT_HOST`: Qdrant service host (default: qdrant)
- `QDRANT_PORT`: Qdrant service port (default: 6333)
- `COLLECTION_NAME`: Name of the Qdrant collection (default: RAG-3.0)

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📬 Contact

- **Developer**: SUDIPTA ROY
- For any questions or feedback, please open an issue in the repository.