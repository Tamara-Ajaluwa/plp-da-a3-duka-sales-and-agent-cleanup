# Duka Sales & Agent Transactions Cleanup

Data cleaning, exploratory analysis, and performance reporting using Python and Pandas for **Duka Electronics Sales** and **Agent Transactions**.

## Repository Contents
- `duka_sales_and_agent_cleanup.ipynb` — Complete notebook containing data inspection, cleaning pipelines, analysis, and documented insights.
- `premium_online_nairobi_mombasa.csv` — Filtered export of Premium (`unit_price >= KES 28,000`) Online orders in Nairobi and Mombasa.
- `agent_transactions_cleaned.csv` — Cleaned agent transaction dataset with duplicates, invalid entries, extreme outliers, and unregistered agent IDs removed.

## Summary of Work

### Engagement 1: Duka Electronics Sales Analysis
- **Inspection & Feature Engineering:** Parsed `order_date` values and engineered `revenue`, `month`, `weekday`, `is_weekend`, and `price_band` (`Premium` vs. `Value`).
- **Branch & Product Rankings:** Ranked branches by total revenue and order volume, and contrasted top products by revenue (high-ticket electronics) versus units sold (high-volume accessories).
- **Temporal Trends & Filtering:** Compared weekday against weekend sales metrics, computed the percentage difference between the highest and lowest revenue months, and exported filtered Premium online orders.

### Engagement 2: Agent Transactions Cleanup & Analysis
- **Data Cleaning Pipeline:** Removed 12 exact duplicate records, standardized `txn_type` casing (`Deposit` and `Withdrawal`), and normalized mixed date formats into `YYYY-MM-DD`.
- **Anomaly & Integrity Handling:** Converted corrupted/missing amounts (`N/A`, `NaN`), removed extreme IQR outliers (`250,000` spikes), and filtered out orphan transactions tied to invalid agent ID `AG099`.
- **Merged Performance Metrics:** Joined cleaned transactions with `agents.csv` to evaluate activity across cities, transaction types, and top-performing agents.

## Data Privacy & Governance
All customer and agent records are handled under strict data minimization and access-control standards. Pseudonymized identifiers (`order_id`, `agent_id`) are used in place of personally identifiable information (PII) such as full names, phone numbers, or national IDs. Unsanitized raw financial logs are excluded from public repositories so that only schema-validated outputs and aggregated insights are shared.# plp-da-a3-duka-sales-and-agent-cleanup
