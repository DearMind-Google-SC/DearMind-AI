# DearMind-AI

FastAPI Powered AI Model Server for **DearMind**, a digital art therapy service built for the **Google Solution Challenge 2025**.

---

## 🧠 What is DearMind?

**DearMind** is a mobile-based digital art therapy service that helps users express emotions through drawings and short journals.  
The app provides AI-powered emotion analysis, self-care activity recommendations, and personalized visual rewards based on consistent emotional journaling.

This repository contains the **FastAPI-powered AI server**, which supports:

- RAG-based Emotion Analysis
- Reward picture & letter generation
- AI chatbot

---

## 🛠️ Tech Stack

| Layer          | Technology |
|----------------|------------|
| Model Servng   | FastAPI |
| AI Integration | Vertex AI (Gemini + Imagen) |
| Deployment     | GCP Clud Run |
| Docs           | FastAPI |

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/DearMind-Google-SC/DearMind-AI.git
cd DearMind-AI
```

### 2. Build Docker Image

```bash
docker build -t dearmind-ai .
```

### 3. Run Docker Container

```bash
# If you have your GOOGLE_APPLICATION_CREDENTIALS file in your local storage
docker run -d \
-p 8000:8080 \
-v /path/to/key.json:/secrets/key.json:ro \
-e GOOGLE_APPLICATION_CREDENTIALS=/secrets/key.json \
dearmind-ai

# If you already have your credential values mounted in your environment variable
# For Linux & Mac
docker run -d -p 8000:8080 -v ~/.config/gcloud:/root/.config/gcloud dearmind-ai
# For Windows
docker run d -p 8000:8080 -v ${HOME}\.config\gcloud:/root/.config/gcloud dearmind-ai
```

---

## 📘 API Documentation

Once the server is running, access the API docs at:

```bash
http://localhost:8000/docs
```

---

## 🚢 Deployment

This server is deployed on Google Cloud Run.

---

## 👥 Contributors

- AI: Seunghwan Oh (오승환)      
- PM, Backend, Frontend, and Design: See full team credits in the project presentation

---

## 📄 License

This project is licensed under the MIT License.

