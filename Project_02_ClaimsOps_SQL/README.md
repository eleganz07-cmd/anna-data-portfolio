# Project 02 — Claims Ops KPI Query Pack (BigQuery + MySQL)

## Summary
This project provides a KPI query pack for claims operations reporting. It supports tracking throughput (received vs closed), backlog risk (aging buckets), cycle time, and SLA performance.

**Use case:** Utility + medical-claims-style workflows where teams monitor volume per week, backlog, and cycle time to maintain service levels.

## Business Questions
1. Are we closing claims as fast as we receive them each week?
2. What does our open backlog look like by aging bucket?
3. How does average cycle time vary by domain (utility vs medical)?
4. What percentage of closed claims meet an SLA of ≤ 5 days?

## Tools
- BigQuery (primary execution environment)
- MySQL 8+ (portable query equivalents)
- Tableau / Looker Studio friendly outputs

## Dataset
Source file: `data/claims_synthetic.csv`

Expected columns:
- `claim_id`
- `domain` (utility / medical)
- `received_date`
- `closed_date` (nullable for open claims)
- `status` (open / closed)
- `age_bucket` (e.g., 0-7, 8-14, 15-30, 31-60, 61-90, 90+)

## How to Run (BigQuery)
1. Create dataset: `claims_ops_portfolio`
2. Upload CSV as table: `claims`
3. Run queries from:
   - `sql/bigquery_kpis.sql`

## Deliverables
- BigQuery KPI queries: `sql/bigquery_kpis.sql`
- MySQL KPI queries: `sql/mysql_kpis.sql`
- Query result screenshots (V1):
  - `docs/bq_weekly_received_closed.png`
  - `docs/bq_backlog_aging.png`
  - `docs/bq_cycle_time_domain.png`
  - `docs/bq_sla_rate.png`

## Results (V1 Screenshots)

### Weekly Received vs Closed
![Weekly Received vs Closed](docs/bq_weekly_received_closed.png)

### Backlog Aging Buckets (Open)
![Backlog Aging Buckets](docs/bq_backlog_aging.png)

### Avg Cycle Time by Domain (Closed)
![Avg Cycle Time by Domain](docs/bq_cycle_time_domain.png)

### SLA Rate (≤ 5 days)
![SLA Rate](docs/bq_sla_rate.png)

## Next Improvements (V2)
- Add parameterized SLA thresholds (5/10/15 days)
- Add month-over-month trends + rolling averages
- Add QA checks for null dates, invalid statuses, and missing domains

