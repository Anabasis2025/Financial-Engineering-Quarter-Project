# Final_Term_Paper

**Overview:**
This repository contains my submission for my Final Term Paper for MSDS 451: Financial Engineering. The goal of the paper was to present the comprehensive development and validation of the Anabasis Transformational Technology Fund (ATTF), a rules-based quantitative portfolio management system designed to capture alpha in transformational technology sectors. The core hypothesis of this project is that we can utilize tools from data science, technical analysis, and financial engineering to earn excess returns relative to index funds and broad technology benchmarks.

## Project Summary
The Final Term Paper presents a structured investment prospectus on the ATTF. Besides detailing how the fund operates, the various trading strategies utilized, and the business aspects to make the fund a reality, I also added three main strategic tweaks to the strategies in order to validate the applicability of the Fund's thesis. I added an Ensemble ML strategy which combined XGBoost, RandomFroest, and GradientBoosting predictions through simple averaging, providing model diversification that reduces variance from any single algorithm’s biases. Additional enhancements include a 200-day moving average filter which excludes stocks in downtrends, concentration to the top 5 positions, and regime-based position scaling. Rather than training an HMM on the full sample, which has introduced look-ahead bias in previous assignments, the final hybrid regime-switching strategy uses expanding-window technical indicator thresholds calculated monthly using only past data. Classification features include 50-day SPY momentum, 20-day cumulative returns, VIX level, 20-day realized volatility, and drawdown from rolling 252-day highs. Threshold quantiles are recalculated each month from the prior three years, ensuring no future information contaminates regime assignments. To reduce excessive trading from noisy regime signals, a three-month smoothing filter requires regime persistence before triggering allocation changes, which reduces switches from 118 to 30 over the backtest period. Finally, and most important, I conducted forward out-of-sample validation using the training cutoff of October 11, 2025. Predictions generated as of that date were compared against actual realized returns over three forward horizons, 1-day, 1-week, and 1-month. This provided temporal validation to my research, ensuring that no future information contaminated signal generation.

## Results
Strategy evaluation revealed that Ensemble ML is the optimal strategy, delivering 28.37% CAGR with a 0.79 Sharpe ratio net of fees. Maximum drawdown of -38.02% was comparable to benchmark performance and represents tolerable risk for the ATTF’s focus on aggressive growth. The hybrid regime-switching system achieved 14.77% CAGR with a 0.83 Sharpe by dynamically allocating strategies based on expanding-window technical indicator classification. The system identified 30 regime transitions over the 10-year sample, averaging approximately 3 switches annually. Bear regime detection enabled defensive cash positioning during the 2018 correction, 2020 crash, and 2022 technology selloff, reducing maximum drawdown to -50.47%, comparable to Clenow’s -47.70%. Turnover remains modest at 8.6% annually, maintaining transaction cost efficiency. The Clenow strategy delivered 27.91 % CAGR with a 0.72 Sharpe, representing exceptional performance and only slightly behind the Ensemble ML strategy. The main issue with Clenow as a momentum strategy was the -47.7% drawdown during the COVID market crash. Clenow exhibits a higher volatility than any of the ML strategies or benchmarks. Extended 26-year validation using weighted sector proxy ETFs enabled comprehensive strategy assessment across complete market cycles. The ML strategy maintained 23.96% CAGR with a 0.690 Sharpe over the full 26-year period, demonstrating genuine predictive capacity despite lower performance than recent 10-year results. This validation confirms ML strategies can work properly implemented with rigorous temporal alignment. Quarterly momentum strategies achieved exceptional 1.40 Sharpe over 26 years with 21.76% CAGR, representing world-class risk-adjusted performance.


**Outperformance:** Ensemble Machine Learning

The Ensemble Machine Learning Strategy was the leading strategy at the end of my research. Clenow achieved incredible CAGR and Sharpe as well well, however, it's volatility and maximum drawdown were too significant to make it a consideration for being the leading strategy for the ATTF. While the hybrid regime-switching strategy trailed Clenow's CAGR, it had the highest Sharpe ratio out of all the main strategies, and an aggressive hybrid strategy actually produced the greatest CAGR during alternative strategy testing. Most importantly, the Ensemble Machine Learning strategy produced the greatest positive return during real-world out-of-sample validation, solidifying its place as the main ATTF strategy moving forward. These results provide valuable empirical evidence that guides strategy selection for the ATTF mandate by eliminating approaches fundamentally unsuited to momentum-driven innovation sectors, preventing costly capital deployment in strategies destined to fail.

**Data:**
The dataset was sourced via API from [Polygon.io](https://polygon.io/), spanning 46 securities across the six sleeves. 

## Repository Contents

- `Kyle_Krug_FE_Term_Paper.ipynb` - Jupyter Notebook code
- `Kyle_Krug_FE_Term_Paper.html` - HTML
- `Kyle_Krug_Financial_Engineering_Term_Paper.pdf` - Research report
- `requirements.txt` - Dependencies
  
## AI Usage Declaration

I developed this code consulting official documentation (Pandas, scikit-learn), open-source GitHub repositories, community discussions, literature from the class bibliography, and my previous classwork. To validate and troubleshoot my code, I also used Anthropic's Claude.

## Setup and Running
1. **Install dependencies:**
```bash
pip install -r requirements.txt
