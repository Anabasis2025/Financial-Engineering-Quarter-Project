# Financial_Engineering_Quarter_Project

This repository contains my work for MSDS 451: Financial Engineering. The research represents a complete evolution from initial portfolio construction through advanced algorithmic trading strategies and rigorous performance validation. The central thesis is that the sectors of the ATTF follow adoption-driven momentum patterns and are poorly suited to traditional diversification or mean-reversion approaches. I reject the efficient market hypothesis in favor of an adaptive markets framework, and I use fully transparent quantitative rules to express thematic conviction while minimizing human bias.

## Project Summary
The Financial_Engineering_Quarter_Project repo presents the complete development of the Anabasis Transformational Technologies Fund, synthesizing all quantitative research conducted throughout MSDS 451. The work represents systematic progression from foundational portfolio theory through advanced algorithmic trading strategies and rigorous backtesting, and out-of-sample validation. The objective was twofold. First, to design a multi-strategy quantitative fund capable of generating consistent alpha in transformational technology sectors. Second, to develop a comprehensive business analysis establishing both the fund’s viability and the minimum resources required for launch.

## Results
This comprehensive research demonstrates that systematic, rules-based quantitative management can generate consistent excess returns in transformative technology sectors when strategies undergo rigorous validation preventing look-ahead bias, overfitting, and data mining. The project evolved from simple momentum rules through Monte Carlo optimization and machine learning to sophisticated regime-switching systems, culminating in critical discovery and correction of look-ahead bias that provided invaluable lessons about temporal validation importance in quantitative finance.
Portfolio expansion from 22 to 46 securities revealed critical insights about strategy-market fit, and the importance of accounting for look-ahead bias was demonstrated after the fund’s ML Ridge regression CAGR decreased from a staggering 100+ percent over multiple assignments and weeks of analysis to 5% after being corrected for. Monte Carlo simulation across 200 synthetic scenarios provided a sobering perspective on path-dependence and uncertainty. This validates that a fund cannot use only single-trajectory historical backtests to validate expected performance when strategies exhibit path-dependence.
From a business perspective, the ATTF concept appears viable with the appropriate caveats. The recommended strategy allocation should target 20-28% CAGR and provide the ATTF with intermediate-term momentum combined with long-term trend confirmation in Clenow, a hybrid momentum- ML allocation, and Ensemble ML allocation that isn’t sensitive to target horizon specifications, feature set design, or the behavior of a small number of mega-cap winners. Critical to the ATTF becoming realized would be to allocate the necessary funding for data, infrastructure, and regulatory support as well as a diverse team to manage the myriads of investment fund requirements.

**Conclusion:**

In conclusion, this research validates that the adaptive-markets perspective provides a more realistic framework than strict efficient-markets hypothesis for understanding transformational technology sectors and achieving alpha. Behavioral biases, information asymmetries, and regime shifts create exploitable patterns that systematic momentum and machine learning strategies can capture when properly validated. The ATTF demonstrates that thematic conviction combined with quantitative discipline can generate sustainable alpha, provided investors maintain realistic expectation about drawdowns, costs, and the difference between historical exceptional periods and sustainable long-term performance.

**Data:**
The dataset was sourced via API from [Polygon.io](https://polygon.io/), spanning 46 securities across the six sleeves. I also compiled universe data across 8 files: `fred_macro_features.csv`, 'hmm_features.csv', 'portfolio_prices.csv', 'portfolio_returns.csv', 'proxy_returns.csv', 'sleeve_returns.csv', 'spy_benchmarks.csv', and 'universe_metadata.csv' for local analysis covering October 2015 - October 2025.

## Repository Contents

- `Programming_Assignment_1` - Basic Time Series analysis on Bitcoin
- `Checkpoint_A` - Development of portfolio philosophy
- `Programming_Assignment_2` - Monte Carlo portfolio optimization development
- `Checkpoint_B` - Development of regime-aware and momemtum strategies
- `Programming_Assignment_3` - Introduced feature engineering, fee analysis, benchmark comparisons, and functional regime classifcation
- `Checkpoint_C` - Introcution of fee sensitivity analysis, 200-path Monte Carlo optimization, 26-year backtestin strategies, comprehensive strategy evaluation, and fixed look-ahead bias in ML Ridge regression
- `Final_Term_Paper` - Added Ensemble ML strategy, added expanding-window technical indicator hybrid regime-switching strategy, conducted forward out-of-sample testing, succesfully validating Ensemble ML as a viable lead strategy for the ATTF
  
## AI Usage Declaration

I developed this code consulting official documentation (Pandas, scikit-learn), open-source GitHub repositories, community discussions, literature from the class bibliography, and my previous classwork. To validate and troubleshoot my code, I also used Anthropic's Claude.

## Setup and Running
1. **Install dependencies:**
```bash
pip install -r requirements.txt
