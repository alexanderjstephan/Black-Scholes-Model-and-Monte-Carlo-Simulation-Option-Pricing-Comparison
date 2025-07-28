# Black-Scholes Model and Monte Carlo Simulation Option Pricing Comparison

## Overview
This project develops python functions to price theoretical options using the Black-Scholes model and Monte Carlo simulation. Alongside the Black-Scholes model pricing, this project calculates the Black-Scholes Greek values for the options. Using these functions, the price of a MSFT option with varying expiration and strike price values was calculated using both functions and the Monte Carlo simulation was compared to the baseline Black-Scholes price to evaluate its accuracy.

## Methodology
Data was collected from the target stock over the previous month to calculate volatility. From there, the risk-free rate was approximated using the 10-year treasury bond interest rate and values were plugged into the particular call and put solutions to the Black-Scholes differential equation to calculate option value. Using partial derivatives of the particular Black-Scholes solutions, the greek variables of the option were determined. Monte Carlo simulation was created following Geometric Brownian Motion and risk-free rate. 10,000 possible stock trajectories were simulated and the adjusted average payoff was used as the value of the option. Lastly, Monte Carlo simulation was compared to the Black-Scholes price of the option for varying expiration times and strike prices.

## Results
Monte Carlo simulation closely follows Black-Scholes price except for deep out-of-the-mponey or short-dated options. Greeks behaved as predicted. Primary error in the Monte Carlo simulation was due to the simulation giving an option a value of zero, while Black-Scholes gave the option a near-zero value, resulting in high error.

## Credits
- **Data:** Yahoo Finance
- **Libraries:** pandas, yfinance, numpy, matplotlib, seaborn, scipy, jupyter
- **Background Reading:**
  -  Option Strike Prices: How It Works, Definition, and Example, Investopedia
  -  American vs. European Options: What's the Difference?, Investopedia
  -  What is options trading? A beginner's guide to the basics, Ally.com
  -  Monte Carlo Simulation, datascience.eu
  -  Gamma, Merrill
  -  Options Vega - The Greeks, CME Group
  -  What Is Rho? Definition, How It's Used, Calculation, and Example, Investopedia
  -  Option Greeks: The 4 Factors to Measure Risk, Investopedia
  -  Historical Volatility (HV), Corporate Finance Institute
  -  What is The Monte Carlo Simulation?, Amazon Web Services
  -  What Is Delta in Derivatives Trading, and How Does It Work?, Investopedia
  -  Black-Scholes Model: What It Is, How It Works, and Options Formula, Investopedia
  -  Black-Scholes Model Assumptions, Macroption
  -  How to Use Monte Carlo Simulation With GBM, Investopedia
  -  Option Greeks, Corporate Finance Institute
  -  Monte Carlo Simulation: What It Is, How It Works, History, 4 Key Steps, Investopedia
  -  Monte Carlo Simulation, Corporate Finance Institute
  -  Heat Map in Matplotlib, Python Charts
  -  In the Money vs. Out of the Money: What's the Difference?, Investopedia
-  **Author:** Alexander Stephan
