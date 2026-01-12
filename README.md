# gold-price-forecasting
Time series analysis and forecasting of gold prices (2013-2025) using Moving Average, ARIMA, Exponential Smoothing, and GARCH models
Overview:
This project performs end-to-end time series analysis and forecasting of gold prices using classical statistical methods. It includes exploratory data analysis (EDA), stationarity testing, model selection, volatility modeling, and out-of-sample forecasting. The notebook implements ARIMA and ARIMA-GARCH frameworks to model both the mean process and conditional volatility of gold returns.
The objective is to understand historical gold price dynamics and construct models capable of forecasting future price levels and returns.

Key Objectives:
Import, clean, and preprocess historical gold price data
Perform exploratory time series visualization and diagnostics
Test for stationarity using statistical tests
Identify appropriate time-series model orders
Build and compare multiple forecasting models
Model volatility clustering using GARCH
Evaluate model performance using error metrics

Dataset:
File used: Gold Price1.csv
Contains historical gold price observations
Columns include:Date / Timestamp
                Gold price values
                Unused and extraneous columns are dropped during preprocessing

Methods and Workflow:
1. Data Preprocessing:
   Reading CSV data with pandas
   Handling redundant unnamed columns
   Renaming fields where required
   Converting dates to datetime format
   Indexing by date for time-series operations
   Handling missing values
   
3. Exploratory Data Analysis:
   Line plots of gold price evolution
   Distributional analysis
   Autocorrelation diagnostics:ACF plots
                               PACF plots
   Time-series decomposition:Trend
                             Seasonality
                             Residual components
4. Stationarity Testing:
   Augmented Dickey–Fuller (ADF) test
   Differencing procedure if required
   Analysis of returns series to achieve stationarity
   
5. Modeling Approaches:
   Models implemented include:
   Simple ARIMA models on price and returns
   Holt–Winters Exponential Smoothing
   ARIMA on returns + GARCH on residuals (volatility modeling)
   Packages used:
   statsmodels,arch,pmdarima
   
5. Volatility Modeling (GARCH):
   Residuals from ARIMA are modeled using:
   GARCH(1,1) with t-distribution innovations
   Captures volatility clustering typical in financial returns
   
7. Model Evaluation:
   Metrics computed include:
   Mean Squared Error (MSE)
   Mean Absolute Error (MAE)
   Mean Absolute Percentage Error (MAPE)
   Residual diagnostics and Ljung–Box test
   
8. Forecasting:
   In-sample and out-of-sample forecasts
   Confidence intervals for forecasts
   Visualization of forecasted paths versus observed data

8.Technologies Used:
   Python 3.x
   Jupyter Notebook
   Libraries:pandas
             numpy
             matplotlib
             seaborn
             statsmodels
             arch
             scikit-learn
             
9.Results and Insights:
   Gold price series is non-stationary in levels but stationary in returns
   ARIMA models effectively capture mean dynamics
   GARCH models capture time-varying volatility
   Combined ARIMA+GARCH provides improved financial modeling realism
   Forecast graphs illustrate expected forward movement and risk bands 
   
10.Future Enhancements:
   Include machine learning models (LSTM, XGBoost for time series)
   Add rolling forecast-origin validation
   Add dashboard or web app interface
   Incorporate macroeconomic exogenous variables (X-models)
