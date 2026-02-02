# Project 01 — Claims Operations Dashboard (Tableau)

## Summary
Built a quick Claims Ops dashboard to track weekly inflow vs. closures and identify backlog aging risk.  
Focus: volume, cycle time, and backlog visibility for utility + medical claims-style workflows.

## Business Question
1) Are we closing claims as fast as we receive them each week?  
2) How much open work is sitting in each aging bucket (backlog risk)?

## Tools
- Tableau Public
- SQL-ready dataset structure (claim_id, received_date, closed_date, status, domain)
- Lightweight documentation + screenshots (V1)

## Key Metrics
- Weekly Volume: Received vs Closed
- Backlog Aging Buckets (Open)
- Cycle Time (typical range: 3–5 business days, up to 30 days depending on complexity)

## Screenshots (V1)

### Weekly Received vs Closed
![Weekly Received vs Closed](docs/tableau_weekly_received_vs_closed_v1.png)

### Backlog Aging Buckets (Open)
![Backlog Aging Buckets](docs/tableau_backlog_aging_open_v1.png)

## What I’d Improve in V2
- Add filters: Domain (utility vs medical), Status, Month/Week
- Add KPI tiles: Open Backlog, Avg Cycle Time, % Closed ≤ 5 days
- Add trendline + target line (capacity planning)


## Screenshots (V1)

### Weekly Received vs Closed
![Weekly Received vs Closed](docs/tableau_weekly_received_vs_closed_v1.png)
<img width="1318" height="647" alt="tableau_weekly_received_vs_closed_v1" src="https://github.com/user-attachments/assets/f2984f2d-db33-4b85-93f7-7a5f0a9a3d3a" />

### Backlog Aging Buckets (Open)
![Backlog Aging Buckets](docs/tableau_backlog_aging_open_v1.png)
<img width="1318" height="647" alt="tableau_backlog_aging_buckets_open_v1" src="https://github.com/user-attachments/assets/253faf25-99d6-4228-beb5-0de428abf8b4" />

