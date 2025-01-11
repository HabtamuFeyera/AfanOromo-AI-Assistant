# Afan Oromo Knowledge Assistant

## Overview
The **Afan Oromo Knowledge Assistant** is an AI-powered application designed to provide users with accurate, context-aware responses to their questions about the Afan Oromo language, culture, and history. This project combines state-of-the-art Generative AI technologies with a commitment to preserving and promoting Afan Oromo knowledge in the digital age. 

The assistant is built using OpenAI's language models, LangChain, vector databases, and FastAPI. It is a robust showcase of advanced AI capabilities while delivering real-world value to Afan Oromo-speaking communities.


## Features
- **Multilingual Query Support**: Accepts user questions in Afan Oromo or English.
- **Context-Aware Responses**: Leverages a curated knowledge base to provide accurate, detailed answers.
- **Scalable Knowledge Base**: Allows for dynamic updates to the database for continuous improvement.
- **Fast and Reliable**: Powered by FastAPI and optimized for performance and scalability.


## Project Goals
1. **Knowledge Accessibility**: Provide easy access to Afan Oromo language and cultural information.
2. **Language Preservation**: Promote and preserve Afan Oromo in digital spaces.
3. **Technical Excellence**: Showcase expertise in AI technologies, including OpenAI, LangChain, and FastAPI.


## Project Structure
```plaintext
AfanOromo-AI-Assistant/
├── backend/
│   ├── main.py             # FastAPI application entry point
│   ├── routes/
│   │   ├── query.py        # Endpoint for handling user queries
│   │   ├── upload.py       # Endpoint for uploading new data
│   ├── services/
│   │   ├── embeddings.py   # Logic for generating and handling embeddings
│   │   ├── retrieval.py    # Logic for vector database queries
│   │   ├── ai_response.py  # OpenAI integration for generating responses
│   ├── models/
│   │   ├── query_model.py  # Pydantic models for query requests
│   ├── config.py           # Configuration file for API keys and settings
│   ├── requirements.txt    # Python dependencies
├── data/
│   ├── raw/                # Original Afan Oromo data sources
│   ├── processed/          # Cleaned and preprocessed data
│   ├── embeddings/         # Vector embeddings stored here
├── frontend/
│   ├── src/
│   │   ├── pages/
│   │   │   ├── index.js    # Home page for the interface
│   │   ├── components/
│   │   │   ├── QueryForm.js # Form for user input
│   │   │   ├── Response.js  # Component to display AI responses
│   │   ├── services/
│   │   │   ├── api.js      # API calls to the backend
│   ├── public/             # Static assets
│   ├── package.json        # Frontend dependencies
├── deployment/
│   ├── Dockerfile          # Containerize the application
│   ├── docker-compose.yml  # Orchestrate services
│   ├── cloud-config/       # Cloud deployment scripts
├── docs/
│   ├── README.md           # Project overview and setup instructions
│   ├── API.md              # Documentation for API endpoints
│   ├── CONTRIBUTING.md     # Contribution guidelines
├── tests/
│   ├── backend_tests.py    # Unit tests for backend
│   ├── frontend_tests.js   # Unit tests for frontend
└── .gitignore              # Files and directories to ignore in Git
```


## Setup and Installation
### Prerequisites
1. Python 3.10+
2. Node.js 14+
3. Docker (for deployment)
4. OpenAI API Key

### Backend Setup
1. Clone the repository:
   ```bash
   git clone https://github.com/HabtamuFeyera/AfanOromo-AI-Assistant.git
   cd AfanOromo-AI-Assistant/backend
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Set up environment variables in a `.env` file:
   ```plaintext
   OPENAI_API_KEY=your_openai_api_key
   VECTOR_DB_URL=your_vector_db_url
   ```
4. Run the backend:
   ```bash
   uvicorn main:app --reload
   ```

### Frontend Setup
1. Navigate to the frontend directory:
   ```bash
   cd ../frontend
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Start the development server:
   ```bash
   npm run dev
   ```

### Running Tests
- Backend tests:
  ```bash
  pytest
  ```
- Frontend tests:
  ```bash
  npm run test
  ```


## Deployment
### Docker Deployment
1. Build and run the containers:
   ```bash
   docker-compose up --build
   ```
2. Access the application at `http://localhost:8000` for the backend and `http://localhost:3000` for the frontend.

### Cloud Deployment
Use cloud providers like AWS, Azure, or Google Cloud to host the backend, frontend, and vector database. Refer to the `deployment/cloud-config` directory for configuration files.


## Usage
1. **Querying the Assistant**:
   - Open the frontend interface.
   - Enter a question in Afan Oromo or English.
   - Receive detailed responses powered by AI.
2. **Updating the Knowledge Base**:
   - Use the `POST /add-data` endpoint to upload new documents for indexing.


## Contributing
Contributions are welcome! Please refer to the `CONTRIBUTING.md` file for guidelines on how to get started.


## License
This project is licensed under the MIT License. See the `LICENSE` file for details.


## Acknowledgments
- Afan Oromo community and contributors.
- OpenAI for providing state-of-the-art AI models.
- Developers of LangChain, Pinecone, and FastAPI for their invaluable tools.

