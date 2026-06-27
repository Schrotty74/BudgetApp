<img src="icon.png" alt="BudgetApp Icon" width="160">

# 💶 BudgetApp

![License](https://img.shields.io/badge/license-GPL--3.0-green)
![PWA](https://img.shields.io/badge/PWA-ready-blue)
![HTML5](https://img.shields.io/badge/HTML5-pure-orange)
![JavaScript](https://img.shields.io/badge/JavaScript-vanilla-yellow)
![Maintained](https://img.shields.io/badge/maintained-yes-brightgreen)
![Mobile](https://img.shields.io/badge/mobile-friendly-blueviolet)
![No Server](https://img.shields.io/badge/no%20server-offline%20only-lightgrey)
![localStorage](https://img.shields.io/badge/storage-localStorage%20only-informational)
![No Tracking](https://img.shields.io/badge/tracking-none-success)
![No Login](https://img.shields.io/badge/login-not%20required-success)

[![Live Demo](https://img.shields.io/badge/🚀%20Live%20Demo-open-brightgreen)](https://schrotty74.github.io/BudgetApp)

## 📱 Screenshots

<table>
  <tr>
    <td><img src="screenshots/demo-top.png" width="300" alt="Overview & Chart"></td>
    <td><img src="screenshots/demo-bottom.png" width="300" alt="Income & Expenses"></td>
  </tr>
  <tr>
    <td colspan="2" align="center"><sub>📋 Screenshots with sample data</sub></td>
  </tr>
</table>

**Track your monthly income & expenses at a glance**

A Progressive Web App (PWA) for simple household budget management — runs directly in the browser, no installation needed, works offline.

🇩🇪 [Deutsche Version](README_de.md)

---

## ✨ Features

- 📊 **Dashboard** — Monthly balance, income & expenses at a glance
- 🍩 **Donut chart** — Visual breakdown of expense categories
- 📥 **Excel import** — Read `.xlsx` files directly (income & expenses are detected automatically, whitespace is normalised)
- 📤 **Excel export** — Export your budget as a `.xlsx` file
- 🖨️ **PDF export** — Print-ready export of your monthly overview
- ✏️ **Full editing** — Add, edit and delete entries inline
- 👆 **Swipe to delete** — Remove entries with a swipe gesture on mobile
- 🌗 **Dark / Light mode** — Toggle between dark and light theme (☀️ / 🌙)
- 🌐 **Language switch** — Switch between German and English at any time
- 💾 **Local storage** — All data stays exclusively on your device
- 📴 **Offline-ready** — Service Worker caches the app for use without internet
- 📱 **Installable** — Add to iPhone/iPad Home Screen or install as a desktop app

---

## 🔒 Privacy

**No data ever leaves your device.** The source code contains zero personal financial data. All entries are stored exclusively in the browser's local storage (localStorage) and are only visible on your device.

---

## 📱 Install as an App

**iPhone / iPad (Safari):**
1. Open `schrotty74.github.io/BudgetApp` in Safari
2. Tap the Share icon
3. Select „Add to Home Screen"
4. Tap „Add"

**Mac / Windows (Chrome or Edge):**
1. Open the page
2. Click the install icon in the address bar
3. Confirm „Install"

---

## 📥 Excel Import

The app automatically recognises `.xlsx` files as long as they contain sections labelled **Einnahmen** (Income) and **Ausgaben** (Expenses). Whitespace variations in section headers are handled automatically.

Supported frequencies: `Monatlich` · `Alle 2 Monate` · `Quartalsweise` · `Jährlich` · `Variabel`

---

## 🛠 Technology

- Pure HTML / CSS / JavaScript — no frameworks, no build step
- [SheetJS](https://sheetjs.com) for Excel import & export
- Service Worker for offline support
- localStorage for local data persistence

---

## 📄 License

GPL-3.0 — see [LICENSE](LICENSE)
