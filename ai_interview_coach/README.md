# 🎯 AI Interview Coach

An AI-powered interview preparation web app built with Flask + Claude API.

---

## 📁 Project Structure

```
ai_interview_coach/
├── app.py                  ← Main Flask backend
├── requirements.txt        ← Python dependencies
├── templates/
│   └── index.html          ← Full frontend UI
└── uploads/                ← Temp folder for CV uploads (auto-created)
```

---

## ⚙️ Setup Instructions

### 1. Clone / Download the project
```bash
cd ai_interview_coach
```

### 2. Create a virtual environment
```bash
python -m venv venv

# Windows
venv\Scripts\activate

# Mac/Linux
source venv/bin/activate
```

### 3. Install dependencies
```bash
pip install -r requirements.txt
```

### 4. Set your Anthropic API Key
```bash
# Windows
set ANTHROPIC_API_KEY=your_api_key_here

# Mac/Linux
export ANTHROPIC_API_KEY=your_api_key_here
```

> Get your API key from: https://console.anthropic.com

### 5. Run the app
```bash
python app.py
```

### 6. Open in browser
```
http://localhost:5000
```

---

## 🚀 Features

| Feature | Description |
|---|---|
| CV Upload | Upload PDF resume, AI extracts your skills & experience |
| Job Role Selection | Choose from 12 different job roles |
| Personalized Questions | 5 questions tailored to YOUR CV + role |
| Live AI Evaluation | Score (1-10) + Strengths + Improvements per answer |
| Final Report | Overall score, hire recommendation, next steps |

---

## 🔧 Tech Stack

| Layer | Technology |
|---|---|
| Backend | Python + Flask |
| AI | Anthropic Claude (claude-sonnet-4) |
| PDF Parsing | pdfplumber |
| Frontend | HTML + CSS + Vanilla JS |
| Session | Flask sessions |

---

## 📝 API Routes

| Route | Method | Description |
|---|---|---|
| `/` | GET | Main page |
| `/upload` | POST | Upload CV + generate questions |
| `/evaluate` | POST | Evaluate single answer |
| `/report` | POST | Generate final report |

---

## 💡 How It Works

1. User uploads CV (PDF) + selects job role
2. Flask extracts text using `pdfplumber`
3. Claude generates 5 personalized interview questions
4. User answers each question
5. Claude evaluates each answer with score + feedback
6. Final report generated with hire recommendation

---

## 🌟 Possible Enhancements

- [ ] Voice input (Web Speech API)
- [ ] Save session history to database (SQLite)
- [ ] Urdu language support
- [ ] Export report as PDF
- [ ] Timer per question
- [ ] Multiple difficulty levels
