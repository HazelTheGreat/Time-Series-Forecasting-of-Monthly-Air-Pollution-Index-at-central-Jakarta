# Time Series Forecasting of Monthly Air Pollution Index at Central Jakarta

This repository contains data analysis, visualization, and time series forecasting models for the monthly Air Pollution Index (API/ISPU) in Central Jakarta.

## Overview

Air quality in urban environments fluctuates due to weather, industrial activity, and traffic patterns. This project analyzes historical monthly air pollution data from Central Jakarta to identify underlying trends and seasonality, building predictive models for future air quality forecasting.

* **Core Focus:** Time Series Analysis, Trend & Seasonality Decomposition, Forecasting
* **Target Location:** Central Jakarta, Indonesia

## Methodology

1. **Exploratory Data Analysis (EDA):** Analyzing historical pollution trends and inspecting data distributions.
2. **Stationarity & Preprocessing:** Checking stationarity using Augmented Dickey-Fuller (ADF) tests and applying differencing or transformations.
3. **Decomposition:** Separating time series data into trend, seasonal, and random components.
4. **Model Selection:** Fitting time series models such as ARIMA/SARIMA, Exponential Smoothing (Holt-Winters), or Prophet.
5. **Evaluation:** Assessing performance using evaluation metrics such as RMSE, MAE, and MAPE.

## Tech Stack

* **Programming Language:** R / Python
* **Key Packages & Libraries:**
  * `tidyverse`, `ggplot2` (Data manipulation & visualization)
  * `forecast`, `tseries`, `lubridate` / `statsmodels`, `pmdarima` (Time series modeling & diagnostic testing)

## Repository Structure

```text
Time-Series-Forecasting-of-Monthly-Air-Pollution-Index-at-central-Jakarta/
├── data/               # Raw and processed historical datasets
├── notebooks/          # Analysis scripts, RMarkdown (.Rmd) or Jupyter Notebooks
├── output/             # Exported visual plots and model evaluation results
└── README.md           # Documentation
