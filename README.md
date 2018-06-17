
### Welcome to Demand Prediction Project using ARIMA Model

An **ARIMA** model is a class of statistical models for analyzing and forecasting time series data.
It explicitly caters to a suite of standard structures in time series data, and as such provides a simple yet powerful method for making skillful time series forecasts.
**ARIMA** is an acronym that stands for AutoRegressive Integrated Moving Average. It is a generalization of the simpler AutoRegressive Moving Average and adds the notion of integration.

The parameters of the ARIMA model are defined as follows:

**p**: The number of lag observations included in the model, also called the lag order.

**d**: The number of times that the raw observations are differenced, also called the degree of differencing.

**q**: The size of the moving average window, also called the order of moving average.

Use **(p,d,q)** to denote the orders for the non-seasonal components of the ARIMA models and 

**(P,D,Q,s)** to denote the orders for the seasonal components of the ARIMA model.


# Usage

## How to Run

Since this is Jupyter Notebook, we have to first install **runipy**

**pip install runipy**

Then on command line:

**runipy <name-of-jupyter-notebook>.ipyng**


## Importing Data

Data should be import from Oracle Server.

Data has following columns:
- 'ORDER_DATE' 
- 'FINISH_DATE'
- 'CUSTOMER_CODE'
- 'CUSTOMER_GPS_LAT',
- 'CUSTOMER_GPS_LON'
- 'DELIVERY_DISTANCE'
- 'PRODUCT_PRICE'

Data is saved inside the data folder.

## Prepare Data in Hourly Time-Series Format

The data has to be grouped in into hourly time series.

And for each hour number of orders will be assigned.

This will be done by **Preprocessing Step**.

For forecasting, only univariate time series(number of calls) were used.

## Build and Train ARIMA Model

In this project, **SARIMAX Model** was used, since time series is cyclic.

Used parameters:

(p,d,q) - (1,0,1)

(P,D,Q,s) - (1,1,0,24)

Those paramters were found using Grid Search.

But number of cycle should be tuned more when there will be available memory for storaga.

## Visualization of Results

First,line plot in HTML format for **predicted** and **actual** number of calls will be created and placed inside charts folder.

Then, HTML table will be also created and placed in inside charts folder.

## Requirements

- Python 3.6.1
- numpy==1.14.3
- pandas==0.22.0
- statsmodels==0.9.0
- bokeh==0.12.16
- jupyter==1.0.0
- jupyter-client==5.2.3
- jupyter-console==5.2.0
- jupyter-core==4.4.0
- notebook==5.4.1
- runipy==0.1.5
- ipywidgets==7.2.1





