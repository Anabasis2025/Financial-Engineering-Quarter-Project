# Programming Assignment 2: Portfolio Optimization

## Overview
This repository contains my submission for Programming Assignment 2. The objective is to extend the ATTF analysis from Checkpoint A by applying Monte Carlo simulation and portfolio optimization to determine optimal sleeve allocations.

## Research Question
- Can Monte Carlo simulation ientify superior portfolio allocations

## Repository Contents
`Krug_Programming_Assignment_2.ipynb` - code. `Krug_Programming_Assignment_2.html` - HTML export with plots. `Krug_Programming_Assignment_2.docx` - Research Paper. `attf_polygon_data_extended (1).csv` - Daily OHLCV price data for ATTF securities from Checkpoint A.

## Results
Monte Carlo simulation improved ATTF Sharpe ratios by 8.5% Optimal allocation increases AI infrastructure weighting from 40 to 67% and reduces Space and Robotics from 30 to 3%. Long-only constraints remain appropriate for momentum-based strategies.

## Data
The dataset was sourced via API from Polygon.io. I also compiled the daily close prices into attf_polygon_data_extended (1).csv for local analysis covering October 2015 - October 2025, spanning 20 securities across four sleeves.

## AI Use Declaration
I developed this code using the jump-start code provided by Professor Miller, consulting official documentation (Pandas, scikit-learn), open-source GitHub repositories, community discussions, the Mathematical Finance book, and my previous classwork. To validate and troubleshoot my code, I also used Anthropic's Claude.
 
## Setup and Running
Clone this repository or download the dependencies:
```
pip install -r requirements.txt
```

