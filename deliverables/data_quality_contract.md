
# Retail Data Quality Contract

## 1. Purpose
Define measurable quality rules for reliable retail reporting.

## 2. Data Sources
- retail-orders-raw.csv
- retail-data-dictionary.csv

## 3. Quality Dimensions and Rules

### Completeness
- Order ID must not be missing.
- City must not be empty.
- Discount must be present and between 0 and 100.

### Uniqueness
- Duplicate order IDs must be investigated.
- Do not delete duplicates until the business owner confirms the correct rule.

### Validity
- Quantity must be greater than zero.
- Unit price must be positive.
- Customer segment must be Student, Fresher, or Professional.
- Category must match the documented allowed values.
- Payment status must be Paid or Pending.

### Consistency
- Customer segments and payment statuses should use consistent capitalization.
- Dates must use YYYY-MM-DD format.

### Freshness
- Check the latest order date against the agreed reporting schedule.
- Escalate when expected data is delayed.

## 4. Failure Severity

Critical:
- Missing order IDs
- Unresolved duplicate identifiers affecting reporting

Major:
- Invalid dates, quantities, prices, or discounts
- Invalid payment statuses

Minor:
- Inconsistent capitalization or formatting

## 5. Escalation Actions
- Critical: Pause affected reporting and notify the data owner.
- Major: Flag affected records and investigate.
- Minor: Record the issue and correct it according to approved rules.

## 6. Ownership
- Business owner: Retail Operations
- Quality monitoring: Data Analyst
- Escalation: Data Lead

## 7. Monitoring
Run the Python data-profiling notebook daily.
Export the quality report and rows requiring investigation.
Review failures before publishing business KPIs.

## 8. Current Status
The dataset contains detected quality issues.
Refer to data_quality_report.csv for measured results.
Resolve business-rule questions before treating KPIs as final.