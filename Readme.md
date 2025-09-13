---
⚖️ Law Assistant AI Agent

![Banner Image] (assets/banner image.jpg)

A smart Law Assistant AI Agent powered by n8n workflows, Google Gmail/Drive, and LLMs. It processes client legal queries received by email, references the Constitution of Kenya (2010) from a vector database, and replies automatically in a professional format.
---

🎯 Key Features

📩 Automatic email processing via Gmail Trigger

📚 Constitutional Knowledge Base from Google Drive, chunked into vector embeddings

🧠 AI-powered classification of legal vs non-legal emails

🤖 AI Agent responses with references to the Constitution of Kenya (2010)

🚨 Filters irrelevant emails (ads, personal, business)

📝 Professional structured replies signed automatically

🔄 Seamless n8n workflow for end-to-end automation

---

🛠️ How It Works

1. Client sends an email with a query

2. Gmail Trigger activates when new mail arrives

3. Text Classifier checks if the email is legal-related or irrelevant

If non-legal → ignored

If legal → passed forward

4. Google Drive Trigger ensures the Kenyan Constitution (2010) is always up-to-date

5. Embeddings + Qdrant Vector DB store and retrieve constitutional knowledge

6. AI Agent (Gemini + Ollama) generates context-aware replies

7. Reply Node sends professional email back to client, signed automatically

> Visual representation of your Law Assistant AI Workflow

![Law assistant image](<assets/Law assistant workflow.png>)

---

🔹 Status Nodes (Workflow Steps)

Node Status Description

📩 Gmail Trigger Captures new incoming emails
📂 Google Drive Trigger Syncs latest Constitution files
🧩 Text Classifier Distinguishes law vs other emails
🗄️ Qdrant Vector Store Stores Constitution in vector form
🧠 AI Agent (Gemini + Ollama) Generates professional legal replies
✉️ Reply Node Sends AI reply via Gmail

---

📁 Repository Structure

├── workflows/ # n8n workflow JSON files  
├── src/ # AI Agent logic  
├── docs/ # Documentation & diagrams  
├── README.md # This file  
└── package.json # Node.js dependencies

---

⚙️ Installation

1. Clone the repository:

git clone https://github.com/your-username/law-assistant-ai-agent.git  
cd law-assistant-ai-agent

2. Install dependencies:

npm install

3. Set environment variables:

GMAIL_OAUTH2_TOKEN → Gmail API token

GOOGLE_DRIVE_API_KEY → Google Drive API key

QDRANT_API_KEY → Qdrant vector DB API key

OLLAMA_API_URL → Local Ollama service

N8N_WEBHOOK_URL → n8n workflow webhook URL

4. Start the AI Agent:

npm start

---

📊 Workflow Diagram

Visual representation of flow:
Gmail → Text Classifier → Qdrant DB → Gemini AI → Reply via Gmail

---

🤝 Contributing

We welcome contributions!

Fork the repository

Create a feature branch:

git checkout -b feature/your-feature

Make your changes

Submit a pull request

---

📄 License

This project is licensed under the MIT License – see LICENSE for details.

---

📌 Notes

Ensure Gmail & Google Drive APIs are properly configured

Test workflows in a staging environment before production

Regularly update the Constitution Knowledge Base for accuracy

🚀 Created with ❤️ by Ezra Wambugu – Legal Tech Specialist

-
