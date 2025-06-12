# copacabana-project
Forecasting price intervals for Iron Condor strategies using GARCH models and backtesting in R.
# 📈 The Copacabana Project: Volatility Forecasting for Options Strategies

Welcome to the **Copacabana Project**, a quantitative research framework designed to forecast short-term volatility and optimize the use of **Iron Condor** strategies on U.S. ETFs like **SPY** and **QQQ**.

> “Not all confidence intervals are created equal — especially when they define your risk envelope.” 🧠

---

## 🎯 Objective

This project aims to:

- Forecast future price intervals using **GARCH-family models**
- Simulate and backtest **Iron Condor profitability** based on these intervals
- Identify the best **confidence levels** and **forecast horizons**
- Build a fully automated and reproducible pipeline in **R**
- Lay the foundation for future use of **machine learning** to enhance model adaptability

---

## 🛠 Tools & Libraries

- Language: **R**
- Key packages: `quantmod`, `rugarch`, `PerformanceAnalytics`, `ggplot2`, `dplyr`
- Data source: **Yahoo Finance** (via `quantmod`)

---

## 📊 Methodology

- GARCH modeling with `eGARCH(1,1)` using skewed t-distribution (`sstd`)
- Forecast horizon: **32 calendar days**
- Rolling backtest on **126 sequential Fridays** (2022–2025)
- Simulated Iron Condor:
  - **+100 USD** if SPY closes **within forecast interval**
  - **−300 USD** if it breaches
- Multiple confidence intervals tested: **10%, 12%, 15%, 17%, 20%**

---

## 📁 Structure

```plaintext
├── copacabana_backtest.R        # Full forecasting and backtest pipeline
├── /data                        # Optional folder for exported results
├── /plots                       # Auto-generated performance visualizations
├── README.md                    # This file
