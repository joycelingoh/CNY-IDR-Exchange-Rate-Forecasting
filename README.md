# CNY/IDR Exchange Rate Forecasting

A time series forecasting project that compares several forecasting methods to predict the **Chinese Yuan (CNY) to Indonesian Rupiah (IDR) exchange rate**.

## 📌 About

This project uses daily CNY/IDR closing exchange rate data from **January 2024 to May 2026**, consisting of **630 observations**. The data is divided chronologically into **80% training data and 20% testing data**.

The main goal is to compare different forecasting approaches and determine which model provides the most accurate predictions.

## 🔍 Methods

Five forecasting methods were compared:

* **ARIMA** – models the relationship between current and past values after differencing the non-stationary series.
* **SARIMA** – extends ARIMA by considering possible seasonal patterns.
* **Double Moving Average (DMA)** – smooths the data twice to capture the underlying trend.
* **Random Forest** – uses lagged exchange rate values as predictors in an ensemble of decision trees.
* **NNAR** – uses lagged observations as inputs to a neural network for forecasting.

The models were evaluated using **RMSE, MAE, and MAPE**, where lower values indicate better forecasting performance.

## 📊 Results

| Model         |       RMSE |        MAE |       MAPE |
| ------------- | ---------: | ---------: | ---------: |
| **DMA(24)**   | **64.025** | **49.929** | **1.985%** |
| ARIMA(0,1,0)  |    128.639 |    108.585 |     4.336% |
| NNAR(5,9)     |    128.751 |    108.689 |     4.340% |
| SARIMA        |    128.936 |    108.919 |     4.350% |
| Random Forest |    131.176 |    111.813 |     4.466% |

### 🏆 Best Model

**DMA(24)** achieved the best performance with a **MAPE of 1.985%**. It was better at following the strong upward trend in the CNY/IDR exchange rate compared with the other models.

The results suggest that the exchange rate during the study period was mainly characterized by a **strong trend**, making the smoothing-based DMA approach more effective than the other methods tested.

## 🛠️ Workflow

1. Data Collection
2. Data Preprocessing
3. Exploratory Data Analysis
4. Stationarity Testing
5. Train-Test Split
6. Model Development
7. Model Evaluation
8. Model Comparison

## 📄 Research Paper

**A Comparative Study of ARIMA, Double Moving Average, Random Forest, and Neural Network Autoregression Models for CNY/IDR Exchange Rate Forecasting**

**Authors:**

* Joycelin
* Carmenita Angelica

**BINUS University**
