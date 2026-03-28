# Day 11 – Walk-Forward Validation (EURUSD)

## 📌 Project Overview
This project focuses on evaluating whether a trading strategy that performs well on historical data can remain effective when applied to new, unseen data.

After identifying optimal strategy parameters in the previous project (Day 10), this stage introduces a more realistic evaluation approach by separating parameter selection from performance testing.

The goal is to reduce the risk of overfitting and assess the robustness of the strategy.

## 🎯 Objective
To answer a key question:

**Do optimized strategy parameters remain effective outside the data used to select them?**

This project aims to:
- separate training and testing data  
- optimize parameters on historical data  
- evaluate performance on unseen data  
- assess robustness and generalization  

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

### 1. Data Split (Train vs Test)
The dataset is divided into two parts:

- **Training Set (70%)** → used to select optimal parameters  
- **Test Set (30%)** → used to evaluate performance on unseen data  

This ensures that the model is not evaluated on the same data it was optimized on.


### 2. Parameter Optimization (Training Phase)
Using the training data:

- Multiple combinations of moving average parameters are tested  
- Strategy performance is evaluated using return and Sharpe ratio  
- The best-performing parameter combination is selected  

---

### 3. Out-of-Sample Testing (Test Phase)
The selected parameters are then applied to the test dataset:

- No re-optimization is performed  
- Strategy performance is evaluated under new conditions  

This simulates how the strategy would behave in a real-world scenario.


### 4. Performance Evaluation
The strategy is evaluated using:

- Total Return  
- Annual Return  
- Volatility  
- Sharpe Ratio  
- Maximum Drawdown  


## 📈 Visualizations

### Test Set Performance (Equity Curve)
Shows how the strategy performs on unseen data compared to a buy-and-hold approach.

### Drawdown Chart
Highlights periods of loss and the depth of declines during the test phase.

## 📊 Results Interpretation

The training optimization table shows which parameter combinations appeared strongest based on historical data.

The test results reveal whether those selected parameters remain effective when applied to new data.

This comparison helps determine whether the strategy has true predictive strength or was simply fitted to past conditions.


## 🧠 Analyst Interpretation

This project demonstrates the importance of separating parameter selection from performance evaluation.

The training phase identifies parameter combinations that appear optimal based on historical data. However, strong performance in this phase does not guarantee success in future conditions.

By applying the selected parameters to the test set, the analysis provides a more realistic assessment of strategy robustness.

If performance remains stable in the test phase, it suggests that the strategy may generalize well. If performance deteriorates significantly, it indicates that the optimized parameters may have been overfitted to historical data.

This highlights a key principle in quantitative finance:

👉 A strategy should not only perform well in-sample, but also maintain performance out-of-sample.


## 💡 Key Takeaways

- Strong historical performance does not guarantee future success  
- Overfitting is a major risk in strategy development  
- Separating training and testing data improves reliability  
- Walk-forward validation provides a more realistic evaluation framework  
- Robust strategies perform consistently across different datasets  


## ⚠️ Limitations

- Single split (no rolling walk-forward windows)  
- No transaction costs included  
- Limited parameter search space  
- Single asset (EURUSD)  


## 🚀 Next Step
The next project focuses on feature engineering to build richer inputs for machine learning-based market prediction.



## 📁 Project Structure
```text
day-11-walk-forward-validation/
├── day11_walk_forward_validation.ipynb
├── outputs/
│   ├── charts/
│   │   ├── day11_test_performance.png
│   │   └── day11_test_drawdown.png
│   └── tables/
│       ├── day11_train_optimization.csv
│       ├── day11_test_metrics.csv
│       └── day11_test_data.csv
└── README.md
