Detailed Project Report: Multi-Model USD/INR Exchange Rate Forecasting (2004–2026)
This report presents a complete end-to-end forecasting framework for the USD/INR exchange rate. The project compares statistical, machine-learning, and deep-learning approaches using a common evaluation pipeline and summarizes all preprocessing, stationarity tests, model diagnostics, forecasting results, and comparative performance metrics.
Project Objective
Develop a robust forecasting system for USD/INR exchange rates and compare ARIMA, XGBoost, SimpleRNN, and LSTM models using RMSE-based evaluation.
Dataset Summary
Source: Yahoo Finance (INR=X)
Time Period: 2004–2026
Observations: 5,856 daily records
Target Variable: Close price (USD/INR exchange rate).
Data Quality Checks
Missing values: 0
Duplicate dates: None
No imputation or interpolation was required.
Exploratory Data Analysis
The series exhibited a long-term upward trend, structural volatility, and changing mean levels, indicating that the raw series was non-stationary.
Stationarity Testing
ADF p-value: 0.99127
KPSS p-value: 0.01000
Conclusion: The original series was non-stationary.
Transformations Applied
1. Log transformation
2. First-order differencing
After transformation:
ADF p-value: 0.00000
KPSS p-value: 0.10000
The transformed series was treated as stationary.
ARIMA Baseline
Auto-ARIMA selected ARIMA(1,1,0).
Training observations: 4,684
AIC: -36,405.79
Ljung–Box residual test p-values at lags 10 and 20 were approximately 1.0, indicating no significant remaining autocorrelation.
ARIMA Forecast Accuracy
Train size: 4,684
Test size: 1,172
RMSE: 5.2938
XGBoost Model
Features used: lag_1, lag_7, lag_30, rolling mean, rolling standard deviation, and EMA-based trend indicators.
Training samples: 4,660
Testing samples: 1,166
RMSE: 9.6468
Deep Learning Models
A 30-day sliding window and MinMax scaling were used.
SimpleRNN RMSE: 0.6632
LSTM RMSE: 0.2900
USD/INR Historical Trend
 
Model Performance Comparison
 
30-Day Forecast Results
The ARIMA(1,1,0) model was used to generate a 30-day out-of-sample forecast. The forecast suggests a gradual upward movement in the USD/INR exchange rate.
 
Date	Forecast USD/INR
2026-08-04	84.1434
2026-08-05	84.3082
2026-08-06	84.3034
2026-08-07	84.3045
2026-08-08	84.3038
2026-08-09	84.4
2026-08-10	84.3633
2026-08-11	84.459
2026-08-12	84.435
2026-08-13	84.4858
2026-08-14	84.5268
2026-08-15	84.588
2026-08-16	84.6024
2026-08-17	84.63
2026-08-18	84.5721
2026-08-19	84.6997
2026-08-20	84.7144
2026-08-21	84.7313
2026-08-22	84.7652
2026-08-23	84.6494
2026-08-24	84.8453
2026-08-25	84.9053
2026-08-26	84.9361
2026-08-27	84.9219
2026-08-28	84.9307
2026-08-29	84.9681
2026-08-30	85.0139
2026-08-31	85.0484
2026-09-01	85.1076
2026-09-02	85.1137
Final Model Comparison
Model	RMSE	Relative Performance
LSTM	0.2900	Best
SimpleRNN	0.6632	Excellent
ARIMA(1,1,0)	5.2938	Moderate
XGBoost	9.6468	Weakest
Key Findings
•	USD/INR became stationary after log differencing.
•	ARIMA effectively captured the linear structure of the series.
•	XGBoost underperformed due to limited explanatory variables and the sequential nature of the problem.
•	SimpleRNN significantly improved forecasting accuracy over ARIMA.
•	LSTM achieved the lowest RMSE and reduced forecasting error by approximately 94% relative to ARIMA.
Conclusion
The study demonstrates that while classical ARIMA models provide interpretable and statistically sound forecasts, deep-learning sequence models are substantially more effective for capturing nonlinear temporal dependencies in exchange-rate data. Among all evaluated approaches, LSTM produced the most accurate forecasts and emerged as the recommended production model for short-term USD/INR forecasting.
