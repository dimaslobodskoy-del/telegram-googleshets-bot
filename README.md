# Telegram → Google Sheets Bot

A simple and functional Telegram bot that records purchase or expense data directly into a Google Spreadsheet using **Google Apps Script**.

This project is great for tracking personal expenses, small business purchases, or team spending — all through Telegram messages.

---

## 🚀 Features

- Automatically logs messages into Google Sheets  
- Creates a new sheet for each month (e.g., `2025-10`)  
- Supports custom text commands  
- Validates data format and prevents incorrect entries  
- Built entirely with Google Apps Script — no external hosting required  

---

## 💬 Message Format

Send messages to the bot in this format:

card.food.12.5.lunch
cash.transport.8.bus


Each message must contain:


For example:
> `card.food.12.5.lunch` → adds a row:
| Name | Date | Card or Cash | Type | Sum | Comm |
|------|------|---------------|------|-----|------|
| John Doe | 2025-10-06 | Card | Food | 12.5 | Lunch |

---

## ⚙️ Commands

| Command | Description |
|----------|--------------|
| `del` | Deletes all entries from the current month's sheet (keeps header) |

---

## 🧠 Technologies Used

- **Google Apps Script**
- **Telegram Bot API**
- **Google Sheets API**

---

## 🪄 Setup Instructions

1. Create a new bot using [@BotFather](https://t.me/BotFather) and copy the token.
2. Open [Google Apps Script](https://script.google.com/).
3. Create a new project and paste the code from [`Code.gs`](./Code.gs).
4. Replace the placeholder token:
   ```js
   const TELEGRAM_TOKEN = 'YOUR_TELEGRAM_TOKEN';

