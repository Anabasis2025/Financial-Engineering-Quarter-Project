# Checkpoint_A 

**Overview:**
This repository contains my submission for Checkpoint Assignment A. The objective is to validate whether an activley managed, rules-based ETF (using momentum-based security selection and trend-following) can outperform passive exposure to transformational technologies.

## Project Summary
Checkpoint A tests the core thesis of the Anabasis Transformational Technologies Fund that systematic, rules-based management improves performance for innovation-focused portfolios.

The backtests implement:
- Ten distinct strategies combining momentum signals, portfolio weighting schemes, and rebalancing frequencies.
- Two momentum approaches: Baseline (90-day) and Daul-momentum (60-day + 120-day combined)
- Three portoflio weighting schemes: Equal-weight, Volatility-parity, and Mean-variance optimization
- Three rebalancing frequencies: Monthly, Quarterly, and Annual
- Walk-forward validation: 1-year training windows and 3-month test periods for out-of-sample robustness
- Benchmarks: Internal Equal-Weight passive benchmark
- Security selection: Top 2 per sleeve based on momentum rankings
- Transaction costs: 15 basis points per trade
- Statistical validation: Deflated-Sharpe-ratio analysis to guard against multiple testing bias
- Stress testing: Synthetic dot-com crash scenario

## Results
**Best Strategy:** S1 - Baseline Momentum + Equal Weight
- Total Return: 4,459% | Sharpe: 1.25 | Max Drawdown: -64.2%

**Passive Benchmark (B1):**
- Total Return: 1,837% | Sharpe: 1.12 | Max Drawdown: -63.4%

**Outperformance:** S1 beats passive by 143% in total returns with superior risk-adjusted performance.

Monthly rebalancing outperforms quarterly/annual. Equal-weight beats volatility-parity and mean variance optimization. Walk-forward validation confirms robustness.

**Data:**
The dataset was sourced via API from [Polygon.io](https://polygon.io/). I also compiled the daily close prices into `attf_polygon_data_extended.csv` for local analysis covering October 2015 - October 2025, spanning 20 securities across the four sleeves.

## Repository Contents

- `Krug_Checkpoint_A_Enhancements_Final.ipynb` - Jupyter Notebook code
- `Krug_Checkpoint_A_Enhancements_Final.html` - HTML
- `Kyle Krug_Checkpoint_Assignment_A_Final.docx` - Research report
- `requirements.txt` - Dependencies
  
## AI Usage Declaration

I developed this code consulting official documentation (Pandas, scikit-learn), open-source GitHub repositories, community discussions, the literature mentioned in the research section of the paper, and my previous classwork. To validate and troubleshoot my code, I also used Anthropic's Claude.

## Setup and Running
1. **Install dependencies:**
```bash
pip install -r ../requirements.txt

