# Day 3 – Volatility & Risk Analysis (EURUSD)

##  Objective
The goal of this project is to understand the risk characteristics of the EURUSD market by analyzing how volatile it is, how risk changes over time, and how much potential loss a trader might face.

---

## 📊 Dataset
- Asset: EURUSD  
- Source: Data prepared in Day 1  
- Frequency: Daily price data  

---

## 🛠️ Tools Used
- Python  
- Pandas  
- NumPy  
- Matplotlib  

---

## 🔍 What Was Done
This project focused on measuring and visualizing risk using:

- **Volatility** → to measure how unstable the market is  
- **Rolling Volatility** → to see how risk changes over time  
- **Value at Risk (VaR)** → to estimate potential losses  
- **Drawdown Analysis** → to understand peak-to-loss declines  

---

## 📈 Key Visualizations
- Rolling volatility chart  
- Return distribution with VaR threshold  
- Drawdown over time  

---

## 📊 Key Results
| Metric | Description |
|--------|------------|
| Daily Volatility | Measures how much price moves day-to-day |
| Annualized Volatility | Yearly estimate of market risk |
| Value at Risk (95%) | Estimated worst daily loss under normal conditions |
| Max Drawdown | Largest observed loss from peak to bottom |

---

## 🧠 Analyst Interpretation
This analysis shows that market risk is not constant. The rolling volatility chart reveals periods where the market becomes more unstable, meaning price movements become larger and less predictable.

The Value at Risk (VaR) helps quantify potential losses by showing how much could be lost on a bad trading day. This gives a realistic expectation of downside risk instead of relying on guesswork.

The drawdown chart highlights how much loss a trader could experience over time. Even in relatively stable markets, there are periods where prices decline significantly.

Overall, the results emphasize that risk management is essential. Understanding how risk behaves is just as important as identifying profitable opportunities in the market.

---

## 📁 Project Structure
day-03-volatility-risk/
│
├── day03_volatility_risk_analysis.ipynb
├── outputs/
│   ├── charts/
│   │   ├── day03_rolling_volatility.png
│   │   ├── day03_var_distribution.png
│   │   └── day03_drawdown.png
│   └── tables/
│       └── day03_risk_summary.csv
## 🚀 Key Takeaways
- Market risk changes over time and is not constant  
- High volatility periods increase uncertainty and potential losses  
- Extreme losses can occur even in stable markets  
- Drawdowns show the real impact of holding positions  
- Risk management is critical for long-term trading success  

---

## 🔮 Next Step
The next stage will focus on building trading strategies and testing their performance using the insights gained from risk and volatility analysis.
## 📊 Sample Visualization

![Rolling Volatility](outputs/charts/day03_rolling_volatility.png)
