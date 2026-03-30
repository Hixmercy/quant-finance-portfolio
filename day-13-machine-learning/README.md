# Day 13 – Machine Learning for Market Direction (EURUSD)

## 📌 Project Overview

This project introduces a machine learning approach to predicting market direction using engineered features.

After building structured datasets in the previous project (Day 12), this stage applies a predictive model to estimate whether EURUSD will move up or down the next day.

The project also goes beyond prediction by translating model outputs into a trading strategy and evaluating its real-world performance.


## 🎯 Objective

To answer a key question:

**Can machine learning improve decision-making in trading by predicting next-day market direction?**

This project aims to:
- train a predictive model using engineered features  
- evaluate classification performance  
- convert predictions into a trading strategy  
- assess strategy performance using financial metrics  


## 📊 Dataset

- **Asset:** EURUSD  
- **Frequency:** Daily data  
- **Source:** Feature dataset created in Day 12  
- **Contents:** Engineered features + target variable  

## 🛠️ Tools Used

- Python  
- Pandas  
- NumPy  
- Matplotlib  
- scikit-learn  

## ⚙️ Methodology

### 1. Feature Dataset
The dataset contains engineered features that describe:

- recent returns  
- trend  
- volatility  
- momentum  
- price structure  

These features provide a richer representation of market behavior.

### 2. Target Variable
A binary target is used:

- `1` → next-day price increase  
- `0` → next-day price decrease or no change  

This transforms the problem into a classification task.

### 3. Train/Test Split
The dataset is split into:

- **Training Set (70%)** → model learning  
- **Test Set (30%)** → performance evaluation  

The split preserves time order to reflect real-world conditions.


### 4. Model Training
A logistic regression model is used:

- simple  
- interpretable  
- suitable for baseline classification  


### 5. Prediction
The model generates predictions on the test dataset only.


### 6. Strategy Construction
Predictions are converted into trading decisions:

- predict up → take long position  
- predict down → stay out  

This ensures evaluation reflects actual trading behavior.


### 7. Performance Evaluation

Two levels of evaluation are used:

#### Model Performance
- Accuracy  
- Classification report  

#### Strategy Performance
- Total return  
- Annual return  
- Volatility  
- Sharpe ratio  
- Maximum drawdown  


## 📈 Visualizations

### 1. ML Strategy vs Buy-and-Hold
This chart compares the performance of the machine learning strategy against a passive benchmark.

It helps evaluate:
- profitability  
- consistency  
- relative performance  

### 2. Drawdown Chart
Shows how much the strategy declines during losing periods.

This highlights:
- downside risk  
- recovery behavior  
- real trading experience  

### 3. Feature Coefficients
Displays how strongly each feature influences the model.

This provides insight into:
- which signals matter most  
- model interpretability  


## 📊 Metrics Explained

### Model Metrics

| Metric | Meaning |
|--------|--------|
| Accuracy | Percentage of correct predictions |
| Precision/Recall | Quality of classification performance |


### Strategy Metrics

| Metric | Meaning |
|--------|--------|
| Total Return | Overall profitability |
| Annual Return | Average yearly return |
| Volatility | Degree of variability |
| Sharpe Ratio | Risk-adjusted performance |
| Max Drawdown | Largest loss from peak |

## 🧠 Analyst Interpretation

This project demonstrates that machine learning can be used to identify patterns in financial data, but prediction accuracy alone does not guarantee a successful trading strategy.

The model attempts to learn relationships between engineered features and future market direction. While it may achieve reasonable accuracy, the key question is whether those predictions translate into meaningful financial performance.

The equity curve provides insight into how the strategy performs over time relative to a passive benchmark. It reflects not only prediction quality, but also the effectiveness of the trading rule derived from those predictions.

The drawdown chart highlights the practical risks of the strategy. Even if returns are positive, large drawdowns can make the strategy difficult to follow in real-world conditions.

The feature coefficient output adds interpretability by showing which inputs have the strongest influence on the model’s decisions. This helps move the model away from being a black box and provides insight into the underlying drivers of predictions.

Overall, this project shows that machine learning is a powerful tool, but its effectiveness depends on how it is integrated into a complete trading framework.


## 💡 Key Takeaways

- Machine learning can detect patterns in market data  
- Prediction accuracy does not guarantee trading success  
- Strategy evaluation must go beyond classification metrics  
- Feature quality plays a major role in model performance  
- Interpretability helps improve understanding of model behavior  


## ⚠️ Limitations

- Simple linear model (logistic regression)  
- No hyperparameter tuning  
- Single asset (EURUSD)  
- No transaction costs included  
- No risk-based position sizing  


## 🚀 Next Step

The next project focuses on combining multiple strategies into a portfolio to improve stability and reduce

## 📁 Project Structure

text
day-13-machine-learning/
├── day13_machine_learning.ipynb
├── outputs/
│   ├── charts/
│   │   ├── day13_ml_vs_buyhold.png
│   │   ├── day13_ml_drawdown.png
│   │   └── day13_feature_coefficients.png
│   └── tables/
│       ├── day13_metrics.csv
│       ├── day13_predictions.csv
│       └── day13_feature_coefficients.csv
└── README.md
