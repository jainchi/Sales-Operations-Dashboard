Built a 6-page Power BI dashboard analyzing sales, budget, forecast, inventory, production, and logistics performance from a 7-fact-table dataset (Sales, Budget, Forecast, Production, Shipment, Returns, Inventory) spanning 2023–2026.

Key work:

Designed a star schema connecting 7 fact tables to shared dimensions (Product, Customer, Region, Salesperson, Warehouse, Plant, Transport), including a custom Year-Month bridge table to resolve relationship mismatches between Budget/Forecast (Year+MonthNo grain) and the Date dimension.

Diagnosed and fixed a relationship fan-out bug causing Budget figures to be double-counted by region.

Identified and resolved ambiguous relationship paths (two active routes into a fact table for the same filter), consolidating to a single clean lineage.

Built 30+ DAX measures including dynamic Top-N rankings (RANKX + SWITCH + parameter tables), time-intelligence-scoped comparisons (aligning partial-year Actuals against full-year Budget/Forecast), and a corrected Capacity Utilization measure using AVERAGEX instead of SUM to avoid comparing a static capacity limit against a time-series total.

Verified suspicious or "broken-looking" metrics (Forecast Accuracy, On-Time Delivery, Inventory reconciliation) against raw source data before trusting them — distinguishing genuine data-quality characteristics of the dataset from actual modeling bugs.
Delivered 6 pages: Executive Overview, Sales, Budget vs Actual, Forecast, Inventory, and Operations — each with KPI cards, comparative visuals, and a Key Insights summary grounded in verified numbers.
