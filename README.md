# Short-term-PV-energy-forecasting-

This project develops a data-driven short-term solar photovoltaic (PV) forecasting framework using panel-level and meteorological data.
It combines machine learning and deep learning approaches to predict PV generation and visualize results through an interactive Streamlit dashboard.

##Project Overview

The goal is to forecast short-term (1–24 hour ahead) PV energy generation to support smart energy planning and grid management in tropical regions.
The system integrates data preprocessing, feature engineering, model training, evaluation, and visualization into one workflow.

##Methodology

Data Preprocessing

Combined and cleaned 3-year meteorological and PV generation data (60+ rooftop sites).

Resampled to 5-minute intervals and merged panel-level PV output with weather variables.

Feature Engineering

Added temporal features (hour, day, month).

Generated lag features for short-term memory effects.

Computed rolling averages for trend smoothing.

Model Development

Baseline: Persistence model for benchmarking.

Machine Learning: Random Forest, XGBoost (optimized via RandomizedSearchCV).

Deep Learning: LSTM sequence model trained for temporal dependency capture.

Evaluation Metrics

Regression metrics: RMSE, MAE, R²

Event-based metrics: Precision, Recall, F1-score for low-generation detection.

Explainability (SHAP)

Used SHAP analysis on XGBoost to identify top influencing features (irradiance, lag power, temperature).

Visualization Dashboard (Streamlit)

Displays real-time forecasts, baselines, and meteorological correlations.

Includes hourly patterns, irradiance relationships, and short-term fluctuation analysis.
