# Fraud & Anomaly Detection — PaySim Financial Transactions

## Overview
Designed a controls-testing framework to formalise anomaly detection 
work performed during audit engagements at KPMG. Applied four 
pre-defined anomaly types to 6.3 million synthetic financial 
transactions using SQL.

## Tools
- SQL (SQLite via DB Browser)
- Microsoft Excel
- Looker Studio

## Dataset
Kaggle PaySim Synthetic Financial Transactions — 6,362,620 rows

## Key Findings
1. 100% of confirmed fraud concentrated in TRANSFER and CASH_OUT 
   transaction types only
2. Large transaction outlier detection achieved 13.15% precision rate —
   102x the baseline fraud rate of 0.129%
3. Off-hours transactions (22:00–06:00) show a fraud rate 6.4x higher 
   than business hours, accounting for 32.5% of all confirmed fraud 
   despite representing only 7% of total volume
4. Near-duplicate payment pattern not detected in synthetic dataset — 
   recommended for testing against live transaction data

## Recommended Controls
- Automated hold on TRANSFER and CASH_OUT transactions exceeding 
  3 standard deviations above type mean
  ## Live Dashboard
[View interactive dashboard](https://datastudio.google.com/reporting/1ab80814-0646-4ace-ab5b-a82cd32dc1f0)
- Step-up authentication for transactions initiated between 22:00–06:00
- Near-duplicate payment detection rule for production deployment
