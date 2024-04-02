# Unemployment Rate Forecasting | Time Series

## Overview
This project is centered on forecasting the monthly unemployment rate of the District of Columbia from 1960 to 2019 using SARIMA models. The aim is to apply the Box-Jenkins methodology for time series analysis to fit an appropriate model for predicting future unemployment rates.

## Data Source
The dataset was obtained from FRED Economic Data, which offers extensive economic data series, including the monthly unemployment rate for various regions

## Methodology
The project begins by splitting the data into a training set (first 708 entries) for model building and a test set (last 12 entries) for validation. A Box-Cox transformation was applied to stabilize variance and normalize the data. Various SARIMA models were then estimated, and the best fitting model was chosen based on the lowest AICc (Akaike Information Criterion corrected).

## Key Steps
1. Exploratory Data Analysis (EDA): Initial data examination to identify trends, seasonality, and variance in unemployment rates.
2. Data Transformation: Use of the Box-Cox transformation to normalize the data distribution.
3. Decomposition: Analysis to identify and remove trend and seasonality, achieving stationarity in the time series data.
4. Differencing: Application of differencing methods to further stabilize the variance.
5. Model Identification and Selection: Identification of candidate SARIMA models through ACF and PACF analysis, followed by selection based on the principle of parsimony and the lowest AICc.
6. Diagnostic Checking: Validation of the chosen model to ensure that residuals resemble white noise and the model is well-fitted.
7. Forecasting: Using the final model to forecast future unemployment rates and compare the forecasts with actual observed values in the test data.

## Final Model
The SARIMA model selected for forecasting was SARIMA (2,1,2)(1,0,1)[12] based on its lower AICc value and diagnostic checks. However, despite passing most diagnostic checks, the model failed the Shapiro-Wilk normality test and McLeod-Li test, indicating non-normal residuals.

## Results and Conclusion
Forecasting with the final model showed that predicted values were within the 95% confidence interval but did not closely match the test data. Thus, it was concluded that SARIMA (2,1,2)(1,0,1)[12] is not an accurate model for forecasting the monthly unemployment rate for the District of Columbia.

## References
- FRED Economic Data: Monthly unemployment rate of the District of Columbia from 1960 to 2019
- Additional resources and lecture slides used in the analysis are available on the UCSB course space.

## Appendix
The appendix of the project contains detailed plots and analyses, including:

- EDA visuals
- Box-Cox Transformation plots
- Decomposition results
- Differencing method details
- ACF and PACF analysis plots
- Diagnostic checking for selected models
- Forecasting comparisons
