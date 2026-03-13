# 💬 Chat with Dad
> AI-powered father roleplay chat — powered by Google Gemini 2.0 Flash

![HTML](https://img.shields.io/badge/HTML-single%20file-00e5a0?style=flat-square&logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-vanilla%20ES6-00b8ff?style=flat-square&logo=javascript&logoColor=white)
![Gemini](https://img.shields.io/badge/Gemini-2.0%20Flash-4285F4?style=flat-square&logo=google&logoColor=white)
![No Install](https://img.shields.io/badge/install-none%20required-00e5a0?style=flat-square)

---

## 🧠 What Is This?

**Chat with Dad** is a single-file HTML app that lets you have a realistic conversation with a virtual version of your father — powered by Google's Gemini AI.

- ✅ Works for **anyone** — just enter your name and your dad's name
- ✅ **No installation**, no server, no npm — just open the HTML file
- ✅ Speaks in **Hinglish** (Hindi + English) and addresses you personally
- ✅ Saves your session in the browser — **no login needed**

---

## 🚀 Quick Start

### 1. Get a Free Gemini API Key
Go to [aistudio.google.com/app/apikey](https://aistudio.google.com/app/apikey), sign in with Google, and click **Create API Key**.

### 2. Open the App
```bash
# Clone the repo
git clone https://github.com/your-username/chat-with-dad.git

# Open in browser — that's it!
open gemini-chat.html
```
Or just **download** `gemini-chat.html` and double-click it.

### 3. Fill the Setup Screen

| Field | Example |
|-------|---------|
| Your Name | Ashwani |
| Your Dad's Name | Bishnu Ji |
| Gemini API Key | `AIza...` |

### 4. Start Chatting 🎉
Type anything and press **Enter** to talk to your dad.

---

## ✨ Features

| Feature | Details |
|---------|---------|
| 🌍 Universal | Anyone can use it — fully dynamic names |
| 🧠 Remembers You | Setup saved in localStorage — skip it next visit |
| 🌑 Dark Modern UI | Neon green/blue accents, animated grid background |
| 💬 Labeled Bubbles | Each message shows your name vs your dad's name |
| ⌛ Typing Animation | Animated dots while waiting for the reply |
| 💾 Persistent Chat | Last 20 messages saved across page refreshes |
| 🔄 Reset Button | Change names anytime from the settings bar |
| ⌫ Clear Chat | Delete all messages with one click |
| ⌨️ Enter to Send | No need to click the button |

---

## 🗂 File Structure

```
chat-with-dad/
├── gemini-chat.html     ← The entire app (HTML + CSS + JS in one file)
└── README.md            ← This file
```

Everything lives in **one file**. No build step, no dependencies, no frameworks.

---

## 🛠 How It Works

When you send a message, the app dynamically builds a character prompt:

```js
const CHARACTER_PROMPT =
  "You are " + dadName + ", a father talking to your child " + userName + ". " +
  "You are warm but firm. You speak in Hinglish. " +
  "Address your child as '" + userName + "' or 'beta' sometimes. " +
  "Ashwani says: [your message]"
```

This is sent to the **Gemini API**, which replies in character. Your names are injected into every prompt so the AI always knows who it's talking to and who it's playing.

---

## 🎨 Customization

### Change the Personality
Find `CHARACTER_PROMPT` in the `<script>` section and edit the description:
```js
// Make him funnier, stricter, speak only Hindi — anything you want
"You are very strict and only speak in Hindi..."
```

### Change the Colors
Edit the CSS variables at the top of `<style>`:
```css
:root {
  --accent:  #00e5a0;   /* neon green  */
  --accent2: #00b8ff;   /* blue        */
  --bg:      #080b10;   /* background  */
}
```

### Change the AI Model
Find the fetch URL and swap the model name:
```js
// Default (fast + free)
models/gemini-2.0-flash:generateContent

// Higher quality
models/gemini-1.5-pro:generateContent
```

---

## 🔧 Troubleshooting

| Problem | Fix |
|---------|-----|
| API key error / 400 | Check the key is copied fully. Regenerate at aistudio.google.com |
| No reply received | Check your internet connection |
| Chat history gone | Browser localStorage was cleared |
| App looks broken | Use a modern browser (Chrome recommended) |
| Setup keeps showing | Fill all three fields before clicking Start |

---

## 🔐 Privacy

- Your API key is stored **only in your browser's localStorage**
- Messages go **directly from your browser → Google's Gemini API**
- **No third-party server** receives your data
- Revoke your key anytime at [aistudio.google.com](https://aistudio.google.com)

> ⚠️ Never share your API key publicly or commit it to this repo.

---

## 🧱 Tech Stack

| Technology | Purpose |
|-----------|---------|
| HTML5 | App structure |
| CSS3 (custom properties + animations) | Dark theme, glowing effects |
| Vanilla JavaScript (ES6+) | All logic — API calls, rendering, state |
| Google Gemini 2.0 Flash | AI brain behind the dad's replies |
| Browser localStorage | Saving chat + user settings |
| Google Fonts (Syne + DM Mono) | Typography |

---

## 📄 License

MIT — free to use, modify, and share.

---

<p align="center">Made with ❤️ for everyone who wants to talk to their dad.</p>
