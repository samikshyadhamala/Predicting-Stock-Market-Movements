# Predicting-Stock-Market-Movements
# 📈 Predicting Stock Direction Using Market Sentiment and Machine Learning

This project explores the integration of historical financial data and social media sentiment (Reddit) to forecast one-day-ahead stock price movements. By utilizing supervised machine learning and ensemble tree-based models, the project provides a transparent and accurate framework for short-term trading decisions.

---

## 🚀 Project Overview

### 🔎 Problem
Stock markets are volatile and difficult to predict using historical price data alone.

### 💡 Solution
A sentiment-driven approach that combines traditional market indicators (Open, Close, High, Low, Volume) with Reddit-based sentiment analysis.

### ⭐ Key Highlight
Implementation of **Explainable AI (SHAP Analysis)** to interpret model decisions and ensure transparency.

---

## 📊 Dataset

- Source: Kaggle dataset  
- Rows: 12,069  
- Features: 14  

### Features Include:
- Financial data: Adj Close, Volume, Open, High, Low
- Reddit sentiment data: Post scores, comment counts, sentiment labels

### 🎯 Target Variable
Binary Classification:
- `1` → Price Increase  
- `-1` → Price Decrease  

---

## 🛠️ Methodology

### 1️⃣ Preprocessing
- Data cleaning
- Temporal feature engineering (Year, Month, DayOfWeek)
- Removal of rare neutral classes for statistical stability

### 2️⃣ Exploratory Data Analysis (EDA)
- Mann-Whitney U Test
- Chi-Square Test
- Identification of statistically significant predictive drivers

### 3️⃣ Models Trained
- Random Forest
- LightGBM
- Gradient Boosting

### 4️⃣ Optimization
- Hyperparameter tuning using `GridSearchCV`
- Cross-validation for improved generalization

---

## 📈 Key Results

| Model | Test Accuracy | ROC-AUC |
|-------|--------------|----------|
| **Random Forest (Best)** | **92.74%** | **0.9714** |
| LightGBM | 91.48% | 0.9684 |
| Gradient Boosting | 90.68% | 0.9535 |

The Random Forest model achieved the best performance after fine-tuning.

---

## 🔍 Explainable AI (XAI)

To avoid black-box predictions, this project uses **SHAP (Shapley Additive Explanations).**

### 🌍 Global Interpretation
- Adjusted Close and Volume are the strongest predictive drivers.
- Reddit sentiment contributes marginal but meaningful predictive power.

### 🎯 Local Interpretation
- SHAP force plots provide instance-level explanations.
- Enables transparency for individual daily predictions.

---

