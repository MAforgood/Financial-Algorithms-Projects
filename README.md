# Financial-Algorithms-Projects
These Are My Projects For Financial Algorithms Course Spring 2024
## Project 1 :VWAP Indicator
This strategy implementation employs the Volume Weighted Average Price (VWAP) indicator and utilizes its intersection with candlestick close prices.

When the indicator crosses above the candlestick close prices (cross over), it suggests a bullish trend, indicating it's favorable to place a buy order.

Conversely, when the indicator crosses below the candlestick close prices (cross under), it suggests a bearish trend, indicating it's better to place a sell order.

Additionally, stop loss (SL) and take profit (TP) levels are not defined in this strategy to allow for customizable risk management according to individual preferences.

To test the strategy over monthly intervals, timestamp data is utilized. By testing the strategy over monthly intervals, we aim to derive desired outcomes. Furthermore, the application of this strategy is observed across the top ten market-leading coins over monthly intervals.

For further details and implementation, kindly refer to the code and accompanying documentation.

## Project 2 : Combining Indicators
## Strategy 1: Moving Average and MACD Strategy

    Utilizes Moving Average (MA) and Moving Average Convergence Divergence (MACD) indicators.
    Generates long entry on close crossing above MA and MACD line crossing above signal line.
    Signals short entry on close crossing below MA and MACD line crossing below signal line.
    Exit conditions: opposite crossovers or specified date range (startYear to endYear).

## Strategy 2: Combined Moving Average and ATR Strategy with Date Range

    Combines Moving Average (MA) and Average True Range (ATR) indicators with a date range.
    Generates long entry on close crossing above MA and close exceeding MA plus multiplier times ATR.
    Signals short entry on close crossing below MA and close below MA minus multiplier times ATR.

## Project 3 :Time Series Analysis Project
This project involves conducting time series analysis on cryptocurrency data using various statistical techniques.
## Step 1: Unit Root Test (ADF Test)

    Retrieve historical data of the top five cryptocurrencies with the highest market capitalization from Yahoo Finance for a one-year period from November 1, 2022, to November 1, 2023, across three different timeframes (daily, four-hourly, and hourly).
    Apply the Augmented Dickey-Fuller (ADF) test to determine if the collected data are stationary with a confidence level of 90%. If multiple cryptocurrencies (and timeframes) exhibit stationary behavior above 90%, select the combination with the highest degree of stationarity and plot its price chart within the specified timeframe. If none of the top five cryptocurrencies are stationary within the specified timeframe and timeframes, explore lower-market-cap cryptocurrencies until identifying one with at least 90% stationarity.

## Step 2: Parameter Determination Using ACF and PACF

    For the identified stationary time series, plot the Autocorrelation Function (ACF) and Partial Autocorrelation Function (PACF) graphs.
    Determine appropriate values for the AR (Autoregressive), MA (Moving Average), and ARMA (Autoregressive Moving Average) parameters (p and q) based on the ACF and PACF plots.
    Utilize data from 11 months for training the AR, MA, and ARMA models (with determined parameters) and reserve the remaining month for testing purposes.
    Evaluate the performance of each model using Mean Squared Error (MSE) and Mean Absolute Percentage Error (MAPE).

## Step 3: Optimal Parameter Determination

    Employ a brute-force search method to discover optimal combinations of p and q values for each of the three models.
    Conduct a comprehensive search within the parameter space, ranging from 1 to 50 for both p and q values.
    Determine optimal values by selecting combinations that result in the lowest MSE and MAPE values. Compare these optimal values with those obtained from the ACF and PACF plots.

## Project 4 : ARIMA and GARCH Strategy Implementation

in this Project, we design a strategy utilizing two models: ARIMA for predicting future time series values and GARCH for estimating remaining volatility. The strategy aims to predict price changes in cryptocurrencies and generate buy/sell signals accordingly.
## Step 1: Data Collection and Preparation

    Retrieve historical data for Bitcoin and Ethereum over the past two years, on a daily timeframe.
    Split the data into a training period from July 1, 2021, to July 1, 2023, and a testing period from July 1, 2023, to November 1, 2023.

## Step 2: Strategy Implementation

    Implement the strategy using a Rolling Window technique.
    Use ARIMA models with various combinations of p, q, and d parameters within the ranges of p={0,...,5} and q={0,...,5}.
    Train ARIMA models and GARCH models on each window and generate buy/sell signals.
    Save the signals obtained from this strategy in a CSV file.

## Step 3: Backtesting

    Write a Backtest function to simulate buying and selling based on the generated signals with an initial capital of $100.

## Step 4: Performance Evaluation

    Calculate Performance Evaluation metrics including PEAMSE and M as demonstrated in class.
    Implement the ratioRSharp function to calculate the Sharpe ratio.
    Implement the equity function and plot daily equity curves for the GARCH strategy, ARIMA strategy, and Buy & Hold strategy.
    Analyze the results using these metrics and equity curves to draw conclusions about the effectiveness of the strategies.

