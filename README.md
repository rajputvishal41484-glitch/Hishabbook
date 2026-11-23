# HisabBook – Smart Expense Manager

A local-first, mobile-first personal expense manager built as an installable Progressive Web App (PWA).

## Included
- Dashboard: today/month/year totals, transaction count, six-month chart, category summary and recent activity.
- Expense CRUD: amount, title, category, date, payment method and notes.
- Built-in categories plus custom category add/edit/delete.
- Reports: daily, monthly, quarterly, half-yearly, yearly and inclusive custom date range; category filter; totals, transaction count, highest transaction, calendar-day average, daily and category breakdowns.
- Transaction search, category/date filters and sorting.
- Overall and per-category monthly budgets with usage and remaining amount.
- CSV export, JSON backup/restore and print-to-PDF (use the browser's Print > Save as PDF).
- INR default, currency setting, Hindi/English interface, light/dark/system theme.
- IndexedDB persistence and PWA offline cache.

## Run locally
Because browser storage and service workers need a web origin, do not open `index.html` directly from the file manager.
1. Extract the ZIP.
2. Serve this folder over localhost or HTTPS (for example, `python -m http.server 8000` on a computer).
3. Open `http://localhost:8000` in Chrome.
4. On Android Chrome, use menu > **Install app** / **Add to Home screen**.

## Android package
This deliverable is a working PWA and can be installed on Android from Chrome. A signed APK/AAB is not included. To publish a native Android package, wrap the PWA with Capacitor, configure the Android project, test on devices, then build/sign the APK or AAB in Android Studio.

## Data and privacy
Expense records are stored in the browser's IndexedDB on that device. There is no cloud account or cross-device sync in this version. Clearing browser/app storage can erase data; use **Settings > Backup data** regularly. Restore a JSON backup from **Settings > Restore backup**.

## Accuracy notes
- Amounts are rounded to 2 decimal places at entry and aggregated in integer paise-equivalent cents to reduce floating-point drift.
- Date ranges are inclusive.
- Calendar quarters are Jan–Mar, Apr–Jun, Jul–Sep and Oct–Dec.
- Half-years are Jan–Jun and Jul–Dec.
- Monthly budget records are scoped to the current calendar month.
- Reports calculate daily average across every calendar day in the selected date range, including days with no expense.
