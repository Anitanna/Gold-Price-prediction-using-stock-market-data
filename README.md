#                                                                   GOLD PRICE FORECASTING USING STOCK MARKET DATA

## Chapter 1

### Introduction

Gold has been considered as a precious metal since the past. Thus the prediction of its price has been of great importance. Today, one of the most important and favorite subjects of economists and financial analysts is to explain the process of price fluctuations that have created different methods and attitudes in this regard. The easiest way to gain exposure to gold is through the stock market via which you can invest in actual gold bullion or the shares of gold mining companies. A stock market is a market that mediates the exchange of buying and selling of company stocks.Predicting how the stock market will operate is not simple. It dependsupon several factors such as supply, demand, factors related to a particular company, Interest rates, Current political scenario and exchange rates,etc. Like any investment option stock market is also risky. It is very volatile and extremely unpredictable. This means that the shares we bought can decrease or increase based upon the factors. All these factors play a significant role in making share prices volatile and it is very difficult to predict gold prices with a high degree of accuracy. Efficiently predicting the stock trends helps to minimize the risk of loss and maximizes profit.
The primary objective of this project is to analyze the historical prices of gold and predict the prices of gold using machine learning algorithms for the next four days. Here we use process of using predictive analysis of historical data to estimate and predict customer’s future demand for gold. We collected the historical data through Web Scraping. The data is then Preprocessed and we applied a Stationarity test to the data. Then we are using the Linear Regression model and SARIMA Model for predicting the prices.After performing the calculations we select the best model for predicting the prices, in this case its Regression Model.

## Chapter 2

### Libraries and Methods

#### Libraries

Stock Market Forecasting is achieved by scraping data from the web using libraries such as Beautiful Soup which provides ways to navigate, search, and alter parse trees , requests with which We can fetch content from a URL using requests library. There are two main functions within Requests: making API requests and obtaining raw HTML content from websites, and Pandas is used for analysis of data.
Matplotlib is used for data visualization and NumPy for mathematical operations. Our model uses the Sklearn library which is widely used for machine learning models. This library provides many efficient machine learning tools, including classification, regression, clustering and dimensionality reduction. Another library we used was Statsmodels. It is also a Python package that lets users explore data, estimate statistical models, and run statistical tests.

#### Methods

#### * Web Scraping
Data is collected through Web Scraping using Python library’s Beautiful Soup and requests. Gold is transacted every 5 days from Monday to Friday.The timestamp of the dataset we collected through web scraping ranges from 2019-07-11 to 2021-07-17.For demand prediction, we needed at least two years of data, and web scraping could only yield up to 100 rows at a time. To solve this issue, we collected data as separate data frames from each site.Later, we concatenated each data frame into one.

#### * Data Stationarity

Stationarity can be defined in precise mathematical terms, but for our purpose we mean a flat looking series, without trend, constant variance over time, a constant autocorrelation structure over time and no periodic fluctuations. To check the stationarity of the data, data along with the dates was plotted.the data is non-stationary, since the mean values is not constant along time.

#### * Model Training

To predict the Price of Gold for the next 4 Days two models were used.

#####  * Linear Regression Model

A linear regression is a statistical technique used to predict future values based on past values. Our project uses a multiple regression model with input parameters as the moving average of the past 2 days and the past 5 days.The Linear Regression Model is trained using the training data , “fit” method is used to fit the dataset to a linear model and the price is predicted using the “Predict” Method .R square for regression,Root Mean Square Error value and Mean Absolute Percentage Error are also computed.

#####  * SARIMA Model

Seasonal Autoregressive Integrated Moving Average(SARIMA) is an extension of ARIMA that explicitly considers seasonal components of univariate time series data. The seasonal component of the series is further enhanced by adding additional hyperparameters to specify the autoregression (AR), the differentiating (I) and the moving average (MA).

## Chapter 3 

### Result

• The linear regression model has a Mean Absolute Percentage Error (MAPE) of 0.86 percent and the SARIMA model has a Mean Absolute Percentage Error (MAPE) of 2.14

• Using MAPE as an evaluation metric when comparing the linear regression model and SARIMA model, the MAPE of SARIMA is larger than that of linear regression.

## Chapter 4

### Conclusion

Since Mean Absolute Percentage Error (MAPE) of SARIMA is larger than that of linear regression. we conclude the best model for predicting gold prices is the Linear Regression model for our given data.We use only price data for this analysis. As part of a continuing effort, additional related features, such as interest rate, bond price or oil price, may also be introduced as part of a multivariate time series model.

## References

1. [1]demand forecasting methods ofemergency resources from the perspective of artificial intelligence XiaoxinZhu1· Guanghai Zhang1 · Baiqing Sun Published online: 25 May 2019 © Springer Nature B.V. 2019
2. privat Khaemasunun, P. (2007). Forecasting Thai Gold Prices, College of Innovation, Thammasat University, Thailand, vol. 23, no. 3, pp. 96–103.
3. Forecasting Gold Price using Data Mining Techniques by Considering New Factors,A. Hatamlou and M. Deljavan,Department of Computer Science, Khoy Branch, Islamic Azad University, Khoy, Iran, 26 April 2018
4. Stock Market Forecasting Using Time Series Analysis - KDnuggets
5. https://www.adityabirlacapital.com/abc-of-money/factors-affecting-stockmarket

