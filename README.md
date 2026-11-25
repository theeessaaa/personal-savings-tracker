# Savings Passbook

A simple savings tracker for your phone. It keeps your **Personal**, **Travel**, and **Gadget** savings separate, tracks how much you save every **payday cut-off** (15th and 30th), and keeps an eye on your **credit card** balances.

**Current version:** 1.1.0 – see [CHANGELOG.md](CHANGELOG.md) for what's new.

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
- **Credit cards** – see the balance to pay and available credit for each card, log payments and purchases, and get a due-date reminder
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

### 6. Track your credit cards
1. Go to **Credit cards → Add a credit card**.
2. Enter a **nickname** (e.g. BPI Amore Visa), the **credit limit**, the **balance to pay now**, and the **due day** (optional).
   > Use a nickname only. Never type your card number.
3. Use **Log card activity** to record:
   - **Payment** – money you paid to the card (lowers the balance to pay)
   - **Purchase** – something you charged to the card (raises the balance to pay)
4. Each card shows:
   - **To pay** = starting balance + purchases − payments
   - **Available** = credit limit − balance to pay
   - How much of your limit is used, and when the next payment is due
5. When your new statement arrives, tap **Edit** on the card and type the statement balance in **Balance to pay** to match it.

Card payments also show in the monthly table (by 15th / 30th cut-off) and in **History**. Credit cards are **not** counted in your total savings.

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
| `CHANGELOG.md` | List of changes in each version |

---

## Versioning

The app uses **MAJOR.MINOR.PATCH** version numbers (e.g. `1.1.0`):
- **MINOR** goes up for new features (1.0.0 → 1.1.0)
- **PATCH** goes up for bug fixes (1.1.0 → 1.1.1)

The current version is shown at the bottom of the app. Tap **What's new** to see the changes.

## Updating the app

When you release a new version:
1. Change the version number in **both** files so they match:
   - `index.html` → `const APP_VERSION='1.1.0';` (and add the new version at the top of `CHANGES`)
   - `sw.js` → `const VERSION = 'savings-v1.1.0';`
2. Add the changes to `CHANGELOG.md`.
3. Upload the changed files to the repo (**Add file → Upload files → Commit changes**). Use a commit message like `v1.1.0: add credit cards`.
4. Optional: create a release in GitHub (**Releases → Draft a new release**, tag `v1.1.0`).
5. Wait 1–2 minutes for GitHub Pages to update.
6. Open the app once while online, close it fully, then reopen it. You'll see the **What's new** note.

Updating the files does **not** erase your saved goals and deposits.
