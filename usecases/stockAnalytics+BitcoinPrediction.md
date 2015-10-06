### Modeling stock market data 
(Chapter 4 in Practical Data Science cookbook)

Summary of the analysis done:

- Data sets:
Current data for stocks tracked by the website finviz.com (--> Need to sign up for a fee to get the data now )
and daily histories of stock prices obtained from Yahoo! Finance.

- Exploratory data analysis 
eg: aggregating the stock price based on sector (and/or industry) using R functions such as aggregate() and ddply().

- They used Relative Valuation technique - it compares a stock's price and valuation ratios to similar stocks to
arrive at a decision about whether the stock might be overvalued or undervalued.

- They took the average of different attributes based on sector and industry, and compared them with the attributes of individual stocks to determine whether the stock is undervalued or not.

- Then, they selected stocks which are undervalued beyond a certain limit and collected their historical data from the Yahoo finance dataset.

- They plotted 50-day and 200-day moving averages of stock prices for these stocks to find out the trend over a period of time.

- Other data summaries - opening price, closing price, high and low over a selected period also help in understanding the behavior of the stock.


As far as I understand, this looks like a good example from the data mining point of view. But from the algorithm perspective, I'm not sure if it can be a good use case.


### Bitcoin Prediction Problem

Come up with models which can effectively predict price variation in bitcoin.

### Datasets

- [OKCoin] (https://www.okcoin.com/about/rest_api.do#spapi) provides APIs to fetch recent bitcoin transactions.

Each bitcoin transaction will have the following information:
- date: transaction time,
- date_ms: transaction time in milliseconds,
- price: transaction price,
- amount: quantity in BTC (or LTC),
- tid: transaction ID,
- type: buy/sell


Other datasets:
- [Datadives] (https://www.datadives.com/dataset.php?datasetid=ds_5)
- [bitcoincharts] (http://api.bitcoincharts.com/v1/csv/)

They will have only the following fields: (Timestamp, Bitcoin price, Amount transacted)


### Research Papers and Algorithms used:

- [Bayesian regression and Bitcoin] (http://arxiv.org/pdf/1410.1231v1.pdf) 

This paper used bayesian regression and latent source model to identify a set of patterns in the past price movements to predict future returns. They used data from okcoin.com (mentioned above).


- [Automated Bitcoin Trading via Machine Learning Algorithms] (http://cs229.stanford.edu/proj2014/Isaac%20Madan,%20Shaurya%20Saluja,%20Aojia%20Zhao,Automated%20Bitcoin%20Trading%20via%20Machine%20Learning%20Algorithms.pdf)

This paper used machine learning algorithms such as glm, svm and random forests to predict the sign change (increase/decrease) in the price of bitcoins. They used 2 datasets: (1) Daily data with price and 26 additional features about the Bitcoin network and market obtained from [Blockchain Info](https://blockchain.info)(2) 10-second and 10-minute interval Bitcoin price data, obtained from OKCoin.com

Models are created using glm, svm and random forests and compared for Accuracy, Precision, Specificity and Sensitivity.


Going forward, we can try to implement some of these models using the algorithms used in these papers and using newer techniques such as deep learning if possible, to give a comparative study.

 
