# Retail Inventory Analytics and Forecasting

Analyzing inventory performance, pricing strategy, demand patterns, and future demand to support smarter retail decisions

## Business Problem

Leadership has flagged recurring **stockouts** (lost sales) on fast-moving items alongside **overstock** (dead capital) on slow movers, and wants a data-driven view of demand, inventory health, and pricing sensitivity to guide replenishment decisions. The analysis focuses on:

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
| Analytical queries | Python (pandas, numpy) |
| Dashboarding | Power BI (DAX) |

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
│   │   └── retail_store_inventory.csv         
│   └── processed/
│       └── retail_inventory_enriched.csv     
│
├── notebooks/                                  
│   ├── phase1_cleaning_feature_engineering.py         
│   └── phase3_statistical_testing.py
|
├── sql/
|   └── retail_inventory_analysis.sql         
│
├── dashboards/
│   └── retail_inventory_dashboard.pbix          
│
├── reports/                                    
│   ├── business_impact_summary.md              
│   └── executive_summary.md              
│
└── docs/
    └── data_dictionary.md                     
```
