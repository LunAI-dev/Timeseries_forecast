# 📈 Timeseries Forecast

A hybrid time series forecasting pipeline for **revenue and operational KPIs**, designed for realistic business scenarios where interpretability and robustness matter more than novelty.

This experiment is part of my [Data Science Lab](https://github.com/LunAI-dev/data-science-lab); a playground of applied ML and DL experiments where chaos meets logic.

---

## ⚗️ Project Overview

In most business environments, forecasting needs are pragmatic:  
- Short-term accuracy for operations and staffing  
- Medium/long-term stability for budgeting and planning  

This project explores a **hybrid approach** that combines:  
- **ARIMA** for local autoregressive structure  
- **Prophet** for capturing trend and seasonality  
- **XGBoost** for nonlinear relationships and feature-driven adjustments  

By blending these perspectives, the pipeline achieves balanced performance even under noisy or incomplete data conditions.

---

## 🧰 Tech Stack

| Component | Description |
|------------|-------------|
| **pandas / numpy** | Data manipulation, time series preprocessing |
| **statsmodels (ARIMA)** | Classical autoregressive modeling |
| **Prophet (Meta)** | Seasonality and trend decomposition |
| **XGBoost** | Feature-based nonlinear regression |
| **matplotlib / seaborn** | Visual exploration and diagnostics |
| **scikit-learn** | Preprocessing, pipelines, and evaluation metrics |

---

## 🧩 Workflow

1. **Synthetic Data Simulation**  
   Generates realistic revenue and operational KPI series with seasonal patterns, promotions, and random noise.  
   Used as a proxy for real-world commercial data with missingness and irregularities.

2. **Exploratory Visualization**  
   Quick look at trends, seasonality, and volatility to understand baseline behavior.

3. **Modeling Stage**  
   - **ARIMA** for short-term signal extraction  
   - **Prophet** for interpretable trend/seasonality capture  
   - **XGBoost** leveraging lag features, rolling stats, and calendar effects  

4. **Hybrid Ensemble**  
   A simple mean blending of the three model outputs.  
   This ensemble often outperforms any single method in both RMSE and robustness.

5. **Diagnostics & Comparison**  
   Evaluates RMSE, MAE, and residual structure.  
   Visual plots show each model’s strengths and where blending adds value.
