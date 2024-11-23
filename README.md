# RAG Chatbot with Azure OpenAI

A Retrieval Augmented Generation (RAG) chatbot that can understand and answer questions about uploaded PDF documents. Built with Azure OpenAI, FastAPI, and React.

## 🌟 Features

### PDF Processing Engine
- Intelligent text extraction from PDF documents
- Advanced text chunking with customizable overlap
- Optimized document processing using LangChain's RecursiveCharacterTextSplitter

### Vector Storage System
- Efficient document storage using ChromaDB
- Full metadata support for enhanced document tracking
- Fast similarity search for accurate information retrieval

### Advanced Chat Management
- Persistent conversation history
- Context-aware response generation
- Hallucination prevention system
- Powered by Azure OpenAI API

### Modern Architecture
- RESTful API endpoints using FastAPI
- Full CORS support for cross-origin requests
- React-based frontend with real-time updates
- Responsive UI with modern design principles

## 🛠️ Technical Stack

- **Backend**: FastAPI, Python 3.8+
- **Frontend**: React, Tailwind CSS
- **Vector Database**: ChromaDB
- **LLM**: Azure OpenAI
- **PDF Processing**: PyPDF2
- **Text Processing**: LangChain

## 🚀 Getting Started

### Prerequisites

- Python 3.8 or higher
- Node.js 14 or higher
- Azure OpenAI API access
- npm or yarn

### Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/rag-chatbot.git
cd rag-chatbot
```

2. Install backend dependencies:
```bash
pip install -r requirements.txt
```

3. Install frontend dependencies:
```bash
cd frontend
npm install lucide-react @radix-ui/react-alert @radix-ui/react-card
npm install
```

4. Create a `.env` file in the root directory:
```env
AZURE_API_KEY=your_api_key
AZURE_ENDPOINT=your_endpoint
AZURE_DEPLOYMENT_NAME=your_deployment_name
```

### Running the Application

1. Start the backend server:
```bash
python api/main.py
```

2. Start the frontend development server:
```bash
cd frontend
npm start
```

The application will be available at `http://localhost:3000`

## 🔍 How It Works

1. **Document Upload**:
   - Upload PDF documents through the UI
   - Documents are processed and chunked automatically
   - Text chunks are vectorized and stored in ChromaDB

2. **Query Processing**:
   - User questions are vectorized
   - Relevant context is retrieved from the vector store
   - Azure OpenAI generates accurate, context-aware responses

3. **Hallucination Prevention**:
   - Explicit context inclusion in prompts
   - Strict context-based response generation
   - Conversation history tracking for consistency

## 📝 API Endpoints

- `POST /upload`: Upload and process PDF files
- `POST /query`: Submit questions and receive answers

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## ✨ Acknowledgments

- Azure OpenAI for the language model
- LangChain for text processing utilities
- ChromaDB for vector storage
- FastAPI for the backend framework
- React for the frontend framework










The error occurs because the package name has changed. Let me help you with the correct installation commands and package versions.



# Installation Guide for RAG Chatbot Dependencies

## Core Dependencies

```bash
# Install Azure OpenAI SDK
pip install openai

# Install other required packages
pip install langchain
pip install chromadb
pip install PyPDF2
pip install fastapi
pip install python-multipart
pip install uvicorn
pip install python-dotenv

# Optional: Install all at once using requirements.txt
```

## Requirements.txt
```text
openai>=1.0.0
langchain>=0.1.0
chromadb>=0.4.18
PyPDF2>=3.0.1
fastapi>=0.104.1
python-multipart>=0.0.6
uvicorn>=0.24.0
python-dotenv>=1.0.0
```

## Notes:
1. The `azure-openai` package is now part of the main `openai` package
2. Use the OpenAI SDK version 1.0.0 or higher for Azure OpenAI support
3. Make sure to use Python 3.8 or higher

## Code Update
Update the import statement in your code from:
```python
from azure.openai import AzureOpenAI
```
to:
```python
from openai import AzureOpenAI
```

## Troubleshooting
If you encounter any issues:
1. Make sure your Python version is compatible (3.8+)
2. Clear your pip cache: `pip cache purge`
3. Update pip: `python -m pip install --upgrade pip`
4. Create a new virtual environment if needed:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
```


The main change is that we now use the unified `openai` package instead of the separate `azure-openai` package. This change was made when OpenAI released version 1.0.0 of their Python SDK, which includes Azure OpenAI support.

The rest of your code should work as is, just make sure to update the import statement as shown above. Would you like me to show you the updated main code with the correct imports?