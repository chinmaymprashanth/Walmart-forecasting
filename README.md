

## 🛒 M5 Forecasting: Walmart Sales Prediction using LightGBM

### 📌 Overview

This project tackles the **M5 Forecasting Challenge**, a time series forecasting problem involving Walmart sales data across thousands of products. The objective is to predict future daily sales at the product level using historical sales, calendar events, and price data.

### 🎯 Goal

Build a model to predict daily product-level sales for a 28-day forecast horizon and evaluate performance using **RMSE**.

---

### 📂 Dataset

The data comes from the [M5 Forecasting - Accuracy](https://www.kaggle.com/competitions/m5-forecasting-accuracy) competition and includes:

* `sales_train_validation.csv`: Historical daily unit sales per product.
* `calendar.csv`: Maps days to actual dates and includes event info.
* `sell_prices.csv`: Product prices across stores and time.
* `sales_train_evaluation.csv`: Final 28-day actual sales for evaluation.

---

### ⚙️ Feature Engineering

Key features engineered:

* **Lag features**: sales of past 7, 14, and 28 days
* **Rolling mean**: 7-day and 28-day moving averages
* **Date-based features**: day of week, month, etc.
* **Event/holiday encodings** from `calendar.csv`

---

### 🧠 Model

* Model: `LightGBM Regressor`
* Trained on transformed long-format data with lag-based features.
* Handled data for all 3 categories (`FOODS`, `HOUSEHOLD`, `HOBBIES`).

---

### 📊 Evaluation

* ✅ Final RMSE on evaluation set: **3.45**
* ✅ Visual comparison of actual vs predicted sales
* ✅ Feature importance chart to interpret model behavior

---

### 📈 Visualizations

1. **Actual vs Predicted Sales** for 5 randomly chosen products
2. **Feature Importance Plot**


---

### 🧪 Tools & Libraries

* Python, Pandas, NumPy
* LightGBM
* Scikit-learn
* Seaborn & Matplotlib
* Jupyter Notebook

---

### 🚀 Future Improvements

* Incorporate **promotions** and **SNAP** benefits
* Try **XGBoost** or **CatBoost** models
* Add holiday lags or weather data
* Streamlit dashboard for interactive forecast exploration

---

### 📁 Project Structure

```
📦 m5-forecasting-lightgbm
├── notebooks/
│   └── 01_model_training.ipynb
├── model/
│   └── final_lightgbm_model.pkl
├── output/
│   └── forecast_lightgbm_long1.csv
├── data/
│   ├── raw/       <- calendar.csv, sales_train_validation.csv, etc.
│   └── processed/ <- transformed long format files
├── README.md
└── requirements.txt
```

---

### 📌 Note on Data

```markdown
📦 Raw data not included due to size. You can download it directly from the [Kaggle competition page](https://www.kaggle.com/competitions/m5-forecasting-accuracy/data).
```


---

### ✅ Status

Project complete and ready for portfolio/demo purposes.

---

