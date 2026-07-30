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
├── data/                  # Raw and cleaned datasets (raw data not committed if large/licensed)
├── notebooks/             # Python cleaning, feature engineering, EDA, statistical testing
├── sql/                   # Query bank organized by theme and difficulty level
├── dashboards/            # Power BI file(s)
├── reports/               # Written reasoning: causal discussion, business impact summary, executive summary
├── models/                # Forecasting models (Phase 5 extension)
└── README.md
```
