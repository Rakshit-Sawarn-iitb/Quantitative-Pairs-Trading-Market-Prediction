# 📈 Quantitative Pairs Trading & Market Prediction

A complete quantitative finance pipeline that combines **statistical arbitrage**, **machine learning**, and **backtesting** to model and simulate trading strategies based on **pairs trading**.

This project identifies tradable stock pairs, builds predictive models (Random Forest and XGBoost), generates buy/sell signals, and evaluates trading performance through simulation.

---

## 🧠 Project Highlights

- 📉 Historical stock analysis and visualization  
- 🧪 Statistical tests: **ADF**, **Cointegration**, and **Correlation**  
- 🧮 Feature engineering from time series data  
- 🤖 Machine Learning models: **Random Forest** & **XGBoost**  
- 💡 Trading signal generation (Buy/Sell/Hold)  
- 📊 Full trading simulation with portfolio tracking and P&L  

---

## 🛠️ Workflow Overview

### 1. Imports
Essential libraries:
- `pandas`, `numpy`, `matplotlib`, `seaborn`
- `yfinance`, `pandas_datareader` for stock data
- `statsmodels` for econometric tests
- `scikit-learn`, `xgboost` for machine learning

---

### 2. Data Visualization

Plotting time series trends of stock pairs to visually identify co-moving pairs, such as:
- **ADBE** (Adobe) and **MSFT** (Microsoft)

---

### 3. Stationarity & Cointegration Analysis

We assess pair suitability for trading using:
- **ADF Test**: Checks for stationarity
- **Cointegration Test**: Validates long-term relationship
- **Correlation**: Measures degree of linear relationship

✅ Result: **ADBE and MSFT** found to be cointegrated and hence, tradable.

---

### 4. Feature Engineering

Built custom features:
- **Price Ratios**
- **Rolling Means**
- **Rolling Std Dev**
- **Z-scores**
- **Lags and Returns**

These were used as input features for both ML models.

---

### 5. Predictive Modeling

#### ✅ Model 1: Random Forest Regressor
- Trained to predict future price ratios
- Achieved decent prediction accuracy

#### ✅ Model 2: XGBoost Regressor
- Outperformed Random Forest in prediction accuracy
- Less prone to overfitting due to gradient boosting

---

### 6. Signal Generation

Buy/Sell signals were generated using predicted ratios:

```python
# Sample Logic (Random Forest)
if Predicted_Ratio > Actual_Ratio * 1.01:
    signal = 'Buy'
elif Predicted_Ratio < Actual_Ratio * 0.99:
    signal = 'Sell'
else:
    signal = 'Hold'
