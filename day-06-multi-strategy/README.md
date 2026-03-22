# Day 6 – Multi-Strategy Comparison (EURUSD)

## 📌 Project Overview
This project compares multiple trading strategies applied to the EURUSD market to understand how different approaches perform under the same conditions.

Rather than focusing on a single strategy, this analysis evaluates three distinct trading styles:

- Trend-following (SMA)
- Mean-reversion (RSI)
- Momentum-based (MACD)

The goal is to understand not only which strategy performs better, but also how risk, consistency, and market conditions influence performance.

---

## 🎯 Objective
To answer a key question:

**Which trading strategy performs best, and under what conditions?**

This project emphasizes:
- comparing multiple strategies  
- evaluating performance using risk-adjusted metrics  
- understanding trade-offs between return and risk  

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

## ⚙️ Strategies Implemented

### 1. SMA Strategy (Trend-Following)
- Uses 20-day and 50-day moving averages  
- Enters trades when short-term trend exceeds long-term trend  

👉 Best suited for trending markets  

---

### 2. RSI Strategy (Mean-Reversion)
- Buys when market is oversold (RSI < 30)  
- Exits when momentum normalizes  

👉 Best suited for sideways or range-bound markets  

---

### 3. MACD Strategy (Momentum)
- Uses difference between short and long-term averages  
- Captures acceleration or deceleration in price movement  

👉 Balances trend and momentum signals  

---

## 🔍 Methodology

- Compute indicators (SMA, RSI, MACD)  
- Generate trading signals  
- Apply signals to historical returns  
- Construct equity curves  
- Evaluate performance using key metrics  

---

## 📈 Visualizations

### Strategy Comparison Chart
This chart compares how each strategy grows over time.

It helps answer:
- Which strategy grows more consistently?  
- Which experiences more fluctuations?  

---

## 📊 Performance Metrics Explained

| Metric | Meaning |
|--------|--------|
| Total Return | Overall profit or loss over the period |
| Volatility | How much returns fluctuate (risk level) |
| Sharpe Ratio | Return relative to risk taken |
| Drawdown | Largest loss from peak to bottom |

---

## 🧠 Analyst Interpretation

This analysis shows that different trading strategies behave very differently depending on how the market moves.

The trend-following strategy (SMA) tends to perform better when the market moves in a clear direction over time. It benefits from sustained upward or downward trends but may struggle when the market becomes unstable or moves sideways.

The mean-reversion strategy (RSI) attempts to capture short-term reversals. It performs better when the market frequently changes direction but may underperform when strong trends persist.

The momentum-based strategy (MACD) reacts to changes in market speed and direction. It can capture early signs of trend formation but may generate false signals during volatile periods.

Looking at the performance metrics provides deeper insight:

- **Total Return** shows how much each strategy gained overall, but does not reflect how smooth or stable the journey was.

- **Volatility** highlights how unpredictable each strategy is. Higher volatility means larger fluctuations, which can increase emotional and financial pressure.

- **Sharpe Ratio** is one of the most important measures because it balances return and risk. A strategy with a higher Sharpe ratio is generally more efficient and reliable.

- **Drawdown** shows the worst-case loss experienced. Even profitable strategies can have significant drawdowns, which are critical for real-world trading decisions.

The key takeaway is that no strategy is consistently superior in all market conditions. Each strategy has strengths and weaknesses depending on whether the market is trending, ranging, or volatile.

This reinforces an important principle:

👉 Successful trading often involves combining strategies or adapting to changing market conditions rather than relying on a single approach.

---

## 💡 Key Takeaways

- Different strategies perform better under different market conditions  
- High returns alone do not guarantee a good strategy  
- Risk and consistency are just as important as profitability  
- Sharpe ratio is a key measure of strategy quality  
- Drawdowns reveal the real challenges of trading  
- Combining strategies may improve overall performance  

---

## ⚠️ Limitations

- No transaction costs included  
- No position sizing or capital allocation  
- Single asset (EURUSD)  
- Simplified strategy logic  

---

## 🚀 Next Step

The next stage will focus on optimizing strategies and improving risk-adjusted performance through better filtering and parameter tuning.

---

## 📁 Project Structure
```text
day-06-multi-strategy/
├── day06_multi_strategy.ipynb
├── outputs/
│   ├── charts/
│   │   └── day06_strategy_comparison.png
│   └── tables/
│       ├── day06_metrics.csv
│       └── day06_data.csv
└── README.md
