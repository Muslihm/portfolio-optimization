# Portfolio Optimization Project - GMF Investments

## Project Overview
This project implements a comprehensive portfolio optimization framework using time series forecasting for GMF Investments. The project analyzes three key assets: TSLA (high-growth), BND (low-risk bonds), and SPY (market index ETF).

## Project Structure
portfolio-optimization/
├── .vscode/ # VS Code configuration
├── .github/ # GitHub Actions workflows
├── data/
│ └── processed/ # Processed data files
├── notebooks/ # Jupyter notebooks
│ ├── 01_preprocess_explore_data.ipynb # Task 1
│ ├── init.py
│ └── README.md
├── src/ # Source code
├── tests/ # Unit tests
├── scripts/ # Utility scripts
├── .gitignore
├── requirements.txt
└── README.md

## Task 1 - Preprocess and Explore Data

### Completed Objectives:
- ✅ Extracted historical data from YFinance (2015-2026)
- ✅ Cleaned and validated data (no missing values)
- ✅ Conducted comprehensive exploratory data analysis
- ✅ Calculated key risk metrics (VaR, Sharpe Ratio, etc.)
- ✅ Performed stationarity testing (ADF test)
- ✅ Identified trends, patterns, and outliers

### Key Findings:
1. **TSLA**: High volatility (70%+ annualized), strong upward trend, significant outliers
2. **BND**: Low volatility (5% annualized), stable returns, minimal outliers
3. **SPY**: Moderate volatility (18% annualized), steady upward trend
4. **Stationarity**: All assets require d=1 differencing for ARIMA modeling

### Risk Metrics Summary:
| Asset | VaR (95%) | CVaR (95%) | Sharpe Ratio | Volatility |
|-------|-----------|------------|--------------|------------|
| TSLA  | -4.92%    | -6.87%     | 0.42         | 72.3%      |
| BND   | -0.41%    | -0.58%     | 0.15         | 5.1%       |
| SPY   | -1.68%    | -2.34%     | 0.53         | 18.2%      |

## Next Steps
- Proceed to Task 2: Develop forecasting models (ARIMA/SARIMA)
- Task 3: Portfolio optimization using predicted returns
- Task 4: Performance evaluation and client recommendations

## Installation
```bash
pip install -r requirements.txt
Running the Analysis
jupyter notebook notebooks/01_preprocess_explore_data.ipynb
Dependencies

    Python 3.8+

    yfinance 0.2.28+

    pandas 2.0.3+

    numpy 1.24.3+

    matplotlib 3.7.2+

    seaborn 0.12.2+

    statsmodels 0.14.0+

    scipy 1.10.1+
