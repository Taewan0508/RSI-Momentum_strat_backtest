# RSI-Momentum_strat_backtest
This project implements and backtests a simple RSI (Relative Strength Index) Momentum Trading Strategy using Python.
It is designed as an introductory quantitative finance project to help develop skills in data handling, technical indicators, backtesting logic, and performance evaluation.

## 📌 Project Overview

- Downloads stock price data (e.g., TSLA or any user-chosen ticker) using yfinance
- Computes daily returns
- Calculates the RSI indicator using gains/losses over a 14-day lookback period
- Generates trading signals:
  - Buy when RSI < 30 (oversold)
  - Sell when RSI > 70 (overbought)
- Backtests performance vs. Buy-and-Hold benchmark
- Visualizes strategy equity curve and price with RSI signals

rsi_momentum_strategy/
│
├── rsi_strategy.ipynb        # Main notebook with full analysis
├── README.md                 # Project documentation
├── results/
│   ├── performance_plot.png  # Equity curve comparison
│   ├── rsi_chart.png         # Price + RSI visualization
│
└── data/
    └── ticker_data.csv       # (Optional) Saved price data for reproducibility
