# Checkpoint_A 

**Goal:**
Validate whether an actively managed, rules-based ETF (using dual-momentum and trend-following) can outperform passive exposure to transformational technologies.

## Project Summary
Checkpoint A tests the core thesis of the Anabasis Transformational Technologies Fund that systematic, rules-based management improves performance for innovation-focused assets.

The backtests implement:
- Three momentum strategies: Baseline (90-day), Dual-momentum (60-day + 120-day), and Walk-Forward Validation
- Portfolio weighting: Equal-weight allocation within selected securities
- Benchmarks: Internal Equal-Weight passive benchmark
- Security selection: Top 2 per sleeve based on momentum rankings
- Walk-forward validation with 1-year training windows and 3-month test periods for robustness

## How to Run Checkpoint A
1. **Install dependencies:**
```bash
pip install -r ../requirements.txt```
