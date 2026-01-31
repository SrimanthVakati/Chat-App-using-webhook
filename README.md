# 🤖 AI Chat App using Webhook (n8n + Google Gemini)

This project is an **AI-powered chat application** built using **n8n workflows**, a **Webhook API**, and **Google Gemini (PaLM) AI model**. It allows users to send a message via HTTP POST request and receive an AI-generated response in real-time.

---

## 📌 Project Overview

The system works as a lightweight AI chat backend:

1. User sends a message via HTTP POST request
2. Webhook receives the request
3. AI Agent processes the message
4. Google Gemini generates the AI response
5. Response is returned to the user via Webhook

---

## 🧠 Architecture Flow

```
Client (POST Request)
        │
        ▼
   Webhook Node
        │
        ▼
     AI Agent
        │
        ▼
Google Gemini Model
        │
        ▼
Respond to Webhook → Client Response
```

---

## 🔧 Technologies Used

* **n8n** – Workflow automation platform
* **Webhook API** – For message input/output
* **LangChain AI Agent (n8n node)**
* **Google Gemini (PaLM) Chat Model**
* **REST API Architecture**
* **JSON-based workflow configuration**

---

## 📂 Project Components

### 1. Webhook Node

* Method: `POST`
* Path: `0bd026ef-f7e6-454d-ba95-chatapp`
* Purpose: Receives user messages

### 2. AI Agent Node

* Input: `{{$json.body.message}}`
* Role: Processes user message and sends it to AI model

### 3. Google Gemini Chat Model

* AI Engine for generating responses
* Connected as language model to AI Agent

### 4. Respond to Webhook Node

* Sends AI response back to the client

---

## 📥 API Usage

### Endpoint

```
POST /webhook/0bd026ef-f7e6-454d-ba95-chatapp
```

### Request Body (JSON)

```json
{
  "message": "Hello, how are you?"
}
```

### Response (Example)

```json
{
  "reply": "Hello! I'm doing great. How can I help you today?"
}
```

---

## 🚀 How to Run the Project

1. Install **n8n**
2. Import the workflow JSON file into n8n
3. Configure **Google Gemini (PaLM) API credentials**
4. Activate the workflow
5. Copy the webhook URL
6. Send POST requests using:

   * Postman
   * Curl
   * Frontend app
   * Mobile app

---

## 💡 Use Cases

* AI Chatbot backend
* AI customer support bot
* AI automation agent
* AI assistant API
* SaaS AI chat integration
* WhatsApp/Telegram AI bot backend

---

## 🔐 Security Notes

* Secure webhook endpoint
* Use API authentication
* Rate limiting recommended
* Environment variable storage for API keys

---

## 📈 Future Enhancements

* Multi-user chat support
* Conversation memory
* User authentication
* Database integration
* Frontend UI
* Voice input/output
* Multi-language support

---

## 👨‍💻 Author

**Project by:** Srimanth Sri
**Domain:** AI Automation / AI Agents / Workflow Automation
**Platform:** n8n + Generative AI

---

## 📄 License

This project is open-source and free to use for learning, development, and research purposes.

---

✨ *Built with AI, Automation, and Innova
