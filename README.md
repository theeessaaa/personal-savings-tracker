# Savings Passbook

A simple savings tracker for your phone. It keeps your **Personal**, **Travel**, and **Gadget** savings separate and tracks how much you save every **payday cut-off** (15th and 30th).

It works **offline** once installed, and all your data stays on your phone.

---

## Features

- **Three kinds of savings**
  - **Personal** – one pot per savings bank account (e.g. Union Bank, Maya Savings)
  - **Travel** – one pot per country (e.g. Japan, South Korea)
  - **Gadgets** – one pot per device, tagged as Phone, iPad, or MacBook
- **Payday cut-offs** – every deposit is filed under the **15th** (days 1–15) or **30th** (days 16–end of month) cut-off
- **Monthly table** – see each pot's 15th, 30th, and month totals
- **Year view** – bar chart of every month, split by cut-off
- **Goals with progress bars** – set a target and see how much is left
- **Edit goals** – change the name, target, category, or device anytime
- **Withdrawals** – log money you took out
- **History** – see and delete past entries
- **Backup and restore** – save your data to a file and load it back

---

## Install on your phone (Android / Chrome)

1. Open the app link in **Chrome**:
   `https://theeessaaa.github.io/personal-savings-tracker/`
2. Tap **⋮** (top right) → **Install app** (or **Add to Home screen**).
3. A green **₱** icon appears on your home screen.
4. Open it once while online. After that it works **without internet**.

> Opening `index.html` straight from your Files app won't install it. It has to be opened from the GitHub Pages link.

---

## How to use

### 1. Clear the sample data
The app starts with example goals and deposits. Scroll to the bottom and tap **Clear sample data** to start fresh.

### 2. Add your goals
Go to **Goals → Add a goal**:
| Category | What to type as the name | Example |
|---|---|---|
| Personal | Your bank account | Union Bank |
| Travel | The country | Japan |
| Gadget | The device model (then pick Phone / iPad / MacBook) | iPhone 17 Pro |

Add a **target amount** if you have one (optional).

### 3. Log a deposit every payday
In **Log a payday deposit**:
1. Choose **Deposit** (or **Withdrawal**)
2. Pick the pot
3. Enter the amount
4. Check the date – the **cut-off fills in by itself** (1–15 → 15th, 16–31 → 30th). Change it if your payday came early or late.
5. Tap **Add to passbook**

### 4. Track your progress
- **Top section** – total saved, this cut-off, this month, and the change from last month
- **Monthly table** – use **‹ ›** to move between months
- **Year view** – tap any month to open it in the table
- **Goals** – progress bar and amount left for each pot

### 5. Edit a goal
Tap **Edit** on a goal card to change its name, target, category, or device, then tap **Save**. Your deposits stay with the goal.

---

## Back up your data (important)

Your data is saved **only on your phone**. Clearing Chrome's data or uninstalling the app will erase it.

- **Back up:** bottom of the app → **Backup and restore** → **Download backup file**. Do this every payday.
- **Restore / move to a new phone:** **Backup and restore** → pick the backup file under **Restore from a backup file**.

---

## Files in this repo

| File | What it does |
|---|---|
| `index.html` | The app itself |
| `sw.js` | Makes the app work offline |
| `manifest.webmanifest` | App name, colours, and icon for installing |
| `icon-192.png`, `icon-512.png` | App icons |
| `README.md` | This guide |

---

## Updating the app

1. Upload the new files to the repo (**Add file → Upload files → Commit changes**).
2. If you changed any file, also change the version in `sw.js`:
   ```js
   const VERSION = 'savings-v2'; // bump to savings-v3, v4, ...
   ```
3. Wait 1–2 minutes for GitHub Pages to update.
4. Open the app once while online, close it fully, then reopen it.

Updating the files does **not** erase your saved goals and deposits.
