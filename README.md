# Forecast-Driven-Operational-Planning-in-a-Restaurant_Diploma_2026

All of the code for the thesis work is concentrated in one notebook — "Full Pipeline – Full Code Base". Two data files granted from a restaurant are also attached: Main Dataset – raw restaurant data (the main analytical dataset covering October 2023 – October 2025) and Restaurant Test Out Of Sample.xlsx (the out-of-sample evaluation set covering December 2025 – February 2026).

## Notebook Structure
 
- **Imports** — libraries and configuration.
- **Free Products / Refunds** — investigation and handling of refunds and zero-price entries.
- **General Orders Statistics** — descriptive statistics on orders on the raw export.
- **Categories Investigation** — review and merging of raw product categories.
- **Exploration of Anomalous Categories** — exclusion of non-menu categories (workshops, deposits, lunch).
- **Product Dataset Formation** — food product cleaning and SKU/name standardization.
- **Beverages Dataset Formation** — beverage cleaning and `Wariant` field parsing.
- **Food Statistics & Investigation** — per-segment analysis of food, general statistics.
- **Short term VS Long term products** — removal of products with <30 days of activity.
- **Beverages Stats** — per-segment analysis of beverages.
- **Key EDA** — key exploratory analysis.
- **Dataset creation** — daily product-level panel construction and missing-month interpolation.
- **Anomaly checks/sales** — detection and removal of banquet and internal-consumption checks.
- **Clustering** — feature engineering and selection for clustering.
- **Clustering with comparison** — comparison of K-Means, K-Means+PCA, K-Means cosine across k = 2…7.
- **Clusters Analysis** — profiling of the three resulting clusters:
  - **Cluster 0 — Absolutely chaotic** — low-frequency, beverage-dominated.
  - **Cluster 1 — Workhorses** — core menu, sells almost daily.
  - **Cluster 2 — Chaotic with Patterns** — intermittent with weekly/seasonal patterns.
- **Baselines for Clusters for Binary Predictions** — Lag-7, SKU mean, weekday mean baselines.
- **Chaotic Clusters Binary** — binary classification for Cluster 0.
- **Workhorses Continuous** — direct quantity regression for Cluster 1.
- **Chaotic with Patterns** — binary classification pipeline for Cluster 2.
- **Test Dataset cleansing** — preparation of the out-of-sample dataset.
- **Expected Quantity Comparison** — hybrid pipeline construction and comparison vs. global model.
- **Daily Prep + Procurement** — operational simulation: daily preparation and procurement across 1/4/7-day windows.
