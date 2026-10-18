<div align="center">

# Cattle Feed Billing

**Counter billing, stock and sales reports for श्री गणेश ट्रेडर्स (Shree Ganesh Traders), a cattle feed dealer.**

<img src="assets/screenshots/01-dashboard.webp" alt="Dashboard showing the day's sales, bill count, stock on hand and low stock" width="100%" />

<img src="https://img.shields.io/badge/Next.js_16-000000?style=flat-square&logo=nextdotjs&logoColor=white" alt="Next.js" />
<img src="https://img.shields.io/badge/React_19-20232A?style=flat-square&logo=react&logoColor=61DAFB" alt="React" />
<img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript" />
<img src="https://img.shields.io/badge/Tailwind_CSS_4-38B2AC?style=flat-square&logo=tailwindcss&logoColor=white" alt="Tailwind CSS" />
<img src="https://img.shields.io/badge/PostgreSQL_(Neon)-4169E1?style=flat-square&logo=postgresql&logoColor=white" alt="PostgreSQL" />
<img src="https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white" alt="Vercel" />

</div>

---

> This repository is a **public project showcase**. It does not contain the application source code, and the source is not open source. The application is maintained in a private repository.

Customer names and mobile numbers in the screenshots below are masked. The shop name, products and on-screen figures are from the working application.

---

## Overview

The shop sells cattle feed at the counter. A sale has to produce a bill the customer can take away and reduce the bags left in stock at the same time. The owner also needs low-stock warnings, a record of what is still owed, and a report that opens in Excel.

The application is the counter desk: write a bill, keep stock honest, take a payment, and review the day from a phone or a larger screen. Shop screens require a sign-in. Each bill records who wrote it.

## Key features

- **Bills at the counter.** Customer, mobile number, who billed, and the product lines. A line is refused when there is not enough stock.
- **Stock that moves with the sale.** Add a product, restock it, or edit its rate and minimum. Saving a bill reduces the quantity in the same step.
- **Low stock.** Products under their minimum are marked on the dashboard, in product search, and on a filter in the stock list.
- **Customers by mobile number.** The number matches the customer, so a later visit can bring back their name, earlier bills and what is still owed.
- **Payments.** A bill can be paid, partly paid or still pending, in cash or online. A later payment is recorded against that customer.
- **Print and WhatsApp.** The bill prints in Marathi. The shop can send a PDF and a private link, which the customer opens without an account.
- **Sales records.** Bills for a chosen period, newest first, with the period total and a search by bill number or customer.
- **Reports.** Filter by period, product, customer or who billed. Charts on the page, and the same period downloaded as an Excel workbook.

A rate typed on a bill applies to that bill only. It does not change the product's usual price.

The Payments screen is part of the application. A screenshot of it was not available for this showcase.

## Screenshot gallery

### Dashboard

The day's sales, bill count, stock on hand and how many products are under the minimum.

<img src="assets/screenshots/01-dashboard.webp" alt="Dashboard for the trading day" width="100%" />

The same day on a phone, in the light theme. The larger screen uses a sidebar. The shop can follow light, dark or the system appearance.

<img src="assets/screenshots/10-mobile.webp" alt="Phone layout of the dashboard in the light theme" width="320" />

### Billing

Product search shows the rate, the units in stock and a low-stock mark before a line is added.

<img src="assets/screenshots/02-new-bill.webp" alt="New bill with product search and stock levels" width="100%" />

Two lines on a bill. Quantity and rate are set per line, and the amount is calculated before the bill is saved.

<img src="assets/screenshots/03-bill-filled.webp" alt="Bill with two product lines, quantities and rates" width="100%" />

A Marathi bill, ready to print or to send as a PDF on WhatsApp.

<img src="assets/screenshots/04-bill-print.webp" alt="Print preview of a Marathi bill with print and WhatsApp actions" width="100%" />

### Stock

Each product has a selling rate, the quantity on hand and a minimum. A row can be restocked, edited or removed.

<img src="assets/screenshots/05-stock.webp" alt="Stock list with rates, quantities, minimums and low-stock marks" width="100%" />

### Sales

Bills for the chosen period, newest first, with the period total.

<img src="assets/screenshots/06-sales.webp" alt="Sales records for a day with the total and bill list" width="100%" />

### Reports

A month's summary set beside the previous period, with the sales trend.

<img src="assets/screenshots/07-reports.webp" alt="Reports summary with sales figures and a sales trend" width="100%" />

Units sold, share of sales, the largest customers and who wrote the bills. Names on the customer chart are replaced with C1 to C5.

<img src="assets/screenshots/08-reports-charts.webp" alt="Report charts for products, sales share, customers and billers" width="100%" />

Busy hours across the week, and each product's units, average rate, sales and share.

<img src="assets/screenshots/09-reports-tables.webp" alt="Busy-hours heatmap and product performance table" width="100%" />

## Technology

| Area | What it uses |
| --- | --- |
| Interface | Next.js 16, React 19, TypeScript, Tailwind CSS 4 |
| API | Next.js route handlers in the same project |
| Database | PostgreSQL on Neon |
| Sign-in | Shop account, session cookie, hashed passwords, a limit on failed attempts |
| Charts, files | ApexCharts on the reports page, ExcelJS for the workbook, jsPDF for the bill PDF |
| Hosting | Vercel |

No other services are part of this project.

## Workflows

1. Sign in. Shop screens stay behind the account.
2. Read Today: sales, bills, stock on hand and anything under its minimum.
3. Write a bill. Search a product, set the quantity and, if needed, a rate for this bill. Mark it paid, partly paid or pending.
4. Save. The bill, any payment taken now, and the new stock quantities are stored together. A product that drops under its minimum is called out.
5. Print the Marathi bill, or send a PDF and a private link on WhatsApp.
6. Restock from the stock list, look up a period in Sales, record a later payment, and download the report.

The Excel file follows the filters on the reports page: summary, sales over the period, products, who billed, customers, bills and their lines, busy hours, and products that are low.

## Highlights

- One save updates the bill and the stock together, after checking that the quantity is available.
- The customer's mobile number is how the shop finds their earlier bills and dues.
- Reports compare the chosen period with the one before it.
- The printed bill is laid out in Marathi for the counter.
- The layout is usable on a phone, with the main sections along the bottom.

## Privacy

This repository only presents the project. It does not include the application source, environment files, database access, or customer records. Do not treat it as an open-source release of the application.

## Contact

**Shubham Deshmukh**

- Studio: [software-studio.nexoralab.workers.dev](https://software-studio.nexoralab.workers.dev/)
- LinkedIn: [shubham-deshmukh1720](https://www.linkedin.com/in/shubham-deshmukh1720)
- GitHub: [@shubhamdsk](https://github.com/shubhamdsk)
