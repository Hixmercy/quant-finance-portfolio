# Day 7 – Risk Optimization & Position Sizing (EURUSD)

## 📌 Project Overview
This project focuses on improving trading strategy performance by introducing risk control through dynamic position sizing.

Rather than using a fixed position size for every trade, this approach adjusts exposure based on market volatility. This allows the strategy to reduce risk during unstable periods and take advantage of more stable conditions.

The goal is to create a more balanced and realistic trading system that prioritizes consistency and risk management.

---

## 🎯 Objective
To enhance a trading strategy by:

- Controlling risk dynamically  
- Adjusting position size based on market conditions  
- Improving risk-adjusted performance  
- Reducing drawdowns  

---

## 📊 Dataset
- **Asset:** EURUSD  
- **Frequency:** Daily data  
- **Source:** Dataset prepared in Day 1  

---

## 🛠️ Tools Used
- Python  
- Pandas  
- NumPy  
- Matplotlib  

---

## ⚙️ Strategy Concept

The base strategy is a simple trend-following approach using moving averages:

- Enter the market when short-term trend (SMA 20) is above long-term trend (SMA 50)  
- Exit when the trend weakens  

---

## 🔥 Key Improvement: Risk-Based Position Sizing

Instead of trading the same size every time, this strategy adjusts position size based on volatility.

### How it works:

- When market volatility is **high** → reduce position size  
- When market volatility is **low** → increase position size  

This approach is known as **volatility targeting**.

---

## 🔍 Methodology

### 1. Calculate Strategy Signals
- Generate buy/exit signals using moving average crossover  

### 2. Measure Market Risk
- Compute rolling volatility using recent returns  

### 3. Adjust Position Size
- Scale position size inversely with volatility  
- Cap maximum exposure to avoid excessive leverage  

### 4. Compute Strategy Returns
- Apply position size to returns  
- Construct equity curve  

### 5. Evaluate Performance
- Analyze return, volatility, Sharpe ratio, and drawdown  

---

## 📈 Visualizations

### 1. Strategy vs Buy-and-Hold
Shows how the risk-adjusted strategy performs relative to a passive approach.

### 2. Drawdown Chart
Highlights the worst periods of loss and how deep declines can be.

### 3. Rolling Volatility
Illustrates how market risk changes over time.

---

## 📊 Performance Metrics Explained

| Metric | Meaning |
|--------|--------|
| Return | Overall profitability of the strategy |
| Volatility | How unstable the returns are |
| Sharpe Ratio | Efficiency of return relative to risk |
| Max Drawdown | Largest loss experienced |

---

## 🧠 Analyst Interpretation

This project demonstrates the impact of incorporating risk control into a trading strategy.

The results show that adjusting position size based on volatility helps manage exposure during uncertain market conditions. During periods of high volatility, the strategy reduces risk, which helps limit potential losses. In calmer periods, it increases exposure to take advantage of more stable price movements.

While the overall return remains modest, the approach improves the structure and consistency of the strategy. However, the relatively low Sharpe ratio indicates that the strategy is not yet highly efficient in converting risk into strong returns.

The drawdown results show that even with risk management, significant losses can still occur. This highlights that risk control reduces but does not eliminate downside risk.

Overall, the strategy becomes more realistic and robust, but further improvements are needed to enhance performance.

---

## 💡 Key Takeaways

- Risk should be actively managed, not ignored  
- Position sizing plays a critical role in strategy performance  
- High volatility periods require reduced exposure  
- Risk-adjusted performance is more important than raw return  
- No strategy is risk-free, even with optimization  

---

## ⚠️ Limitations

- No transaction costs included  
- Single asset (EURUSD)  
- No diversification  
- Fixed volatility target  
- Simplified position sizing model  

---

## Next Step
The next project will focus on building a performance dashboard to present strategy results clearly and support better decision-making.

---

## 📁 Project Structure
```text
day-07-risk-optimization/
├── day07_risk_optimization.ipynb
├── outputs/
│   ├── charts/
│   │   ├── day07_equity.png
│   │   └── day07_drawdown.png
│   └── tables/
│       ├── day07_metrics.csv
│       └── day07_data.csv
└── README.md
