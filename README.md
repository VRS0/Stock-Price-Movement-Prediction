# 📈 Stock Price Prediction
A machine learning project that predicts whether a stock price will go **up or down** the next day — framed as a binary classification problem.

---

##  What It Does
Given historical stock data, the model outputs:

| Label | Meaning |
|-------|---------|
| `1` | Price going **up** → Buy signal |
| `0` | Price going **down** → Skip |

---

##  Features
Built from raw price data using common technical indicators:

- **Moving Averages (MA)** — smooths out short-term noise to reveal the trend
- **Daily Returns** — measures the day-to-day percentage change in price
- **RSI (Relative Strength Index)** — detects overbought or oversold conditions
- **Lagged Returns** — uses yesterday's movement as a predictive signal

---

##  Models Trained
Three classifiers were trained and compared:

- Logistic Regression
- Decision Tree
- Random Forest

The best performer was selected based on accuracy on the test set.

---

##  Results
The final model predicts next-day stock direction with **~70% accuracy** — a solid baseline for a binary market prediction task.

>  Educational Project

---

##  Future Improvements
- Add more technical indicators (MACD, Bollinger Bands)
- Try LSTM for sequence-based prediction
- Backtest on multiple stocks and timeframes
