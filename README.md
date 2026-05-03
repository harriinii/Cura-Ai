# Cura AI

Cura AI is a high-end Full-Stack RAG (Retrieval-Augmented Generation) application designed for smart complaint prioritization in hostels. It uses artificial intelligence to analyze student reported issues, consults the local hostel policy, and automatically tags them with a priority level along with the reasoning.

## 🌟 Features

- **Automated Complaint Prioritization**: Uses LangChain and Google's Gemini Flash model to classify the priority (e.g., Priority 1, Priority 2, Priority 3) of incoming complaints.
- **RAG Architecture**: The AI reads directly from `hostel_policy.txt` utilizing ChromaDB for local vector storage, grounding its decisions in the actual rules of the hostel.
- **Premium User Interface**: Built with React and Tailwind CSS, featuring a stunning 'Glassmorphism' dark mode design, accented with Electric Violet and Emerald Green. Smooth animations are powered by Framer Motion.
- **Warden Dashboard**: A comprehensive admin view showing all logged complaints, their automatically assigned priorities, and the AI's step-by-step reasoning for full transparency.

## 🏗️ Architecture

1. **Frontend (React.js)**: Captures user input (Student Portal) and displays insights (Admin Dashboard).
2. **Backend (Python / FastAPI)**: Handles API requests securely.
3. **Vector Database (ChromaDB)**: Chunks and embeds the `hostel_policy.txt` to enable semantic search capabilities.
4. **LLM (Gemini Flash via LangChain)**: Interprets context and rules from ChromaDB to assign accurate, policy-based prioritizations.

## 🚀 Getting Started

### 1. Backend Setup

Navigate to the `backend` directory, create a virtual environment, and install dependencies:

```bash
cd backend
python -m venv venv
# On Windows
venv\Scripts\activate
# On Mac/Linux
source venv/bin/activate
pip install -r requirements.txt
```

### 2. Environment Variables

Create a `.env` file in the root backend directory (based on `.env.template`) and add your Gemini API Key:

```env
GEMINI_API_KEY=your_actual_gemini_api_key_here
```

### 3. Run the Backend Server

Start the FastAPI server:

```bash
uvicorn app.main:app --reload
```

The server will start on `http://localhost:8000`. You can test the endpoints using the Swagger UI at `http://localhost:8000/docs`.

### Next Steps...

The frontend implementation utilizes Vite, React, Tailwind UI, and Framer Motion for the premium dark mode experience.
