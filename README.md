# 📰 AI News Automation Workflow

This repository contains the complete workflow for an automated AI system that:
- Fetches top news from Google News (Tech)
- Parses RSS XML
- Extracts top articles
- Generates video scripts using Gemini & OpenAI
- Creates a JSON2Video render job
- Waits for rendering completion
- Uploads the final video to YouTube
- Sends updates through Telegram

The entire process is automated end-to-end using n8n.

---

## 📌 Overview

The workflow takes a single trigger (Telegram or manual run), retrieves the latest tech news, processes the top story, generates all required assets (script, prompts), creates the video using JSON2Video API, uploads the result, and finally sends you a Telegram message with the video link.

---

## 🧩 Workflow Diagram

The workflow structure is shown in the image below:

![Workflow Diagram](assets/workflow.png)

---

## 🛠️ Tech Stack

- **n8n** (Or any automation orchestration tool)
- **Google News RSS**
- **Gemini (Build Topic + Content Params)**
- **OpenAI** (Script, prompts, voiceover text)
- **JSON2Video API**
- **Telegram Bot API**
- **YouTube Upload API**

---

## 🚀 End-to-End Flow

1. **Trigger Workflow**
   - Telegram or manual start

2. **Fetch Top Tech News**
   - Google News endpoint

3. **Parse RSS XML**
   - Extract items and metadata

4. **Select Top Article**
   - Custom JS filtering logic

5. **Generate Video Topic**
   - Gemini "Build Topic" node

6. **Generate Script & Prompts**
   - OpenAI message model

7. **Create Video Render Task**
   - JSON2Video

8. **Check Rendering Status**
   - Poll until done

9. **Upload Video to YouTube**

10. **Send Confirmation to Telegram**

---

## 📬 Contact

For questions or improvements, feel free to open an issue or reach out.

---

### ⭐ If you like this project, consider giving the repo a star!
