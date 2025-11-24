# Financial-Time-Series-Assignment
**Name:** Kyle Krug
**Course:** MSDS 451
**Assignment:** Program Assignment 1
___

## Overview
This repository contains my submission for Programming Assignment 1.
The objective is to predict **direction of Bitcoin's next-day return (up or down)** using lagged technical features and expanding walk-forward cross-validation.
This adapts the WTI jump-code I was provided to Bitcoin (BTC).

___

## Repository Contents
`Krug_Programming_Assignment_1.ipynb1` - Jupyter Notebook code.
`Krug_Programming_Assignment_1.html` - HTML export with outputs and plots.
`Krug_Programming_Assignment_1.pdf` - Research report.
`data/btc_historical_data.csv` - Daily OHLCV Bitcoin data (resampled from Kaggle minute-level file).
`requirements.txt` - Dependencies.

___

## Setup and Running
Clone this repository or download the files.
Install dependencies:
```bash
pip install -r requirements.txt
```

___

## Results
Logistic Regression: Accuracy = 0.526, AUC = 0.51
XGBoost: Accuracy = 0.509, AUC = 0.504
Both models hovered near random guessing showing the difficulty of daily BTC forecasting.
Adding Federal Funds Rate features did not improve predictive power.

___

## Data
The original dataset is [Bitcoin Historical Data (Kaggle)](https://www.kaggle.com/datasets/mczielinski/bitcoin-historical-data?select=btcusd_1-min_data.csv).
For this assignment, I resampled it to daily OHLCV (Open, High, Low, Close, Volume) covering 2012-2025.
The smaller resampled file used in this analysis is included in the files section.

___

## AI Usage Declaration
I developed this code consulting official documentation (Polars, scikit-learn), open-source GitHub repositories, community discussions, and my previous classwork.
To validate and troubleshoot my code, I also used Anthropic's Claud
