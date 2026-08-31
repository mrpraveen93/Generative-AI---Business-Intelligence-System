# AI-Analyst-RAG-System
RAG-based AI Business Analyst using SQL, FAISS, LangChain and Llama 3.3 70B
# AI Analyst – RAG-Based Business Intelligence System

## 📌 Project Overview

AI Analyst is a Generative AI-powered Business Intelligence application that allows users to ask business questions in natural language.

The system analyzes both structured and unstructured data using SQL and Retrieval-Augmented Generation (RAG).

It automatically determines whether a question requires SQL, RAG, or both, and generates a business-friendly response using an LLM.

## 🎯 Objectives

- Analyze structured event-management data using SQL.
- Retrieve business information from PDF documents using RAG.
- Automatically classify questions as SQL, RAG, or BOTH.
- Generate business insights using an LLM.
- Provide an easy-to-use web interface for business users.

## 🏗️ Architecture

User Question
        ↓
Question Classification
        ↓
 ┌──────┼──────┐
 ↓      ↓      ↓
RAG    SQL    BOTH
 ↓      ↓      ↓
FAISS SQLite  SQL + RAG
 └──────┼──────┘
        ↓
      LLM
        ↓
Business Response
        ↓
     Gradio UI

## 🛠️ Technologies

- Python
- Pandas
- SQLite
- LangChain
- Hugging Face
- FAISS
- Sentence Transformers
- Groq
- Llama 3.3 70B
- Gradio
- PyPDFLoader

## 📊 Data

The project uses:

- Event Management Excel dataset
- Business Reports PDF
- Operations Playbook PDF

The structured data contains Events, Vendors, and Monthly Summary information.

## 🔎 RAG Pipeline

1. Load PDF documents.
2. Extract document text.
3. Split documents into chunks.
4. Generate embeddings.
5. Store embeddings in FAISS.
6. Retrieve relevant documents based on the user question.
7. Send retrieved context to the LLM.
8. Generate the final response.

## 🗄️ SQL Pipeline

Structured Excel data is loaded using Pandas and stored in SQLite.

The LLM generates SQL queries based on the user's natural-language question.

The query is executed against SQLite and the result is converted into a business-friendly answer.

## 🔀 Intelligent Routing

The system supports three routes:

### RAG
Used for document-based and qualitative questions.

Example:
"What are the vendor selection criteria?"

### SQL
Used for numerical and structured-data questions.

Example:
"Which city generated the highest revenue?"

### BOTH
Used when a question requires both business data and contextual information.

Example:
"Which event type generates the most revenue and what strategy should management use?"

## 📈 Key Insights

- Jaipur generated the highest revenue.
- Chennai generated the lowest revenue.
- Wedding events generated the highest revenue among event types.
- The system can answer questions using SQL, RAG, or both.

## 💻 Application

The final application is built using Gradio.

Users can enter natural-language business questions and receive:

- AI-generated answer
- Query route
- SQL query when applicable
- Retrieved document sources
- Business insights

## 🚀 Future Scope

- Real-time database integration
- Power BI integration
- Predictive analytics
- AI recommendation system
- Authentication and role-based access
- Enterprise document integration
- Voice-based AI Analyst

## 👨‍💻 Author

PRAVEEN MANDANGI
