
# KPI Dictionary and Data Quality Contract

## Project Overview
This project analyzes a retail orders dataset to define business KPIs,
identify data-quality issues, and document quality rules for reliable reporting.

## Objectives
- Define measurable business KPIs.
- Profile retail data for completeness and validity.
- Detect duplicate identifiers and invalid values.
- Generate data-quality reports.
- Document quality thresholds and escalation procedures.

## Tools Used
- Python
- Pandas
- Jupyter Notebook in VS Code
- Microsoft Excel / ONLYOFFICE
- GitHub

## Project Structure
- data/: Raw retail dataset and data dictionary
- src/: Data-profiling notebook
- deliverables/: KPI dictionary, quality reports, and data-quality contract

## Dataset Columns
- order_id
- order_date
- customer_segment
- city
- category
- quantity
- unit_price
- discount_pct
- payment_status

## Data Quality Checks
The notebook checks missing values, duplicate order IDs,
date validity, quantity, price, discount, category, customer segment,
and payment status.

## Deliverables
- kpi_dictionary.xlsx
- data_quality_report.csv
- rows_requiring_investigation.csv
- data_quality_contract.md
- data_profiling.ipynb

## How to Run
1. Install Python and Pandas.
2. Open the project folder in VS Code.
3. Open src/data_profiling.ipynb.
4. Run the notebook cells in order.
5. Review the quality report and investigate flagged rows.

## Important Notes
The sample dataset contains data-quality issues.
Duplicate order IDs and invalid records require investigation.
Revenue figures are estimates based on available fields and valid data.
Business definitions should be confirmed before production use.