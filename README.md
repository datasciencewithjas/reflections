
### Welcome to Demand Prediction Project using ARIMA Model

An **ARIMA** model is a class of statistical models for analyzing and forecasting time series data.
It explicitly caters to a suite of standard structures in time series data, and as such provides a simple yet powerful method for making skillful time series forecasts.
**ARIMA** is an acronym that stands for AutoRegressive Integrated Moving Average. It is a generalization of the simpler AutoRegressive Moving Average and adds the notion of integration.

The parameters of the ARIMA model are defined as follows:

**p**: The number of lag observations included in the model, also called the lag order.

**d**: The number of times that the raw observations are differenced, also called the degree of differencing.

**q**: The size of the moving average window, also called the order of moving average.

# Usage

## Prepare Data in Hourly Time-Series Format

The data has to be grouped in into hourly time series.
And for each number of orders will be assigned.
This will be done by PreProcessing Step.


## Build and Train ARIMA Model

parameters :  



### Requirements

- Keras==2.1.6
- tensorflow==1.8.0
- numpy==1.14.3
- pandas==0.22.0
- scikit-learn==0.19.1

