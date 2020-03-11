# Predicting-Stock-Market
Using time series forecasting to see if I can predict the stock market from various points in time.

## Project Purpose
The stock market has seen some extraordinary growth since the end of the great recession. During my time at Flatiron, the topic of investing came up numerous times. Having a finance and economics background, as well as over half a decade of experience investing in different markets, I felt pretty confident that it is **not** possible to accurately predict the future of the stock market. One friend insisted it could be done, and I felt that it could not. So while this project was about predicting the stock market, the purpose was actually to prove that it cannot be done.

Disclaimer: I am not at all suggesting that one cannot make sound investment decisions based on myriad factors. The topic was mostly about whether or not machine learning could be used to predict the stock market.

## Data
I downloaded CSV files of three different stocks, Apple, Tesla, and Netflix, from yahoo finance. The files contained the daily closes of each stock from the time period starting at 01/01/2011 and ending at the present day (at the time of the project). 

## Methodology
I would perform 6 different forecasts on 3 different stocks. All training data would start from 01/01/2011. For the 6 different forecasts, I would train on data ending at:
* 03/26/2018 (my birthday)
* 1 year out from current date
* 6 months out from current date
* 3 months out from current date
* 1 month out from current date
* 1 week out from current date

I would then fit each model and forecast out to the current date, and finally overlay the forecast with a graph of the actual closes. This would show how well the forecast compared to reality.

While I did perform traditional time series forecasting, I found Facebook Prophet to be easier to use and more interpretable. You can see the full project in the jupyter notebook, but for the purpose of this README, I will only display pictures from the Prophet models. 

## Model Example
