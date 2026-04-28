# 📍 Lead Generation System—V1 google map scrap

Automated pipeline that scrapes business leads from Google Maps,
analyzes them with AI, and stores results in Airtable — built with n8n.

---

## ⚙️ How It Works

1. **Apify** scrapes businesses from Google Maps automatically
2. System checks **Google Sheets** to avoid duplicate leads
3. New leads get saved to **Airtable** with full business data
4. **AI Agent (Gemini)** analyzes each lead and returns:
   - Lead score (0–10)
   - Main problem & opportunity
   - Suggested outreach message
   - Opportunity type (web_dev / seo / ads / automation)
5. Airtable record gets updated with the AI analysis
6. **Gmail** sends alert if a duplicate lead is detected

---

## 🧠 Tech Stack

- **n8n** — Workflow automation
- **Apify** — Google Maps scraper (`nwua9Gu5YrADL7ZDj`)
- **Google Gemini** — AI lead analysis
- **Airtable** — Lead database
- **Google Sheets** — Duplicate prevention
- **Gmail** — Duplicate alerts

---

## 📊 AI Analysis Output (per lead)

```json
{
  "name": "business name",
  "score": 8,
  "category": "high value lead",
  "main_problem": "no website found",
  "opportunity": "build landing page with booking system",
  "opportunity_type": "web_dev",
  "outreach_message": "..."
}
```

---

## 🚀 Features

- ✅ Auto duplicate detection
- ✅ AI scoring & opportunity analysis
- ✅ Arabic output for Arab market targeting
- ✅ Gmail alerts for duplicates
- ✅ Scalable batch processing

---

## 📁 Files

| File | Description |
|------|-------------|
| `lead-generation-v1.json` | n8n workflow — import directly |

---

## 📥 How to Use

1. Import `lead-generation-v1.json` into your n8n instance
2. Connect your credentials:
   - Apify OAuth2
   - Google Sheets OAuth2
   - Airtable Token
   - Gmail OAuth2
   - Google Gemini API
3. Run Apify actor manually or on schedule
4. Check Airtable for results

---

> Built by [Ahmed Reda](https://github.com/ae382101-dot)
