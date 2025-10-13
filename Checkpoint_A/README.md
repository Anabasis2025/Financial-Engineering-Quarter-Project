# Checkpoint_A 

**Goal:**
Validate whether an actively managed, rules-based ETF (using momentum-based security selection and trend-following) can outperform passive exposure to transformational technologies.

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

## How to Run Checkpoint A
1. **Install dependencies:**
```bash
pip install -r ../requirements.txt```
