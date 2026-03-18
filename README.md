# TS_Academy_Capstone_Project-
Using SARIMA MODEL to forecast truck sales. 

download the project' jupyter notebook here: [TS_Academy_capstonePROJECT_grp16.ipynb](https://github.com/user-attachments/files/26093383/TS_Academy_capstonePROJECT_grp16.ipynb)

**PROJECT OVERVIEW**

This project applies Time Series Analysis to forecast monthly truck sales using the SARIMA (Seasonal ARIMA) model.

It demonstrates a complete data science workflow:

Reading in dataset >>> statistical testing >>> model building >>> forecasting >>> evaluation


**OBJECTIVE**
- Analyze historical truck sales data
- Identify trends, seasonality, and patterns
- Build and validate a SARIMA model
- Forecast future truck sales with high accuracy


**DATASET**
- Source: Kaggle
  -https://www.kaggle.com/datasets/ddosad/dummy-truck-sales-for-time-series
- Dataset:dummy Truck sales dataset; source:
- type: Univariate 


**LIBRARIES**
- Python
- Pandas
- NumPy
- Matplotlib & Seaborn
- Statsmodels
- Scikit-learn


**PROJECT WORKFPLOW**
1. Data Loading & Exploration
- Dataset imported and inspected
- Dataset checks:
   - Shape
   - Data types
   - Summary statistics
     
2. **Data Preprocessing**
- Converted `Month-Year` column to datetime format
- Set datetime as index
- Sorted data chronologically

3. **Missing Values Analysis**
- Checked for null values
- No missing values found

4. **Exploratory Data Analysis (EDA)**
- Histogram and boxplot of truck sales
- Identified right-skewed distribution
- Time series visualization to observe patterns

5. **Time Series Analysis**
- Trend Analysis
  - Rolling mean (12-month window)
- Decomposition
  - Separated into:
  - Trend
  - Seasonality
  - Residuals

- Stationarity Test
  - Used Augmented Dickey-Fuller (ADF) Test
  - Applied:
    - First-order differencing
    - Seasonal differencing (lag = 12)
   
6. **ACF & PACF Analysis**
- Determined model parameters:
  - ARIMA Order: (1,1,3)
  - Seasonal Order: (1,1,3,12)

7. **Train-Test Split**
- 80% training
- 20% testing

8. **Model Building (SARIMA)**
- Model: SARIMAX
- Captures both trend and seasonality

9. **Forecasting**
- Generated predictions for test data
- Extended forecast for 48 months into the future

10. **Model Evaluation**
- Metrics used:
- MAE (Mean Absolute Error)
- RMSE (Root Mean Squared Error)
- RMS
- MAPE (Mean Absolute Percentage Error)

**Results:**
- MAPE: 3.30% which denotes an Excellent accuracy (<10%)
- Stable error distribution (RMSE ≈ MAE)

11. **Residual Analysis**
- Residual plots analyzed
- ACF of residuals checked
- Confirmed model adequacy

**Key note of the project**
- Strong seasonality in truck sales
- Data required differencing to achieve stationarity
- SARIMA model effectively captured temporal patterns
- Forecasting performance is highly accurate and reliable

**Contributors**
- Group 16 – Novara Cohort 2025
