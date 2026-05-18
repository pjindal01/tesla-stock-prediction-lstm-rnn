# tesla-stock-prediction-lstm-rnn
Tesla stock price forecasting using LSTM and SimpleRNN for 1-, 5-, and 10-day horizons. GridSearchCV hyperparameter tuning. SimpleRNN best val loss 1.76e-4 (scaled). Deployed via Streamlit. Python · TensorFlow · Keras
[Uploading R# 📈 Tesla Stock Price Prediction — LSTM vs SimpleRNN

> Forecasts Tesla closing price 1, 5, and 10 days ahead using LSTM and SimpleRNN. Hyperparameters tuned with GridSearchCV. Deployed via Streamlit.

---

## 📌 Problem Statement
Stock price forecasting using deep learning models that can capture sequential dependencies in time-series data. This project compares LSTM and SimpleRNN architectures on Tesla (TSLA) historical price data and selects the best model for short-term forecasting.

## 📊 Key Results

| Metric | LSTM | SimpleRNN |
|---|---|---|
| Best 1-day val loss (scaled) | 2.91e−4 | **1.76e−4** |
| Hyperparameter tuning | GridSearchCV | GridSearchCV |
| Forecasting horizons | 1-day, 5-day, 10-day | 1-day, 5-day, 10-day |

> **Finding:** SimpleRNN achieved lower validation loss on the 1-day forecast. LSTM showed stronger performance on longer horizons. Both models were tuned via GridSearchCV.

## 🛠️ Tech Stack
`Python` · `TensorFlow` · `Keras` · `LSTM` · `SimpleRNN` · `GridSearchCV` · `MinMaxScaler` · `Streamlit` · `Matplotlib`

## 📁 Project Structure
```
Tesla_Stock_Prediction/
│
├── Tesla_Stock_Price_Prediction.ipynb   ← Main notebook
├── TSLA.csv                             ← Dataset (place here)
├── requirements.txt
└── README.md
```

## ▶️ How to Run
```bash
pip install -r requirements.txt
jupyter notebook Tesla_Stock_Price_Prediction.ipynb
# Expected runtime: 15–25 minutes (GridSearchCV is slow — this is normal)
```

## 📂 Dataset
- **Source:** [Yahoo Finance / Kaggle TSLA historical data](https://finance.yahoo.com)
- **Features used:** Date, Open, High, Low, Close, Adj Close, Volume
- **Target:** Adjusted closing price (normalized)

## 🔍 Pipeline Steps
1. Load and explore TSLA.csv
2. Normalize prices using MinMaxScaler
3. Create time-series sequences (sliding window)
4. Build SimpleRNN model → train → evaluate
5. Build LSTM model → train → evaluate
6. GridSearchCV for hyperparameter tuning
7. Compare 1-day, 5-day, 10-day forecasts
8. Plot actual vs predicted prices
9. Deploy via Streamlit

## ⚠️ Honest Limitations
- Stock price prediction is inherently uncertain
- Model does not incorporate news sentiment or macroeconomic data
- Results should not be used for actual trading decisions

---
*Project completed as part of AI/ML Internship at Labmentix Pvt. Ltd. (2025–2026)*
EADME_Tesla_LSTM.md…]()
