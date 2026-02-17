# AI Lead Generation Automation (n8n)

This project is a fully AI-driven lead generation and outreach workflow built using **n8n**.

## 🔍 What it does
- Accepts a business query (e.g. "salons in Noida sector 62")
- Fetches businesses from Google Maps (via SerpAPI)
- Extracts ratings, reviews count, address, website
- Uses AI to analyze business reputation
- Automatically sends a personalized outreach email
- Stores leads in Google Sheets

## 🧠 AI Capabilities
- Business analysis using LLMs
- Context-aware email generation
- Automated decision-making (IF logic)

## 🛠 Tech Stack
- n8n (workflow automation)
- SerpAPI (Google Maps data)
- LLM API (OpenRouter / Gemini)
- Google Sheets
- SMTP (email)

## 📂 Files
- `ai-lead-generation.json` → n8n workflow export

## 🚀 How to use
1. Import the JSON file into n8n
2. Add your API keys (SerpAPI, AI, SMTP)
3. Trigger the workflow via webhook

## 📌 Notes
- This is an append-only workflow (no row updates)
- Designed for scalability and production use

## 👤 Author
Arpita Mishra
