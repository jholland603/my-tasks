# My Tasks

A lightweight, personal task tracker that lives in your browser and syncs to GitHub. No accounts, no subscriptions, no servers — just a single HTML file and your own GitHub repo.

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

### 4. Create a Personal Access Token
Go to [github.com/settings/personal-access-tokens/new](https://github.com/settings/personal-access-tokens/new) and create a fine-grained token with:
- **Repository access:** Only `my-tasks`
- **Permissions → Contents:** Read and write

Copy the token immediately — you won't be able to see it again.

### 5. Connect the app
Open your live URL, enter your repo name and token in the setup screen, and click **Save & Connect**. Your tasks will sync automatically from that point on.

> **Tip:** Save your token in a password manager so you can easily paste it on new devices.

---

## Sections

Tasks are automatically placed into sections based on their due date:

| Section | Due Date |
|---------|----------|
| **Today** | Today or overdue |
| **Tomorrow** | Tomorrow |
| **7 Days** | 2–7 days from now |
| **14 Days** | 8–14 days from now |
| **Backlog** | Beyond 14 days, or no due date |
| **Completed** | Checked off tasks |

Tasks move between sections automatically when you change their due date. You can also drag and drop to move them manually — manual placement is always respected.

---

## Task Fields

| Field | Description |
|-------|-------------|
| **Company** | Company or client ID (disabled for personal tasks) |
| **Description** | The task name — click to edit |
| **URL** | A link related to the task — click to open, hover to edit |
| **Notes** | Free-form notes — click ✎ to open editor |
| **Due** | Due date — click to open date picker |
| **Created** | Creation date — defaults to today |

---

## Features

**Work / Personal**
Each task has a type dot next to the description — burgundy for Work, green for Personal. Click the dot to toggle. Use the **All / Work / Personal** filter buttons to show only what you need.

**Search**
Type in the search bar to filter all sections at once. Matches company, description, notes, and URL. Matched text highlights in yellow.

**Sorting**
Click the **Company**, **Due**, or **Created** column headers to sort. Click again to reverse. Click a third time to return to manual order. Sort preferences sync across devices.

**Drag to reorder**
Grab the ⠿ handle on the left of any row to drag it to a new position within a section, or drop it onto a different section entirely.

**Overdue tasks**
Rows with a past due date are highlighted in red so they stand out immediately.

**Clean up completed**
At the bottom of the Completed section, enter a number of days and click **Clean up** to delete completed tasks older than that threshold.

---

## Data & Sync

Your tasks are saved to `tasks.json` in your GitHub repo. Every save creates a commit, giving you a full history you can restore from at any time.

Settings (sort preferences) are saved to `settings.json` in the same repo.

Both files are created automatically the first time you use the app — you don't need to create them manually.

**Your GitHub token** is stored only in your browser's localStorage. It is never written to any file in your repo.

---

## Using on Multiple Devices

Open the live GitHub Pages URL on any device, enter your token once in the setup screen (click ⚙ in the top right), and your tasks will sync automatically. The token is stored locally per device.

> **Mobile tip:** If pasting the token is difficult, tap the 👁 button to reveal the field as plain text first.

---

## Files in the Repo

| File | Purpose |
|------|---------|
| `index.html` | The entire app — one file |
| `tasks.json` | Your task data |
| `settings.json` | Your sort preferences |
| `CHANGELOG.md` | Version history |
| `README.md` | This file |

---

## Current Version

**v1.35** — see `CHANGELOG.md` for full version history.
