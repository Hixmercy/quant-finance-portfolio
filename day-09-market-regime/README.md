# Day 9 – Market Regime Detection & Strategy Performance (EURUSD)

## 📌 Project Overview
This project introduces a structured approach to defining market conditions and evaluating how a trading strategy performs under different environments.

Instead of relying on visual interpretation, market regimes are defined quantitatively using volatility. This allows for a more rigorous analysis of when a strategy performs well and when it struggles.

The goal is to move beyond general performance evaluation and understand how strategy behavior changes depending on market conditions.

---

## 🎯 Objective
To answer a key question:

**Does strategy performance depend on market conditions?**

This project focuses on:
- defining market regimes formally  
- separating data into distinct environments  
- evaluating strategy performance within each regime  

---

## 📊 Dataset
- **Asset:** EURUSD  
- **Frequency:** Daily data  
- **Source:** Derived from previous projects (Day 7 strategy output)  

---

## 🛠️ Tools Used
- Python  
- Pandas  
- NumPy  
- Matplotlib  

---

## ⚙️ Methodology

### 1. Measure Market Volatility
Rolling volatility is calculated using recent price returns to quantify how unstable the market is over time.

---

### 2. Define Market Regimes
A threshold is created using the median level of volatility.

- **High Volatility Regime:** periods where volatility is above the threshold  
- **Low Volatility Regime:** periods where volatility is below the threshold  

This creates a clear and objective way to classify market conditions.

---

### 3. Assign Regime Labels
Each time period is labeled based on its volatility level, allowing the dataset to be segmented into different environments.

---

### 4. Evaluate Strategy Performance by Regime
The trading strategy is analyzed separately within each regime using:

- Annual Return  
- Volatility  
- Sharpe Ratio  
- Number of observations  

This helps determine how the strategy behaves under different market conditions.

---

## 📈 Visualizations

### Market Regime Chart
Displays rolling volatility alongside the threshold used to define regimes.

This helps illustrate how the market transitions between high-risk and low-risk environments over time.

---

### Strategy Performance by Regime
Shows how the strategy performs in each regime.

This highlights whether the strategy is better suited to stable or volatile conditions.

---

## 📊 Performance Metrics Explained

| Metric | Meaning |
|--------|--------|
| Annual Return | Average yearly performance within a regime |
| Volatility | Degree of fluctuation in returns |
| Sharpe Ratio | Risk-adjusted return efficiency |
| Observations | Number of data points in each regime |

---

## 🧠 Analyst Interpretation

This analysis demonstrates that trading strategy performance is strongly influenced by market conditions.

By defining regimes using volatility, the study moves from a subjective interpretation of market behavior to a structured and measurable approach.

The results show that the strategy does not perform uniformly across all environments. In some cases, it performs better during low-volatility periods where price movements are more stable. In other cases, performance may decline during high-volatility periods due to increased uncertainty and larger price fluctuations.

The Sharpe ratio provides additional insight into how efficiently the strategy converts risk into returns within each regime. Differences in Sharpe ratio between regimes indicate that the strategy is more effective under certain conditions than others.

This confirms an important principle:

👉 A trading strategy is not universally effective — its performance depends on the environment in which it is applied.

---

## 💡 Key Takeaways

- Market conditions can be defined objectively using volatility  
- Strategy performance varies across different environments  
- Risk-adjusted metrics provide deeper insight than returns alone  
- A single strategy may not be suitable for all market conditions  
- Understanding regimes helps improve decision-making and strategy design  

---

## ⚠️ Limitations

- Regimes are defined using a simple volatility threshold  
- Only one asset (EURUSD) is analyzed  
- No transaction costs included in this stage  
- Strategy logic remains relatively simple  

---

##  Next Step
The next project focuses on parameter optimization and model validation to ensure that strategy improvements are robust and not overly fitted to historical data.

---

## 📁 Project Structure
```text
day-09-market-regime/
├── day09_market_regime.ipynb
├── outputs/
│   ├── charts/
│   │   ├── day09_regime.png
│   │   └── day09_regime_equity.png
│   └── tables/
│       ├── day09_regime_performance.csv
│       └── day09_data.csv
└── README.md
