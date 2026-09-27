# 🤖 WhatsApp AI Agent — n8n Automation

An intelligent **WhatsApp AI Agent** built with **n8n**, **OpenAI**, **Supabase**, and **Green-API**.

This project connects WhatsApp with an AI-powered automation workflow that can receive messages, process them with an AI agent, use persistent data from Supabase, and automatically send intelligent responses back to the user.

---

## 🚀 Project Overview

The **WhatsApp AI Agent** works as an automated conversational assistant.

A user sends a message on WhatsApp → Green-API receives the message → n8n processes the request → OpenAI generates an intelligent response → Supabase can store/retrieve relevant data → the response is sent back to WhatsApp.

### 🔄 Workflow

```text
┌──────────────┐
│   WhatsApp   │
│    User      │
└──────┬───────┘
       │
       │ Message
       ▼
┌──────────────┐
│  Green-API   │
│ WhatsApp API │
└──────┬───────┘
       │
       ▼
┌──────────────┐
│     n8n      │
│  Automation  │
└──────┬───────┘
       │
       ▼
┌──────────────┐
│  OpenAI AI   │
│    Agent     │
└──────┬───────┘
       │
       │ Data / Memory
       ▼
┌──────────────┐
│   Supabase   │
│   Database   │
└──────┬───────┘
       │
       ▼
┌──────────────┐
│  Green-API   │
│ Send Message │
└──────┬───────┘
       │
       ▼
┌──────────────┐
│   WhatsApp   │
│   Response   │
└──────────────┘
```

---

## ✨ Features

* 💬 **WhatsApp AI Conversations**
* 🤖 **OpenAI-powered AI Agent**
* ⚡ **n8n workflow automation**
* 🗄️ **Supabase database integration**
* 🔄 **Automated message processing**
* 📲 **Automatic WhatsApp replies**
* 🧠 AI-powered conversational responses
* 🔐 API-based integration architecture
* 🔧 Modular workflow that can be extended for different business use cases

---

## 🛠️ Tech Stack

| Technology    | Purpose                                |
| ------------- | -------------------------------------- |
| **n8n**       | Workflow automation & AI orchestration |
| **OpenAI**    | AI model / response generation         |
| **Supabase**  | Database & persistent data             |
| **Green-API** | WhatsApp API integration               |
| **WhatsApp**  | User communication interface           |

---

## 🧩 How It Works

### 1️⃣ User Sends a WhatsApp Message

The user sends a message through WhatsApp.

### 2️⃣ Green-API Receives the Message

Green-API handles the WhatsApp communication and provides the incoming message to the automation workflow.

### 3️⃣ n8n Processes the Request

n8n acts as the central automation layer.

It receives the message and passes the required information to the AI Agent.

### 4️⃣ OpenAI Generates the Response

The AI Agent processes the user's message and generates an appropriate response using OpenAI.

### 5️⃣ Supabase Handles Data

Supabase can be used to store and retrieve conversation-related or application data, allowing the workflow to be extended with persistent information.

### 6️⃣ Response Is Sent Back to WhatsApp

The generated response is sent through Green-API and delivered to the user on WhatsApp.

---

## 📸 Workflow Preview

Add your n8n workflow screenshot here:

```markdown
![n8n Workflow](screenshots/workflow.png)
```

You can create a `screenshots` folder in the repository and place your workflow screenshot inside it.

---

## 📂 Project Structure

```text
whatsapp-ai-agent/
│
├── README.md
│
├── workflow/
│   └── whatsapp-ai-agent.json
│
├── screenshots/
│   └── workflow.png
│
└── .gitignore
```

> The exported n8n workflow can be placed inside the `workflow` folder.

---

## ⚙️ Setup

### Prerequisites

Before running the workflow, make sure you have:

* Node.js
* n8n
* OpenAI API access
* Supabase project
* Green-API account
* WhatsApp account/device for Green-API integration

---

### 1. Install n8n

```bash
npm install -g n8n
```

Start n8n:

```bash
n8n
```

Then open:

```text
http://localhost:5678
```

---

### 2. Configure OpenAI

Create an OpenAI API credential in n8n and connect it to the AI Agent node.

**Important:** Never upload your API key to GitHub.

---

### 3. Configure Supabase

Create a Supabase project and configure the required database/table.

Then add your Supabase credentials inside n8n.

Example environment variables:

```env
SUPABASE_URL=your_supabase_url
SUPABASE_KEY=your_supabase_key
```

> Keep credentials private and never commit real keys to the repository.

---

### 4. Configure Green-API

Create/configure your Green-API instance and connect it to your WhatsApp account.

Add the required Green-API credentials to the n8n workflow.

Example:

```text
GREEN_API_INSTANCE_ID=your_instance_id
GREEN_API_TOKEN=your_api_token
```

---

### 5. Import the n8n Workflow

Open n8n:

```text
http://localhost:5678
```

Then:

```text
Import Workflow
        ↓
Select workflow JSON
        ↓
Configure credentials
        ↓
Activate workflow
```

---

## 🔐 Security

This project uses external API credentials, so **never commit secrets to GitHub**.

Do not upload:

```text
❌ OpenAI API keys
❌ Supabase service-role keys
❌ Green-API tokens
❌ Passwords
❌ Private credentials
❌ Personal WhatsApp information
```

Use n8n Credentials or environment variables instead.

### `.gitignore`

```gitignore
.env
*.env
credentials.json
secrets.json
node_modules/
```

---

## 💡 Possible Use Cases

This AI Agent architecture can be adapted for:

* 🛒 E-commerce customer support
* 🏪 Business WhatsApp assistants
* 📚 Educational assistants
* 📅 Appointment booking
* ❓ FAQ automation
* 🎧 Customer support
* 🏨 Hotel/restaurant inquiries
* 📦 Order status automation
* 🧑‍💼 Lead collection
* 📈 Business workflow automation

---

## 🔮 Future Improvements

Some possible improvements include:

* 🧠 Long-term conversation memory
* 👤 User-specific profiles
* 📊 Admin dashboard
* 📈 Conversation analytics
* 🔎 RAG-based knowledge retrieval
* 📄 PDF/document knowledge base
* 🔔 Automated notifications
* 🧑‍💼 CRM integration
* 🗓️ Appointment scheduling
* 🌐 Multi-language support
* 🛠️ Additional business tools for the AI Agent

---

## 🎯 What I Learned

Building this project helped me practice:

* n8n workflow automation
* AI Agent architecture
* OpenAI API integration
* WhatsApp API integration
* Supabase database integration
* API authentication
* Webhook-based workflows
* Automation design
* AI-powered customer communication

---

## 👨‍💻 Author

**Nazakat Ali**

AI Student | AI Automation | Python | n8n | AI Agents

Interested in building practical **AI automation systems, AI agents, chatbots, and API integrations**.

---

## ⭐ Support

If you find this project useful, consider giving the repository a ⭐.

---

### 📌 Disclaimer

This project is created for educational, portfolio, and automation-development purposes. API providers and their respective services are subject to their own terms and policies.
