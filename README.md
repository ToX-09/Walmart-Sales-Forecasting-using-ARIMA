# 🛒 Walmart Sales Forecasting using ARIMA

This project forecasts weekly sales for Walmart stores using classical time series modeling with **ARIMA**. It focuses on a granular level: individual `Store` and `Department` combinations, specifically `Store 1 - Dept 1`. Forecasts like these help businesses optimize inventory, reduce stockouts, and enhance planning accuracy.

---

## 📊 Problem Statement

Retailers like Walmart need to forecast product sales weekly to:
- Maintain optimal inventory levels
- Prevent overstock and understock situations
- Reduce holding costs and improve supply chain efficiency

---

## 🧠 Approach

This project uses the **ARIMA(1,1,1)** model for univariate time series forecasting. Here's the step-by-step approach:

- 📦 **Data Merging**: Combined sales, store, and feature datasets.
- 📈 **EDA**: Trends, seasonality, holiday impact, and outliers.
- 🧪 **Stationarity Check**: ADF Test + First-order differencing.
- 🔁 **ACF & PACF**: Determine ARIMA parameters.
- 📉 **Model Training**: ARIMA(1,1,1) on training set.
- 📊 **Evaluation**: RMSE, MAE, and MAPE on 12-week test set.

---

## 📂 Dataset

Source: [Kaggle - Walmart Store Sales Forecasting](https://www.kaggle.com/competitions/walmart-recruiting-store-sales-forecasting)

Files used:
- `train.csv`: Weekly sales per Store/Dept
- `features.csv`: Temperature, Fuel Prices, Holidays, CPI, Unemployment
- `stores.csv`: Store Type & Size metadata

---

## 📌 Results

| Metric | Value |
|--------|-------|
| MAE    | 2943.68 |
| RMSE   | 3302.16 |
| MAPE   | 13.67% |

✅ The model performs with a reasonably low error, especially considering sales volatility across departments and holiday spikes.

---

## 💼 Business Impact

> “This ARIMA-based forecasting model enables Walmart to anticipate weekly sales trends. It helps reduce overstocking and stockouts, potentially improving inventory efficiency by **15%** and cutting down holding costs.”

---

## 🛠️ Tech Stack

- Python (Pandas, NumPy, Matplotlib, Seaborn)
- Statsmodels (ARIMA)
- Scikit-learn (Evaluation Metrics)
- Jupyter Notebook

---

## ▶️ Run Locally

1. Clone the repository  
2. Place the dataset files inside a folder named `data/`  
3. Run the notebook:

```bash
pip install -r requirements.txt
jupyter notebook 01_arima_sales_forecasting.ipynb
```

---

## 📸 Sample Output

![Sales Forecast Sample](preview_forecast.png)

---

## 🧾 License

This project is for academic and portfolio use. Dataset provided by Walmart via Kaggle.

---

## ✨ Author

**Arkajyoti Sarkar**  
B.Tech in CSE (Data Science), MAKAUT  
LinkedIn: [@arkajyoti-sarkar](https://www.linkedin.com/in/arkajyoti-sarkar/)
