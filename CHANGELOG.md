# Changelog

All notable changes to Savings Passbook are listed here.
Versions follow [Semantic Versioning](https://semver.org/): **MAJOR.MINOR.PATCH**

- **MAJOR** – big changes that may not work with old backups
- **MINOR** – new features (e.g. 1.0.0 → 1.1.0)
- **PATCH** – bug fixes and small tweaks (e.g. 1.1.0 → 1.1.1)

---

## [1.1.0] – 2026-11-25

### Added
- **Credit cards** section
  - Add a card with a nickname, credit limit, current balance to pay, and due date
  - See each card's **balance to pay**, **available credit**, and how much of the limit is used
  - Due date reminder (e.g. "Due Dec 5 · in 10 days")
  - Log **payments** and **purchases**, tagged by payday cut-off (15th / 30th)
  - Edit a card's name, limit, due day, or balance (to match your latest statement)
- Credit cards tile in the top summary (total to pay and total available)
- **Card payments** table in the monthly view, split by cut-off
- Credit card activity in **History**, with a "Credit cards" filter
- App version shown at the bottom of the app
- **What's new** note that shows once after each update

### Changed
- Summary tiles show in a 2×2 grid on phones

---

## [1.0.0] – 2026-11-25

### Added
- Personal (by bank account), Travel (by country), and Gadget (Phone / iPad / MacBook) savings
- Deposits and withdrawals tracked by payday cut-off (15th and 30th)
- Monthly table and year view by cut-off
- Goals with targets, progress bars, and editing
- History with delete
- Works offline and can be installed on your phone
- Backup and restore (file, copy, or paste)
