# Monte Carlo Pricing of European and Asian Options

## Overview

This project applies Monte Carlo simulation techniques to price European and Asian call options under the Geometric Brownian Motion (GBM) framework. The project investigates convergence behaviour, path dependence, and volatility sensitivity while comparing Monte Carlo estimates with analytical pricing methods.

## Objectives

- Simulate stock price paths using Geometric Brownian Motion
- Price European call options using Monte Carlo simulation
- Compare Monte Carlo European prices against the Black–Scholes analytical solution
- Price arithmetic Asian call options
- Analyse Monte Carlo convergence behaviour
- Investigate volatility sensitivity for both European and Asian options
- Explore path dependence and terminal price distributions

## Mathematical Background

We assume the stock price follows Geometric Brownian Motion:


$dS_t = r S_t dt + \sigma S_t dW_t$


Under the risk-neutral measure, the discrete-time simulation formula is:


$S_{t+\Delta t} = S_t \exp\left((r - \frac{1}{2}\sigma^2)\Delta t + \sigma \sqrt{\Delta t} Z\right)$

where $(Z \sim N(0,1)$).

For a European call option, the payoff at maturity is:

$max(S_T - K, 0)$, where K is the strike price


The Monte Carlo price is the discounted expected payoff:


$C = e^{-rT} \mathbb{E}[\max(S_T - K, 0)]$

## Features

- GBM stock path simulation
- European option pricing
- Asian option pricing
- Monte Carlo convergence analysis
- Volatility sensitivity analysis
- Comparison with Black–Scholes pricing
- Terminal stock price distribution visualisation
- Error bar visualisations for repeated simulations

## Technologies Used

- Python
- NumPy
- SciPy
- Matplotlib
- Jupyter Notebook

## Key Findings

- Monte Carlo estimates converge toward the Black–Scholes price as the number of simulations increases
- Asian options are consistently cheaper than European options due to volatility dampening from averaging
- European options exhibit greater sensitivity to volatility than Asian options
- 
## Future Improvements

- Variance reduction techniques
- Quasi-Monte Carlo methods
- Stochastic volatility models
- Barrier and lookback option pricing
- GPU acceleration for simulations

## Author

Nitheesh Dharmapalan
