# Can Machine Learning Improve Portfolio Risk-Adjusted Returns?

## Project Goal

This project compares machine learning-based portfolio allocation with traditional investment strategies.

## Research Question

Can machine learning improve portfolio risk-adjusted returns compared to traditional portfolio allocation methods?

## Dataset

We use historical stock and ETF price data from Yahoo Finance.

The project currently includes two 20-year dataset options:

- Option 1: AAPL, MSFT, NVDA, SPY, BND, EFA, VNQ
- Option 2: AAPL, MSFT, NVDA, SPY, BND, XLF, XLE

We changed from VOO because VOO does not have complete 20-year historical data for our selected time period.

## Assets / Tickers Used

### Common Assets Used in Both Dataset Options

These assets are included in both dataset options.

#### Individual Stocks

- AAPL - Apple Inc.  
  Represents a large technology company.

- MSFT - Microsoft Corporation  
  Represents a large technology and software company.

- NVDA - NVIDIA Corporation  
  Represents a semiconductor and artificial intelligence-related company.

#### Benchmark / Portfolio ETFs

- SPY - SPDR S&P 500 ETF Trust  
  Used as the main market benchmark and Buy and Hold benchmark.

- BND - Vanguard Total Bond Market ETF  
  Used as the bond asset for the 60/40 portfolio strategy.

### Dataset Option 1: International + Real Estate Portfolio

This option adds international developed market and real estate exposure.

- EFA - iShares MSCI EAFE ETF  
  Represents international developed markets outside the U.S. and Canada.

- VNQ - Vanguard Real Estate ETF  
  Represents the U.S. real estate sector through REITs.

### Dataset Option 2: Sector ETF Portfolio

This option adds U.S. sector ETF exposure.

- XLF - Financial Select Sector SPDR Fund  
  Represents the U.S. financial sector.

- XLE - Energy Select Sector SPDR Fund  
  Represents the U.S. energy sector.

## Benchmark Strategies

- Buy and Hold SPY
- Equal Weight Portfolio
- 60/40 Portfolio
- Mean-Variance Optimization

## Evaluation Metrics

- Cumulative Return
- Annual Return / CAGR
- Annual Volatility
- Sharpe Ratio
- Maximum Drawdown
- Portfolio Weights

## Folder Structure

- `data/`: raw and cleaned datasets
- `notebooks/`: Google Colab notebooks
- `src/`: reusable Python functions
- `results/`: charts and tables
- `papers/`: literature review notes
