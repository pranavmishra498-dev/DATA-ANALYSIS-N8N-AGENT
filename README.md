# 🤖 n8n Data Analysis Agent

An AI-powered data analysis agent built with **n8n**, **OpenAI**, **Google Sheets**, and **Gmail**.

The agent accepts a user's question through an n8n chat interface, uses an AI Agent to understand the request, retrieves data from Google Sheets, and can send the resulting analysis through Gmail.

## 🔄 Workflow

```text
User Question
     ↓
n8n Chat Trigger
     ↓
AI Agent
 ┌───┼───────────────┐
 ↓   ↓               ↓
OpenAI  Google Sheets  Gmail
Model   Data Tool      Email Tool
 ↓
Analysis / Response
```

## ✨ Features

- 💬 Chat-based data analysis
- 🤖 AI Agent powered by OpenAI
- 📊 Reads data from Google Sheets
- 🧠 Conversation memory
- 📧 Gmail integration for sending results
- ⚙️ Built entirely with n8n
- 🔌 Easy to extend with additional data sources and tools

## 🧩 Current Components

| Component | Purpose |
|---|---|
| Chat Trigger | Receives the user's question |
| AI Agent | Understands the request and coordinates tools |
| OpenAI Chat Model | Provides the AI reasoning/model |
| Simple Memory | Maintains recent conversation context |
| Google Sheets Tool | Retrieves rows from the configured spreadsheet |
| Gmail Tool | Sends messages/results through Gmail |

The exported workflow uses an OpenAI chat model and a memory window of 30 messages.

## 🚀 Setup

### 1. Import the workflow

Import:

`workflow/data-analysis-agent-sanitized.json`

into your n8n instance.

### 2. Configure OpenAI

Create/connect your OpenAI credential in n8n and attach it to the **OpenAI Chat Model** node.

### 3. Configure Google Sheets

Open **Get row(s) in sheet in Google Sheets** and replace:

`YOUR_GOOGLE_SHEET_URL`

with your spreadsheet URL.

Then connect your Google Sheets OAuth credential.

### 4. Configure Gmail

Open **Send a message in Gmail**, set the destination email address, and connect your Gmail OAuth credential.

### 5. Test

Start the workflow and ask questions such as:

- What is the average sales value?
- Which category has the highest sales?
- Show the top 5 records by revenue.
- What trends can you identify in this dataset?

## 🔐 Security

**Do not upload API keys, OAuth tokens, private spreadsheet links, or credential IDs to GitHub.**

This public version intentionally replaces personal configuration with placeholders. You should configure credentials directly inside n8n.

## 📁 Repository Structure

```text
n8n-data-analysis-agent/
├── README.md
├── LICENSE
├── .gitignore
├── workflow/
│   └── data-analysis-agent-sanitized.json
└── screenshots/
    └── .gitkeep
```

## 🛠️ Tech Stack

- n8n
- OpenAI
- Google Sheets
- Gmail
- AI Agent / LangChain nodes

## 👨‍💻 Author

**Pranav Mishra**

GitHub: https://github.com/pranavmishra498-dev
