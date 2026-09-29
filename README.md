# Time Series Forecasting of Monthly Air Pollution Index in Central Jakarta

## Abstract

Air quality in urban areas is influenced by industrial activity, vehicular emissions, seasonal weather patterns, and macro-environmental shifts. This research presents a time series analysis and forecasting framework for the monthly Air Pollution Index (ISPU) in Central Jakarta. Utilizing historical monthly data from 2010 to 2021, the study evaluates long-term trends, seasonal variations, and structural anomalies, such as the sharp decline in pollutant levels during COVID-19 mobility restrictions. Multiple forecasting models—including ARIMA, SARIMA, Holt-Winters Exponential Smoothing, Facebook Prophet, and Neural Network Autoregression (NNAR)—were implemented in R and benchmarked using error metrics (RMSE, MAE, and MAPE) to identify the optimal model for air quality prediction.

---

## Authors & Contributors

* **Hazel Zaki Adityo** — NIM: 2702329576 — [@HazelTheGreat](https://github.com/HazelTheGreat)
* **Anthony** — NIM: 2702377612

---

## Project Objectives

1. **Trend & Seasonality Analysis:** Deconstruct historical ISPU time series data into trend, seasonal, and irregular components.
2. **Anomaly Detection:** Identify significant structural shifts in air pollution levels, particularly during the 2020–2021 COVID-19 pandemic lockdowns.
3. **Model Benchmarking:** Fit, compare, and validate multiple statistical, machine learning, and time series algorithms.
4. **Predictive Analytics:** Generate accurate future forecasts to assist environmental monitoring and public health planning.

---

## Dataset Overview

* **Data Source:** Monthly Air Pollution Index (ISPU / Indeks Standar Pencemar Udara) records for Central Jakarta.
* **Time Horizon:** 2010 – 2021 (Monthly aggregations).
* **Target Variable:** Monthly ISPU value (representing primary criteria pollutants such as PM10, PM2.5, SO2, CO, O3, and NO2).

---

## Methodology & Pipeline

1. **Exploratory Data Analysis (EDA) & Preprocessing**
   * Missing value imputation and time series object creation (`ts` class).
   * Visual inspection of trajectory, distribution, and volatility.
   * Anomaly detection to isolate COVID-19 pandemic outliers.

2. **Stationarity Testing & Transformation**
   * Augmented Dickey-Fuller (ADF) test and Kwiatkowski-Phillips-Schmidt-Shin (KPSS) test.
   * Log transformation and regular/seasonal differencing ($d$, $D$) to achieve stationarity.

3. **Time Series Decomposition**
   * Additive and multiplicative decomposition models.
   * Extraction of underlying long-term trends and repeating monthly seasonal patterns.

4. **Model Architecture & Training**
   * **ARIMA / SARIMA:** Autoregressive Integrated Moving Average with seasonal parameters $(p, d, q) \times (P, D, Q)_s$.
   * **Exponential Smoothing:** Holt-Winters additive and multiplicative models.
   * **Facebook Prophet:** Additive model incorporating trend changepoints and seasonality.
   * **Neural Network Autoregression (NNAR):** Feedforward neural network with lagged values as inputs.

5. **Evaluation & Model Selection**
   * Train-test split (historical training set vs. out-of-sample testing set).
   * Accuracy metrics comparison: Root Mean Squared Error (RMSE), Mean Absolute Error (MAE), and Mean Absolute Percentage Error (MAPE).

---

## Key Research Findings

* **Seasonality:** Strong yearly seasonal cycles corresponding to dry and rainy seasons in Jakarta, with pollution levels peaking during dry months due to lower atmospheric dispersion.
* **Structural Break (COVID-19 Impact):** A marked reduction in average ISPU values occurred between 2020 and 2021, directly correlated with Large-Scale Social Restrictions (PSBB) and reduced vehicular traffic.
* **Model Performance:** Comparative evaluation demonstrated that models capturing both seasonal components and structural shifts (e.g., SARIMA / NNAR) achieved the lowest RMSE for out-of-sample forecasting.

---

## Tech Stack & Dependencies

* **Language:** R
* **Data Manipulation & Visualization:** `tidyverse`, `ggplot2`, `dplyr`, `lubridate`
* **Time Series & Forecasting:** `forecast`, `tseries`, `prophet`, `nnet`
* **Evaluation:** `Metrics`

---

## Repository Structure

```text
Time-Series-Forecasting-of-Monthly-Air-Pollution-Index-at-central-Jakarta/
├── data/               # Raw and cleaned monthly ISPU datasets (2010–2021)
├── scripts/            # R scripts for preprocessing, decomposition, and modeling
├── reports/            # RMarkdown (.Rmd), compiled HTML/PDF reports, and paper draft
├── outputs/            # Saved plots, visual diagnostics, and forecast tables
└── README.md           # Main project documentation
