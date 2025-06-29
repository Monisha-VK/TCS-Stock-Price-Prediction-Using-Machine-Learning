# TCS-Stock-Price-Prediction-Using-Machine-Learning
Developed a predictive model for TCS stock prices using machine learning, achieving ~0.74 R² and delivering key insights through professional data visualizations.
#  TCS Stock Price Prediction Using Machine Learning

This project aims to predict the **closing stock price of Tata Consultancy Services (TCS)** using historical data and a Linear Regression model. By exploring daily price movements and engineered time-based features, it provides insights into stock trends and builds a predictive model with solid performance.

---

##  Objective
To analyze TCS historical stock data, identify key factors influencing its price, and build a regression model capable of forecasting future closing prices.

---

##  Dataset
- Historical stock data for TCS containing:
  - Date
  - Open, High, Low, Close prices
  - Volume
- Engineered features:
  - Previous Close
  - Day of Week
  - Month

---

##  Tools & Technologies
- Python (pandas, numpy)
- Jupyter Notebook
- Data Visualization: matplotlib, seaborn
- Machine Learning: scikit-learn (Linear Regression)
- Model Serialization: pickle

---

## 📊 Key Steps
- **Data Preprocessing:**
  - Converted dates, extracted day/month, created Previous Close feature.
  - Removed missing or anomalous entries.
- **EDA:**
  - Plotted historical closing prices to identify trends.
  - Analyzed moving averages (50-day & 200-day) to observe momentum.
- **Model Building:**
  - Split data into training/testing sets (80/20).
  - Trained Linear Regression model.
  - Evaluated using R² (~0.74) and RMSE (~354).
- **Visualizations:**
  - Historical price trend
  - Moving averages
  - Actual vs Predicted prices scatter plot.

---

##  Sample Visualizations

**1️. Historical TCS Closing Prices Over Time**  
Shows the steady growth of TCS stock, with notable rises post-2016 and post-COVID recovery.

**2️. TCS Closing Price with 50-day and 200-day Moving Averages**  
Illustrates market trends and momentum.

**3️. Actual vs Predicted Close Prices**  
Highlights model performance; points closer to the diagonal indicate better predictions.

---

##  Model Saving
The trained model is saved using pickle for future use:
```python
import pickle
with open('TCS_Stock_Predictor.pkl', 'wb') as file:
    pickle.dump(model, file)
