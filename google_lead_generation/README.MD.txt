# Google Maps Lead Generation – n8n Automation

This project is an end-to-end **Google Maps Lead Generation system** built using **n8n** and **SerpAPI**.

## 🔹 Features
- Search businesses from Google Maps
- Extract:
  - Company name
  - Phone number
  - Address
  - Website
  - Company rating
- Fetch **individual Google reviews**
  - Reviewer name
  - Review rating
  - Review comment
- Merge company + review data
- Store clean data in **Google Sheets**

## 🔹 Tech Stack
- n8n
- SerpAPI (Google Maps Search & Reviews)
- JavaScript (n8n Code nodes)
- Google Sheets

## 🔹 Workflow Overview
1. Google Maps Search (SerpAPI)
2. JavaScript parsing (company + phone)
3. Split in batches (per company)
4. Google Maps Reviews (SerpAPI)
5. Split reviews
6. Merge company & review data
7. Store in Google Sheets

## 🔹 How to Use
1. Import the JSON workflow into n8n
2. Add your own:
   - SerpAPI API key
   - Google Sheets credentials
3. Run the workflow

## 🔹 Use Cases
- Lead generation
- Sales outreach
- Business intelligence
- AI automation demos

## 🔹 Notes
- API keys are NOT included
- This project is for educational and demo purposes

---

⭐ If you find this useful, give it a star!
