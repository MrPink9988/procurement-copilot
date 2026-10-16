# Procurement Copilot — Option A prototype

A responsive, GitHub Pages-ready, browser-only sourcing comparison demo. No backend, API key, build step, or dependencies.

## Start
Open `index.html` in a browser. For a local web server, run `python3 -m http.server 8000` in this directory and visit `http://localhost:8000`.

## Publish on GitHub Pages
1. Create a new GitHub repository and upload `index.html`, `styles.css`, and `app.js` to its root.
2. Open **Settings → Pages**; select **Deploy from a branch**, branch **main**, folder **/(root)**, and save.
3. Open the GitHub Pages URL once deployment finishes.

## Features
- Two preloaded fictional procurement projects.
- Create/rename/delete projects and add/edit/remove supplier quotations.
- Side-by-side comparison with best-value highlighting.
- Four adjustable scoring criteria and live ranking.
- Decision report with supplier notes and review checklist.
- Excel-compatible SpreadsheetML XML export (opens in Microsoft Excel; can be saved as `.xlsx`).
- Print / Save as PDF using the browser.
- Browser-local persistence via `localStorage`.

## Scoring
For positive values, each supplier receives a 0–100 score per criterion relative to the best supplier. Lower is better for price and delivery; higher is better for warranty and scope. The weighted average is normalized over applicable nonzero weights. Zero/missing values are excluded for that supplier; this can make incomplete offers look deceptively strong. **Do not use these scores for real procurement decisions without verification and an appropriate missing-data policy.**

## Limitations and security
**Demonstration only.** No actual document upload, PDF/Excel parsing, AI analysis, multiuser accounts, audit log, source citations, server-side storage, or security controls. Data entered in the browser remains in its local storage, but can be read by other scripts with access to this origin. Do not use real confidential supplier offers. Avoid browser extensions or shared devices for sensitive data. Clearing browser data erases changes. Export backups if needed.

The exported file uses Excel 2003 XML Spreadsheet format (`.xml`), not native `.xlsx`. Open it with Excel and use **Save As → Excel Workbook (.xlsx)**.
