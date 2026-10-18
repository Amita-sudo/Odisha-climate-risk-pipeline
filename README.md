# Spatiotemporal Climate Risk & Precipitation Volatility Modeling Engine (1961–2025)

## 📌 Project Overview
This repository features an end-to-end data engineering and statistical pipeline designed to ingest, clean, and process 65 years of manual daily precipitation ground logs across all 29 administrative districts in Odisha, India. The system automates data-wrangling routines, engineers micro-climatic risk indices, and executes automated statistical trend loops to deliver a dashboard-ready data structure for Power BI business intelligence layers.

## 📁 Repository Blueprint
* 📄 `Odisha_Climate_Analysis.ipynb` — Master pipeline notebook handling batch file ingestion, text cleansing, and statistical trend modeling.
* 📊 `Odisha_Climate_Risk_Dashboard.pbix` — Production-grade Power BI desktop file containing interactive regional analysis matrices.
* 📄 `requirements.txt` — Package dependency configuration log ensuring complete code reproducibility.
* 🖼️ `dashboard_preview.png` — High-resolution layout capture of the functional dashboard view.

## 🛠️ Data Pipeline Architecture (ETL)
1. **Extraction & Ingestion**: Programmatic batch loading and vertical stacking of multiple generational CSV data blocks (1961–1990, 1991–2020, 2021–2025) bypassing local memory limitations.
2. **Data Cleansing & Normalization**: Automated string-matching routines resolving database typographical anomalies (e.g., standardizing `Rayagadaagada`, `Anugul`, `Jajapur`), case-sensitivity issues, and executing strict ISO-8601 datetime parsing.
3. **Feature Engineering**: Algorithmic deployment of the Simple Daily Intensity Index (SDII) to isolate changes in precipitation velocity (total rain volume divided by active rainy days >2.5mm).
4. **Statistical Modeling Engine**: Automated looped execution of non-parametric **Mann-Kendall Trend Tests** and **Sen's Slope Estimators** across all 29 districts concurrently to mathematically separate structural climate shifts from atmospheric noise.

## 📊 Analytical Insights & Power BI Layout
* **The Volatility Signature**: Major coastal districts like Ganjam demonstrate high multi-year variance ("No Trend" with an insignificant P-value of 0.249), proving climate change manifests as intense weather whiplash (extreme flood years followed immediately by droughts) rather than linear progressive shifts.
* **Interactive Design**: The dashboard transforms complex mathematical matrices into user-responsive visual grids using conditional color scaling (Crimson for drying zones, Deep Blue for wetting zones) to give policymakers instant regional risk clarity.

### 🖼️ Dashboard Preview
![Dashboard Layout](dashboard_preview.png)
