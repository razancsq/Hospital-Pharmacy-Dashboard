# Hospital Pharmacy Dashboard

##Prototype Design Summary

Before starting the Power BI implementation, a complete set of dashboard prototypes was designed to organize the project structure and identify the most important information that hospital management needs for daily decision-making.

The design starts with an Executive Summary, providing a quick overview of the pharmacy through key indicators such as total medications, total stock items, low stock alerts, and items approaching expiration. This allows users to understand the current pharmacy status immediately.

The second dashboard focuses on Inventory Status and Warehouse Distribution, because understanding how inventory is distributed across different warehouses and medication categories is essential for stock monitoring and resource planning.

The third prototype introduces Search and Filter, making it easy to locate medications using different search options such as item description, scientific name, internal code, NUPCO code, and category. This helps users quickly access the information they need.

The fourth dashboard highlights Critical Inventory Items, since low-stock and reorder alerts are among the highest priorities in hospital pharmacy management. Presenting these items clearly helps support faster decision-making and reduces the risk of shortages.

The fifth prototype presents High Consumption Analysis, allowing users to identify the most frequently consumed medications, monitor monthly consumption trends, and compare stock coverage with expected demand.

The sixth dashboard is dedicated to Expiring Soon Items, making it easier to monitor medications based on their remaining shelf life and identify products that require immediate attention before expiration.

To provide more detailed analysis, separate dashboards were designed for important medication groups. One dashboard focuses on Ophthalmic Supplies, while another focuses on Antibiotics, allowing category-specific monitoring instead of viewing all medications in a single report.

Another important consideration was identifying Slow-Moving Medications. This dashboard helps detect excess inventory, estimate months of supply, and identify medications that may require stock optimization.

A dedicated dashboard was also created for the Tablets Category, providing a focused view of tablet inventory, stock levels, and consumption trends.

Finally, two supporting dashboards complete the prototype. The Data Flow Architecture illustrates how data moves from multiple Excel sources through Power Query into Power BI, while the KPIs & Performance Metrics dashboard summarizes the overall pharmacy performance using key indicators, alerts, inventory distribution, and system status.

Together, these twelve prototypes provide a clear roadmap for building a practical, organized, and user-friendly Hospital Pharmacy Dashboard that supports inventory monitoring, improves operational visibility, and helps hospital staff make timely and informed decisions.

## Data Cleaning

Before building the dashboard, all four Excel source files were cleaned and standardized to improve data quality and Power BI performance.

The following preprocessing steps were performed:

- Removed duplicate records and empty rows within the data tables.
- Deleted unnecessary empty columns.
- Removed extra blank rows outside the data blocks to reduce file size.
  - In the main pharmacy store file, approximately 8,892 empty cells (228 columns × 39 rows) were removed, reducing the file size from **27 MB** to **4 MB**.
- Trimmed unnecessary whitespace from text fields.
- Standardized date formats across all datasets.
- Replaced missing quantity values with **0** where appropriate.
- Validated data types (numeric, text, and date).
- Renamed selected columns to English for consistency and to avoid language conflicts.

*Note*: The expired items dataset contained four records with an expiry date of `31/12/9999`. These values were temporarily replaced with the date from the previous row for prototype development, but they should be verified because incorrect expiry dates represent a potential patient safety risk.