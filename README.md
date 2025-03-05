# Time Series Forecasting for Portfolio Management Optimization 

## Overview

This project involves using forecasted financial data to optimize an investment portfolio consisting of three key assets:

1. **Tesla Stock (TSLA)**: A high-growth, high-risk stock in the consumer discretionary sector (Automobile Manufacturing).
2. **Vanguard Total Bond Market ETF (BND)**: A bond ETF for stability and low risk.
3. **S&P 500 ETF (SPY)**: An ETF tracking the S&P 500 Index for diversified market exposure.

We utilize historical data, develop forecasting models, and then apply optimization techniques to maximize returns while minimizing risk.

### Data Sources:
- **Tesla (TSLA)**: Historical stock prices (Open, High, Low, Close, Volume) from Yahoo Finance covering January 1, 2015, to January 31, 2025.
- **Vanguard Total Bond Market ETF (BND)** and **S&P 500 ETF (SPY)**: Financial data sourced similarly.

The dataset includes:
- Date (timestamp for each trading day)
- Open, High, Low, Close prices
- Volume (number of shares traded)

### Purpose:
This analysis aims to forecast future stock prices, identify trends, and use optimization techniques to find the best portfolio mix based on predicted market movements.

---

## Methodology

### Data Fetching:
- Data is fetched using the **YFinance** library, which allows downloading historical stock data for each asset.
- **TSLA** data is used for its forecasted prices from January 31, 2025, through January 19, 2026.
- Forecasted prices for **BND** and **SPY** are generated using simple moving averages or other chosen methods.

### Time Series Forecasting:
- The models selected (ARIMA, SARIMA, LSTM) are trained on historical data to predict future prices. The forecasted values are then analyzed to identify trends, volatility, and risk.

### Portfolio Optimization:
- Optimization is performed using the forecasted data, where we calculate portfolio returns, volatility, and the Sharpe ratio.
- The portfolio is optimized using the **SciPy** optimization library to maximize the Sharpe Ratio, adjusting the asset allocation to achieve the best risk-return profile.

---

## Results and Visualization
- **Portfolio Weights**: The optimal allocation between **TSLA**, **BND**, and **SPY** based on forecasted trends and the Sharpe ratio.
- **Expected Return and Volatility**: Metrics for the portfolio’s expected return and its associated risk.
- **Risk-Return Analysis**: A visualization of cumulative returns for each asset and the portfolio as a whole.

By the end of this project, you will have a well-optimized portfolio based on forecasted market trends, balancing high-growth potential with stability and diversification.

---

## Requirements:
- Python 3.x
- Required Libraries:
  - `yfinance`
  - `pandas`
  - `numpy`
  - `matplotlib`
  - `scipy`
  - `statsmodels`
  - `tensorflow` (for LSTM)
