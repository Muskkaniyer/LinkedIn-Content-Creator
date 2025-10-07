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



