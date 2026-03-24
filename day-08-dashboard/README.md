# Day 8 – Strategy Dashboard & Performance Report (EURUSD)

## 📌 Project Overview
This project focuses on presenting trading strategy results in a clear and structured format through a performance dashboard.

After building, improving, and optimizing strategies in previous projects, this stage consolidates all key insights into a single view that supports better understanding and decision-making.

The goal is not just to analyze performance, but to communicate it effectively.

---

## 🎯 Objective
To create a dashboard that summarizes:

- Strategy performance  
- Risk characteristics  
- Trading activity  
- Market conditions  

in a way that is easy to interpret for both technical and non-technical audiences.

---

## 📊 Dataset
- **Asset:** EURUSD  
- **Frequency:** Daily data  
- **Source:** Derived from previous project outputs (Day 7)  

---

## 🛠️ Tools Used
- Python  
- Pandas  
- NumPy  
- Matplotlib  

---

## ⚙️ What This Project Does

This dashboard brings together multiple aspects of strategy evaluation:

### 1. Performance Tracking
- Displays how the strategy grows over time  
- Compares performance against a buy-and-hold approach  

### 2. Risk Analysis
- Highlights periods of losses using drawdown  
- Shows how risk evolves over time using rolling volatility  

### 3. Trading Activity
- Tracks how frequently the strategy trades  
- Helps assess whether the strategy is efficient or overly active  

### 4. Market Condition Awareness
- Introduces a structured way to view market conditions using volatility  
- Distinguishes between high-risk and low-risk environments  

---

## 📈 Visualizations

### Strategy Performance (Equity Curve)
Shows how the strategy grows over time compared to a passive approach.

This helps answer:
- Is the strategy profitable?  
- Is growth consistent?  

---

### Drawdown Chart
Shows the decline from peak performance.

This helps understand:
- how severe losses are  
- how long recovery periods may take  

---

### Rolling Volatility
Tracks how market risk changes over time.

This highlights:
- periods of stability  
- periods of increased uncertainty  

---

## 📊 Key Metrics Explained

| Metric | Meaning |
|--------|--------|
| Total Return | Overall profit or loss |
| Annual Return | Average yearly performance |
| Volatility | Degree of fluctuation (risk level) |
| Sharpe Ratio | Efficiency of return relative to risk |
| Max Drawdown | Largest loss experienced |

---

## 🧠 Analyst Interpretation

The dashboard provides a comprehensive view of the strategy’s performance by combining return, risk, and trading behavior into a single framework.

The equity curve shows how the strategy evolves over time, allowing us to assess whether growth is steady or inconsistent. While the strategy may generate positive returns, the path to achieving those returns can vary significantly.

The drawdown chart highlights the practical challenges of trading by showing periods where the strategy experiences losses. This is especially important, as even profitable strategies can go through difficult phases.

Rolling volatility provides insight into changing market conditions. It shows that risk is not constant and that the market can shift between stable and unstable periods.

By introducing a structured way to view market conditions, the analysis moves beyond simple observation and becomes more systematic. This helps evaluate whether the strategy behaves differently under varying levels of market risk.

Overall, the dashboard demonstrates that successful strategy evaluation requires balancing multiple factors, including return, risk, and consistency. It reinforces that performance should not be judged by profit alone, but by how the strategy behaves under different conditions.

---

## 💡 Key Takeaways

- Clear presentation is essential for effective decision-making  
- Strategy performance must be evaluated alongside risk  
- Drawdowns reveal the real challenges of trading  
- Market conditions change over time and affect performance  
- Structured analysis improves understanding beyond visual observation  

---

## ⚠️ Limitations

- Simplified dashboard (not interactive)  
- Based on a single asset (EURUSD)  
- No transaction costs included in this stage  
- Limited to historical analysis  

---

## 🚀 Next Step
The next project introduces formal market regime detection, allowing strategy performance to be evaluated under clearly defined market conditions.

---

## 📁 Project Structure
```text
day-08-dashboard/
├── day08_dashboard.ipynb
├── outputs/
│   ├── charts/
│   │   ├── day08_equity_dashboard.png
│   │   ├── day08_drawdown_dashboard.png
│   │   └── day08_rolling_vol.png
│   └── tables/
│       └── day08_report.csv
└── README.md
