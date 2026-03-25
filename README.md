# 🤖 Career Conversation AI Agent (Digital Twin)

An AI-powered conversational agent that represents me (Sai Thanmayi) and interacts with users about my career, skills, and experience.

It allows users to explore my profile, ask questions, and optionally share their contact details. If a user shows interest, the system sends a real-time notification.
## 🌐 Live Demo

Try the app here:
👉 https://huggingface.co/Thanmayi6

---

## 🚀 Features

### 💬 Conversational Career Agent

* Acts as a digital version of me
* Answers questions about my background, skills, and experience
* Uses structured prompts with personal data

### 🧠 Custom Function-Based Agent

* Built using OpenAI function calling
* No external agent frameworks used
* Custom tool execution and control loop

### 📩 Contact Capture + Notifications

* Detects when a user wants to connect
* Records:

  * Email
  * Name (optional)
  * Notes
* Sends real-time alerts using Pushover

### ❓ Unknown Question Tracking

* Logs questions the agent cannot answer
* Helps improve responses over time

### 🌐 Web Interface

* Built using Gradio ChatInterface
* Simple and interactive UI
* Ready for Hugging Face deployment

---

## 🛠️ Tech Stack

* Python
* OpenAI API (GPT-4o-mini)
* Gradio
* Hugging Face Spaces
* Pushover API
* PyPDF

---

## 📂 Project Structure

```
.
├── app.py              # Main agent + UI logic
├── 4_lab4.ipynb        # Lab experimentation
├── me/
│   ├── linkedin.pdf    # Profile data source
│   ├── summary.txt     # Personal summary
├── README.md
```

---

## ⚙️ How It Works

1. User interacts with the agent via chat
2. System prompt injects:

   * Personal summary
   * LinkedIn data
3. The model generates responses
4. If needed, it calls tools:

   * `record_user_details()` → saves contact info
   * `record_unknown_question()` → logs unknown questions
5. Tool execution triggers:

   * Real-time notification via Pushover

---

## 📁 Setup Personal Data

This project uses personal data to power the agent. You must provide your own files:

1. Create a folder:

```
mkdir me
```

2. Add the following files:

* `linkedin.pdf` → Export your LinkedIn profile as a PDF
* `summary.txt` → Write a short summary about yourself

Example:

```
me/
├── linkedin.pdf
├── summary.txt
```

---

## 🔐 Environment Variables

Create a `.env` file in the root directory:

```
PUSHOVER_TOKEN=your_token_here
PUSHOVER_USER=your_user_key_here
OPENAI_API_KEY=your_openai_api_key
```

---

## ▶️ Run Locally

```
pip install -r requirements.txt
python app.py
```

---

## 🌍 Deployment

This app is designed to be deployed on **Hugging Face Spaces** using Gradio.

---

## 📬 Contact Workflow

If a user:

* Shows interest
* Wants to connect
* Shares their email

👉 The system:

1. Records their details
2. Sends a Pushover notification instantly

---

## 📌 Highlights

* ✅ Real-world use case (career + networking)
* ✅ Custom-built agent (no frameworks)
* ✅ Tool/function calling implementation
* ✅ External API integration
* ✅ Deployment-ready UI

---

## 🌟 Purpose

This project demonstrates:

* Building AI agents from scratch
* Function/tool calling workflows
* API integrations
* Deployable AI applications

---

## 🙌 Inspiration and Acknowledgment

* Based on Lab 4 experimentation - Ed Donner!
* Extended into a real-world personal AI agent

---
