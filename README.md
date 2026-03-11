# Financial Health & KPI Interactive Dashboard

## Project Overview
This repository contains a comprehensive Power BI dashboard designed for **The Finance Group**. The solution provides a monthly-level analysis of the company's financial health, integrating P&L, Cash Flow, and Operational metrics into a single interactive interface.



[Image of financial dashboard overview]


## Key Features
* **Executive KPIs:** Real-time tracking of Revenue, Gross Margin %, EBITDA %, and Net Cash.
* **Budget Variance Analysis:** Visual comparison of Actual vs. Budgeted revenue with automated color-coding (Red/Green).
* **Cash Flow Management:** A waterfall visual detailing the transition from Inflows to Outflows.
* **Liquidity Tracking:** Receivables aging analysis categorized into 30/60/90+ day buckets.
* **Full Interactivity:** Dynamic filtering by Region, Product Category, and Date Range with drill-down capabilities.

## Technical Logic & DAX
The dashboard utilizes a **Star Schema** data model for optimal performance. Key DAX measures include:

* **Net Cash:** Calculated by aggregating unpivoted cash attributes.
* **EBITDA %:** Margin analysis using safe division logic.
* **Time Intelligence:** Custom Calendar table support for chronological sorting and period comparisons.



## Data Transformation (Power Query)
1.  **Unpivoting:** Cash Inflow/Outflow columns were unpivoted to enable Waterfall chart breakdown.
2.  **Conditional Columns:** Created aging brackets (0-30, 31-60, 61-90, 90+) from raw day counts.
3.  **Data Typing:** Ensured all financial metrics are set to Fixed Decimal for currency accuracy.

## Assumptions
* Data spans from January 2023 to December 2024.
* "Product" vs "Service" categorization is based on the prefix of the item name.
* Budget figures are static monthly targets.

## How to Use
1.  Download the `Financial_Health_Dashboard.pbix` file from the `Dashboard/` folder.
2.  Open in **Power BI Desktop**.
3.  If prompted, update the data source path to point to the CSV file in the `Data/` folder.

---
**Author:** Data Analyst @ The Finance Group  
**Tooling:** Power BI, Power Query, DAX
