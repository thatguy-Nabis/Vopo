# 🎤 VoPo — Voice to Prompt

Convert your voice into perfectly engineered AI prompts, powered by **Gemini 1.5 Flash** (free tier).

---

## 📁 Structure

```
vopo/
├── app.py           # Flask backend (Gemini API)
├── requirements.txt
└── index.html       # Frontend (standalone, no build step)
```

---

## 🚀 Quick Start

### 1. Backend (Flask)

```bash
# Install dependencies
pip install -r requirements.txt

# Set your FREE Gemini API key (get one at aistudio.google.com)
export GEMINI_API_KEY="AIza..."   # macOS/Linux
set GEMINI_API_KEY=AIza...        # Windows CMD

# Run the server
python app.py
```

Flask runs on **http://localhost:5000**

### 2. Frontend

Open `index.html` in **Chrome or Edge** (required for Web Speech API).

> ⚠️ Firefox does not support the Web Speech API.

---

## 🔌 API Endpoints

| Method | Endpoint           | Description                        |
|--------|--------------------|------------------------------------|
| GET    | `/health`          | Health check                       |
| POST   | `/generate-prompt` | Generate enhanced prompt from text |
| POST   | `/improve-prompt`  | Improve an existing prompt         |

---

## ✨ Features

- 🎙 **Real-time voice recognition** — Web Speech API with start/stop toggle
- 🤖 **AI-powered enhancement** — Gemini 1.5 Flash (free tier)
- 🖼 **4 prompt modes** — General, Image, Text, Code
- ✨ **Improve button** — iterative prompt refinement
- 📋 **One-click copy** to clipboard

---

## 🔑 Getting a Free Gemini API Key

1. Go to [aistudio.google.com](https://aistudio.google.com)
2. Sign in with your Google account
3. Click **Get API key** → **Create API key**
4. Copy and export as `GEMINI_API_KEY`

The free tier supports **1,500 requests/day** with Gemini 1.5 Flash.

---

## 🛠 Tech Stack

| Layer    | Technology               |
|----------|--------------------------|
| Frontend | HTML/CSS/JS, Web Speech API |
| Backend  | Python Flask + CORS      |
| AI       | Google Gemini 1.5 Flash  |
