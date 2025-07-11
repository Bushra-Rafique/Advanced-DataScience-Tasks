# Advanced Task 3: Energy Consumption Time Series Forecasting

## Objective:
Forecast short-term household energy usage using historical time-based patterns from real-world electrical consumption data.

## Dataset:
- **Name**: Household Power Consumption Dataset  
- **Source**: UCI Machine Learning Repository (https://archive.ics.uci.edu/ml/datasets/individual+household+electric+power+consumption)  
- **File Used**: `household_power_consumption.txt`  
- **Target Variable**: `Global_active_power` (kilowatts)

## Workflow Summary:

### Data Preprocessing:
- Parsed datetime from `Date` and `Time` columns
- Filtered and cleaned missing values (`?`)
- Converted `Global_active_power` to numeric
- Resampled the time series to **hourly average**

### Feature Engineering:
- Extracted time-based features:
  - Hour of the day
  - Day of the week
  - Weekend indicator
- Created lag-based features for XGBoost:
  - Lag 1 hour
  - Lag 24 hours


## Models Used:

### 1. **ARIMA**
- AutoRegressive Integrated Moving Average
- Trained on hourly values
- Forecasted next 30 days
- Evaluated with MAE & RMSE

### 2. **Prophet**
- Facebook’s additive time series model
- Captured daily and weekly seasonality
- Produced future dataframe and forecasts

### 3. **XGBoost**
- Used lag + time features for regression
- Supervised learning approach to forecasting
- Outperformed others in some scenarios


## Evaluation Metrics:

| Model   | MAE   | RMSE  |
|---------|-------|--------|
| ARIMA   | 0.669927| 0.829697 |
| Prophet | 0.563392 | 0.728328 |
| XGBoost | 0.376205 | 0.548930 |


## Visualization:
- Actual vs Forecasted plots for 30-day horizon
- X-axis: Time (hourly)
- Y-axis: Global active power (kW)
- Clear overlay of model predictions

## Skills Gained:
- Time series modeling with ARIMA, Prophet, and XGBoost
- Time feature engineering (lags, hour, day)
- Forecast evaluation (MAE, RMSE)
- Visualization of temporal predictions

## Tools & Libraries Used:
- Python
- pandas, numpy
- matplotlib, seaborn
- statsmodels (ARIMA)
- Prophet (from `prophet`)
- scikit-learn
- XGBoost
