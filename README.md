# 🧠 AI Life Tracker (Local & Private)

A privacy-focused dashboard to track your habits, fitness, diet, and mood.
**100% Local.** No data leaves your device. Powered by [Ollama](https://ollama.com/) for a personal AI Coach that runs entirely on your computer.

## ✨ Features

* **🤖 Personal AI Coach:** Get daily "Report Cards" and answers to health questions using Llama 3 (running locally).
* **📊 Visual Trends:** Interactive charts for Weight, Activity, Hydration, and Diet Quality.
* **😊 Mood Tracker:** Log how you feel and visualize mood trends on a calendar.
* **🔒 Privacy First:** All data is stored in your browser's `LocalStorage`. No database, no cloud, no tracking.
* **☀️ Aesthetic UI:** A clean, bright interface designed to make tracking feel good.

---

## 🛠️ Prerequisites: Setting up AI (Ollama)

To use the AI Coaching features, you must have **Ollama** installed and running on your computer.

### Step 1: Install Ollama
Download and install Ollama from the official website: [ollama.com](https://ollama.com).

### Step 2: Download a Model
Open your terminal (Command Prompt on Windows, Terminal on Mac) and run this command to download the AI model:

    ollama pull llama3

*(Note: You can also use `mistral`, `gemma`, or others. Just make sure to type the matching name in the tracker's settings box).*

### Step 3: ⚠️ Enable Browser Access (Critical)
By default, web browsers block websites from talking to local programs for security. You must explicitly allow the tracker to talk to Ollama.

**Choose one of the methods below:**

#### Option A: The Permanent Fix (Recommended for Windows)
1.  Press the **Windows Key** and type "env".
2.  Select **"Edit environment variables for your account"**.
3.  Click **"New..."** under the top section (User variables).
4.  **Variable name:** `OLLAMA_ORIGINS`
5.  **Variable value:** `*`
6.  Click **OK** on all windows.
7.  **Restart Ollama** (Quit it from the taskbar icons and open it again).

#### Option B: The Temporary Command (Run every time)
If you don't want to change settings, you must run this command *every time* you want to use the AI features:

**For Windows (Command Prompt):**

    set OLLAMA_ORIGINS=* && ollama serve

**For Mac / Linux:**

    OLLAMA_ORIGINS="*" ollama serve

---

## 🚀 How to Install & Run

1.  **Download the Code:**
    * Click the green **Code** button above -> **Download ZIP**.
    * Extract the folder.
    * *(Or use `git clone https://github.com/yourusername/life-tracker.git`)*.

2.  **Run the App:**
    * Simply double-click the `index.html` file.
    * It will open in your default browser.

3.  **Start Tracking:**
    * Enter your height (first time only).
    * Log your day.
    * Click **"💾 Update My Day"** to see the AI generate your feedback!

---

## ⚙️ Data Management

* **Export:** Click "Export JSON" to save a backup file of your history.
* **Reset:** Use "Factory Reset" to wipe all local data and start fresh.
* **Recover:** If you clear your browser cache, your data will be lost unless you have an Export file!

---

## ❓ Troubleshooting

**Q: The AI says "Connection Failed" or "Error".**
* **A:** Is Ollama running? Check your taskbar icons.
* **A:** Did you set `OLLAMA_ORIGINS="*"`? See **Step 3** in prerequisites.
* **A:** Is the model downloaded? Run `ollama list` in terminal to check if `llama3` is listed.

**Q: Can I host this on GitHub Pages?**
* **A:** You can host the file, but **the AI features will NOT work online**. Browsers block secure websites (HTTPS) from talking to local insecure servers (HTTP). For full AI functionality, run the file locally on your computer.

---

## 🤝 Contributing
Feel free to fork this project! Ideas for improvements:
* Add a Dark Mode toggle.
* Add voice input for logging meals.
* Create more chart types.

---
*Created with ❤️ & AI*
