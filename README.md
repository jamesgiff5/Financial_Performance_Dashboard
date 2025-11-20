# 📊 Financial Performance and Forecast Accuracy Dashboard

This project analyzes revenue trends, cost behavior, margin movement, forecast accuracy, cash timing, and expense patterns for a synthetic small sized company operating from January 2023 through June 2025.

The Power BI model connects GL actuals, budget and forecast data, AR, AP, and employee expense claims into a single view that helps explain how different parts of the business contribute to overall performance.

---

## ⚠️ Important Note About the Synthetic Data

The raw dataset was generated independently across several tables, so the financial figures do not reconcile the way real accounting systems do.  
Values that should normally match across GL, budget, forecast, AR, AP, and expense data do not align because each table was produced with its own generation logic.

This is a common limitation with synthetic datasets and means the dollar amounts should not be interpreted as precise financials.

The purpose of this project is to demonstrate:
- Clear financial modeling and dashboard structure  
- Strong analytical reasoning  
- Meaningful business insights drawn from patterns and relationships  
- Clean data modeling, DAX, and visualization techniques  

The focus is on analytical workflow and interpretation, not on the literal accuracy of the simulated numbers.

---

## 📈 Executive Summary

The dashboards show a company with steady revenue growth, stable margins, and a predictable cost structure across its six divisions. Even though the synthetic dataset produces uniform dollar amounts, the trends behave realistically, making it easy to see how different divisions contribute to growth, how margin holds across periods, and where operating costs put pressure on profit.

Supporting pages reveal the operational dynamics behind the numbers. Forecast variance patterns show where planning discipline is weaker. Cash timing and working capital show how effectively the company converts sales into cash. AR, AP, and expense claim views surface process speed, overdue behavior, and approval discipline. Together, the dashboards demonstrate how finance leaders interpret performance, identify issues, and guide decisions.

---

## 🧮 Modeling and Measures

All DAX measures were centralized in a single _Measures table and built with Tabular Editor 2 for organization, formatting consistency, and faster development.  
Display folders reflect a clean enterprise style layout for reporting and maintenance.

Full technical documentation is available here:  
📘 `/docs/Data_Model_Enrichment_Process.md`

---

# Analysis and Insights

## 1. Revenue, Margin, and Division Mix

Even though the absolute values are synthetic, the structure reveals realistic patterns:
- Revenue grows steadily with seasonal movement and volume increases expected in a multi channel business.  
- Margins remain strong and relatively stable, showing that operating costs scale predictably with revenue.  
- Divisions follow a logical hierarchy: Wholesale and Retail at the top, then a gradual step down across the remaining four divisions.

**Insight:**  
In a real company, leaders would look at which divisions drive volume, which carry heavier cost structures, and which contribute disproportionately to profit. Even though the values here are synthetic, the workflow mirrors how CFOs evaluate divisional performance, margin stability, and revenue mix.

---

## 2. Cost Mix by Division

The cost mix view shows realistic directional patterns, even if totals are flattened by synthetic generation:
- Wholesale carries a higher COGS share, consistent with resale and distribution activity.  
- Retail and E Commerce lean on Payroll and OpEx, matching labor and marketing driven operations.  
- Product Development and Private Label show lower COGS but higher overhead, aligned with design or merchandising roles.

**Insight:**  
The page demonstrates how cost mix analysis highlights where efficiency programs should focus. In a real business, this would guide decisions around pricing, staffing, sourcing, and budget priorities.

---

## 3. Forecast Accuracy and Variance Review

Budget and forecast data was generated separately from GL actuals, so totals do not reconcile.  
Even so, variance patterns still provide meaningful signals:
- Some quarters show significant variance for certain divisions.  
- Others show closer alignment between planned and actual outcomes.  
- You can see when expectations overshoot or undershoot, and by how much.

**Insight:**  
This page demonstrates the workflow of evaluating forecast quality and understanding whether planning assumptions were directionally accurate.

---

## 4. Profitability and Cash Efficiency

The numbers themselves are synthetic, but the relationships behave realistically:
- Cash coming in faster than it goes out reflects strong conversion timing.  
- The profit bridge illustrates how revenue, COGS, and OpEx interact to produce operating profit.  
- Division level profit views show relative contribution, even if magnitudes are equalized.

**Insight:**  
This mirrors how finance teams evaluate margin structure, cash timing, and the levers that most influence profitability.

---

## 5. Working Capital, AR, AP, Customers, Vendors

The generator only produced five customers and five vendors, all with similar amounts, so segmentation is limited. Still, the structure functions correctly:
- AR and AP aging works as expected.  
- Days to receive and days to pay follow realistic patterns.  
- Overdue invoices cluster in the final quarter due to how the data was produced.

**Insight:**  
This page demonstrates how to analyze working capital cycles and cash timing, even when synthetic data does not allow for deep customer or vendor analysis.

---

## 6. Employee Expense Claims

Expense category totals and average claim amounts are uniform, but the operational metrics still provide usable signals:
- Reimbursement takes about two weeks, which is reasonable.  
- A rejection rate of about 27 percent is unusually high and would raise questions in a real company.  
- Outstanding claims remain small and well controlled.

**Insight:**  
This page shows how a dashboard helps evaluate employee spend behavior, compliance issues, and process efficiency, even when synthetic inputs flatten category level differences.

---

## Conclusion and Next Steps

This dashboard surfaces the core financial story of the company and highlights where leadership should focus next. The patterns in margin stability, cost mix, cash timing, forecast variance, and expense behavior show opportunities to tighten planning, streamline operations, and improve control processes.

If this were a real organization, the next logical steps would include building driver based forecasting models, refining reimbursement rules, monitoring customer and vendor payment patterns more closely, and expanding divisional analysis with more granular data. With richer operational inputs, this framework could evolve into a full performance management system that supports quarterly planning, variance reviews, and ongoing decision support.

---

## 📚 Data Source

This project uses a synthetic multi-table finance dataset provided by **ExcelX**.  
Dataset link: [excelx.com practice finance data](https://excelx.com/practice-data/finance-accounting/?utm_source=chatgpt.com)
