# VentaExpress — Q4 2024 Sales Data Cleaning & Executive Reporting (Excel)

**Business context:** VentaExpress is a growing e-commerce company. As Junior Data Analyst, I was asked by the Operations Director to turn a raw, unprocessed quarterly sales export into a clean, decision-ready executive report — identifying data quality issues, calculating the KPIs leadership needed, and packaging the findings into a report a non-technical stakeholder could act on immediately.

**Method:** Spreadsheet-based data auditing, cleaning documentation, KPI calculation, and dashboard-style reporting in Microsoft Excel.

**Year:** 2024 (Q4: October–December)

---

## 📁 Repository Contents

| File | Description |
|---|---|
| [`quarterly-sales-analysis-ventaexpress-2024.xlsx`](./quarterly-sales-analysis-ventaexpress-2024) | Full workbook: raw data, cleaned data, KPI calculations, charts, and executive summary |

> 💡 **Note on language:** this README is written in English for portfolio purposes, but the Excel workbook itself remains in Spanish, its original working language.

> [![Open in Google Sheets](https://img.shields.io/badge/Open-Google%20Sheets-34A853?logo=google-sheets&logoColor=white)](https://docs.google.com/spreadsheets/d/e/2PACX-1vRvTMai_O05CDQKLlM4vGKLfNdac24pdmpgBpP7s5LzA_jKqW6esvlNjn6QYT5wDQ/pubhtml)

---

## 🎯 Project Objectives

1. Identify and document data quality issues in a real, unprocessed sales export.
2. Apply a systematic, justified cleaning methodology.
3. Organize the data following spreadsheet best practices (separate raw vs. cleaned layers).
4. Calculate the KPIs relevant to strategic decision-making.
5. Build visualizations that communicate the findings effectively.
6. Structure a clear, actionable executive report.

---

## 🗂️ Dataset Overview

- **Source:** VentaExpress Q4 2024 order-level export
- **Size:** 754 raw transaction records → 3,044 valid transactions after cleaning
- **Fields:** sale date, city, product (category / type / storage spec), unit price, quantity, order total, customer name, email, order ID

## 🛠️ Workbook Structure

The workbook is organized into five sheets, separating raw input from analysis — a standard practice for auditability:

| Sheet | Purpose |
|---|---|
| `Datos_originales` | Raw, untouched source export |
| `Datos_Limpios` | Cleaned dataset (standardized categories, corrected city names, parsed dates) |
| `Análisis` | Formula-driven KPI calculations |
| `Visualizaciones` | Pivot summaries + charts (revenue by category, city, and month) |
| `Informe_ejecutivo` | Executive summary: findings, methodology, limitations, and recommendations |

---

## 🔍 Data Quality Audit

The raw export contained several issues typical of unprocessed operational data. These were identified and documented as part of the audit trail preserved in the workbook:

- **Missing values:** 19 records with blank `Unit Price` / `Total Amount` fields
- **Character encoding errors:** garbled accented characters from a lost encoding conversion (e.g., `"M√©xico"` instead of `"México"`)
- **Inconsistent text formatting:** mixed casing and stray whitespace in city names (e.g., `"BOGOTá"`, `"Cali.  "`, `"Monterrey  "`), which would otherwise break category grouping
- **Heterogeneous date formats:** multiple date representations standardized into a single consistent format to enable month-over-month comparison
- **Duplicate records:** none found (0 duplicates)

Each issue and its resolution is documented on the `Informe_ejecutivo` sheet as part of the audit trail.

---

## 📊 Key Findings

| Metric | Value |
|---|---|
| Total Q4 revenue | $3,879,201.82 |
| Average revenue per transaction | $1,274.38 |
| Total valid transactions | 3,044 |
| Best-selling product (by units) | Laptop — 850 transactions |
| Top-performing city (by revenue) | Cali |
| Best-performing month | October |

**Average unit price by category**

| Category | Avg. Unit Price |
|---|---|
| Tablet | $1,477.75 |
| Phone | $1,333.03 |
| Headphones | $1,188.30 |
| Laptop | $1,129.80 |

---

## 📈 Visualizations

**Revenue by product category** — Laptops lead in unit volume, but Tablets generate the highest total revenue, indicating a stronger margin per unit:

![Revenue by category](./images/chart_revenue_by_category.png)

**Revenue by city** — Cali narrowly leads over Mexico City, while Tulum trails at under 10% of Cali's revenue — a clear outlier worth investigating:

![Revenue by city](./images/chart_revenue_by_city.png)

**Monthly revenue trend** — Sales are remarkably stable across the quarter (within ~1% of each other month to month), suggesting organic, non-seasonal demand rather than a holiday-driven spike:

![Monthly revenue trend](./images/chart_monthly_trend.png)

**KPI calculation sheet** — formulas built directly into the workbook (`Análisis` sheet), so results update automatically if the underlying data changes:

![Analysis sheet](./images/analysis_sheet_crop.png)

---

## 💡 Strategic Recommendations

**1. Product portfolio — balance volume and margin**
Laptops are the volume driver but Tablets are the profit driver. Recommend cross-selling bundles (Laptop + Tablet/Headphones) to capture margin from the existing traffic Laptops generate, and increasing marketing investment behind Tablets given their superior revenue-per-unit-shipped.

**2. Geographic strategy**
Cali is the strongest market and should get reinforced inventory and sales support to avoid stockouts. Tulum's underperformance (under 10% of Cali's revenue) warrants an immediate market audit — a shift to an e-commerce/ship-only model may reduce fixed costs if a physical presence isn't paying off.

**3. Inventory planning**
Because monthly demand is stable (within ~1% variance across the quarter), the company can negotiate consistent-volume purchasing with suppliers rather than reactive ordering, reducing both stockout and overstock risk.

**4. Data collection gap**
Recommend adding **age** and **gender** fields to the sales intake form to enable customer segmentation in future analyses.

---

## 🧰 Skills Demonstrated

- Data quality auditing and documentation
- Systematic data cleaning methodology (text normalization, encoding fixes, date standardization, missing-value handling)
- Formula-based KPI design (dynamic, non-hardcoded calculations)
- Data visualization and executive-level reporting
- Structuring a multi-sheet workbook for auditability and reuse

---

## 👀 How to View This Project

GitHub does not render Excel formulas, formatting, or embedded charts — it only shows a plain grid preview (or none, for large files). To review this project without downloading Excel:
