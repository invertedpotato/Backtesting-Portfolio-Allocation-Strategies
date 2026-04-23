# Backtesting-Portfolio-Allocation-Strategies
# Portfolio Strategy Backtesting Framework

**Python | Pandas | NumPy | SciPy | Matplotlib**

## Overview

This project backtests 6 portfolio allocation strategies on 30 industry monthly returns (1926–2018, 1,110 months). All strategies use rolling-window optimization to avoid look-ahead bias.

## Strategies Tested

| Strategy | Description |
|----------|-------------|
| Rolling Max Sharpe (MSR) | Maximizes Sharpe ratio using past 10-60 months |
| Dynamic MSR | MSR with dynamic allocation to risk-free asset |
| Rolling Global Minimum Variance (GMV) | Minimizes portfolio volatility using past 10-60 months|
| Dynamic GMV | GMV with dynamic allocation based to risk-free asset |
| Three-Asset Dynamic | Allocates between risk-free, GMV, and MSR |
| Rolling Max Return | 100% in highest expected-return asset|

## Key Findings

| Metric | Cap-Weighted Market | Dynamic GMV (50-month) |
|--------|--------------------|------------------------|
| Sharpe Ratio | 0.50 | **0.69** |
| Max Drawdown | -49.9% | **-22.0%** |
| 5% CVaR (monthly) | -9.7% | **-4.8%** |
| 5% Cornish-Fisher VaR | -6.8% | **-3.3%** |

**Conclusion:** Dynamic GMV reduced tail risk by approximately 50% while improving risk-adjusted returns.

## Risk Metrics Implemented

- Sharpe Ratio
- Maximum Drawdown
- Skewness & Kurtosis
- Historical VaR
- Historical CVaR (Expected Shortfall)
- Cornish-Fisher Modified VaR (accounts for non-normal returns)

## How to Run

1. Clone this repository
2. Install requirements: `pip install -r requirements.txt`
3. Open `BacktestingStrategies.ipynb` in Jupyter Notebook
4. Run all cells

## Requirements

- Python 3.8+
- pandas
- numpy
- scipy
- matplotlib

## Files

- `BacktestingStrategies.ipynb` - Main analysis notebook
- `requirements.txt` - Package dependencies
- `data/` - Industry returns data (30 industries, 1926-2018)

## Author

Ashvin Budhirja | ashvinbudhiraja9@gmail.com | 
