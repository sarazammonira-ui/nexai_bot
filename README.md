# NEXAI Telegram Bot — Render.com Deploy Guide

## ফাইল তালিকা
```
nexai-bot/
├── tg-bot.py          ← মূল bot ফাইল
├── requirements.txt   ← Python dependencies
├── render.yaml        ← Render config
└── README.md          ← এই ফাইল
```

---

## Step-by-Step Deploy

### ধাপ ১ — GitHub Repository বানান
1. https://github.com এ যান
2. **New repository** তৈরি করুন (নাম: `nexai-bot`)
3. এই ৩টি ফাইল upload করুন:
   - `tg-bot.py`
   - `requirements.txt`
   - `render.yaml`

### ধাপ ২ — Render.com এ Deploy করুন
1. https://render.com এ যান
2. GitHub দিয়ে Sign Up / Login করুন
3. Dashboard থেকে **"New +"** → **"Background Worker"** বেছে নিন
4. আপনার `nexai-bot` repository connect করুন
5. Settings:
   - **Name:** nexai-telegram-bot
   - **Runtime:** Python 3
   - **Build Command:** `pip install -r requirements.txt`
   - **Start Command:** `python tg-bot.py`
   - **Plan:** Free
6. **"Create Background Worker"** বাটনে ক্লিক করুন

### ধাপ ৩ — Deploy হওয়া দেখুন
- Render logs এ দেখবেন: `✅ NEXAI Bot সফলভাবে চালু হয়েছে!`
- এখন bot ২৪/৭ চলবে!

---

## ⚠️ Render Free Plan সম্পর্কে
- Free plan এ **750 hours/month** পাবেন
- Bot কখনো sleep করবে না (Background Worker)
- একটু slow হতে পারে প্রথমবার start এ

---

## 🔄 Bot Update করতে
GitHub এ নতুন ফাইল push করলে Render automatically redeploy করবে।
