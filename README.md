# GA4 Analytics Dashboard

<p align="center">
  <img src="https://img.shields.io/badge/Google%20Analytics-4-orange?style=for-the-badge&logo=google-analytics" alt="GA4">
  <img src="https://img.shields.io/badge/License-MIT-green?style=for-the-badge" alt="MIT License">
  <img src="https://img.shields.io/badge/No%20Backend-Required-blue?style=for-the-badge" alt="No Backend">
  <img src="https://img.shields.io/badge/Single%20File-HTML-red?style=for-the-badge" alt="Single File">
</p>

<p align="center">
  A powerful, self-hosted Google Analytics 4 dashboard in a single HTML file. No backend required. Your data stays between you and Google.
</p>

<p align="center">
  <a href="#-features">Features</a> •
  <a href="#-demo">Demo</a> •
  <a href="#-quick-start">Quick Start</a> •
  <a href="#-google-cloud-setup">Google Cloud Setup</a> •
  <a href="#-screenshots">Screenshots</a>
</p>

---

## ✨ Features

### 📊 Comprehensive Analytics
- **Overview** — Sessions, users, page views, bounce rate with trend charts
- **Acquisition** — Channel breakdown, traffic sources, campaign performance
- **Audience** — Demographics (age, gender), devices, geography, interests
- **Engagement** — Top pages, events, activity heatmap by day/hour
- **User Flow** — Sankey diagram visualizing navigation paths
- **E-commerce** — Revenue, transactions, AOV, top products
- **Conversions** — Funnel visualization, conversion events, rates

### 🎯 Key Features
| Feature | Description |
|---------|-------------|
| **Period Comparison** | Compare metrics vs previous period with % change |
| **Real-time Users** | Live visitor count with auto-refresh |
| **Export CSV** | Download any report as CSV |
| **Demo Mode** | Try without Google OAuth setup |
| **Single File** | No build process, no dependencies |
| **Privacy First** | Data flows directly from Google to your browser |
| **Responsive** | Works on desktop, tablet, and mobile |

### 🛠 Tech Stack
- Vanilla JavaScript (no framework)
- Chart.js for visualizations
- D3.js + d3-sankey for user flow
- Google Analytics Data API v1
- Google Identity Services for OAuth

---

## 🎮 Demo

**Try it instantly** — No setup required!

1. Download `index.html`
2. Open it in your browser
3. Click **"Try Demo Mode"**

Demo mode shows realistic sample data so you can explore all features before connecting your GA4 property.

---

## 🚀 Quick Start

### Option 1: Direct Download
1. Download `index.html`
2. Open in any modern browser
3. Use Demo Mode or connect your GA4

### Option 2: Local Server (for OAuth)
```bash
# Clone the repo
git clone https://github.com/ch-bas/ga4-dashboard.git
cd ga4-dashboard

# Serve locally (choose one)
npx serve .              # Node.js
python -m http.server    # Python 3
php -S localhost:8000    # PHP

# Open http://localhost:3000 (or :8000)
```

### Option 3: GitHub Pages
1. Fork this repo
2. Go to Settings → Pages
3. Enable GitHub Pages from main branch
4. Access at `https://<your-username>.github.io/ga4-dashboard`

---

## 🔧 Google Cloud Setup

To connect your real GA4 data, you need a Google Cloud OAuth Client ID.

### Step 1: Create Project
1. Go to [Google Cloud Console](https://console.cloud.google.com/)
2. Create a new project or select existing
3. Note your project name

### Step 2: Enable API
1. Go to **APIs & Services → Library**
2. Search for "Google Analytics Data API"
3. Click **Enable**

### Step 3: Configure OAuth Consent
1. Go to **APIs & Services → OAuth consent screen**
2. Select **External** user type
3. Fill in app name, support email
4. Add scopes: `analytics.readonly`
5. **Add yourself as a Test User** (important!)
6. Save and continue

### Step 4: Create Credentials
1. Go to **APIs & Services → Credentials**
2. Click **Create Credentials → OAuth client ID**
3. Application type: **Web application**
4. Add Authorized JavaScript origins:
   - `http://localhost:3000` (local development)
   - `http://localhost:8000` (Python server)
   - `https://<your-username>.github.io` (GitHub Pages)
5. Copy the **Client ID**

### Step 5: Connect
1. Open the dashboard
2. Paste your Client ID
3. Click "Sign in with Google"
4. Select your GA4 property
5. Explore your data! 🎉

---

## 📸 Screenshots

<details>
<summary><b>Overview Dashboard</b></summary>
<p align="center">
  <i>Screenshot: Main overview with KPIs and trend chart</i>
</p>
</details>

<details>
<summary><b>Acquisition Channels</b></summary>
<p align="center">
  <i>Screenshot: Channel breakdown with donut chart</i>
</p>
</details>

<details>
<summary><b>Audience Demographics</b></summary>
<p align="center">
  <i>Screenshot: Age, gender, device, and geo data</i>
</p>
</details>

<details>
<summary><b>User Flow (Sankey)</b></summary>
<p align="center">
  <i>Screenshot: Navigation paths visualization</i>
</p>
</details>

<details>
<summary><b>Activity Heatmap</b></summary>
<p align="center">
  <i>Screenshot: Users by day and hour</i>
</p>
</details>

---

## 📁 Project Structure

```
ga4-dashboard/
├── index.html      # The entire dashboard (single file!)
├── README.md       # This file
├── LICENSE         # MIT License
└── screenshots/    # Screenshots for README
```

Yes, it's really just one HTML file. That's the point. 🎯

---

## 🔒 Privacy & Security

- **No backend server** — Everything runs in your browser
- **No data storage** — Nothing is saved or sent anywhere except Google
- **Direct API calls** — Your browser talks directly to Google's servers
- **Open source** — Audit the code yourself

Your analytics data never touches any third-party server.

---

## 🤝 Contributing

Contributions are welcome! Here are some ideas:

- [ ] Add more chart types
- [ ] Custom date range picker
- [ ] Data caching/offline support
- [ ] Additional GA4 dimensions
- [ ] Themes (dark mode, custom colors)
- [ ] PDF export
- [ ] Scheduled email reports (would need backend)

### Development
```bash
# Clone
git clone https://github.com/ch-bas/ga4-dashboard.git

# Make changes to index.html

# Test locally
npx serve .

# Submit PR
```

---

## 📋 FAQ

<details>
<summary><b>Why single file?</b></summary>
Simplicity. Download one file, open it, done. No npm install, no build process, no configuration. It also makes it easy to host anywhere — GitHub Pages, Netlify, or even email it to a colleague.
</details>

<details>
<summary><b>Is my data safe?</b></summary>
Yes. The dashboard runs entirely in your browser. Your OAuth token and analytics data never leave your machine except to communicate directly with Google's APIs. There's no middleman server.
</details>

<details>
<summary><b>Why do I need OAuth setup?</b></summary>
Google requires OAuth for accessing Analytics data. The setup is one-time and gives you full control over what the app can access. You can revoke access anytime from your Google account settings.
</details>

<details>
<summary><b>Can I use this for client reporting?</b></summary>
Yes! You can white-label it by editing the HTML. Add your logo, change colors, remove the "Demo Mode" button, etc. The MIT license allows commercial use.
</details>

<details>
<summary><b>Does it work with Universal Analytics?</b></summary>
No, this dashboard is built specifically for Google Analytics 4 (GA4). Universal Analytics was sunset in July 2023.
</details>

---

## 📄 License

MIT License — Use it however you want. See [LICENSE](LICENSE) for details.

---

## 🙏 Acknowledgments

- [Chart.js](https://www.chartjs.org/) — Beautiful charts
- [D3.js](https://d3js.org/) — Sankey diagrams
- [Google Analytics Data API](https://developers.google.com/analytics/devguides/reporting/data/v1) — The data source
- Inspired by [Porter Metrics](https://portermetrics.com/) dashboard templates

---

<p align="center">
  <b>If this helped you, consider giving it a ⭐</b>
</p>
