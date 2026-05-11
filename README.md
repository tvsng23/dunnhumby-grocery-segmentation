# Household Segmentation for Grocery Retail
## Dunnhumby — The Complete Journey Dataset Analysis

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Machine Learning](https://img.shields.io/badge/ML-Clustering-green)
![Status](https://img.shields.io/badge/Status-Completed-success)

### 1. Project Overview
This project investigates the purchasing behavior of 2,500 loyalty-card households from a mid-sized U.S. grocery retailer over a two-year period. The goal is to identify distinct customer segments to move away from "one-size-fits-all" marketing towards data-driven, personalized strategies.

### 2. Key Insights (K=2 Behavioral Clusters)
Our analysis identified two primary segments that drive the retailer's economy:

* **Cluster 1: High-Value Core Loyalists (~36% of households)**
    * **Behavior:** Highly engaged "power users" with an average recency of 7 days and over 200 trips.
    * **Value:** Contributes an average of **$6,459** in total spend (4.5x more than Cluster 0).
    * **Trend:** Positive spending slope (+0.098), indicating growing loyalty and share of wallet.
    * **Strategy:** Priority for retention, early access to new products, and premium rewards.

* **Cluster 0: At-Risk Sporadic Shoppers (~64% of households)**
    * **Behavior:** Infrequent shoppers with an average recency of 36 days.
    * **Value:** Lower average spend ($1,405) and low engagement with marketing coupons.
    * **Trend:** Negative spending slope (-0.003), signaling a high risk of churn.
    * **Strategy:** Aggressive "win-back" campaigns, personalized discounts on frequently bought categories.

### 3. Methodology & Features
We engineered a **16-feature behavioral vector** categorized into 6 MECE groups: RFM, Basket, Category, Promotion, Temporal, and Store Loyalty.
* **Dimensionality Reduction:** PCA and t-SNE were used for visualization and to confirm non-linear cluster boundaries.
* **Algorithms Compared:** K-Means (Best Silhouette), Agglomerative Hierarchical (Ward), and DBSCAN (Outlier detection).
* **Top Discriminating Features:** Marketing engagement (`campaign_exposure_count`), shopping regularity (`active_weeks_ratio`), and total spend (`monetary`).

### 4. Repository Structure
```text
.
├── notebooks/          # Main analysis notebook (Data cleaning, EDA, Clustering)
├── output/             
│   ├── ...             # Processed feature matrices and cluster labels
│   ├── ...
│   └── figures/        # Visualizations (PCA, Radar charts, Correlation)    
├── reports/            # Final Analysis Report (PDF)
├── .gitignore          # Rules to exclude raw data and temporary files
├── requirements.txt    # Python dependencies
└── README.md           # Project documentation
