# 🛒 M5 Forecasting: Walmart Sales Prediction using LightGBM

## 📌 Overview

This project tackles the **M5 Forecasting Challenge**, a time series forecasting problem involving Walmart sales data across thousands of products. The objective is to predict future daily sales at the product level using historical sales, calendar events, and price data.

---

## 🎯 Goal

Build a model to predict daily product-level sales for a **28-day forecast horizon** and evaluate performance using **RMSE**.

---

## 📂 Dataset

The data comes from the [M5 Forecasting - Accuracy](https://www.kaggle.com/competitions/m5-forecasting-accuracy/data) competition and includes:

- `sales_train_validation.csv`: Historical daily unit sales per product.
- `calendar.csv`: Maps days to actual dates and includes event info.
- `sell_prices.csv`: Product prices across stores and time.
- `sales_train_evaluation.csv`: Final 28-day actual sales for evaluation.

---

## ⚙️ Feature Engineering

Key features engineered:

- Lag features: past 7, 14, and 28 days
- Rolling means: 7-day and 28-day moving averages
- Date-based features: day of week, month, year
- Event/holiday flags from `calendar.csv`

---

## 🧠 Model

- Model: **LightGBM Regressor**
- Trained on long-format time series with lag-based features
- Covers all 3 item categories: `FOODS`, `HOUSEHOLD`, `HOBBIES`

---

## 📊 Evaluation

- ✅ **Final RMSE on evaluation set**: **3.45**
- ✅ Actual vs predicted plots for 5 random items
- ✅ Feature importance bar chart

---

## 📈 Visualizations

- 📌 Actual vs Predicted Sales (5 random products)
- 📌 Feature Importance (LightGBM)

---

## 🧪 Tools & Libraries

- Python, Pandas, NumPy
- LightGBM, Scikit-learn
- Seaborn, Matplotlib
- Jupyter Notebook

---

## 📦 Files in This Repository

- `Data_exploration.ipynb` – Initial EDA and insights
- `Feature_engineering_and_model.ipynb` – Feature creation + model training
- `final_lightgbm_model.pkl` – Saved LightGBM model
- `requirements.txt` – Dependencies
- `README.md` – Project documentation

---

## 🚀 Future Improvements

- Incorporate SNAP/EBT and promotion features
- Experiment with XGBoost or CatBoost
- Add holiday lags or weather-based external regressors
- Create a Streamlit dashboard for interactive exploration

---

## 📌 Notes

- The file `forecast_lightgbm_long1.csv` is **not included** due to GitHub size limits.
- Raw M5 data is **not included**. Download it from the [Kaggle competition page](https://www.kaggle.com/competitions/m5-forecasting-accuracy/data).
- To regenerate forecasts, place the raw files in `data/raw/`, load `final_lightgbm_model.pkl`, and run the notebook.

---

## ✅ Status

Project complete and ready for portfolio/demo purposes 🚀
