# Forecasting-Monthly-Wine-Sales
Used ARIMA, SARIMA, and exponential smoothing models to forecast monthly wine sales. Recommended the most accurate forecasting model with 95% confidence limits for business planning.


# 🍷 Vintage Insights: Time Series Forecasting of Wine Sales

---

## 🚀 Project Overview
📈 **Goal:** Analyze and forecast sales for two product lines — **Sparkling Wine** and **Rose Wine** — using robust time series methods, enabling the business to make informed decisions on inventory and marketing.

✅ **Datasets analyzed:**
- `Sparkling.csv`: Monthly sales data for Sparkling Wine (1980-1996)
- `Rose.csv`: Monthly sales data for Rose Wine (1980-1996)

---

## 🔍 Detailed Workflow & Tasks
✅ **1. Data Preparation & Time Series Conversion:**  
- Parsed `YearMonth` into `datetime64` to enable temporal analysis.

✅ **2. Exploratory Data Analysis & Decomposition:**  
- Plotted time series graphs to visually inspect trends and seasonality.
- Used both **additive and multiplicative seasonal decomposition** to dissect underlying patterns.

✅ **3. Data Splitting:**  
- Created training and test sets with **test data starting from 1991**, per rubric specification.

✅ **4. Built & Evaluated Forecasting Models:**  
- Implemented on training data, evaluated using RMSE on the test set:
  - Simple Exponential Smoothing (SES)
  - Holt’s Double Exponential Smoothing
  - Holt-Winters (Additive & Multiplicative)
  - Naïve, Simple Average, Linear Regression
  - **Automated ARIMA** (parameters selected via lowest AIC)

✅ **5. Stationarity Checks:**  
- Performed Augmented Dickey-Fuller (ADF) tests (alpha = 0.05) on original and differenced data.
- Documented hypotheses and interpretation to confirm stationarity.

✅ **6. Comprehensive Model Comparison Table:**  
| Model                     | Sparkling RMSE | Rose RMSE |
|----------------------------|---------------|-----------|
| SES                        | 1304.93       | 48.75     |
| Holt’s Double Exp          | 5291.88       | 46.31     |
| Holt-Winters Additive      | 378.95        | 17.65     |
| Holt-Winters Multiplicative| 403.41        | -         |
| Naïve, Simple Avg, Linear  | ~1275-3864    | ~9-51     |
| **ARIMA (auto_arima)**     | **355.93**    | **17.24** |

✅ **7. Forecasted Future Sales:**  
- Built optimal ARIMA models on the **entire dataset** and forecasted **12 months into the future**, including confidence intervals to guide business planning.

---

## 💼 Business Insights & Recommendations
- 📊 ARIMA models delivered the most accurate forecasts (lowest RMSE) for both wine types.
- 📈 Sparkling Wine sales showed a growing trend, supporting marketing investment.
- 📉 Rose Wine sales declined, suggesting the need for targeted promotions or portfolio reassessment.
- 🔍 Recommended regular model updates with new data, plus scenario planning for robust supply chain and inventory alignment.

---

## 📊 Key Visualizations
- **Time Series Plots:** Showcased sales trends from 1980-1996.
![ARIMA model Time series graph for Sparkling](https://github.com/user-attachments/assets/c9111fdb-f747-4fe1-b83b-d6cb74df51a3)

![ARIMA model Time series graph for Rose](https://github.com/user-attachments/assets/a9862d10-eb9b-44be-967b-7f0708fc8ffe)

- **Seasonal Decomposition:** Revealed trend + seasonality for Sparkling and Rose.
Please check the model report attached with the repository for the Trend anda Seasonality graphs.

- **Model Forecast Comparisons:** Displayed fits of smoothing & regression models.
Please check the report for the model Forecast Comparisons.

- **ARIMA 12-Month Forecasts:** Projected future sales with confidence bands.
![ARIMA Forecast: 12-Month Time Series Projection (Sparkling)](https://github.com/user-attachments/assets/c185e102-b709-4955-8a8e-38ba4734476b)

![ARIMA Forecast: 12-Month Time Series Projection(Rose)](https://github.com/user-attachments/assets/ff046269-6acb-4a64-bb43-6b80d2e78aa4)
---

## 🛠️ Tools & Skills Covered
- 🐍 **Python:** pandas, numpy, matplotlib, seaborn, statsmodels, pmdarima
- 📈 Time Series Analysis & Forecasting
- 📉 Statistical Testing (ADF for stationarity)
- ⚙️ Automated ARIMA modeling with AIC optimization
- 📝 Business reporting & actionable strategic recommendations

---

## ⚙️ How to Run
- Clone this repository, install packages (`pip install -r requirements.txt`), and open the Jupyter notebooks (`TSF_sparkling.ipynb`, `TSF_Rose.ipynb`) to explore the full analysis.

---

## 🤝 About Me
I completed this project end-to-end, from data cleaning through rigorous forecasting and business strategy, demonstrating my expertise in time series modeling and data-driven decision-making.

🔗 [LinkedIn](https://linkedin.com/in/yourprofile)

---

✅ **Thanks for exploring my time series forecasting work!**
