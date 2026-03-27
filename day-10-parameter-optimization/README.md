# Day 10 – Strategy Parameter Optimization (EURUSD)

## 📌 Project Overview
This project focuses on improving trading strategy performance by systematically testing different parameter combinations rather than relying on arbitrary choices.

In earlier projects, moving average values such as 20 and 50 were used as default settings. This project evaluates whether those values are actually optimal by testing multiple combinations and comparing their performance.

The goal is to move from intuition-based parameter selection to a data-driven approach.

## 🎯 Objective
To answer a key question:

**Do different parameter choices significantly affect strategy performance?**

This project aims to:
- evaluate multiple parameter combinations  
- compare performance across configurations  
- identify parameter sensitivity  
- improve strategy robustness  


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

## ⚙️ Methodology

### 1. Define Parameter Grid
A range of moving average combinations is tested:

- Short-term windows: 10, 20, 30  
- Long-term windows: 50, 100, 150  

Each pair represents a different trading rule.


### 2. Strategy Construction
For each parameter combination:

- Calculate short and long moving averages  
- Generate trading signals  
- Compute strategy returns  
- Build equity curve  


### 3. Performance Evaluation
Each combination is evaluated using:

- Total Return  
- Sharpe Ratio (risk-adjusted performance)  

### 4. Results Aggregation
All combinations are stored in a results table for comparison.


### 5. Visualization
A heatmap is created to visualize how performance varies across parameter combinations.

## 📈 Visualizations

### Sharpe Ratio Heatmap
Displays performance across parameter combinations.

This helps identify:
- strong-performing regions  
- weak-performing configurations  
- sensitivity to parameter changes  

## 📊 Results Table Explained

The results table summarizes:

- each parameter combination  
- corresponding return  
- corresponding Sharpe ratio  

This allows for direct comparison of strategy performance under different configurations.


## 🧠 Analyst Interpretation

This analysis demonstrates that strategy performance is highly sensitive to parameter selection.

Different combinations of moving average windows produce significantly different outcomes. Some configurations generate higher returns, while others produce more stable and risk-efficient performance.

The Sharpe ratio provides deeper insight by showing how well each configuration balances return and risk. In many cases, the highest return does not correspond to the best Sharpe ratio, highlighting the importance of evaluating performance beyond profit alone.

The heatmap further reveals that performance is not random, but follows identifiable patterns across parameter combinations. This suggests that certain ranges of parameters are more suitable for the market conditions observed.

However, an important limitation of this approach is that all results are based on historical data. Selecting the “best” parameters from past performance introduces the risk of overfitting, where the strategy is tailored too closely to historical conditions and may not perform well in the future.

This highlights a key principle in quantitative analysis:

👉 The goal is not to find the best parameters for the past, but to identify robust parameters that can perform reasonably well across different conditions.


## 💡 Key Takeaways

- Strategy performance depends heavily on parameter selection  
- Not all parameter combinations are equally effective  
- Risk-adjusted performance is more informative than return alone  
- Visualization helps reveal performance patterns  
- Overfitting is a critical risk in parameter optimization  


## ⚠️ Limitations

- Based entirely on historical data  
- No transaction costs included  
- Limited parameter search space  
- Single asset (EURUSD)  


## 🚀 Next Step
The next project applies walk-forward validation to test whether optimized parameters remain effective on unseen data.


## 📁 Project Structure
```text
day-10-parameter-optimization/
├── day10_parameter_optimization.ipynb
├── outputs/
│   ├── charts/
│   │   └── day10_heatmap.png
│   └── tables/
│       └── day10_results.csv
└── README.md
