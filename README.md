# H&M Revenue Intelligence
H&M Fashion Analytics: Revenue Forecasting & Explainable AI

An end-to-end Data Science project that transforms raw fashion transaction data into actionable revenue forecasts using statistical modeling, deep learning, and explainable AI.

Project Overview

This project explores revenue forecasting in the fashion retail industry using the H&M Personalized Fashion Recommendations dataset.

The objective is to develop a time-series forecasting system capable of predicting future revenue while identifying the key factors influencing revenue patterns.

Starting with approximately 31 million raw transaction records, the project applies statistical sampling, extensive data preprocessing, feature engineering, and comparative model evaluation to build a forecasting pipeline.

Four forecasting approaches are implemented and evaluated:

* SARIMA
* Facebook Prophet
* Long Short-Term Memory (LSTM)
* Seasonal Naive

SHAP analysis is additionally used to investigate the importance of engineered features and understand the factors associated with revenue variations.

Key Highlights

* Reduced approximately 31 million transaction records to a representative 10,000-row sample.
* Applied stratified sampling to preserve temporal, customer, and product diversity.
* Performed comprehensive data cleaning and preprocessing.
* Engineered 54 features from daily transaction aggregates.
* Implemented rolling statistics, lag features, cyclic encoding, and STL decomposition.
* Compared four different time-series forecasting approaches.
* Applied SHAP-based explainability to identify influential revenue predictors.
* Generated a 30-day forward revenue forecast.

Tech Stack

Programming Language

* Python

Data Analysis & Preprocessing

* Pandas
* NumPy

Statistical Modeling

* Statsmodels
* SARIMA
* Prophet

Deep Learning

* TensorFlow / Keras
* LSTM

Machine Learning & Explainability

* XGBoost
* SHAP

Visualization

* Matplotlib
* Seaborn

Project Workflow

1. Data Sampling

Processed the original H&M transaction dataset containing approximately 31 million records.

Applied three-layer stratified sampling based on:

* Transaction dates
* Customer transaction frequency
* Product categories

Final sample: 10,000 transactions.

2. Data Preprocessing

Performed:

* Missing value analysis and treatment.
* Binary flag creation for structural null values.
* Group-based median imputation.
* Redundant feature removal.
* Text standardization.
* Log transformation of price variables.

3. Feature Engineering

Transformed daily transaction aggregates into 54 engineered features.

Key features include:

* Calendar and temporal features.
* Cyclic day-of-week and month encoding.
* Rolling means and standard deviations.
* Autoregressive lag features.
* STL trend, seasonal, and residual components.
* Rolling Z-score anomaly detection.
* Department-level revenue features.

4. Time-Series Forecasting

Implemented four forecasting models:

Model	MAPE	RMSE	MAE
Seasonal Naive	45.89%	0.1773	0.1453
SARIMA	33.58%	0.1515	0.1188
Prophet	36.77%	0.1404	0.1108
LSTM	34.56%	0.1305	0.1003

Best Model: SARIMA(1,1,1) × (1,1,0,7)

SARIMA achieved the lowest MAPE of 33.58%, making it the selected model based on the project’s primary evaluation metric.

5. Explainable AI — SHAP Analysis

Applied SHAP analysis using an XGBoost regression model to investigate the contribution of engineered features to revenue predictions.

Key influential features identified:

* Rolling Z-score.
* 30-day rolling revenue mean.
* Number of unique articles.

The findings provide additional insights into revenue fluctuations and potential business decision-making opportunities.

Dataset

H&M Personalized Fashion Recommendations

Source: Kaggle — H&M Personalized Fashion Recommendations (2020).

The original dataset contains approximately 31 million customer transaction records covering September 2018 to September 2020.

Due to computational constraints, a stratified sample was used for this project.

Project Outcomes

The project demonstrates an end-to-end analytical workflow connecting:

Raw Transaction Data → Data Preprocessing → Feature Engineering → Forecasting Models → Model Evaluation → Explainable AI → Revenue Forecasting

It highlights how statistical time-series models and machine learning techniques can support data-driven decision-making in fashion retail.

Future Improvements

* Experiment with advanced forecasting architectures.
* Optimize model hyperparameters.
* Incorporate external variables such as promotions and holidays.
* Explore hybrid forecasting approaches.
* Develop an interactive revenue forecasting dashboard.

References

* H&M Personalized Fashion Recommendations — Kaggle (2020).
* Taylor & Letham (2018) — Forecasting at Scale.
* Lundberg & Lee (2017) — A Unified Approach to Interpreting Model Predictions.
* Box, Jenkins, Reinsel & Ljung (2015) — Time Series Analysis.

⸻

Project Focus: Data Science | Time-Series Forecasting | Machine Learning | Deep Learning | Explainable AI
