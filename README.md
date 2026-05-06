# Cura AI 

**Cura AI: Smart Hostel Management System**

Cura AI is a high-end Full-Stack RAG (Retrieval-Augmented Generation) application designed for intelligent complaint prioritization. It moves beyond manual registers by using AI to analyze reported issues, consult local hostel policies, and take autonomous action for emergencies.

---

## 📂 Project Structure

```
Cura-AI/
├── 📂 backend/
│   ├── 📄 main.py              # FastAPI endpoints & AI Orchestration
│   ├── 📄 hostel_policy.txt    # Knowledge base for RAG
│   ├── 📂 chroma_db/           # Persistent Vector Storage
│   └── 📄 .env                 # API Keys & Secrets
├── 📂 frontend/
│   ├── 📂 src/
│   │   ├── 📂 components/      # Glassmorphism UI elements
│   │   └── 📄 App.jsx          # Main React logic & Framer Motion
│   ├── 📄 tailwind.config.js   # Custom Electric Violet/Emerald theme
│   └── 📄 vite.config.js       # Build configurations
└── 📄 README.md                # Documentation
```

---

## 🌟 Key Features

- **Automated Prioritization**  
  Uses LangChain and Gemini 1.5 Flash to classify issues into:
  - Priority 1 (Emergency)
  - Priority 2 (Standard)
  - Priority 3 (Routine)

- **RAG Architecture**  
  Grounded in a local `hostel_policy.txt` knowledge base using ChromaDB to ensure decisions follow official rules.

- **Real-Time Emergency Alerts**  
  Integrated with Twilio API to send instant SMS notifications to the warden for critical issues.

- **Premium Glassmorphism UI**  
  Dark-mode dashboard built with React, Tailwind CSS, and Framer Motion.

- **Mobile-Ready**  
  Wrapped with Capacitor for a native Android/iOS experience.

---

## 🏗️ Technical Architecture

- **Frontend:** React.js + Vite (Tailwind CSS + Framer Motion)  
- **Backend:** Python + FastAPI  
- **Orchestration:** LangChain (RAG Pipeline)  
- **Vector Database:** ChromaDB (Semantic Search & Embeddings)  
- **LLM:** Gemini 1.5 Flash (Google Generative AI)  
- **Communication:** Twilio API (SMS Gateway)  
- **Mobile Bridge:** Capacitor  

---

## 🚀 Getting Started

### 1️⃣ Backend Setup

```bash
cd backend
python -m venv .venv
.venv\Scripts\activate   # Windows
# source .venv/bin/activate  # Mac/Linux

pip install -r requirements.txt
```

---

### 2️⃣ Frontend Setup

```bash
cd frontend
npm install
npm run dev
```

---

### 3️⃣ Configuration (.env)

Create a `.env` file inside the `backend` folder:

```env
GEMINI_API_KEY=your_gemini_key
TWILIO_ACCOUNT_SID=your_sid
TWILIO_AUTH_TOKEN=your_token
TWILIO_PHONE_NUMBER=your_twilio_number
WARDEN_PHONE_NUMBER=warden_phone_number
```

---

## 💡 Priority Logic (Risk Assessment)

| Level | Classification | Example Issue              | System Action                      |
|------|--------------|---------------------------|----------------------------------|
| P1   | Emergency     | Electrical spark / Fire   | 🚨 Red Alert + Instant SMS        |
| P2   | Standard      | Water leak / Light issue  | Logged for maintenance           |
| P3   | Routine       | Food feedback             | Stored as non-urgent feedback    |

---

## 🔮 Future Roadmap

- **IoT Integration**  
  Smart sensors for predictive maintenance  

- **Multi-lingual Support**  
  Report issues in native languages  

- **Self-Healing System**  
  Auto-assign maintenance tasks  

---

## 👩‍💻 Developed By

**Harini H**  
AI & ML Student | Computer Science & Engineering
