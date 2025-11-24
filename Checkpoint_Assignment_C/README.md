# Checkpoint_Assignment_C

**Overview:**
This repository contains my submission for Checkpoint Assignment C. The goal of the research was to answer sevearl questions. Can statistical arbitrage through pairs trading exploit correlation structures among AI Infrastructure stocks? How sensitive are strategy returns to variations in fees? Can multi-path Monte Carlo simulation quantify the distribution of expected returns across alternative market scenarios? How does extending the backtest period to 26 years affect strategy performance evaluation?

## Project Summary
Checkpoint Assignment C expands on Programming Assignment 3 and Checkpoint B's research by implementing comprehensive strategy evaluation with extended historical backtesting, pairs trading, multi-path Monte Carlo simulation, and fee sensitivity analysis to answer the assignment requirements. Additionally, I added lots of subsequent analysis, validation, testing, and predictive analysis to determine the validity of the algorithm and strategies. Finally, this is the first assignment where i expanded the ATTF portfolio from 22 to 46 securities and from 4 to 6 thematic sleeves, providing the ATTF with greater exposure across stock market indices.

## Results
This is the first assignment since strategy implementation where Machine Learning did not dominate other strategies. After testing and analysis I was able to fix the ML look-ahead bias that had been pervasive and it reduced ML to 20% CAGR after fees. Clenow achieved the best at 27%. The pairs trading strategy targeting NVDA-AMD as correlated AI chip manufacturers delivered strongly negative returns, confirming that high correlation does not imply cointegration stability necessary for profitable statistical arbitrage. The fee sensitivity analysis confirms that monthly rebalancing frequency strikes an optimal balance between model adaptation to changing market conditions and transaction cost minimization. Extending the backtest 26 years actually is where ML performed the best after eliminating look-ahead bias. ML strategy’s sustainable long-term CAGR of roughly 20-30% was better momentum strategies over a long time horizon, and on par with Clenow's 2015-2025 outperformance. While I wasn't able to test ML for the multi-path Monte Carlo simulations, I was able to determine that Buy-And-Hold outperformed both momentum and hybrid strategies.

**Outperformance:** Clenow momentum

Clenow became the dominant strategy in the expanded ATTF universe. ML and hybrid strategies performed well, however, lower after look-ahead bias was resolved. Mean-Reversion failed to produce necessary alpha to make it an appropriate trading strategy. Pairs trading delivered negative returns due to lack of cointegration stability among correlated securities. These results provide valuable empirical evidence that guides strategy selection for the ATTF mandate by eliminating approaches fundamentally unsuited to momentum-driven innovation sectors, preventing costly capital deployment in strategies destined to fail.

**Data:**
The dataset was sourced via API from [Polygon.io](https://polygon.io/), spanning 46 securities across the six sleeves.

## Repository Contents

- `Krug_Checkpoint_C_Final.ipynb` - Jupyter Notebook code
- `Krug_Checkpoint_C_Final.html` - HTML
- `Kyle_Krug_Checkpoint_Assignment_C.pdf` - Research report
- `requirements.txt` - Dependencies
  
## AI Usage Declaration

I developed this code consulting official documentation (Pandas, scikit-learn), open-source GitHub repositories, community discussions, literature from the class bibliography, and my previous classwork. To validate and troubleshoot my code, I also used Anthropic's Claude.

## Setup and Running
1. **Install dependencies:**
```bash
pip install -r requirements.txt

