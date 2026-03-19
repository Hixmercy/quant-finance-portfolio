# Day 1 – Market Data & Return Analysis (EURUSD)

## 📌 Objective
This project analyzes the historical behavior of EURUSD using daily market data to understand returns, volatility, and drawdown characteristics. The goal is to establish a foundation for future trading strategy development.

---

## 📊 Dataset
- Source: Alpha Vantage API
- Asset: EURUSD
- Frequency: Daily data (Open, High, Low, Close)

---

## 🛠️ Tools Used
- Python
- pandas
- numpy
- matplotlib
- requests

---

## 🔍 Key Analysis Performed
- Data extraction from API
- Data cleaning and structuring
- Calculation of:
  - Simple returns
  - Log returns
  - Cumulative returns
- Risk metrics:
  - Annualized return
  - Annualized volatility
  - Maximum drawdown

---

## 📈 Visualizations
- Price series over time
- Daily returns
- Return distribution (histogram)
- Equity curve and drawdown

---

## 📊 Key Metrics
| Metric | Value |
|--------|------|
| Annualized Return | 5.42% |
| Annualized Volatility | 11.87% |
| Max Drawdown | -18.35% |
---

## 📊 Analyst Interpretation
The asset exhibits clear periods of **volatility clustering**, where high-volatility phases are followed by continued instability, a common characteristic of financial time series. Daily returns are largely centered around zero, indicating the absence of consistent directional drift, but are punctuated by occasional extreme movements, reflecting **tail risk**.

The return distribution deviates from normality, suggesting the presence of **fat tails and potential skewness**, which has important implications for risk modeling and strategy design. Additionally, the observed **maximum drawdown** underscores the significant downside risk associated with a passive holding approach.

Overall, these findings highlight that any trading or investment strategy applied to this asset must be evaluated not only on expected returns but also on **risk-adjusted performance and drawdown control**.

---

## 📁 Project Structure
day-01-market-data-analysis/
│
├── notebook.ipynb
├── data/
├── outputs/
│   ├── charts/
│   └── tables/
└── README.md

## 🚀 Next Step
Day 2 will focus on building a technical indicator dashboard (RSI, MACD, Moving Averages) and exploring trading signals.

---
