# Task-5-Energy-Consumption-Time-Series-Forecasting:
   This project focuses on forecasting household electricity consumption using **time series models** and **machine learning**.
We experiment with **ARIMA**, **Facebook Prophet**, and **XGBoost** to predict energy demand and compare their performance.

## Dataset:
We use the **Individual Household Electric Power Consumption Dataset**, which records electricity usage from a single house over four years (2006–2010).
* **File:** `household_power_consumption.txt`
* **Frequency:** 1-minute measurements
* **Target Variable:** `Global_active_power` (kilowatts)

We resample the data into **hourly averages** for easier modeling.


## Methods Used:

### Preprocessing:

* Combine `Date` + `Time` into a `datetime` index
* Keep only `Global_active_power`
* Resample to hourly frequency
* Handle missing values with interpolation

### Models Implemented:

1. **ARIMA (Auto-Regressive Integrated Moving Average):**
   * Classical statistical time series model
   * Captures trends and seasonality

2. **Prophet (by Facebook/Meta):**
   * Flexible forecasting tool for time series
   * Handles seasonality, holidays, and trends easily

3. **XGBoost (Extreme Gradient Boosting):**
   * Machine learning approach
   * Uses engineered time features (`hour`, `dayofweek`, `month`, `is_weekend`)

### Evaluation Metrics:

* **MAE (Mean Absolute Error)** – average magnitude of errors
* **RMSE (Root Mean Squared Error)** – penalizes larger errors

## Results:
After training and testing on the last 30 days of data:
* All models produce forecasts, but their accuracy differs.
* Results are compared using **MAE** and **RMSE**, and plotted visually.

(A bar chart in the notebook shows which model performed best).
