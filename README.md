# Petstore Sales Forecasting Using SARIMA

## Project Overview

This project develops a time-series forecasting solution for a pet retail business using historical monthly sales data. The objective is to forecast future revenue trends and support business decisions related to inventory planning, demand forecasting, and revenue management.

The project analyzes sales data from January 2021 to March 2024 and applies ARIMA and SARIMA models to predict future sales performance.

---

## Business Problem

Management required a data-driven forecasting framework to:

* Forecast future monthly revenue
* Improve inventory planning
* Support demand forecasting
* Identify seasonal sales patterns
* Assist strategic business decision-making

---

## Dataset Information

* Time Period: January 2021 – March 2024
* Frequency: Monthly
* Target Variable: Revenue_INR

---

## Project Workflow

### 1. Data Preparation

* Loaded sales dataset
* Checked data types
* Validated date ranges
* Checked for missing values

### 2. Monthly Revenue Aggregation

Revenue was aggregated at the monthly level to create a time-series dataset suitable for forecasting.

### 3. Exploratory Data Analysis

Key findings:

* Revenue shows an upward growth trend
* Strong seasonal patterns are present
* Sales peaks occur towards year-end
* Revenue fluctuations increase as sales grow

### 4. Stationarity Testing

An Augmented Dickey-Fuller (ADF) test was performed.

Results:

* Original series was non-stationary
* First-order differencing achieved stationarity
* Differencing order selected: d = 1

### 5. Model Development

#### ARIMA Models Tested

* ARIMA(1,1,1)
* ARIMA(2,1,1)
* ARIMA(3,1,1)
* ARIMA(3,1,2)
* ARIMA(4,1,1)

#### SARIMA Models Tested

Multiple seasonal configurations were evaluated to capture yearly seasonality.

### 6. Model Evaluation

Models were compared using:

* AIC
* BIC
* MAE (Mean Absolute Error)
* RMSE (Root Mean Squared Error)

Best Model:

SARIMA(3,1,2)(1,1,0,12)

Performance:

* MAE: ₹430,150
* RMSE: ₹475,086

### 7. Forecasting

The selected SARIMA model was retrained using the complete dataset and used to forecast revenue for the next 12 months.

---

## Key Insights

* Revenue demonstrates consistent long-term growth.
* Strong annual seasonality exists within sales patterns.
* SARIMA significantly outperformed standard ARIMA models.
* Forecasts indicate continued business growth.

---

## Business Recommendations

1. Increase inventory levels before high-demand seasonal periods.
2. Align marketing campaigns with forecasted demand peaks.
3. Optimize procurement schedules using forecast outputs.
4. Use monthly forecasts for budgeting and revenue planning.

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Statsmodels
* Scikit-Learn

---

## Repository Structure

```text
petstore-sales-forecasting/
│
├── data/
├── notebooks/
├── images/
├── requirements.txt
└── README.md
```

---

## Future Improvements

* Facebook Prophet implementation
* XGBoost time-series forecasting
* Automated model selection
* Forecast confidence intervals
* Interactive dashboard using Tableau or Power BI

---

## Author

Siddharth

Aspiring Data Analyst | Business Analytics Enthusiast | Python | SQL | Tableau | Power BI
