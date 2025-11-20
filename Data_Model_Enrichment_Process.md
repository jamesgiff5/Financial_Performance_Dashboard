# 🧮 Measure Management and Modeling Workflow

To keep the data model clean and scalable, all DAX measures were centralized in a dedicated table named _Measures and managed through Tabular Editor 2, following standard enterprise BI modeling practices.

## Why This Matters
Centralizing all measures in one place keeps the model cleaner, faster, easier to reuse, and much simpler for anyone else to understand or maintain.

---

# 1️⃣ Data Model Architecture

The Power BI model follows a clean star schema, ensuring efficient calculation performance and intuitive navigation.

### Fact Tables
- General Ledger  
- Budget  
- Forecast  
- Accounts Receivable  
- Accounts Payable  
- Expense Claims  

### Dimension Tables
- Date  
- Divisions  
- Accounts   
- Categories  

A dedicated _Measures table stores all business KPIs and calculated metrics.  

### 📐 Data Model Diagram

Below is the full semantic model used in this project, showing all fact tables, dimensions, and relationships:

![Financial Data Model](./assets/Financial_Dashboard_Data_Model.jpeg)

---

# 2️⃣ Workflow Summary

## 2.1 Centralized Measures Table
A blank table called _Measures was created exclusively to store all KPIs.  
This keeps the semantic model organized and aligned with best practices for enterprise Power BI development.

---

## 2.2 Development in Tabular Editor 2
The model was opened in Tabular Editor 2 through External Tools, enabling:
- direct metadata editing  
- fast measure creation  
- C sharp scripting support  
- clean, bulk folder assignment  

Tabular Editor allows tasks that take hours in Power BI to be completed in minutes.

---

## 2.3 Batch Creation of Measures (C# Script)
A custom Tabular Editor C sharp script was used to batch-create all project measures from a prepared list of DAX expressions.

The script handled:
- creating each measure object  
- assigning names and DAX formulas  
- applying numeric formatting  
- storing them inside the _Measures table  

This removed repetitive manual entry and ensured consistent formatting across all KPIs.

---

## 2.4 Organized Display Folders
After creation, measures were grouped into clean display folders for a professional model layout:

- Accounts Payable  
- Accounts Receivable  
- Budget and Forecast  
- Cash Flow  
- Cost Mix  
- Expense Claims  
- GL and OpEx  
- KPI (Display)  
- Profit Bridge  
- Profitability  

This structure makes the Fields pane easy for any analyst or developer to navigate.

---

## 2.5 Power Query Transformations Using the M Language

Several parts of the synthetic dataset contained unrealistic artifacts, such as very old AR, AP, and expense claim records that were still marked as unpaid.  
To correct this and produce more realistic financial behavior, the Advanced Editor in Power Query was used to apply targeted M-language transformations.

These adjustments included:
- marking very old AR invoices as Received  
- marking very old AP invoices as Paid  
- normalizing outdated employee expense claims  
- applying consistent date and status logic across tables  

Using the M language allowed these fixes to be applied in bulk, ensuring consistent logic across fact tables and producing more realistic DSO, DPO, and claim-settlement timelines.

---

## 2.6 Synced Back to Power BI
All changes were saved, instantly updating the semantic model inside Power BI Desktop.

---

# 3️⃣ Advanced Modeling Techniques Used

To ensure the model scales and performs efficiently, the following modeling techniques were used:

- marked Date Table with full calendar hierarchy  
- star schema design for fact and dimension separation  
- filter direction control and relationship tuning  
- use of KEEPFILTERS, REMOVEFILTERS, and USERELATIONSHIP  
- dedicated dimension for Divisions (renamed from synthetic raw departments)  
- reusable KPI measures designed for multiple visuals  
- drill-aware dynamic titles for time based drill downs  

These patterns match how BI teams build models for executive dashboards.

---

# 4️⃣ Key DAX Patterns Used

The semantic model includes a range of reusable DAX patterns:

- Time Intelligence such as YTD, QTD, MTD, and prior period comparisons  
- Variance Analysis: absolute, percent, and directional variance  
- Forecast Accuracy and planning bias measures  
- Working Capital Metrics such as DSO, DPO, and invoice aging logic  
- Dynamic titles reflecting drill depth  
- Status-based filters for claims, AR, and AP  
- Cash flow inflow and outflow aggregation  

These patterns form the backbone of most enterprise FP and A analytical models.

---

# ✔️ Outcome

Using Tabular Editor 2 and structured M-language transformations created a fast, standardized, and maintainable workflow for managing all DAX measures and data preparation steps.

This process produced:
- a clean and well-organized semantic model  
- dozens of consistently formatted, auditable measures  
- a professional folder structure  
- realistic working capital behavior  
- a scalable model ready for real business reporting  
