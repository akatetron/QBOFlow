# QBOFlow — Free, Private CSV to QBO Converter

**Convert CSV bank statements to QuickBooks Web Connect (`.QBO`) files, 100% in your browser.**
Your financial data never leaves your device: no uploads, no accounts, no server.

🔗 **Live app:** https://akatetron.github.io/QBOFlow/

## Features

- 🔒 **Zero-upload privacy:** files are read with the browser's FileReader API and converted with JavaScript. There is no backend.
- 📄 **Works with most bank CSVs:**
  - Auto-detects the header row (even below account-info blocks) and guesses the date, payee, amount and debit/credit columns.
  - Supports a single signed Amount column or separate Debit/Credit columns, with an optional sign flip for credit-card exports.
  - Date formats: auto-detect, `MM/DD/YYYY`, `DD/MM/YYYY`, `YYYY-MM-DD`, plus text dates like `Jan 5, 2026`.
  - Amounts like `$1,234.56`, `(45.20)`, `45.20-`, `1.234,56`.
- 🏦 **Bank configuration:** searchable INTU.BID picker (or a custom BID), account type (Checking / Savings / Credit Card), routing and account numbers.
- 👀 **Live preview:** the first 10 transactions, total count, net total, money in/out and date range.
- ♻️ **Duplicate-safe:** each transaction gets a stable `FITID` derived from its contents, so re-importing overlapping statements won't create duplicates.
- ✅ **OFX 1.0.2 (SGML) output:** the format QuickBooks Desktop and QuickBooks Online accept for Web Connect imports.

## How to use

1. Open the [live app](https://akatetron.github.io/QBOFlow/) (or open `index.html` locally).
2. Drop your bank's `.csv` export onto the page.
3. Check the column mapping and bank/account settings.
4. Review the preview, then click **Download .QBO File**.
5. Import into QuickBooks:
   - **Desktop:** File → Utilities → Import → Web Connect Files
   - **Online:** Banking → Upload transactions → select the `.qbo` file

## Tech stack

A single static `index.html`, with no build step:

- [Tailwind CSS](https://tailwindcss.com) (Play CDN)
- [PapaParse](https://www.papaparse.com) for CSV parsing
- [Lucide](https://lucide.dev) icons
- Vanilla JavaScript (ES6)

## Deploying

The site is plain static HTML, so any static host works. On GitHub Pages it's served from the repository root (`.nojekyll` skips Jekyll processing).

## Disclaimer

QBOFlow is not affiliated with Intuit Inc. QuickBooks is a trademark of Intuit Inc. Always review imported transactions before reconciling.
