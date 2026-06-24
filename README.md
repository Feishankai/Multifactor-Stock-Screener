# MultiFactor Stock Screener

A quantitative equity research project that ranks stocks using factor investing principles commonly used by hedge funds, asset managers, and systematic trading firms.

---

## Overview

This project builds a multi-factor stock screener that evaluates stocks based on four widely studied factors:

* Momentum
* Value
* Quality
* Low Volatility

Each factor is standardized using z-score normalization and combined into a composite score. Stocks are then ranked based on their overall factor attractiveness.

The project also includes portfolio construction, performance evaluation, and visualization tools.

---

## Features

### Factor Engineering

#### Momentum

Measures 12-month price performance.

```text
Momentum = Current Price / Price 252 Trading Days Ago - 1
```

#### Value

Uses earnings yield as a valuation metric.

```text
Value = 1 / P/E Ratio
```

Higher values indicate cheaper stocks.

#### Quality

Uses Return on Equity (ROE) as a profitability measure.

```text
Quality = Return on Equity
```

#### Low Volatility

Uses annualized historical volatility.

```text
Volatility = Std(Daily Returns) × √252
```

Lower volatility receives a higher score.

---

## Ranking Methodology

Each factor is converted into a z-score:

```text
z = (x − μ) / σ
```

The final composite score is calculated as:

```text
Composite Score =
Momentum_Z +
Value_Z +
Quality_Z +
LowVol_Z
```

Stocks are ranked from highest to lowest composite score.

---

## Portfolio Construction

The model constructs an equal-weight portfolio from the top-ranked securities.

Workflow:

```text
Market Data
      ↓
Factor Calculation
      ↓
Z-Score Normalization
      ↓
Composite Ranking
      ↓
Top Ranked Stocks
      ↓
Portfolio Construction
      ↓
Performance Analysis
```

---

## Performance Metrics

The project evaluates portfolio performance using:

### CAGR

Compound Annual Growth Rate

Measures annualized portfolio growth.

### Sharpe Ratio

Measures risk-adjusted return.

```text
Sharpe = Return / Volatility
```

### Maximum Drawdown

Measures the largest portfolio decline from a previous peak.

### Win Rate

Percentage of positive return periods.

### Annualized Volatility

Measures portfolio risk.

---

## Visualizations

### Equity Curve

Tracks portfolio growth over time.

### Drawdown Analysis

Visualizes portfolio declines from peak value.

### Factor Correlation Heatmap

Shows relationships between factors.

### Composite Score Distribution

Displays score dispersion across securities.

### Momentum vs Value Scatter Plot

Visualizes factor relationships and rankings.

---

## Technologies Used

### Python

Core development language.

### Libraries

* Pandas
* NumPy
* SciPy
* yFinance
* Plotly
* Matplotlib

---

## Data Source

Market and fundamental data sourced from Yahoo Finance.

Future versions may integrate:

* Financial Modeling Prep
* SEC EDGAR
* Alpha Vantage
* FRED

---

## Results

Example outputs include:

* Ranked stock universe
* Factor score tables
* Portfolio performance metrics
* Interactive visualizations
* Risk analytics

---

## Skills Demonstrated

### Quantitative Finance

* Factor Investing
* Equity Research
* Portfolio Construction
* Risk Analysis

### Data Science

* Data Collection
* Data Cleaning
* Feature Engineering
* Statistical Normalization

### Programming

* Python
* Data Pipelines
* Financial Analytics
* Visualization

---

## Future Enhancements

* Sector-Neutral Factor Models
* Fama-French Multi-Factor Framework
* Portfolio Optimization
* Walk-Forward Backtesting
* Machine Learning Factor Weighting
* Alternative Data Integration
* Benchmark Comparison vs S&P 500

---

## Author

Zander Felder

Student Quantitative Finance & Data Science Projects

Washington, D.C.
