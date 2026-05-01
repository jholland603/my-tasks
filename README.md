# My Day

A personal dashboard and task tracker that lives in your browser and syncs to GitHub. Features a live clock, real-time weather, live stock quotes, favorite links, and a full task management system — all in a single HTML file with no accounts, no subscriptions, and no servers.

---

## Getting Started

### 1. Create a GitHub repo
Go to [github.com/new](https://github.com/new) and create a **public** repository named `my-tasks`.

### 2. Upload the app
In your new repo, click **Add file → Upload files** and upload `index.html`.

### 3. Enable GitHub Pages
Go to **Settings → Pages → Source**, select the `main` branch, and click Save. Your app will be live at:
```
https://jholland603.github.io/my-tasks
```

### 4. Create a GitHub Personal Access Token
Go to [github.com/settings/personal-access-tokens/new](https://github.com/settings/personal-access-tokens/new) and create a fine-grained token with:
- **Repository access:** Only `my-tasks`
- **Permissions → Contents:** Read and write

Copy the token immediately — you won't be able to see it again.

### 5. Connect the app
Open your live URL, click **⚙** in the top right, enter your repo name and token, and click **Save & Connect**.

> **Tip:** Save your token in a password manager. On mobile, tap 👁 to reveal the field as plain text before pasting.

### 6. (Optional) Enable live stock quotes
Sign up for a free API key at [finnhub.io](https://finnhub.io/register), then click **⚙** and paste your key in the **Finnhub API Key** field.

---

## Dashboard

The top of the page shows three widgets:

### 🕐 Clock
Live clock with seconds and full date, updates every second.

### 🌤 Weather
Live 5-day forecast for Rochester, NH powered by **Open-Meteo** (free, no API key required). Refreshes every 30 minutes. Click any forecast day for a detail popup showing:
- Condition
- High / Low temperature
- Precipitation chance
- Rainfall amount (inches)
- Wind speed
- Humidity

### 📈 Markets
Live stock and crypto quotes powered by **Finnhub**. Refreshes every 5 minutes. Default tickers: S&P 500 (SPY), Dow (DIA), Nasdaq (QQQ), TSLA, Bitcoin, Gold (GLD).

**To add a ticker:** type a symbol in the field below the grid and click **+ Add** (or press Enter). Use standard stock symbols for equities (e.g. `AAPL`) and Finnhub format for crypto (e.g. `BINANCE:BTCUSDT`).

**To remove a ticker:** hover over it and click ×.

Your custom ticker list syncs across all devices via `settings.json`.

---

## Favorite Links

A collapsible panel below the dashboard. Click **⭐ Favorite Links** to expand it.

**To add a link:** paste a URL and optional label, then click **+ Add** or press Enter. If no label is provided, the domain name is used automatically.

**To remove a link:** hover the chip and click ×.

Links sync across all devices via `settings.json`.

---

## Task Sections

Tasks are automatically placed into sections based on their due date:

| Section | Due Date |
|---------|----------|
| **Today** | Today or overdue |
| **Tomorrow** | Tomorrow |
| **7 Days** | 2–7 days from now |
| **14 Days** | 8–14 days from now |
| **Backlog** | Beyond 14 days, or no due date |
| **Completed** | Checked off tasks |

Tasks move between sections automatically when you change their due date. Drag and drop to move manually — manual placement is always respected. On load, tasks are rebalanced to their correct section based on current due dates.

---

## Task Fields

| Field | Description |
|-------|-------------|
| **Company** | Company or client ID (disabled for personal tasks) |
| **Description** | The task name — hover to see full text, click to edit |
| **URL** | A related link — click to open, hover to edit |
| **Notes** | Free-form notes — click ✎ to open editor (Ctrl+Enter to save) |
| **Due** | Due date — click to open date picker |
| **Created** | Creation date — defaults to today |

---

## Features

**Work / Personal**
A colored dot next to each description indicates type — burgundy for Work, green for Personal. Click the dot to toggle. Use **All / Work / Personal** filter buttons to show only what you need. New tasks default to the active filter type.

**Search**
Type in the search bar to filter all sections at once. Matches company, description, notes, and URL. Matched text highlights in yellow with a result count shown.

**Sorting**
Click **Company**, **Due**, or **Created** column headers to sort. Click again to reverse, click a third time to return to manual order. Sort preferences sync across devices.

**Drag to reorder**
Grab the ⠿ handle to drag a row to a new position within a section, or drop it onto a different section.

**Overdue tasks**
Rows past their due date are highlighted with a red background so they stand out immediately.

**Clean up completed**
At the bottom of the Completed section, enter a number of days and click **Clean up** to delete completed tasks older than that threshold.

---

## Using on Multiple Devices

Open the live GitHub Pages URL on any device, click ⚙, and enter your token once. Your tasks, sort preferences, tickers, and favorite links all sync automatically via GitHub.

---

## Data & Sync

| File | Purpose |
|------|---------|
| `index.html` | The entire app — one file |
| `tasks.json` | Your task data |
| `settings.json` | Sort preferences, favorite links, and ticker list |
| `CHANGELOG.md` | Version history |
| `README.md` | This file |

Every save creates a GitHub commit, giving you a full history you can restore from at any time.

Your GitHub token and Finnhub key are stored only in your browser's localStorage — never written to any file in your repo.

---

## Current Version

**v1.47** — see `CHANGELOG.md` for full version history.
