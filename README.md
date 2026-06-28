# Fabric Commission Tracker

A clean, self-contained vanilla HTML/CSS/JS prototype for tracking fabric orders, invoices, customer payments, and the commissions earned from manufacturers.

> **Live repo**: https://github.com/abhayvadalia/AV_GROK_Fabric_Commission_Tracker

This is a fully functional browser-based prototype.

## What it does

- **Orders**: Capture customer orders to manufacturers, with line items (fabric, qty, rate) and commission terms (percent or fixed).
- **Invoices & Payments**: Record manufacturer invoices (many-to-many with orders), customer payments against them. Payments automatically generate commission accruals.
- **Commissions**: See exactly what commission was earned, with full traceability back to the payment → invoice → order(s).
- **Import**: Upload CSV files or load realistic sample data. Everything runs 100% in the browser (localStorage).

Commission is only earned when the customer pays (per the business rules).

## How to run

1. Open the folder in Finder
2. Double-click `index.html`
3. Or drag `index.html` into any browser

No build step, no server, no install.

## Key features

- Modern responsive UI (Tailwind via CDN)
- Full CRUD flows for the three modules
- Automatic commission calculation + apportioning on partial/full payments
- Aging buckets + outstanding summaries
- Filters, sorting, search
- File import (CSV) + export
- Data persisted in your browser

## Data model notes (prototype)

- Many-to-many between Orders and Invoices is supported.
- On payment, paid amount is apportioned proportionally to the value of linked order lines.
- Line-level commission rates (percent or fixed) from the order are used.

## Next steps ideas

- Add "Settle Commission" (mark as paid by manufacturer)
- Better CSV mapping UI
- Charts (Chart.js via CDN)
- Multi-user / export to real backend

This prototype follows the requirements captured in the original spec document.
