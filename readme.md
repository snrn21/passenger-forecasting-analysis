# Time Series Forecasting: ARIMA, SARIMA, and Prophet

This repository contains a comparative analysis of time series forecasting models applied to monthly airline passenger data. We explore and evaluate three key models:

- ARIMA (AutoRegressive Integrated Moving Average)  
- SARIMA (Seasonal ARIMA)  
- Prophet (by Meta/Facebook)

Our goal is to forecast future passenger numbers and determine the best-performing model based on forecast accuracy.


## Dataset

- **Source**: Monthly airline passengers dataset (classic time series dataset).
- **Features**: 
  - `month`: Date column (monthly frequency)
  - `passengers`: Number of airline passengers


##  Models Implemented

### 1. **ARIMA**
- Model: `ARIMA(2,1,2)`
- Assumes linear trend, no seasonality.
- **MAE**: `41.84`

### 2. **SARIMA**
- Model: `SARIMA(1,1,1)(1,1,1,12)`
- Accounts for both trend and **seasonal** effects.
- **MAE**: `16.67`, **RMSE**: `21.62`

### 3. **Prophet**
- Facebook's automated time series forecasting library.
- Handles seasonality and changepoints.
- **MAE**: `34.95`, **RMSE**: `41.29`

---

## Results Summary

| Model                   | MAE    | RMSE   |
|------------------------|--------|--------|
| ARIMA(2,1,2)           | 41.84  | 55.22      |
| SARIMA(1,1,1)(1,1,1,12)| **16.67** | **21.62** |
| Prophet                | 34.95  | 41.29  |

 **Best Model**: **SARIMA**, due to its superior handling of seasonality and lowest error values.

---

## Visual Output

All models include plots showing forecasted values versus actuals.
