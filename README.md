# 🚕 NYC Taxi Demand & Fare Analysis

A large-scale data analysis project using PySpark and Machine Learning to uncover fare pricing factors and demand patterns across New York City's taxi network, built on 7+ million trip records.

---

## 📖 Overview

This project investigates two key research questions about NYC taxi behavior using Random Forest models, time-series analysis, and geospatial visualization — providing actionable insights for urban mobility planning and rideshare comparison.

---

## ❓ Research Questions

**RQ1: What are the main factors that affect taxi fare amounts in NYC?**
Modeled fare amounts using a Random Forest Regressor across four time buckets (Weekday/Weekend × Business/Off-Hours). Trip distance emerged as the dominant driver, followed by tolls, airport fees, and congestion surcharges.

**RQ2: How does taxi demand vary by hour of day and ZIP code in NYC?**
Analyzed temporal and spatial demand patterns using heatmaps, multi-line trend plots, and an interactive Folium map highlighting Manhattan's top 5 demand hotspots.

---

## 🔍 Techniques Used

| Task | Method |
|---|---|
| Fare Prediction | Random Forest Regressor (PySpark MLlib) |
| Demand Forecasting | Random Forest Regressor (PySpark MLlib) |
| Feature Engineering | Time bucketing, hour/day extraction |
| Spatial Analysis | ZIP code aggregation + Folium map |
| Visualization | Seaborn heatmaps, line plots, scatter plots |

---

## 📊 Dataset

- **Source:** NYC TLC Yellow Taxi Trip Records (Parquet format)
- **Size:** 7+ million trip records
- **Key Features:** `fare_amount`, `trip_distance`, `passenger_count`, `payment_type`, `tolls_amount`, `congestion_surcharge`, `airport_fee`, `tpep_pickup_datetime`

> ⚠️ Dataset is not included in this repo due to size. Download from [NYC TLC Trip Record Data](https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page).

---

## 📁 Project Structure

```
nyc-taxi-demand-fare-analysis/
│
├── nyc_taxi_analysis.ipynb    # Main analysis notebook
├── requirements.txt           # Python dependencies
└── README.md
```

---

## 🚀 Key Steps

1. **Data Loading** — Load cleaned Parquet dataset via PySpark
2. **Data Cleaning** — Handle nulls, impute missing values with column means
3. **Feature Engineering** — Extract pickup hour, day of week, and time buckets
4. **RQ1 Modeling** — Train Random Forest per time bucket, evaluate R² and RMSE
5. **RQ2 Modeling** — Aggregate demand by hour/ZIP, train and validate model
6. **Visualization** — Heatmaps, residual plots, actual vs. predicted scatter plots
7. **Geospatial Mapping** — Interactive Folium map of top Manhattan demand zones

---

## 🛠️ Libraries

- `pyspark` — Distributed data processing and ML
- `pandas`, `numpy` — Data manipulation
- `matplotlib`, `seaborn` — Static visualizations
- `folium` — Interactive geospatial map
- `scikit-learn` — Supporting ML utilities

---

## 👤 Author

**tompopo777**  
[GitHub Profile](https://github.com/tompopo777)
