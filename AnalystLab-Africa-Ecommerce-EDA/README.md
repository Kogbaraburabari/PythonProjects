# E-Commerce Transactions: Data Cleaning & EDA

**Program:** AnalystLab Africa Internship — Week 1-2
**Tools used:** Python (pandas, matplotlib)

## Objective
Clean a real-world UK online retail transactions dataset (541,909 rows) and conduct exploratory
data analysis to uncover revenue drivers, product performance, and customer behavior patterns.

## Data Cleaning

| Issue | Rows affected | Resolution |
|---|---|---|
| Missing `CustomerID` | 135,080 (25%) | Filled with `"Guest"` to preserve transaction data without falsely attaching an identity |
| Missing `Description` | 1,454 (0.3%) | Dropped — no reliable way to infer the value |
| Exact duplicate rows | 5,268 | Removed to avoid inflating sales totals |
| Inconsistent data types | — | `CustomerID` converted to text/ID form, `InvoiceDate` converted to proper datetime |
| Negative/zero quantities & prices | 9,725 / 1,058 | Kept, but flagged — cross-checking showed these correspond to legitimate cancellations (`InvoiceNo` starting with `"C"`) |

**Result:** 541,909 → 535,187 rows, 0 missing values remaining, 5,268 duplicates removed.

## Key EDA Findings

**Revenue is heavily UK-concentrated**
United Kingdom generated £8.16M — nearly 29× the next-highest country (Netherlands, £284K).

**Bulk sellers vs. repeat favorites differ**
"World War 2 Gliders Asstd Designs" leads in total quantity sold (53,751 units), while
"White Hanging Heart T-Light Holder" is the most frequently reordered item (2,302 separate orders).

**Clear seasonal peak**
Monthly revenue nearly tripled in November 2011 (£1.46M) versus a typical month (~£680K),
consistent with pre-holiday shopping.

**Most unit prices cluster at the low end**
The majority of items are priced under £5, with a long tail of higher-priced products — typical
of a high-volume, low-cost retail catalog.

**Guest checkouts are significant**
Unidentified "Guest" transactions collectively totaled £1.4M — more than any single identified customer.

## Recommendations
1. Prioritize the UK market, but nurture emerging ones — Netherlands, EIRE, and Germany are next-largest
2. Track sales volume and reorder loyalty as separate metrics when planning restocks
3. Plan inventory and marketing around the November peak ahead of time
4. Focus on driving order volume and repeat purchases, since most products are low-cost
5. Encourage account creation at checkout — Guest transactions are the largest "customer" segment by spend

## Files in this project
- [`ecommerce_cleaning_eda.ipynb`](./ecommerce_cleaning_eda.ipynb) — full cleaning, EDA, and visualization code
- [`ecommerce_Summary_Report.docx`](./ecommerce_Summary_Report.docx) — full written summary report
- **Cleaned dataset (full CSV):** [Google Drive](https://drive.google.com/drive/folders/1Tdui9H8Fk80qf97UW0ICNrdPfTWaqLsv?usp=drive_link) — too large for GitHub (47MB)

## Skills applied
`Python` `pandas` `matplotlib` `Data Cleaning` `Data Validation` `Exploratory Data Analysis` `Data Visualization` `Business Insight Reporting`
