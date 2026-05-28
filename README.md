# My Finances — PWA Setup Guide

## What's in this folder

| File | Purpose |
|------|---------|
| `index.html` | The full app |
| `sw.js` | Service worker (enables offline use) |
| `manifest.json` | PWA manifest (enables "Add to Home Screen") |

All three files must be in the **same folder** and served from the same web server.

---

## How to install on your phone

Because PWAs require HTTPS, you need to host these files somewhere before you can install the app. The simplest free options:

### Option A — Netlify Drop (recommended, 2 minutes)
1. Go to **https://app.netlify.com/drop**
2. Drag the entire `finance-tracker` folder onto the page
3. Netlify gives you a free HTTPS URL instantly (e.g. `https://random-name.netlify.app`)
4. Open that URL on your phone
5. **iPhone**: tap the Share button → "Add to Home Screen"
   **Android**: tap the menu (⋮) → "Add to Home Screen", or wait for the install banner in the app
6. Done — the app icon appears on your home screen and works offline

### Option B — GitHub Pages (free, takes ~5 minutes)
1. Create a free GitHub account at github.com
2. Create a new repository (public)
3. Upload the three files
4. Go to Settings → Pages → Source: main branch → Save
5. Your app is live at `https://yourusername.github.io/repo-name`
6. Follow step 4–6 from Option A

### Option C — Any web hosting you already use
Upload the three files to any HTTPS web host and navigate to `index.html`.

---

## Features

- ✅ Add expenses and gains
- ✅ Enter amount, currency (16 currencies), description, date, tags
- ✅ Create and manage tags to classify entries
- ✅ Filter transactions by type or tag
- ✅ Summary stats (total gains, expenses, net balance per currency)
- ✅ Export to Excel (.xlsx) with 3 sheets: all transactions, by currency, by tag
- ✅ Works fully offline after first load
- ✅ Data stored locally on your device (localStorage)
- ✅ Installable as a home screen app (no app store needed)

---

## Data & privacy

All data is stored **only on your device** using the browser's localStorage. Nothing is sent to any server. Uninstalling the browser or clearing site data will erase your entries — export to Excel regularly as a backup.
