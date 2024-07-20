#Power-Generation-Forecast-using-ARIMA-SARIMA
Source Data: https://cea.nic.in/?lang=en <br /> 
We gather conventional power generation data from the government website, which is open source. [check file : actual_dat_pg.csv] <br />
The collected data is cleaned, by handling missing values in the data frame. The ARIMA model at the end is just a trail and run for different p, d, q values. [Please refer to arima_forecast.ipynb][check file : Data_ml] <br />
We use 70% data for training, and 30% data for testing. We run prediction on the 30% testing data, and check accuracy for the model. However, the accuracy seems to be low on the data due to non stationarity of the data. [check file : arima_forcast.ipynb] <br />
We run dickey fuller test on the data to check stationarity, the pi-values from the test suggests the hypothesis. Usually, if pi values are greater than 0.5, the data is assumed to be non stationary. We perform different tests on the data, and perform dicker fuller tests, and generate pi-values for different tests. [check file : adf_stats] <br />
The most accurate tested data appears to be on "LOG_SQRT TIME SHIFTED". Hence, we carry on the testing on this data.  <br />
We perform Seasonal ARIMA on this data, and run prediction and forecasts.
