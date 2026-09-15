
# Project: Pre-Trade and Post-Trade Transaction Cost Analysis

Pre-trade and post-trade transaction cost analysis for a portfolio of 25 stocks, using market impact and implementation shortfall models.

## Project Summary

This project analyzes pre-trade and post-trade transaction costs for 25 stocks using a hypothetical dataset (simulating client trade lists and market data) provided by Professor Kissel for academic purposes.

**Setup:** Loaded datasets into Pandas, imported libraries, and defined Market Impact model parameters.

**Pre-Trade Analysis:** Built functions to estimate Market Impact (MI), Timing Risk (TR), and Price Appreciation (PA), plus POV/Trade Time conversions. MI captures Temporary Impact (liquidity needs) and Permanent Impact (information content). TR measures cost uncertainty from volatility, liquidity risk, and estimation error. PA estimates expected price movement during execution.

Optimal POV rates were then calculated under three strategies:
- **Trader's Dilemma** – balances MI vs. TR using a risk-aversion parameter
- **Minimize Cost** – minimizes total MI + PA cost using an Alpha estimate
- **Price Improvement** – maximizes probability of beating a target cost and Sharpe ratio

Using a for loop, MI, TR, and PA were calculated for all 25 stocks under two scenarios: (1) POV = 10%, and (2) Trade Time = 0.75 days converted to equivalent POV. Trade side was encoded numerically (Buy = 1, Sell = -1). The optimal POV rate was then computed for each stock based on investor strategy choice.

**Post-Trade Analysis:** Calculated Implementation Shortfall (IS) — the gap between paper return and actual portfolio return — decomposed into Delay Cost, Execution Cost, Opportunity Cost, and Fixed Cost. Additional metrics included Arrival Cost, VWAP Slippage, Benchmark Cost, Value Added, and Z-Score. Relative Performance Measure (RPM), a percentile ranking of execution quality, was also computed (e.g., RPM of 90% = top 90% of all executions).

Using a for loop, IS and all decomposed cost/performance metrics were calculated across the 25-stock portfolio.

## Data

The data used in this project is hypothetical/simulated data provided by Professor Kissel for academic purposes, not actual client trading data.

## Files in this Repo

- `Master_Personal_Project.ipynb` – main analysis notebook
- `Case Study 01 - Post Trade Analysis.csv` – post-trade dataset
- `Case Study 02 - Pre Trade Analysis.csv` – pre-trade dataset

## Tools & Libraries Used

- Python
- pandas
- numpy
- matplotlib
- scipy (stats, optimize)

