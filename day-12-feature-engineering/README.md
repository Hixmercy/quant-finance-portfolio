# Day 12 – Feature Engineering for Market Prediction (EURUSD)

## 📌 Project Overview
This project focuses on transforming raw EURUSD market data into a structured set of features that can be used for predictive modeling.

Rather than relying solely on price or a few standard indicators, this stage expands the dataset to capture multiple dimensions of market behavior, including momentum, volatility, recent returns, and price structure.

The goal is to build a richer dataset that can improve the ability of machine learning models to detect patterns and make predictions.


## 🎯 Objective
To answer a key question:

**How can raw market data be transformed into meaningful inputs for predictive models?**

This project aims to:
- create a prediction target  
- generate multiple feature categories  
- capture different aspects of market behavior  
- prepare a dataset for machine learning  


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

### 1. Target Variable Creation
A binary target variable is created to represent next-day market direction:

- `1` → price increases  
- `0` → price decreases or remains unchanged  

This transforms the problem into a classification task.

### 2. Lag Features
Lagged returns are used to capture short-term memory in the market.

Examples:
- return from 1 day ago  
- return from 2 days ago  
- return from 3 and 5 days ago  

These features help the model understand recent behavior.

### 3. Rolling Statistics
Rolling metrics summarize local trends and risk:

- rolling mean (trend)  
- rolling standard deviation (volatility)  

These features provide context beyond single-day movements.


### 4. Momentum Features
Momentum features measure how strongly price has moved over time.

Examples:
- 3-day momentum  
- 5-day momentum  
- 10-day momentum  

These help capture directional strength.

### 5. Price Structure Features
These features describe how price behaves within each day:

- high-low range (intraday volatility)  
- open-close movement (daily direction strength)  

They provide insight into market behavior beyond closing prices.

### 6. Technical Indicator Features
Traditional indicators are included as part of a broader feature set:

- Moving average ratio  
- RSI (Relative Strength Index)  
- MACD (Momentum indicator)  

Rather than relying on them alone, they are used alongside other features.


### 7. Data Cleaning
Rows with missing values (due to rolling calculations) are removed to ensure a clean dataset for modeling.


### 8. Feature Selection
A structured dataset is created containing:

- engineered features  
- target variable  

This dataset is ready for machine learning.


## 📈 Visualizations

### Feature Correlation Matrix
Displays relationships between features.

This helps identify:
- redundant features  
- strongly related variables  
- potential multicollinearity  


### Target Distribution
Shows how balanced the prediction problem is.

This is important because imbalanced data can affect model performance.


## 📊 Feature Summary Table

A feature summary table is created to describe:

- each feature  
- what it represents  
- how it contributes to the model  

This improves interpretability and transparency.

## 🧠 Analyst Interpretation

This project demonstrates that predictive modeling in financial markets depends heavily on how data is structured.

Rather than relying on raw prices alone, the engineered features capture different dimensions of market behavior, including recent history, trend, volatility, and momentum.

Lag features introduce memory into the dataset, allowing the model to consider past movements. Rolling statistics provide context by summarizing recent trends and variability. Momentum features capture directional strength, while price structure features describe how the market behaves within each trading period.

The correlation matrix highlights relationships between features, helping identify whether some variables provide overlapping information. This is important because highly correlated features may reduce model efficiency.

The target distribution provides insight into the nature of the prediction problem. A balanced target suggests that the model is not biased toward one outcome, while an imbalance may require additional handling.

Overall, this project shows that successful machine learning in finance is not just about choosing an algorithm, but about carefully designing the inputs that the model learns from.



## 💡 Key Takeaways

- Feature engineering is a critical step in predictive modeling  
- Raw market data must be transformed into meaningful signals  
- Different feature types capture different aspects of market behavior  
- Correlation analysis helps understand relationships between features  
- Model performance depends heavily on feature quality  


## ⚠️ Limitations

- Features are based on historical data only  
- No feature selection or dimensionality reduction applied  
- Single asset (EURUSD)  
- No advanced statistical modeling (e.g., GARCH) included  


## 🚀 Next Step
The next project applies machine learning techniques to this engineered dataset to predict market direction and evaluate performance.


## 📁 Project Structure
```text
day-12-feature-engineering/
├── day12_feature_engineering.ipynb
├── outputs/
│   ├── charts/
│   │   ├── day12_feature_correlation.png
│   │   └── day12_target_distribution.png
│   └── tables/
│       ├── day12_feature_dataset.csv
│       └── day12_feature_summary.csv
└── README.md
