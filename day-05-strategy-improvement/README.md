# Strategy Improvement & Signal Filtering (EURUSD) Day 5

## 📌 Project Overview
This project builds on the initial trading strategy developed in Day 4 by introducing improvements aimed at making the strategy more realistic, robust, and risk-aware.

Rather than simply building a strategy, the focus here is on **refining and improving performance** by reducing poor-quality trades and incorporating real-world trading costs.

---

## 🎯 Objective
The goal of this project is to answer:

**How can a simple trading strategy be improved to produce more reliable and realistic results?**

This involves:
- reducing false signals  
- improving trade quality  
- accounting for transaction costs  
- evaluating risk-adjusted performance  

---

## 📊 Dataset
- **Asset:** EURUSD  
- **Frequency:** Daily data  
- **Source:** Dataset prepared in Day 1  

The same dataset is used to maintain consistency across all projects.

---

## 🛠️ Tools Used
- Python  
- Pandas  
- NumPy  
- Matplotlib  

---

## ⚙️ Strategy Improvements

### 1. Signal Filtering (SMA + RSI)
The original strategy used only a moving average crossover.

This improved version adds a confirmation layer:

- Enter a trade only when:
  - Short-term trend is above long-term trend (SMA 20 > SMA 50)
  - Momentum is positive (RSI > 50)

 This helps avoid weak or uncertain market conditions.

---

### 2. Transaction Costs
A transaction cost was introduced to reflect real trading conditions.

- Cost applied when entering or exiting a trade  
- Simulates spread and execution costs  

 This ensures the strategy is not unrealistically profitable.

---

### 3. Trade Detection Logic
Trades are identified when position changes occur.

- Position changes → trade executed  
- No change → no cost applied  

This allows accurate cost modeling.

---

## 🔍 Methodology

### Step 1 — Indicator Calculation
- Compute 20-day and 50-day moving averages  
- Compute RSI (14-period)

### Step 2 — Signal Generation
- Generate signals using SMA crossover + RSI filter  

### Step 3 — Position Handling
- Shift signals to avoid look-ahead bias  

### Step 4 — Strategy Returns
- Apply position to daily returns  
- Subtract transaction costs when trades occur  

### Step 5 — Performance Evaluation
- Build equity curve  
- Calculate performance metrics  
- Analyze drawdowns  

---

## 📈 Visualizations

### 1. Strategy vs Buy-and-Hold
This chart compares the improved strategy against a passive approach.

It helps evaluate:
- consistency of growth  
- ability to avoid poor market conditions  

---

### 2. Drawdown Chart
Shows the decline from peak performance.

Helps understand:
- how severe losses are  
- how often they occur  
- recovery periods  

---

## 📊 Performance Metrics

| Metric | Meaning |
|--------|--------|
| Total Return | Overall profit or loss |
| Annual Return | Average yearly return |
| Volatility | Risk level of returns |
| Sharpe Ratio | Return adjusted for risk |
| Max Drawdown | Largest observed loss |

---

## 🧠 Analyst Interpretation
The improved strategy demonstrates how adding structure and discipline can enhance trading performance.

By combining trend signals (moving averages) with momentum confirmation (RSI), the strategy avoids entering trades during weak or uncertain conditions. This leads to fewer but higher-quality trades.

The inclusion of transaction costs highlights the importance of trading efficiency. Strategies that trade too frequently may appear profitable in theory but perform poorly in practice once costs are considered.

The results typically show improved consistency, reduced drawdowns, and better risk-adjusted performance compared to the original strategy.

This reinforces a key principle in quantitative trading:

👉 **Improving signal quality is more important than increasing trading frequency.**

---

## 💡 Key Takeaways
- Filtering signals reduces unnecessary trades  
- Fewer trades can lead to better performance  
- Transaction costs significantly impact strategy results  
- Risk-adjusted metrics are more important than raw returns  
- Strategy improvement is an iterative process  

---

## ⚠️ Limitations
- No transaction slippage beyond fixed cost  
- No short-selling logic  
- No position sizing or capital allocation  
- Uses a single asset (EURUSD)  

---

## 🚀 Next Step
The next stage will compare multiple strategies (SMA, RSI, MACD) to determine which performs best under different market conditions.

---

## 📁 Project Structure
```text
day-05-strategy-improvement/
├── day05_strategy_improvement.ipynb
├── outputs/
│   ├── charts/
│   │   ├── day05_strategy_vs_buyhold.png
│   │   └── day05_drawdown.png
│   └── tables/
│       ├── day05_metrics.csv
│       └── day05_data.csv
└── README.md
