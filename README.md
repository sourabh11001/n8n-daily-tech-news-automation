# 📰 n8n Daily Tech News Automation

This repository contains a **reusable n8n workflow** that automatically collects tech news from multiple RSS feeds, summarizes it using a **Google Gemini AI Agent**, and sends a daily email digest.

⚠️ **No credentials are included in this repository.**  
You must add your own credentials after importing the workflow.

---

## 🚀 What This Workflow Does

The automation runs on a schedule and performs the following steps:

1. Triggers daily at a fixed time
2. Fetches tech news from multiple RSS sources
3. Aggregates articles from the past 24 hours
4. Uses an **AI Agent powered by Google Gemini Chat Model** to generate summaries
5. Formats the output using Markdown
6. Sends the final summary via email

---

## 🧠 Workflow Architecture

### Nodes Used

- **Schedule Trigger** – runs the workflow daily  
- **Set** – defines RSS feed URLs  
- **Split Out** – processes each RSS feed individually  
- **RSS Feed Read** – fetches articles  
- **Aggregate** – combines article content  
- **AI Agent** – controls summarization logic  
- **Google Gemini Chat Model** – provides AI text generation  
- **Markdown** – converts AI output to HTML  
- **Gmail** – sends the email digest  

---

## 🤖 AI & Model Details

This workflow uses **n8n’s AI Agent node** connected to a **Google Gemini Chat Model**.

- The **AI Agent** defines what the AI should do
- The **Gemini Chat Model** generates the summarized content
- The output is clean, readable, and non-technical

---

## 🔐 Credentials Setup (IMPORTANT)

This repository **does NOT include any credentials**.

After importing the workflow into n8n, you must manually add:

### Required Credentials
- **Google Gemini (PaLM) API**
- **Gmail OAuth2**

### Steps to Add Credentials
1. Open your n8n instance
2. Go to **Credentials**
3. Create the required credentials
4. Attach them to the corresponding nodes
5. Activate the workflow

⚠️ Never commit credentials, API keys, or the `.n8n` folder to GitHub.

---

## 📂 Repository Structure
.
├── workflows/
│   └── NEWS_AUTOMATION_TEMPLATE.json
├── .env.example
├── .gitignore
└── README.md


## ▶️ How to Use This Workflow

1. Clone this repository
2. Open your n8n instance
3. Import `NEWS_AUTOMATION_TEMPLATE.json`
4. Add your own credentials inside n8n
5. Test the workflow
6. Activate it

---

## 🔒 Security Notes

- No secrets are stored in this repository
- All credentials must be managed inside n8n
- This workflow is shared as a template
- Safe for public and portfolio use

---

## ⚙️ Requirements

- n8n (self-hosted or cloud)
- Google Gemini API access
- Gmail account with OAuth enabled
- Internet access for RSS feeds

---

## 👤 Author

**Sourabh Bhimagonda Kagilkar**

---

## ⭐ Feedback & Usage

Feel free to fork this repository, customize the workflow, or use it as a base for your own automations.
