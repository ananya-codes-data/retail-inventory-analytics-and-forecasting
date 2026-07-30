# Retail Inventory Analytics and Forecasting

Analyzing inventory performance, pricing strategy, demand patterns, and future demand to support smarter retail decisions

## Business Problem

Retailers lose money two ways: **stockouts** (lost sales) and **overstock** (dead capital). Both are often invisible until it's too late. This project uses daily store-product-level data to surface:

- Where stock is running low or products are chronically out of stock
- Where inventory is sitting idle (dead stock)
- Whether pricing is competitive against competitors
- Whether promotions actually drive incremental sales, or just overlap with naturally high-demand periods

## Dataset

This project uses the [Retail Store Inventory Forecasting Dataset](https://www.kaggle.com/datasets/anirudhchauhan/retail-store-inventory-forecasting-dataset) — synthetic daily records (~73,000 rows) spanning multiple stores, product categories, and regions.

## What This Project Answers

**Inventory health** — Which products are approaching stockout, which are sitting as dead stock, and what would ABC-tiering by revenue contribution reveal about where inventory discipline is strongest and weakest.

**Demand & forecast reliability** — Where the dataset's own demand forecasts are trustworthy versus where they systematically miss, and what that means for relying on automated reordering.

**Pricing competitiveness** — Whether being priced above or below competitors measurably moves units sold, and which categories are most responsive to discounting.

**Seasonal & promotional effects** — Whether running a promotion during an already-strong season adds real incremental lift or is largely redundant spend

## Tech Stack

| Layer | Tool |
|---|---|
| Data cleaning & feature engineering | Python (pandas, NumPy) |
| Statistical testing | Python (scipy) |
| Analytical queries | SQL Server |
| Dashboarding | Power BI (DAX) |
| Forecasting extension | scikit-learn, XGBoost/LightGBM, PyTorch/Keras (LSTM, TFT) |

## Repository Structure

```text
retail-inventory-analytics-and-forecasting/
│
├── README.md
├── LICENSE
├── .gitignore
├── requirements.txt
│
├── data/
│   ├── raw/
│   │   └── retail_store_inventory.csv          # raw Kaggle download (not committed if large)
│   └── processed/
│       └── retail_inventory_enriched.csv       # Phase 1 output — feeds SQL, Power BI, and models
│
├── notebooks/                                  # Python work — cleaning, EDA, stats, modeling
│   ├── phase1_cleaning_feature_engineering.py  # ✅ built
│   ├── phase3_statistical_testing.py           # significance tests (Q18) — pending
│   └── phase5_forecasting_models.ipynb         # ARIMA/XGBoost/LSTM comparison — pending
│
├── sql/                                        # SQL Server query bank
│   └── retail_inventory_analysis.sql           # ✅ built — Q1–17, Q22–24
│
├── dashboards/
│   └── retail_inventory_dashboard.pbix          # Power BI file — pending
│
├── reports/                                    # Written reasoning — not code, not queries
│   ├── business_impact_summary.md              # Q22–24 translated into ₹ recommendations
│   ├── causal_reasoning_notes.md               # Q20 — correlation vs causation discussion
│   ├── experiment_design.md                    # Q21 — hypothetical A/B test design
│   ├── scale_architecture_notes.md             # Q25 — design note for scaling to 500M rows
│   └── executive_summary.md                    # Q26 — one-pager, the artifact reviewers read first
│
├── models/                                     # Phase 5 forecasting extension
│   ├── xgboost_forecast.py
│   ├── lstm_forecast.py
│   └── model_comparison_results.csv
│
└── docs/
    └── data_dictionary.md                      # raw + engineered columns reference (just drafted)
```
