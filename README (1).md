# Lingo — Language Translation Tool

A lightweight, single-file web app that translates text between 38+ languages using a free translation API. No backend, no build step, no API key — just open the file in a browser.

**Live demo:** https://dakshatha12.github.io/language-translator-tool/

## Features

- Enter any text and instantly translate it between languages
- Select source and target language from dropdown menus
- One-click **swap** button to flip source ↔ target
- **Copy** button to copy the translated text to your clipboard
- **Listen** button for text-to-speech playback of the translation
- Character counter (500 character limit per request)
- Responsive layout — works on desktop and mobile
- Keyboard shortcut: `Ctrl/Cmd + Enter` to translate

## How it works

This project uses the [MyMemory Translation API](https://mymemory.translated.net/) — a free, keyless translation service — called directly from the browser via `fetch()`. The UI is plain HTML, CSS, and JavaScript, with no frameworks or dependencies.

## Supported languages

English, Spanish, French, German, Italian, Portuguese, Dutch, Russian, Chinese (Simplified), Japanese, Korean, Arabic, Hindi, Tamil, Telugu, Kannada, Malayalam, Marathi, Bengali, Gujarati, Punjabi, Urdu, Turkish, Vietnamese, Thai, Indonesian, Polish, Swedish, Greek, Hebrew, Ukrainian, Persian, Romanian, Czech, Finnish, Danish, Norwegian, Hungarian, Swahili.

## Getting started

### Run locally
1. Clone this repository
   ```bash
   git clone https://github.com/dakshatha12/language-translator-tool.git
   ```
2. Open `index.html` in any web browser — no installation required.

### Run on GitHub Pages
This repo is already configured for GitHub Pages. Any push to the `main` branch automatically updates the live site at the link above.

## Project structure

```
language-translator-tool/
├── index.html      # Complete app: HTML, CSS, and JavaScript in one file
└── README.md       # Project documentation
```

## Limitations

- The free MyMemory API tier allows roughly 5,000 words/day for anonymous use, and works best with shorter text.
- Translation quality is good for everyday text but not guaranteed to match paid services like Google Translate or Microsoft Translator for nuanced or technical content.

## Possible improvements

- Swap in Google Cloud Translation API or Microsoft Translator for higher accuracy and volume (requires an API key and a small backend to keep the key secure)
- Add translation history
- Add auto-detect for source language
- Add support for file/document translation

## License

This project is open source and free to use for learning and personal projects.
