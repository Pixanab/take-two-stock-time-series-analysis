# Take-Two Interactive (TTWO) Time Series Analysis

This project analyses the historical closing price of Take-Two Interactive Software (TTWO) using time series methods. The goal is to explore price behaviour, test for stationarity, identify an appropriate forecasting model, and evaluate its out-of-sample performance.

## Project Objective
The main objective is to:
- collect and clean daily market data for TTWO,
- perform exploratory data analysis (EDA),
- assess stationarity and autocorrelation,
- identify a suitable ARIMA model,
- forecast future values and compare model accuracy.

## Data Source
The data was downloaded from Yahoo Finance using the yfinance Python library.

- Ticker: TTWO
- Period: 2024-04-24 to 2026-04-24
- Focus variable: Close price

## Dataset Description
The dataset contains daily stock market information, including:
- Date
- Open
- High
- Low
- Close
- Volume
- Dividends
- Stock Splits

For this analysis, the relevant series was the Close price, since it reflects the end-of-day market value and is commonly used for time series modelling.

## Methodology
The workflow includes:
1. Data extraction from Yahoo Finance
2. Data cleaning and column selection
3. Missing value and outlier checks
4. Descriptive statistics
5. Time series plotting and visual inspection
6. Autocorrelation and lag analysis
7. Stationarity testing using ADF and KPSS
8. Differencing and model diagnostics
9. ARIMA model selection using AIC/BIC
10. Forecast generation and performance comparison

## Key Findings
- The raw TTWO close-price series showed a clear upward trend and non-stationary behaviour.
- ACF and PACF diagnostics suggested short-term dependence, supporting ARIMA modelling after differencing.
- The selected model was ARIMA(0, 1, 1), based on model fit and forecasting considerations.
- Residual diagnostics showed the model captured much of the dependence structure, although the forecast remained relatively flat over longer horizons.
- The baseline model performed competitively on the test set, highlighting the difficulty of forecasting stock prices with simple linear models.

## Tools and Libraries
This project uses:
- Python
- pandas
- NumPy
- matplotlib
- yfinance
- statsmodels

## Requirements
Install the required packages with:

```bash
pip install pandas numpy matplotlib yfinance statsmodels
