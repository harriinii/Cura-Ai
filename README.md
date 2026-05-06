# Cura AI 

# Cura AI — Smart Hostel Management System

<p align="center">
  <b>AI-powered complaint prioritization using RAG + LLMs</b><br/>
  Transforming hostel issue management with intelligent automation & real-time alerts
</p>

---

## 🧠 Overview

Cura AI is a Full-Stack AI system that intelligently analyzes student complaints, retrieves relevant hostel policies, and assigns priority levels with reasoning.

Unlike traditional systems, it doesn't just store complaints — it **understands, decides, and acts**.

---

## ✨ Key Features

- 🔹 AI-powered complaint classification (P1 / P2 / P3)  
- 🔹 Retrieval-Augmented Generation (RAG) for grounded decision-making  
- 🔹 Real-time emergency alerts using Twilio API  
- 🔹 Premium glassmorphism UI (React + Tailwind + Framer Motion)  
- 🔹 Mobile-ready using Capacitor  

---

## 🏗️ Architecture

```
User Complaint
      ↓
Frontend (React UI)
      ↓
FastAPI Backend
      ↓
LangChain (RAG Pipeline)
      ↓
ChromaDB ← hostel_policy.txt
      ↓
Gemini LLM (Reasoning + Classification)
      ↓
Priority Output + Explanation
      ↓
🚨 Twilio Alert (if Emergency)
```

---

## 📂 Project Structure

```
Cura-AI/
├── backend/
│   ├── main.py
│   ├── hostel_policy.txt
│   ├── chroma_db/
│   └── .env
│
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   └── App.jsx
│   ├── tailwind.config.js
│   └── vite.config.js
│
└── README.md
```

---

## 🚀 Getting Started

### 🔧 Backend Setup

```bash
cd backend
python -m venv .venv
.venv\Scripts\activate   # Windows
# source .venv/bin/activate  # Mac/Linux

pip install -r requirements.txt
```

---

### 💻 Frontend Setup

```bash
cd frontend
npm install
npm run dev
```

---

### 🔑 Environment Variables

Create a `.env` file inside `backend/`:

```env
GEMINI_API_KEY=your_api_key

TWILIO_ACCOUNT_SID=your_sid
TWILIO_AUTH_TOKEN=your_token
TWILIO_PHONE_NUMBER=your_twilio_number

WARDEN_PHONE_NUMBER=warden_phone
```

---

## ⚡ How It Works

1. Student submits a complaint  
2. System retrieves relevant rules from `hostel_policy.txt`  
3. Gemini LLM analyzes severity using context  
4. Assigns priority:
   - 🔴 P1 → Emergency  
   - 🟡 P2 → Standard  
   - 🟢 P3 → Routine  
5. 🚨 If P1 → instant SMS alert to warden  

---

## 📊 Priority Logic

| Priority | Type       | Example                | Action                        |
|----------|------------|------------------------|-------------------------------|
| 🔴 P1     | Emergency  | Fire, Electric Spark   | Instant SMS + Red Alert UI    |
| 🟡 P2     | Standard   | Water leak             | Logged for maintenance        |
| 🟢 P3     | Routine    | Food feedback          | Stored for review             |

---

## 📸 Screenshots

_Add your UI screenshots here_

```
![Dashboard](./screenshots/dashboard.png)
```

---

## 🎥 Demo

_Add your demo video link here_

```
https://your-demo-link.com
```

---

## 🔮 Future Enhancements

- 🤖 IoT-based predictive maintenance  
- 🌍 Multi-language complaint support  
- 🧠 Automated task assignment system  
- 📊 Analytics dashboard  

---

## 💡 Why This Project Stands Out

- Combines **LLM + RAG + Full Stack Development**
- Real-world use case (hostel/campus management)
- Goes beyond CRUD → **decision-making AI system**
- Includes automation (alerts + prioritization)

---

## 👩‍💻 Author

**Harini H**  
AI & ML Student | Computer Science & Engineering  

---
