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

## 🔧 Technologies Used

- Python
- pandas — data manipulation
- numpy — mathematical operations
- matplotlib — visualization
- yfinance — historical price data
- pandas.DataFrame.rolling() — computing rolling gains/losses

## 📈 Strategy Logic

RSI is computed using this formula:

**_RS_** = Avg Gain(14) / Avg Loss(14)

**_RSI_** = 100 - (100/(1+RS))

where:
- RS = average gain / average loss (14-day lookback)
- Buy signal: RSI < 30
- Sell signal: RSI > 70
### Trading Logic:
if RSI < 30 → Signal = 1 (Buy)
if RSI > 70 → Signal = -1 (Sell)
else → Hold previous position
### Returns:
Daily Return = price.pct_change()
Strategy Return = Daily Return * Signal.shift(1)

## 📊 Results & Visualization

The notebook outputs:
- Price chart with buy/sell markers
- RSI indicator chart
- Equity curve comparison (RSI strategy vs Buy-and-Hold)
- Insightful performance observations
- These help understand whether momentum reversal behavior can outperform simple passive investing.
