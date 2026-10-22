# 📊 Arcus Monitor Dashboard

An advanced, real-time cryptocurrency monitoring dashboard designed to track wallets, open/closed positions, market signals, performance metrics, and historical trading data with zero latency flicker.

---

## 🌟 Overview

**Arcus Monitor** provides professional-grade visualization and diagnostics for multi-wallet crypto trading performance. Built as a self-contained, light-weight application with a sleek dark-themed UI, it offers comprehensive real-time insights into active trades, historical profit & loss (PnL), liquidations, portfolio equity evolution, and market ranking indicators.

---

## 🔥 Key Features

- **⚡ Smooth Anti-Flicker DOM Rendering**: Features an in-house Virtual DOM patching mechanism (`innerHTML` override) to re-render DOM changes dynamically every 5 seconds without resetting CSS animations, dropping element focus, or scrolling jumps.
- **💼 Multi-Wallet Tracking**:
  - Track up to 10 distinct cryptocurrency wallets simultaneously with custom color-coded indicators.
  - Quick-copy wallet addresses directly from the interface.
  - Instant wallet selection and global filter toggle across all metrics.
- **📈 Real-Time Open Positions**:
  - Live breakdown of long and short positions per trading pair.
  - Real-time mark price, entry price, liquidation price, leverage mode (Cross/Isolated), TP/SL tracking, and floating PnL calculation.
  - Interactive position filter checkboxes.
- **📊 Equity & Patrimony Evolution Chart**:
  - Dynamic visual charts mapping portfolio equity growth over time.
  - Split view displaying active open positions alongside recent ledger activities.
  - Toggleable chart indicators for individual entry and exit points (Longs, Shorts, TP, SL, Liquidations).
- **🏆 Top 10 Wallet Ranking**:
  - Aggregated performance rankings comparing profit margins, trade counts, and direction biases (long vs. short volume) across monitored wallets.
- **📜 Historical Operations & Closed Trades**:
  - Full execution history log with pagination, status filters (TP, SL, Manual Close, Liquidations), date range filters, and trade outcome badges.
- **🔍 Auto-Fetch & Diagnostics Console**:
  - Built-in automatic PnL fetch routine with customizable retry intervals.
  - Real-time diagnostic debug console capturing status logs, errors, and CORS connection states with one-click log export.
- **🌐 Dual-Language Support**: Instant switcher between **English (EN)** and **Portuguese (PT-BR)** interface languages.
- **🎨 Modern Responsive UI**: Engineered with a JetBrains Mono & Syne typography stack, macOS-style panel minimization controls, KDE Plasma-inspired "Hide-to-Sidebar" functionality, custom dark-mode scrollbars, and high-contrast status pills.

---

## 🖥️ System Architecture & UI Overview

| Section | Description |
| :--- | :--- |
| **Top Navigation Bar** | Minimalist floating top nav for quick section scrolling and global layout adjustments. |
| **Header Metrics Bar** | Displays overall monitored equity, live 24h PnL summary, active pair count, and real-time network connection pulse. |
| **Wallet Input Panel** | Dynamic configuration grid for inserting, clearing, and auto-fetching wallet address credentials. |
| **Mid-Panel Row** | Live Open Positions breakdown and Real-Time Event Stream log. |
| **Patrimony Chart Area** | Detailed equity evolution graph synced with trade action markers. |
| **Master Signal & Operations Table** | Searchable, paginated data grid detailing active and past positions. |
| **Diagnostic Terminal** | Collapsible system log capturing network requests, errors, and auto-fetch triggers. |

---

## 🚀 Getting Started

### Prerequisites

Arcus Monitor is completely standalone and requires no local backend build environment or compiler dependencies. It runs directly in any modern Web Browser (Chrome, Firefox, Edge, Safari, Brave).

### Running Locally

1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/arcus-monitor.git
   cd arcus-monitor
   ```

2. **Open the Dashboard**:
   Simply double-click `dashboard.html` or open it using your web browser:
   ```bash
   # On macOS
   open dashboard.html

   # On Linux
   xdg-open dashboard.html

   # On Windows
   start dashboard.html
   ```

3. **Using Local Server (Optional)**:
   For optimal asset loading and web-worker behavior, you can host it locally using Python or Node.js:
   ```bash
   # Python 3
   python -m http.server 8000

   # Node.js (npx)
   npx serve .
   ```
   Navigate to `http://localhost:8000` or `http://localhost:3000` in your browser.

---

## 🛠️ Configuration & Multi-Wallet Setup

1. Open the dashboard in your browser.
2. In the **Wallet Input Panel**, enter up to 10 wallet public addresses.
3. Click **Apply Wallets** or enable **Auto-Fetch PnL** to continuously poll live chain data.
4. Use the color-coded toggles next to each address to filter metrics globally for specific accounts.

---

## ⚡ Technical Highlights

- **Zero-Dependency Architecture**: Pure JavaScript (ES6+), HTML5, and CSS3 without bulky third-party frontend frameworks.
- **Diffing Engine**: Includes a lightweight DOM morphing algorithm (`morphChildren` & `syncAttrs`) preventing layout flicker on dynamic refresh cycles.
- **CORS Handling**: Native error detection and user guidance when cross-origin REST requests encounter network restrictions.
- **Adaptive Layout**: Responsive CSS Grid & Flexbox setup tailored for high-resolution trading monitors and mobile viewports alike.

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).
