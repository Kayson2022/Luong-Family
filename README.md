# FinSuite — Personal Investment Tools

A personal finance website hosting two custom-built investment tracking apps.

🌐 **Live site:** `https://YOUR-USERNAME.github.io/finsuite`

---

## Apps

### 📊 Stocks & Funds Tracker
Real-time stocks, ETFs, and mutual funds tracker with 16+ analysis tools.
- Live prices via Finnhub, Alpha Vantage, FMP
- FIFO tax lots, Schedule D export
- Benchmark comparison (SPY/QQQ/DIA)
- Smart alert suggestions, fundamentals panel
- Trade journal, dividend calendar, performance stats
- 20+ currency support

**→ `/stocks/index.html`**

### 💼 401k Investment App
Full retirement portfolio manager across all account types.
- Tracks 401(k), Roth IRA, Brokerage, 529, Yahoo Finance
- Withdrawal Planner with RMDs and sequence-of-returns risk
- Roth Conversion Analyzer with break-even age
- Cost Basis Optimizer (FIFO/LIFO/Highest/Lowest Cost)
- Year-End Tax Planning checklist
- Paycheck Calculator with Roth vs Traditional routing
- IRS 2026 contribution limits (age-based catch-up)

**→ `/portfolio/index.html`**

---

## Setup

### Deploy to GitHub Pages

1. Create a new GitHub repository named `finsuite` (or any name)
2. Upload all files maintaining this structure:
   ```
   index.html
   stocks/
     index.html
   portfolio/
     index.html
   README.md
   ```
3. Go to **Settings → Pages → Source → Deploy from branch → main → / (root)**
4. Your site will be live at `https://YOUR-USERNAME.github.io/finsuite`

### Configuration

Both apps require Firebase project credentials. Edit the `firebaseConfig` object in each app's HTML:

```js
const firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  authDomain: "YOUR_PROJECT.firebaseapp.com",
  projectId: "YOUR_PROJECT_ID",
  // ...
};
```

API keys (Finnhub, Alpha Vantage, FMP) are entered in-app via ⚙️ Settings and stored securely in Firestore per user.

---

## Tech Stack
- **Firebase Auth** — Google Sign-In
- **Cloud Firestore** — all data, settings, API keys synced cross-device
- **Finnhub API** — real-time quotes, fundamentals, news
- **Yahoo Finance** — historical prices, benchmark data
- **Chart.js** — all charts and visualizations
- **GitHub Pages** — free static hosting

---

*Personal use only. Not financial advice. Data sourced from public APIs.*
