# 📘 Textbook of Tomorrow

### *Turn static textbooks & LMS content into interactive learning — instantly.*

<p align="center">
  <img src="extension/icons/icon128.png" alt="Textbook of Tomorrow Logo" width="120">
  <br>
  <i>AI-powered learning, right where students read.</i>
</p>

<p align="center">
  <img src="https://img.shields.io/github/repo-size/KING-OF-FLAME/textbook-of-tomorrow?style=flat-square&color=orange" alt="Repo Size">
  <img src="https://img.shields.io/github/stars/KING-OF-FLAME/textbook-of-tomorrow?style=flat-square" alt="Stars">
  <img src="https://img.shields.io/badge/License-MIT-green.svg?style=flat-square" alt="License">
  <img src="https://badges.frapsoft.com/os/v2/open-source.svg?v=103" alt="Open Source">
</p>

---

## 🌟 About the Project

**Textbook of Tomorrow** is a lightweight AI-powered Chrome extension that transforms **static digital textbooks and LMS readings** into **interactive learning experiences**.

Instead of copying content into ChatGPT or external tools, students can simply:

> **Highlight text → Click an action → Learn instantly**

This project is intentionally built as a **simple, beginner-friendly MVP**, inspired by modern AI-education research — without research-level complexity.

---

## 🎯 What Problem It Solves

* Static PDFs and LMS readings are **passive**
* Students often struggle to:

  * Understand dense explanations
  * Quickly revise content
  * Test their understanding

**Textbook of Tomorrow fixes this directly inside the reading experience.**

---

## ✨ Features (MVP)

✅ **Explain Selected Text**
Student-friendly explanation in simple language

✅ **Summarize Selected Text**
Clear bullet-point summary (**max 5 bullets**)

✅ **Generate 3 Quiz Questions**
Multiple-choice questions (**3 MCQs**) with answers

🚫 No chat history
🚫 No analytics
🚫 No personalization

> **One highlight → one AI response**

---

## 🧠 How It Works (High Level)

```
User highlights text
        ↓
Chrome Extension captures selection
        ↓
FastAPI backend sends text to AI model
        ↓
AI returns clean text output
        ↓
Side panel displays result instantly
```

---

## 🎥 Demo
<table align="center" width="50%">
  <!-- TOP ROW: BIG GIF -->
  <tr>
    <td align="center" colspan="2">
      <img src="1.gif" alt="Main Demo" width="100%">
      <br>
      <i>Main Flow Demo</i>
    </td>
  </tr>

  <!-- SECOND ROW: TWO GIFS SIDE BY SIDE -->
  <tr>
    <td align="center" width="50%">
      <img src="2.gif" alt="Feature One" width="100%">
      <br>
      <i>Feature One</i>
    </td>
    <td align="center" width="50%">
      <img src="3.gif" alt="Feature Two" width="100%">
      <br>
      <i>Feature Two</i>
    </td>
  </tr>
</table>

---

## 🗂 Project Structure

```
textbook-of-tomorrow/
│
├── backend/                         # FastAPI backend
│   ├── app.py                      # Main backend application
│   ├── test.py                     # API test script
│   ├── requirements.txt            # Python dependencies
│   ├── .env.example                # Environment variable template
│
├── extension/                      # Chrome Extension (Frontend)
│   ├── manifest.json               # Extension configuration (MV3)
│   ├── content.js                  # Captures highlighted text
│   ├── service_worker.js           # Background logic
│   ├── sidepanel.html              # Side panel UI
│   ├── sidepanel.css               # Premium UI styling
│   ├── sidepanel.js                # UI logic + API calls
│   └── icons/                      # Extension icons
│       ├── icon16.png
│       ├── icon48.png
│       └── icon128.png
│
├── .gitignore                      # Git ignored files
└── README.md                       # Project documentation
```

---

## 🚀 Getting Started

### 🔧 Prerequisites

* Python 3.9+
* Google Chrome
* OpenAI API key
* XAMPP (for local backend hosting)

---

## ⚙️ Backend Setup (FastAPI)

### 1️⃣ Navigate to backend

```bash
cd backend
```

### 2️⃣ Install dependencies

```bash
pip install -r requirements.txt
```

### 3️⃣ Create `.env`

Create a file at `backend/.env`:

```env
OPENAI_API_KEY=your_api_key_here
OPENAI_MODEL=gpt-4.1-mini
```

> ⚠️ Never commit `.env`. It is ignored via `.gitignore`.

### 4️⃣ Run backend

```bash
uvicorn app:app --reload --port 8000
```

### 5️⃣ Verify

Open in browser:

```
http://127.0.0.1:8000/health
```

Expected:

```json
{"ok": true, "model": "gpt-4.1-mini"}
```

---

## 🧩 Chrome Extension Setup

### 1️⃣ Open Chrome Extensions

```
chrome://extensions
```

### 2️⃣ Enable **Developer Mode**

### 3️⃣ Click **Load unpacked**

Select this folder:

```
textbook-of-tomorrow/extension
```

### 4️⃣ Pin the extension (recommended)

---

## 🖱 How to Use

1. Open any **normal webpage** (or your LMS)
2. Highlight a sentence/paragraph
3. Click the extension icon to open the side panel
4. Choose an action:

   * ✨ Explain
   * 🧾 Summarize
   * 🧠 Quiz (3 MCQs)

AI output appears instantly in the side panel.

---

## 🔒 Security & Privacy

* 🔐 API keys stay in `backend/.env` (never pushed)
* 🚫 No user tracking
* 🚫 No analytics
* 🚫 No saved chat history
* ✅ One request → one response

---

## 🧠 Model Choice

Default model:

```text
gpt-4.1-mini
```

Chosen because it offers:

* Strong quality for explanations + quizzes
* Cost-efficient output tokens for MVP usage
* Fast responses

---

## 🤝 Contributing

Contributions are welcome!

1. Fork the repo
2. Create a branch (`git checkout -b feature/your-feature`)
3. Commit changes (`git commit -m "Add your feature"`)
4. Push (`git push origin feature/your-feature`)
5. Open a Pull Request

---

## 📜 License

This project is licensed under the **MIT License**.

---

## 👨‍💻 Author

**Yash Raj**
GitHub: [KING-OF-FLAME](https://github.com/KING-OF-FLAME)

---

## 🙏 Acknowledgments

* Inspired by AI + Education research
* Built using **FastAPI** and **Chrome Extension Manifest V3**
* Thanks to the open-source community ❤️

---

### ⭐ If you like this project, consider starring the repo!
