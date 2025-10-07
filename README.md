<div align="center">

![n8n](https://img.shields.io/badge/n8n-Automation%20Flow-red.svg)
![OpenAI GPT-5](https://img.shields.io/badge/OpenAI-GPT--5-blue.svg)
![Google Sheets](https://img.shields.io/badge/Google%20Sheets-Integrated-green.svg)
![Tavily API](https://img.shields.io/badge/Tavily%20API-Connected-yellow.svg)
![Status](https://img.shields.io/badge/Workflow-AI%20Driven-purple.svg)

# 🤖 LinkedIn Content Creator

**Automate professional LinkedIn post creation with AI — powered by GPT-5, n8n & Google Sheets**

Generate, refine, and publish thought-leadership posts with zero manual effort.  
Transform trending topics into polished content ready to engage your audience.

[✨ Features](#-features) • [⚙️ Workflow Overview](#-WorkflowOverview) • [📸 Preview](#-preview)

</div>

---

## ✨ Features

- 🔄 **Fully Automated Workflow** — fetch topics, research web content, generate posts, and update your sheet  
- 🧠 **AI-Powered Writing** — GPT-5 crafts original, scannable, inspiring LinkedIn posts  
- 🌍 **Tavily Web Search Integration** — fetches top 3 articles for contextually rich insights  
- 📊 **Google Sheets as CMS** — manage topics and track post completion status  
- 💬 **Ready-to-Publish Output** — includes emojis, hashtags, and reflective CTAs  
- 🧩 **No-Code Setup** — import directly into n8n  

---

## ⚙️ Workflow Overview

### 🧩 Components
| Node | Description |
|------|--------------|
| **Manual / Schedule Trigger** | Starts the workflow manually or at a set time daily |
| **Google Sheets** | Reads a list of “To Do” topics |
| **HTTP Request** | Fetches 3 top articles related to each topic using Tavily API |
| **AI Agent** | Analyzes the articles and crafts an original LinkedIn post |
| **OpenAI Chat Model (GPT-5)** | Powers the content generation |
| **Google Sheets Update** | Writes the final post and marks the topic as “Done” |

---

## 🧠 AI Logic

The AI agent follows an internal SOP (Standard Operating Procedure):

1. **Extract Insights** from top 3 articles  
2. **Paraphrase into new sentences** (7–8 lines, short & scannable)  
3. **Maintain a professional + inspiring tone**  
4. **Add 1–2 emojis & 3–5 hashtags**  
5. **End with a reflective or question-based CTA**

---

## 📊 Example Google Sheet

| Topic | Status | Content |
|-------|---------|----------|
| “AI Product Strategy” | To Do |  |
| “Growth in SaaS Markets” | To Do |  |
| “Leadership in Uncertain Times” | Done | “Innovation thrives on uncertainty 🌱…” |

---

## 🚀 How It Works

1. **Trigger Workflow**  
   - Manually (when you click “Execute”) or automatically at 9 AM.

2. **Fetch Article Data**  
   - Uses Tavily API to retrieve top 3 articles per topic.

3. **Generate Post**  
   - OpenAI Agent transforms insights into a polished post.

4. **Update Google Sheet**  
   - Writes post content and changes status to “Done”.



## 🔑 API Keys Setup

This workflow requires **three APIs** to function properly.  
Follow the quick steps below to connect them inside **n8n** before running the LinkedIn Content Creator workflow.

| Service | Usage | Setup Steps |
|:--|:--|:--|
| 🧠 **OpenAI API Key** | Used by GPT-5 model for AI text generation | 1. Go to your [OpenAI Dashboard](https://platform.openai.com/account/api-keys)  <br>2. Create a new **Secret Key**  <br>3. In n8n → *Credentials* → **OpenAI API** → Paste your key |
| 🌐 **Tavily API Key** | Fetches top 3 web articles related to each LinkedIn topic | 1. Sign up at [Tavily](https://app.tavily.com)  <br>2. Copy your **Bearer Token**  <br>3. In n8n → *HTTP Request node* → under **Headers**, set  <br>`Authorization: Bearer YOUR_KEY` |
| 📊 **Google Sheets OAuth2** | Reads & updates your LinkedIn Topics Sheet | 1. Go to [Google Cloud Console](https://console.cloud.google.com/)  <br>2. Enable **Google Sheets API**  <br>3. Create **OAuth2 credentials**  <br>4. In n8n → *Credentials* → **Google Sheets OAuth2** → Connect your account |

> ⚙️ Once these credentials are connected, the workflow will automatically:
> - Fetch trending topics from Google Sheets  
> - Gather top insights via Tavily  
> - Generate polished LinkedIn posts with OpenAI GPT-5  

---

### ✅ Example Credential Mapping in n8n

| Node | Credential Type | Connected Account |
|:--|:--|:--|
| OpenAI (Generate Post) | OpenAI API | `openai_gpt5_key` |
| Tavily (Fetch Trends) | HTTP Request | `tavily_bearer_token` |
| Google Sheets (Update Topics) | Google Sheets OAuth2 | `linkedin_sheets_auth` |

---

### 💡 Pro Tip
Use **Environment Variables** in n8n for better security:  
```bash
OPENAI_API_KEY=sk-xxxxx
TAVILY_API_KEY=tavily-xxxxx
GOOGLE_CLIENT_ID=xxxxx.apps.googleusercontent.com
GOOGLE_CLIENT_SECRET=xxxxx
```



---

## 🧩 Import the Workflow to n8n

1. Open n8n → *Import Workflow*  
2. Paste the contents of:  
   **`/workflows/linkedin-content-creator.json`**

---


## 🗂 JSON Workflow

The complete JSON (ready to import) file has been attached in repo.


---

---


## 🗂 Google Sheet Preview

Find the link of the attached sheet for your reference.

[LinkedIn Posts](<https://docs.google.com/spreadsheets/d/1zUpfJvuBuuQQrM5A-kl7En4SjXiLGyDTkWCbfSFBThM/edit?usp=sharing>)


---

## 🪄 Tech Stack

- **n8n** (Automation platform)  
- **OpenAI GPT-5** (Content generation)  
- **Google Sheets API** (Data source & output)  
- **Tavily API** (Web search for article content)

---

## 💡 Possible Enhancements

- Add Notion or Airtable as data sources  
- Post directly to LinkedIn via Zapier or Make  
- Generate post carousels or Twitter threads  

---

## 📸 Preview

<img width="1920" height="779" alt="image" src="https://github.com/user-attachments/assets/f49e84af-52db-4118-b843-d5f2dd663b67" />



---

##  Author
**Muskkan Iyer**  
AI Product Analyst | Data Enthusiast | Automation Builder  

- 🌐 [Portfolio](https://github.com/Muskkaniyer)  
- 💼 [LinkedIn](https://www.linkedin.com/in/muskkaniyer/)  
- 📧 [Gmail](mailto:muskkaniyer@gmail.com)  


---

<div align="center">

**⭐ Star this repo if you find it helpful!**

Made with ❤️ by AI enthusiast

</div>



