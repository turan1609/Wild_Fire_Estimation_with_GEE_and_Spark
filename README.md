# Wildfire Risk Prediction with Big Data

![Status](https://img.shields.io/badge/Status-Completed-success)
![Spark](https://img.shields.io/badge/Apache%20Spark-3.5.1-orange)
![Python](https://img.shields.io/badge/Python-3.10-blue)

**Wildfire Risk Prediction** is a comprehensive data mining project designed to predict forest fire risks in Turkey using satellite imagery and meteorological data.

## 🚀 Project Overview
This project processes over **400,000 geospatial data points** using a Big Data pipeline to determine wildfire probability. It integrates multi-source data from NASA and ESA to train machine learning models.

### 📊 Key Features
*   **Big Data Pipeline:** Built on **Apache Spark** to handle large-scale datasets efficiently.
*   **Multi-Source Fusion:** Integrates data from:
    *   🔥 **NASA FIRMS:** Historical fire locations (MODIS).
    *   🏔️ **NASA SRTM:** Topographical data (Elevation, Slope).
    *   ⛈️ **ECMWF ERA5:** Meteorological data (Temp, Wind, Humidity).
    *   🌿 **MODIS:** Vegetation indices (NDVI).
*   **Pseudo-Absence Sampling:** Synthetic negative sample generation to solve class imbalance.
*   **Model Comparison:** Benchmarking 4 different algorithms.

## 🏆 Results
After training on ~370,000 clean data points, **Random Forest** achieved the best performance.

| Model | Accuracy | F1 Score |
|-------|----------|----------|
| **Random Forest** | **88.6%** | **88.5%** |
| Gradient Boosted Trees | 87.9% | 87.8% |
| Linear SVM | 85.3% | 85.1% |
| Logistic Regression | 85.1% | 85.0% |

## 🛠️ Tech Stack
*   **Core:** Python, PySpark, Pandas
*   **Data Source:** Google Earth Engine (GEE) API
*   **Visualization:** Matplotlib, Seaborn
*   **Environment:** Linux (Ubuntu)

## 📂 Project Structure

Project/
├── data/
│ ├── raw/ # Raw CSVs from NASA
│ ├── processed/ # Parquet files (Chunks & Final)
├── notebooks/ # Jupyter Notebooks (Step-by-step)
├── src/ # Source scripts
└── README.md
