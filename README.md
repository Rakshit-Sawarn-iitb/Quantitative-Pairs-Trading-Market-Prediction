# 🚀 Quantitative Pairs Trading & Market Prediction

**💹 93% ROI achieved** in a backtested machine learning-based trading strategy combining statistical arbitrage with model-driven signals.

This project brings together the world of **cointegration-based pairs trading** and **ML predictions** to simulate profitable trades on real historical stock data.

---

## 🧠 What’s Inside?

✅ Cointegration & stationarity tests to identify tradable stock pairs  
✅ Feature engineering from price spreads, rolling stats, and z-scores  
✅ ML Models: Random Forest & XGBoost for predicting price ratio movements  
✅ Model-generated **Buy/Sell signals**  
✅ **Full trading simulation** with realistic assumptions  
✅ 📈 **93% net portfolio gain** after simulated trading on ADBE-MSFT pair!

---

## 🔍 Strategy Breakdown

### 1. 📈 Data Visualization
- Visual exploration of historical price movements for stocks like **ADBE** and **MSFT**

### 2. 🧪 Statistical Testing
- **ADF Test** for stationarity
- **Cointegration Test** to verify long-term relationships
- **Pearson Correlation** for short-term co-movement

> ✅ Found that ADBE-MSFT are cointegrated — ideal for pairs trading.

### 3. 🧮 Feature Engineering
- Spread ratios
- Rolling means and std deviations
- Z-scores & lagged features

Used as input for predictive modeling.

---

## 🧠 Predictive Models

### ✅ Random Forest
- Trained on spread features to predict future price ratio

### ✅ XGBoost (🏆 Top Performer)
- Outperformed Random Forest in accuracy and signal reliability

---

## 📊 Trading Signal Generation

Predicted vs actual ratio used to generate trading signals:

```python
if predicted_ratio > actual_ratio * 1.01:
    signal = 'Buy'
elif predicted_ratio < actual_ratio * 0.99:
    signal = 'Sell'
else:
    signal = 'Hold'
```

Signal markers:
- ✅ Green ^ for Buy  
- ❌ Red v for Sell

---

## 💰 Backtesting Results

**Simulation Parameters:**
- Capital: ₹100,000  
- Transaction fee: 0.1%  
- Strategy: Fully position-based execution on signals

**📈 Final Portfolio Value: ₹193,000**  
**🏆 Net Profit: +₹93,000 (~93%)**  
**📉 Max Drawdown: Low**  
**📊 Win Rate: High with XGBoost**


---

## 📚 References

- QuantInsti Lectures on Pairs Trading
- Investopedia: Pairs Trading
- Statsmodels Docs for ADF and Cointegration

---
