# Historical-Bitcoin-Volatility-Calculation

In this notebook, we will be computing the 20 trading days (or 1 month) Bitcoin historical volatility for the time period starting from September 12, 2014 to December 11, 2022. Historical Volatility gauges the fluctuations of underlying securities by measuring the price changes over a predetermined period of time in the past.

### 1. Import the Libraries
First, we will import the necessary libraries.

### 2.BTC-USD data 
We will fetch the Apple data using the pandas read_csv function. We will then, print the data to visualize it by using the head() function which prints the top 5 rows of the dataset.

### 3. Computing Log Returns 
Now we will compute the daily log returns by using the shift() function for adjusted closing prices of the security. We make use of the numpy library for computing log of today's closing price divided by yesterday's closing price. The log returns are stored in the DataFrame data under the column header 'Log Returns'.

### 4. Computing Historical Volatility
The one month (or 20 trading days) historical volatility will be computed by using the DataFrame.rolling(window).std() function which computes the rolling standard deviation of data['Log Returns'] for a period of 20 trading days. The standard deviation is multiplied by 100 to compute the percentage value for volatility. The historical volatility will be stored in the DataFrame under the column header '20 day Historical Volatility'. 

### 5.Plot the volatility 
We will now plot the historical volatilty to visualise how it changes over the period.
