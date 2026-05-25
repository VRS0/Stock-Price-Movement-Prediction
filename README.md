# 📈 Stock Price Movement Prediction

Binary classification system for predicting next-day stock price direction using engineered technical indicators and machine learning.

---

## Overview

This project frames next-day price movement as a binary classification task — up or down — built on a pipeline of feature engineering, time-series-aware data splitting, and multi-model benchmarking to identify the most reliable trading signal.

---

## Technical Indicators

| Indicator | Description |
|-----------|-------------|
| RSI | Relative Strength Index — momentum oscillator |
| Daily Return | Percentage change in closing price day-over-day |
| Volume Ratio | Current volume relative to rolling average |
| Moving Averages | Short and long-term trend signals (SMA/EMA) |
| HL Range | High-Low spread as a volatility proxy |

---

## Methodology

- **Target Variable** — Binary label derived from next-day closing price direction, with temporal shifting applied to prevent data leakage
- **Data Splitting** — Time-series-aware partitioning with no random shuffling to preserve chronological order and reflect real trading conditions
- **EDA** — Distribution analysis on engineered features and closing price trend visualization across the full time horizon

---

## Models

Six models trained and benchmarked against the same temporal train/test split:

| Model | Type |
|-------|------|
| Logistic Regression | Linear baseline |
| Random Forest | Ensemble / bagging |
| Support Vector Machine | Kernel-based classifier |
| K-Nearest Neighbors | Instance-based learner |
| Decision Tree | Interpretable tree |
| Sequential Neural Network | Custom deep learning (Keras) |

Models evaluated on accuracy, precision, recall, and F1-score to assess trading signal reliability.

---

## Notes

- All features are computed using only past data relative to each row to eliminate lookahead bias
- Scaling is fit exclusively on the training set and applied to the test set
- Model selection prioritizes precision over raw accuracy given the cost asymmetry in trading signals
