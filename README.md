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
```text
  portfolio-optimization-ml/
|
├── literature_review/
│   ├── literature_review.md      ← Narrative summary of the field: what's already known, major findings across your ~10–15 papers
│   ├── annotated_bibliography.md ← One entry per paper: citation + 3–5 sentence summary of what it did and found
│   ├── research_gap.md           ← The specific hole in existing research your project fills (this is your "so what")
│   └── papers/
│       ├── paper1.pdf
│       ├── paper2.pdf
│       └── notes/                ← Raw reading notes per paper, before they get distilled into the bibliography
│
├── data/
│   ├── raw/           ← Data exactly as downloaded from Yahoo Finance. NEVER edit these files by hand.
│   ├── processed/      ← Cleaned versions: missing values handled, returns/volatility calculated.
│   └── external/       ← Anything from outside sources (Fama-French factors, FRED macro data, if used).
│
├── notebooks/           ← Jupyter notebooks, numbered so anyone can follow the project in order.
│   ├── 01_data_collection.ipynb   ← Pulls data via yfinance, saves to data/raw/
│   ├── 02_data_cleaning.ipynb     ← Cleans it, saves to data/processed/
│   ├── 03_eda.ipynb               ← Charts, correlations, summary stats
│   ├── 04_baseline_models.ipynb   ← Buy-and-hold, equal weight, 60/40 benchmarks
│   ├── 05_machine_learning.ipynb  ← Linear Regression, Random Forest, XGBoost
│   ├── 06_lstm_model.ipynb        ← Deep learning model
│   ├── 07_portfolio_optimization.ipynb ← Turns model predictions into actual allocations
│   └── 08_final_results.ipynb     ← Final comparison tables/charts for the poster
│
├── src/                 ← Reusable Python functions (not exploratory — this is your "library").
│   ├── data_loader.py   ← Functions to download/load data (so notebooks don't repeat code)
│   ├── features.py      ← Returns, moving averages, volatility calculations
│   ├── models.py        ← Model definitions (RF, XGBoost, LSTM classes)
│   ├── portfolio.py      ← Allocation logic, rebalancing rules
│   └── evaluation.py     ← Sharpe ratio, drawdown, Sortino ratio functions
│
├── results/
│   ├── figures/          ← Saved chart images (.png) for the poster
│   ├── tables/           ← Saved performance comparison tables (.csv)
│   └── reports/          ← Written summaries, draft text for poster sections
│
├── papers/               ← PDFs of the 10–15 research papers from your literature review
├── README.md             ← Project overview — the front page of your repo
├── requirements.txt      ← List of Python packages needed (so anyone can reinstall your environment)
└── .gitignore            ← Tells Git which files to ignore (see below)
```
