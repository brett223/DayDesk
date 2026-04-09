# DayDesk — Task & Billing Tracker

A lightweight, single-file web app for freelancers and consultants to manage daily tasks and track billable time. No frameworks, no build step, no server — just open `index.html` in any browser.

## Live Demo

Hosted via GitHub Pages: **[https://YOUR-USERNAME.github.io/daydesk](https://YOUR-USERNAME.github.io/daydesk)**

> Replace `YOUR-USERNAME` with your GitHub username after deployment.

---

## Features

- ✅ **Task checklist** with three priority groups — High, Medium, Low
- 🔄 **Three-state progress** — Undone / Partially done / Complete (click the circle)
- 🏷️ **Billing reference** field on every task (e.g. `INV-2024-001`)
- ⏱️ **Time logging** — log hours when completing a task, auto-calculates ZAR value
- 📋 **Subtasks** — expand any task to add sub-items
- 📁 **Custom headings** — group tasks under your own section labels
- 📅 **Upcoming deadlines** — colour-coded by urgency (overdue / soon / ok)
- 🗂️ **Completed archive** — full history of completed tasks with date, hours, and value
- 📊 **Billing report** — filter by date range, export as CSV
- 🤖 **AI assistant** — Claude-powered chat sidebar, aware of your tasks and rate
- 💾 **Local storage** — all data persists in your browser between sessions

---

## Getting Started

### Option 1 — Open Locally

1. Download or clone this repo
2. Open `index.html` in any browser
3. That's it — no install, no server needed

```bash
git clone https://github.com/YOUR-USERNAME/daydesk.git
cd daydesk
open index.html        # macOS
start index.html       # Windows
xdg-open index.html    # Linux
```

### Option 2 — GitHub Pages (Recommended)

1. Fork or push this repo to GitHub
2. Go to **Settings → Pages**
3. Set source to **Deploy from a branch → main → / (root)**
4. Save — your app will be live at `https://YOUR-USERNAME.github.io/daydesk`

---

## Usage

### Adding Tasks
- Type in the `+ Add [priority] task…` bar at the bottom of each priority group
- Press **Enter** to add

### Task States
Click the circle button to cycle through states:
| State | Indicator |
|-------|-----------|
| Todo | Empty circle |
| Partially done | Circle with yellow dot |
| Complete | Green filled circle with ✓ |

Marking a task **Complete** opens the billing modal automatically.

### Billing
1. Set your hourly rate (top left, in ZAR)
2. When completing a task, enter hours spent and a billing reference
3. The rand value is calculated automatically
4. Task moves to the **Completed Archive**

### Exporting
Click **⬇ Report** in the header → filter by date range → **⬇ Export CSV**

### AI Assistant
The right-hand panel is a Claude-powered assistant. It knows your current tasks, deadlines, and hourly rate. Ask it to:
- Prioritise your day
- Estimate time for a task
- Summarise completed work for a client email
- Suggest billing notes

---

## Configuration

All settings are stored in `localStorage` under the key `daydesk_v5`. No external database or account needed.

To reset all data: open the browser console and run:
```js
localStorage.removeItem('daydesk_v5'); location.reload();
```

---

## Tech Stack

| Layer | Choice |
|-------|--------|
| UI | Pure HTML/CSS/JS — zero dependencies |
| Storage | Browser `localStorage` |
| AI | Anthropic Claude API (`claude-sonnet-4-20250514`) |
| Fonts | Google Fonts (Playfair Display, DM Mono, DM Sans) |
| Hosting | GitHub Pages |

---

## File Structure

```
daydesk/
├── index.html     # Entire application (self-contained)
└── README.md      # This file
```

---

## Browser Support

Works in all modern browsers:
- Chrome / Edge 90+
- Firefox 88+
- Safari 14+

---

## License

MIT — free to use, modify, and distribute.
