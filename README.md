[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/7lKBcjfN)
# 44-566 machine-learning project
## Project Description:

To identify Stock price Close value with machine learning, we need to train a machine learning model for predicting Close value based on features like Open, VWAP, Volume, Trades. For this, we need a dataset containing information about Stock data, so that we can predict the Close value.

#### Info regarding Dataset Features

* Date - Trade Data
* Symbol - stock name 
* Series - Type of security 
* Prev Close - Previous data closing price
* Open - Opening price for the day
* High - Highest price for the day
* Low - Lowest price for the day
* Last - Last trade price
* Closes - Closing price
* VWAP - Volume-weighted average price (a ratio of the cumulative share price to the cumulative volume traded over a given time period)
* Volume - volume trades for the day
* Turnover - The turnover ratio is the ratio of sellers to buyers of a stock
* Trades - Number of Trades
* Deliverable Volume - Amount of deliverable volume
* %Deliverble - Percentage of shares that were delivered
Note: All price are in Rupees

## Dataset Link:
[nifty50-stock-market-data](https://www.kaggle.com/datasets/rohanrao/nifty50-stock-market-data?select=ADANIPORTS.csv)

### 1. Initial_exploration notebook

As of now I have performed initial exploration on dataset and in initial_exploration notebook I have examined and performed cleaning on the data by filling null values with 0. Then I have split my data into train and test sets.


### 2. Linear_regression notebook

I have selected a feature to train the model. After execution and seeing outputs, I found that mean square and root mean square values are a bit high, so I have decided to include more features to train the data such that mean squared error dropped from 162.16 to 2.3 and root mean squared error dropped from 12.73 to 1.5. 

I tried to add a few more parameters to check if they impact mean square and root mean square values or not and found out that those features have to impact on mean square and root mean square values. So I decided not to include those parameters as it might overfit my model.

Model has almost similar performance on the test_data as it has performed of the train_data.

