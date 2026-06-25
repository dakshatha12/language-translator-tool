# 🌐 Lingo — Language Translation Tool

A lightweight, single-file web app that translates text between 38+ languages using a free translation API, featuring:

- Clean, newspaper-style UI built with plain HTML/CSS/JS (no frameworks)
- Source ↔ target language selection with a one-click swap
- Live translation via the MyMemory Translation API (no key needed)
- Copy-to-clipboard button
- Text-to-speech playback of the translated text
- Fully responsive, works on desktop and mobile

**🔗 Live demo:** https://dakshatha12.github.io/language-translator-tool/

---

## 📁 Project Structure

```
language-translator-tool/
│
├── index.html        ← Complete app (HTML + CSS + JS, single file)
│   │
│   ├── <style>       ← Newspaper-inspired design system
│   ├── <body>        ← Language selectors, text panes, toolbar
│   └── <script>      ← API calls, copy button, text-to-speech
│
├── README.md         ← Project documentation (this file)
└── .gitignore         ← Standard ignore rules
```

---

## ⚙️ Setup

### 1 — Clone the project

```bash
git clone https://github.com/dakshatha12/language-translator-tool.git
cd language-translator-tool
```

### 2 — No dependencies to install

This project has **zero build steps and zero packages** — it's pure HTML, CSS, and JavaScript running directly in the browser.

---

## 🚀 Running the Project

### Option A — Open directly (recommended)

Just double-click `index.html`, or open it from your browser:

```
file:///path/to/language-translator-tool/index.html
```

### Option B — Run a local server (optional)

```bash
python -m http.server 5500
```

Then open [http://localhost:5500](http://localhost:5500) in your browser.

### Option C — Use the live GitHub Pages version

No setup at all — just visit:

```
https://dakshatha12.github.io/language-translator-tool/
```

---

## 🧪 Testing the Translation API Manually

You can test the underlying API directly from a terminal:

```bash
# Translate "hello" from English to Spanish
curl "https://api.mymemory.translated.net/get?q=hello&langpair=en|es"

# Translate "good morning" from English to Tamil
curl "https://api.mymemory.translated.net/get?q=good%20morning&langpair=en|ta"
```

---

## 🧠 How It Works

```
User input (text + source/target language)
        │
        ▼
translate() function (script in index.html)
   ├── Reads text from the textarea
   ├── Reads selected language codes from dropdowns
   └── Builds a request URL
        │
        ▼
fetch() call to MyMemory Translation API
   └── GET https://api.mymemory.translated.net/get?q=...&langpair=from|to
        │
        ▼
JSON response parsed
   └── data.responseData.translatedText
        │
        ▼
Result displayed in the output pane
   ├── Copy button → navigator.clipboard.writeText()
   └── Listen button → window.speechSynthesis
```

---

## 🌍 Supported Languages

English, Spanish, French, German, Italian, Portuguese, Dutch, Russian, Chinese (Simplified), Japanese, Korean, Arabic, Hindi, Tamil, Telugu, Kannada, Malayalam, Marathi, Bengali, Gujarati, Punjabi, Urdu, Turkish, Vietnamese, Thai, Indonesian, Polish, Swedish, Greek, Hebrew, Ukrainian, Persian, Romanian, Czech, Finnish, Danish, Norwegian, Hungarian, Swahili.

---

## ⚠️ Limitations

- The free MyMemory API tier allows roughly 5,000 words/day for anonymous use
- Works best with shorter text (under ~500 characters per request)
- Translation quality is good for everyday text but may not match paid services like Google Cloud Translation or Microsoft Translator for nuanced or technical content

---

## 🔮 Possible Improvements

- Swap in Google Cloud Translation API or Microsoft Translator for higher accuracy (requires an API key + small backend to keep the key secure)
- Add translation history
- Add auto-detect for source language
- Add support for translating uploaded documents

---

## 📄 License

This project is open source and free to use for learning and personal projects.
