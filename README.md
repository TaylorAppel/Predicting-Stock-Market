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
The first model I ran was a forecast on AAPL, training the data from 01/01/2011 and ending at 03/26/2018. The first step was to graph the training data (black) and the test data (red). 

<img src="https://github.com/TaylorAppel/Predicting-Stock-Market/blob/master/Stocks/AAPL%20graph.png" width="700" height="500">

From there, using Facebook Prophet, we would fit the training data and forecast out to the present day (at the time). I used a confidence interval of 50% for the forecast.

<img src="https://github.com/TaylorAppel/Predicting-Stock-Market/blob/master/Stocks/AAPL%20forecast.png" width="700" height="500">

Finally, I overlayed the forecast with the actual closes to see how well our model performed!

<img src="https://github.com/TaylorAppel/Predicting-Stock-Market/blob/master/Stocks/AAPL%20result.png" width="700" height="500">

As you can see, one cannot just use machine learning to predict the... wait what?? That was a shockingly accurate forecast! So, you may be wondering, **did I just predict the stock market somehow?!**

<img src="https://github.com/TaylorAppel/Predicting-Stock-Market/blob/master/Stocks/Well%20yes.png" width="500" height="300">

Using the exact same methods on TSLA and NFLX as I did for AAPL, you can see that this was most definitely a fluke.

<img src="https://github.com/TaylorAppel/Predicting-Stock-Market/blob/master/Stocks/TSLA%20result.png" width="700" height="500">

<img src="https://github.com/TaylorAppel/Predicting-Stock-Market/blob/master/Stocks/NFLX%20result.png" width="700" height="500">

## Overall Results
As I mentioned earlier, I performed these same methods on different time frames for the forecasts. All can be viewed in the jupyter notebook. But the results were basically as one would expect:
* AAPL had a couple forecasts that were fairly close to the actual closing prices, while the other two hardly did
* Forecasts tended to be more accurate the further out you were forecasting to, which I suspect is mostly attributed to the stock market's consistent bull run since the start of my time period
* Even with generous confidence intervals (as seen in the notebook), the forecasts were rarely close

A couple final things to note. This project was my first time using Facebook Prophet, and was done about a week after first being introduced to time series forecasting. As a result, there was no parameter tuning for the models, and no exogenous variables were added. Doing both of these could very well increase the accuracy of the forecasts. Even still, I'm not convinced the stock market can be predicted with all the technology in the world!

Thank you for checking out my project!
