# Checkpoint_B

**Overview:**
This repository contains my submission for Checkpoint Assignment B. The goal of the research was to answer can momentum-based individual stock selection outperform sleeve-level portfolio diversification on a risk-adjusted basis? Can machine learning methods trained on momentum and volatility generate economically significant alphas net of transaction costs and management fees? Can regime-based tactical allocation reduce maximum drawdown during bear markets while capturing upside in bull markets? Are machine learning strategy returns driven by diversified stock selection across all four sleeves or concentrated in a single winner?

## Project Summary
Checkpoint B expands on Checkpoint A's research by adding several strategies, such as machine-learning walk-forward, Clenow momentum, Monte Carlo sleeve-level optimization for both long-only and shorts-allowed strategies, HMM regime detection, and fee/transaction cost adjustments.

## Results
**Best Strategy:** Machine Learning Walk-Forward
- CAGR: 109.74% | Sharpe: 2.191 | Max Drawdown: -37.46%

**Clenow:**
- CAGR: 17.82% | Sharpe: 0.377 | Max Drawdown: -74.35%

**Outperformance:** Machine Learning Walk-Forward substantially beat all other strategies.

Checkpoint B demonstrates that quantitative portfolio optimization delivers substantial value for managing transformational technology exposures. The ML strategy achieved 109.74% CAGR with 2.191 Sharpe ratio, dominating Monte Carlo optimized portfolios, momentum strategies, and passive benchmarks after accounting for realistic fees and transaction costs. This validates the hypothesis that systematic security selection using momentum, volatility, and trend features can generate economically significant alpha in innovation-driven sectors.

**Data:**
The dataset was sourced via API from [Polygon.io](https://polygon.io/). I also compiled the daily close prices into `attf_polygon_data_extended (1).csv` for local analysis covering October 2015 - October 2025, spanning 22 securities across the four sleeves.

## Repository Contents

- `Krug_Checkpoint_B_Final(v2) (2).ipynb` - Jupyter Notebook code
- `Krug_Checkpoint_B_Final(v2) (2).html` - HTML
- `Kyle Krug_Checkpoint_Assignment_B.pdf` - Research report
- `attf_polygon_data_extended (1).csv` - Daily close prices for 22 securities across four sleeves from October 2015 - October 2025
- `requirements.txt` - Dependencies
  
## AI Usage Declaration

I developed this code consulting official documentation (Pandas, scikit-learn), open-source GitHub repositories, community discussions, the literature mentioned in the research section of the paper, and my previous classwork. To validate and troubleshoot my code, I also used Anthropic's Claude.

## Setup and Running
1. **Install dependencies:**
```bash
pip install -r requirements.txt


