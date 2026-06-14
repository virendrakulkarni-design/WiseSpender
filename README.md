# WiseSpender 💸

WiseSpender is a privacy-first, client-side Progressive Web Application (PWA) designed to help you track, analyze, and forecast your finances without ever sending your sensitive banking data to a third-party server.

By leveraging powerful, on-device Regex parsing, WiseSpender can automatically extract transaction details directly from your bank's notification SMS messages or Emails. 

![WiseSpender](https://via.placeholder.com/800x400.png?text=WiseSpender+Dashboard) *(Replace with actual screenshot)*

## ✨ Key Features

* **🔒 100% Privacy-First:** No backend, no databases, no tracking. All data processing, parsing, and storage happens locally in your browser's IndexedDB. 
* **📱 Progressive Web App (PWA):** Install it directly to your phone or desktop home screen. Works offline!
* **🤖 Smart Bank Parsing:** Advanced Regex engine intelligently reads transaction alerts (from banks like HDFC, SBI, ICICI, Axis, Kotak, etc.) and extracts the exact amount, merchant, and date while stripping away ugly banking routing codes and disclaimers.
* **📧 Direct Gmail Integration:** Securely link your Gmail account using Google OAuth. Fetch and parse thousands of banking emails in seconds.
* **🔁 Strict Recurring Detection:** Automatically detects subscriptions and recurring bills by matching your Source Account, Target Account, and the Exact Amount. Calculates frequency and predicts your next due dates.
* **🔮 AI-style Forecasting:** Analyzes your variable vs. fixed spending habits to predict your expenses for the next month, allowing you to stay ahead of your budget.
* **📊 Visual Analytics:** View beautiful, interactive charts of your spending trends, top categories, and frequent payees.

## 🚀 Getting Started (Hosting & Installation)

Because WiseSpender is entirely client-side, you can host it anywhere for free. 

### Option 1: GitHub Pages (Recommended)
1. Fork or clone this repository.
2. Go to your GitHub repository **Settings** > **Pages**.
3. Under **Build and deployment**, select **Deploy from a branch** and choose your `main` branch.
4. Your app will be live at `https://<your-username>.github.io/WiseSpender/`.

### Option 2: Run Locally
1. Clone the repository: `git clone https://github.com/virendrakulkarni-design/WiseSpender.git`
2. Open the directory and start a local server:
   ```bash
   npx serve .
   ```
3. Open `http://localhost:3000` in your browser.

## 🔑 Setting up Gmail Import (Google Cloud Console)

To enable the Gmail fetching feature, you must provide your own Google OAuth Client ID.

1. Go to the [Google Cloud Console](https://console.cloud.google.com/).
2. Create a new project and navigate to **APIs & Services** > **Library**.
3. Search for **Gmail API** and click **Enable**.
4. Go to **Credentials** > **Create Credentials** > **OAuth client ID**.
5. Choose **Web application**.
6. Under **Authorized JavaScript origins**, add your public URL (e.g., `https://<your-username>.github.io`). **Note: This is critical. Gmail login will fail with an "Origin Mismatch" if your URL is not listed here.**
7. Copy the generated **Client ID**.
8. Open WiseSpender, go to the **Settings** tab, and paste your Client ID into the API Credentials section.

## 🛠 Tech Stack

* **Frontend:** Vanilla HTML, CSS, JavaScript (No heavy frameworks!)
* **Charting:** [Chart.js](https://www.chartjs.org/) (via CDN)
* **Storage:** LocalStorage / IndexedDB
* **APIs:** Google Identity Services (GSI) & Gmail API

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!
Feel free to check the [issues page](https://github.com/virendrakulkarni-design/WiseSpender/issues).

## 📝 License

This project is open-source and available under the [MIT License](LICENSE).
