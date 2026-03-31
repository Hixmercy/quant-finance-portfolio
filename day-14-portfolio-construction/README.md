# Day 14 – Portfolio Construction & Strategy Allocation (EURUSD)

## 📌 Project Overview

This project introduces portfolio-level thinking by combining multiple trading strategies into a single system.

Rather than relying on one strategy alone, the analysis integrates different approaches—trend-following, mean-reversion, and momentum—into a unified portfolio.

The goal is to evaluate whether combining strategies can improve consistency, reduce risk, and produce more stable performance over time.

## 🎯 Objective

To answer a key question:

**Can combining multiple strategies create a more robust and stable trading system than relying on a single approach?**

This project aims to:
- construct multiple strategies  
- combine them into a portfolio  
- evaluate diversification benefits  
- compare portfolio vs individual strategies  

## 📊 Dataset

- **Asset:** EURUSD  
- **Frequency:** Daily data  
- **Source:** Dataset prepared in Day 1  

## 🛠️ Tools Used

- Python  
- Pandas  
- NumPy  
- Matplotlib

## ⚙️ Methodology

### 1. Strategy Construction

Three different strategies are built:

#### Trend Strategy (SMA)
- Uses moving averages to detect long-term direction  
- Captures trending market behavior  

#### Mean-Reversion Strategy (RSI)
- Identifies oversold conditions  
- Assumes price will revert to its average  

#### Momentum Strategy (MACD)
- Captures strength and continuation of price movement  

Each strategy generates its own signals and returns.

### 2. Portfolio Construction

The strategies are combined using equal weighting:

- SMA → 33%  
- RSI → 33%  
- MACD → 34%  

This creates a diversified portfolio of trading signals.

### 3. Equity Curve Construction

Equity curves are calculated for:
- each individual strategy  
- the combined portfolio  
- buy-and-hold benchmark  

### 4. Correlation Analysis

The correlation between strategy returns is analyzed to assess diversification benefits.

- Low correlation → better diversification  
- High correlation → limited benefit  

### 5. Performance Evaluation

Each component is evaluated using:

- Total Return  
- Annual Return  
- Volatility  
- Sharpe Ratio  
- Maximum Drawdown

## 📈 Visualizations

### 1. Portfolio vs Individual Strategies

This chart compares:
- portfolio performance  
- individual strategies  
- buy-and-hold benchmark  

It helps assess whether combining strategies improves overall results.

### 2. Portfolio Drawdown

Shows the depth and duration of losses.

This helps evaluate:
- downside risk  
- stability during difficult periods  

### 3. Strategy Correlation Matrix

Displays how strategy returns relate to each other.

This helps determine whether diversification is effective.

## 📊 Metrics Explained

| Metric | Meaning |
|--------|--------|
| Total Return | Overall profitability |
| Annual Return | Average yearly performance |
| Volatility | Degree of fluctuation |
| Sharpe Ratio | Risk-adjusted performance |
| Max Drawdown | Largest peak-to-trough loss |


## 🧠 Analyst Interpretation

This project demonstrates that portfolio construction is a key step in moving from isolated strategy analysis to a more robust trading framework.

Each individual strategy captures a different aspect of market behavior. The trend strategy performs better in sustained directional movements, the mean-reversion strategy benefits from short-term corrections, and the momentum strategy captures continuation patterns.

When combined, these strategies create a portfolio that is less dependent on any single market condition. The equity curve shows whether this combination leads to smoother and more consistent growth compared to individual strategies.

The drawdown chart provides insight into risk. A well-diversified portfolio should experience smaller or less frequent drawdowns than its components.

The correlation matrix is particularly important because it explains why diversification works. If strategies are highly correlated, they tend to move together, reducing diversification benefits. Lower correlation suggests that strategies respond differently to market conditions, improving overall stability.

The performance metrics confirm whether the portfolio achieves better risk-adjusted performance than individual strategies.

Overall, this project highlights that combining strategies is not just about increasing returns, but about improving consistency and managing risk.

## 💡 Key Takeaways

- Diversification reduces dependence on a single strategy  
- Different strategies perform well under different conditions  
- Correlation plays a key role in portfolio effectiveness  
- Combining strategies can improve stability  
- Risk-adjusted performance is more important than return alone  

## ⚠️ Limitations

- Equal weighting (no optimization of weights)  
- Single asset (EURUSD)  
- No transaction costs included  
- No dynamic allocation or regime switching  

## 🚀 Next Step

The next project integrates feature engineering, prediction, and risk management into a full end-to-end trading system.

## 📁 Project Structure

```text
day-14-portfolio-construction/
├── day14_portfolio_construction.ipynb
├── outputs/
│   ├── charts/
│   │   ├── day14_portfolio_vs_strategies.png
│   │   ├── day14_portfolio_drawdown.png
│   │   └── day14_strategy_correlation.png
│   └── tables/
│       ├── day14_portfolio_metrics.csv
│       ├── day14_portfolio_data.csv
│       └── day14_strategy_correlation.csv
└── README.md
