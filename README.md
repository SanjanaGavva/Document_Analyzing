# Document_Analyzing

An AI-powered PDF Question Answering System built using LangChain, Google Gemini, ChromaDB, and Streamlit. This project allows users to upload and process PDF documents into a vector database and ask questions in natural language. The chatbot retrieves relevant information from the PDF and generates accurate answers using Google's Gemini model.

🚀 Features
📑 Extracts text from PDF documents
✂️ Splits documents into manageable chunks
🧠 Generates embeddings using Gemini Embedding Model
💾 Stores embeddings in Chroma Vector Database
🔍 Performs semantic search to retrieve relevant content
🤖 Uses Gemini 2.5 Flash for answering questions
🌐 Interactive Streamlit Web Interface
💻 Command-line chatbot support
🏗️ Project Structure
AI_PDF_RAG_Chatbot/
│
├── app.py                 # Streamlit web application
├── ingest.py              # Loads PDF and creates vector database
├── rag.py                 # Command-line RAG chatbot
├── docs/
│   └── Notes.pdf          # PDF document to analyze
├── chroma_db/             # Vector database (generated automatically)
├── .env                   # API keys
├── requirements.txt
└── README.md
🛠️ Technologies Used
Python
Streamlit
LangChain
Google Gemini API
ChromaDB
PyPDFLoader
Recursive Character Text Splitter
Retrieval-Augmented Generation (RAG)
⚙️ Installation
1️⃣ Clone the Repository
git clone https://github.com/your-username/AI_PDF_RAG_Chatbot.git
cd AI_PDF_RAG_Chatbot
2️⃣ Create Virtual Environment
python -m venv venv
Windows
venv\Scripts\activate
Linux/Mac
source venv/bin/activate
3️⃣ Install Dependencies
pip install -r requirements.txt
🔑 Configure API Key

Create a .env file in the project root.

GOOGLE_API_KEY=your_google_api_key

Get your API key from:

https://makersuite.google.com/app/apikey

📥 Step 1: Ingest the PDF

Place your PDF inside the docs folder.

Example:

docs/
 └── Notes.pdf

Run:

python ingest.py

Output:

Documents stored successfully!

This will:

Load the PDF
Split it into chunks
Generate embeddings
Store embeddings in ChromaDB
💻 Step 2: Run Command-Line Chatbot
python rag.py

Example:

Ask Question: What is Machine Learning?

Answer:
Machine Learning is a branch of Artificial Intelligence...

Type:

exit

to quit the chatbot.

🌐 Step 3: Run Streamlit Application
streamlit run app.py

The application will open in your browser:

http://localhost:8501
🖥️ Web Interface

The Streamlit application provides:

Text box to enter questions
Submit button
AI-generated answers based on PDF content
🔄 Workflow
PDF Document
      ↓
PyPDFLoader
      ↓
Text Splitting
      ↓
Gemini Embeddings
      ↓
Chroma Vector Database
      ↓
Retriever
      ↓
Gemini 2.5 Flash
      ↓
Final Answer
🧠 How RAG Works
Retrieval Phase
Converts user query into embeddings.
Searches ChromaDB for the most relevant chunks.
Generation Phase
Sends retrieved context and question to Gemini.
Gemini generates a context-aware answer.
📦 Requirements
streamlit
langchain
langchain-community
langchain-google-genai
langchain-chroma
langchain-classic
chromadb
pypdf
python-dotenv
