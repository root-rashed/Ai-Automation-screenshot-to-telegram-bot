# 📸 Screenshot to Telegram Automation

Automatically capture a website screenshot and send it directly to a Telegram chat using HTTP integration and automation workflow.

## 🚀 Overview

This project uses an HTTP request to generate a website screenshot and instantly sends the image to a Telegram chat using a bot.

Target example:
- CoinMarketCap (Applicable for Any website)

---

## ⚙️ How It Works

### Step 1: Make HTTP Request

- Endpoint:
  https://shot.screenshotapi.net/screenshot
- Method: GET
- Authentication: API Key (via query parameter)

### Query Parameters Used

| Parameter | Value |
|-----------|--------|
| token | Your API Key |
| url | Any website Link |
| width | 500 |
| height | 800 |
| output | image |
| file_type | png |

The API returns the screenshot as binary image data.

---

### Step 2: Send Photo to Telegram

- Module: telegram:SendPhoto
- Send Type: send_bydata
- Data Source: Image from HTTP request
- Chat ID: Your Telegram Chat ID
- Caption: update
- Filename: image.png

The image is sent instantly to your Telegram chat.

---

## 🛠 Tech Stack

- HTTP REST API
- ScreenshotAPI
- Telegram Bot API
- Make (Integromat) Automation

---

## 🔑 Setup Instructions

### 1️⃣ Get Screenshot API Key

Register at:
https://screenshotapi.net/

Replace:
"token": "Your API KEY"

With your real API key.

---

### 2️⃣ Create Telegram Bot

1. Open Telegram
2. Search for @BotFather
3. Create a new bot
4. Copy the bot token
5. Get your Chat ID
6. Connect bot inside Make platform

---

### 3️⃣ Import Scenario

1. Import the JSON scenario file into Make
2. Add:
   - Screenshot API key
   - Telegram bot connection
   - Your chat ID
3. Run the scenario

---

## 📸 Use Cases

- Crypto market monitoring
- Website change monitoring
- Automated daily reports
- Web3 dashboard updates
- Price tracking alerts

---

## 🔒 Security Note

- Do NOT upload API keys to public repositories
- Store credentials securely
- Regenerate Telegram tokens if exposed

---

## 👨‍💻 Author

Rashedul Islam  
Automation & Integration Developer
