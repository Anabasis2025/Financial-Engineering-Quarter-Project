## Programming_Assignment_3

**Overview:**
This repository contains my submission for Programming Assignment 3. The goal of the research was to answer can regime detection models identify market conditions in real-time to enable tactical allocation shifts to better strategies.

## Project Summary
Programming Assignment 3 expands on Checkpoint B's research by adding several strategies, such as functioning mean-regression, machine-learning walk-forward, Clenow momentum, hybrid regime-switching,functioning HMM regime detection, sophisticated fee/transaction cost adjustments, additional benchmark comparisons, and feature engineering.

## Results
**Best Strategy:** Machine Learning Walk-Forward
- CAGR: 116.6% | Sharpe: 3.86 | Max Drawdown: -21%

**Clenow:**
- CAGR: 23.5% | Sharpe: 0.59 | Max Drawdown: -69.6%

**Hybrid:**
- CAGR: 40.9% | Sharpe: 1.54 | Max Drawdown: -31.6%

**Outperformance:** Machine Learning Walk-Forward substantially beat all other strategies.

Programming Assignment 3 demonstrates that quantitative portfolio optimization delivers substantial value for managing transformational technology exposures. The ML strategy achieved superior results, dominating Clenow, mean-reversion, hybrid, and passive benchmarks after accounting for realistic fees and transaction costs. This validates the hypothesis that systematic security selection using momentum, volatility, and technical features can generate economically significant alpha in innovation-driven sectors.

**Data:**
The dataset was sourced via API from [Polygon.io](https://polygon.io/). I also compiled the daily close prices into `attf_polygon_data_extended (1).csv` for local analysis covering October 2015 - October 2025, spanning 22 securities across the four sleeves.

## Repository Contents

- `Kyle_Krug_Programming_Assignment_3.ipynb` - Jupyter Notebook code
- `Kyle_Krug_Programming_Assignment_3.html` - HTML
- `Kyle_Krug_Programming_Assignment_3.pdf` - Research report
- `attf_polygon_data_extended (1).csv` - Daily close prices for 22 securities across four sleeves from October 2015 - October 2025
- `requirements.txt` - Dependencies
  
## AI Usage Declaration

I developed this code consulting official documentation (Pandas, scikit-learn), open-source GitHub repositories, community discussions, literature from the class bibliography, and my previous classwork. To validate and troubleshoot my code, I also used Anthropic's Claude.

## Setup and Running
1. **Install dependencies:**
```bash
pip install -r requirements.txt


