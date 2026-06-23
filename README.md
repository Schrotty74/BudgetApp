# 💶 BudgetApo

**Track your monthly income & expenses at a glance**

A Progressive Web App (PWA) for simple household budget management — runs directly in the browser, no installation needed, works offline.

🇩🇪 [Deutsche Version](README.de.md)

---

## ✨ Features

- 📊 **Dashboard** — Monthly balance, income & expenses at a glance
- 🍩 **Donut chart** — Visual breakdown of expense categories
- 📥 **Excel import** — Read `.xlsx` files directly (income & expenses are detected automatically)
- ✏️ **Full editing** — Add, edit and delete entries inline
- 💾 **Local storage** — All data stays exclusively on your device
- 📴 **Offline-ready** — Service Worker caches the app for use without internet
- 📱 **Installable** — Add to iPhone/iPad Home Screen or install as a desktop app

---

## 🔒 Privacy

**No data ever leaves your device.** The source code contains zero personal financial data. All entries are stored exclusively in the browser's local storage (localStorage) and are only visible on your device.

---

## 📱 Install as an App

**iPhone / iPad (Safari):**
1. Open `schrotty74.github.io/BudgetApo` in Safari
2. Tap the Share icon
3. Select „Add to Home Screen"
4. Tap „Add"

**Mac / Windows (Chrome or Edge):**
1. Open the page
2. Click the install icon in the address bar
3. Confirm „Install"

---

## 📥 Excel Import

The app automatically recognises `.xlsx` files as long as they contain sections labelled **Einnahmen** (Income) and **Ausgaben** (Expenses). Example format:

| Column A | Column B | Column C |
|----------|----------|----------|
| 💵 Einnahmen | Betrag (€) | Häufigkeit |
| 🏦 Gehalt | 2000 | Monatlich |
| **📋 Ausgaben** | | |
| 🏠 Miete | 800 | Monatlich |

Supported frequencies: `Monatlich` · `Alle 2 Monate` · `Quartalsweise` · `Jährlich` · `Variabel`

---

## 🛠 Technology

- Pure HTML / CSS / JavaScript — no frameworks, no build step
- [SheetJS](https://sheetjs.com) for Excel import
- Service Worker for offline support
- localStorage for local data persistence

---

## 📄 License

GPL-3.0 — see [LICENSE](LICENSE)
