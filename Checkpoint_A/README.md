# Checkpoint_A 

**Goal:**
Validate whether an actively managed, rules-based ETF (using dual-momentum and trend-following) can outperform passive exposure to transformational technologies.

## Project Summary
Checkpoint A tests the core thesis of the Anabasis Transformational Technologies Fund that systematic, rules-based management improves performance for innovation-focused assets.

The backtests implement:
- Dual-momentum (60 / 120-day) + 200-DMA trend-following entry/exit
- Portfolio weighting: Equal-Weight vs Volatility-Parity vs Mean-Variance
- Benchmarks: Internal Equal-Weight and external QQQ ETF
- Lag-safe signals
- Walk-forward validation and deflated-Sharpe testing for robustness

## How to Run Checkpoint A
1. **Install dependencies:
```bash
pip install -r ../requirements.txt```
