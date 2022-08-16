**Predicting the Future Stock Price of Zoom**

_Research paper_

Roman Bravo, Cal Poly Pomona, United States, [romanbravo@cpp.edu](mailto:romanbravo@cpp.edu)

Erik Correa, Cal Poly Pomona, United States, [erikcorrea@cpp.edu](mailto:erikcorrea@cpp.edu)

Sergio A. Figueroa, Cal Poly Pomona, United States, [safigueroa@cpp.edu](mailto:safigueroa@cpp.edu)

Tallal M. Moshrif, Cal Poly Pomona, United States, [tmmoshrif@cpp.edu](mailto:tmmoshrif@cpp.edu)

**Abstract:**

_In the last year, the stock price of Zoom (ZM), plunged from a high of $559 to a low of $87 per share. Utilizing time series models, and the evaluation of these models, we attempt to forecast the next quarter stock price of ZM and compare the efficacy of our models when it comes to predicting the stock price._

**1 Introduction**

In 2020 Zoom had one of the biggest booms we have seen in the past few years. Covid-19 put the workplace in an environment that we have never seen before and Zoom thrived where others could not. In December of 2019 the company had an average of 10 million users per day. Some people would look at those 10 million users and believe that the company was performing well enough to be a success. What they wouldn't know was that the company was going to skyrocket to places they have never been before. In March of 2020 during the beginning of Covid-19 protocols, the company was accumulating up to 350 million daily users. Zoom is a prime example of a company that benefited from the Covid-19 outbreak and had become one of the very rare success stories of 2020. This was also evident when looking at Zoom stock prices over the past few years. In December of 2019 we see that their stock was sitting at around $70. By October of 2020, that number had jumped up to $559. With that said, a lot has changed since then. Even though there are still restrictions, the world is opening up more and more as of recent. Zoom is still succeeding but not nearly as much as it was toward the beginning of the pandemic. This is why we believe that it would be interesting and beneficial to predict the stock price changes for the future.

**2 Methodology**

The Yahoo Finance tool 'yfinance' was utilized to download our Zoom stock data. The 'yfinance' library allows for the creation of a data set containing the date and price action of a stock that can be downloaded for a given time frame (Mondal, 2021). Next, utilizing the 'pandas' library, a data frame was created. This data frame contained the Zoom stock closing date as the index, and the closing price as a column. The time frame selected was from Zoom stock's IPO to present day, giving us two years' worth of stock price closes for Zoom.

Following the creation of this data frame, in order to create a general forecast, a test train split of the data became necessary—a 80 to 20 percent split of the data was used. The data sets were then fitted onto the Holt-Winters exponential smoothing model. This model encodes past values in a time series to forecast future values—it is a modified exponentially weighted moving average that accounts for an average value, trends, and seasonality over time (SolarWinds, 2019). Furthermore, the dataset was fitted onto the 'fbprophet' model in order to create an additional forecast of the stock price. With 'fbprophet', an open source algorithm is used that accounts for growth, seasonality, holidays, and errors—the output of these factors produce a powerful time series model (Krieger, 2021). Finally, data visualizations along with mean squared error were used to compare the efficacy of both models.

**3 Results and Conclusion**

The results of the analysis indicate that with a more advanced model, such as Facebook Prophet, we can achieve a higher prediction accuracy. To verify the effectiveness of the prediction models, the general Holt-Winters forecast model was compared with Facebook Prophet. The results of both models were evaluated by Mean Absolute Error (MAE), Root Mean Square Error (RMSE), Mean Squared Error (MSE), and MAPE (Mean Absolute Percentage Error). The Facebook Prophet future forecast model achieved a lower RMSE on both the 40 and 60 day rolling window (17.57 and 40.80, respectively) compared to the Holt-Winters forecast prediction (47.28) on 156 days of test data. Facebook Prophet also holds a 22 percent Mean Absolute Percentage Error even after a 120 day future forecast. This evaluation was determined by a functionality for time series cross validation to measure forecast error using historical data. This implementation can prove useful for other companies or investors to predict return on investments. Stock market price prediction plays a critical role in reflecting overall stock market trends and seasonality, and has a strong practical investment value.

**4 Recommendations / Next Steps**

Accurate prediction of stock market return can be a very challenging task due to volatile and non-linearity of the financial stock markets. More advanced techniques such as Artificial Neural Network models can be implemented as a recommendation for this project.

One network model can be recommended for this project, the Multilayer Perceptron (MLP).

MLP is considered as the simplest model of neural network and consists of an input fed into a model using certain weights, the values are fed throughout the hidden layer to produce an output.

Multilayer perceptron is appropriate for predicting stock prices and outperforms the statistical techniques such as regressions for the following reasons:

- It is numeric and fits the financial datasets.
- Distribution of input data is not required.
- Model formulation is not required.
- It can predict unseen data without reprocessing training data.

However, determination of a MLP architecture including learning algorithms, the choice of number of layers, number of neurons in each layer, and (nonlinear) activation functions between the layers is complicated. (Namdari, 2021)

**References**

Google. (n.d.). _Zoom Video Communications Inc (ZM) stock price & news_. Google Finance.

Retrieved May 12, 2022, from https://www.google.com/finance/quote/ZM:NASDAQ?sa=X&ved=2ahUKEwin2Jjvqdv3AhVQg4kEHTbqC1kQ3ecFegQIJxAg

Krieger, Mitchell. _Time Series Analysis with Facebook Prophet: How it Works and How_

_to use it._ Retrieved May 10, 2022, fromhttps://towardsdatascience.com/time-series-analysis-with-facebook-prophet-how-it-works-and-how-to-use-it-f15ecf2c0e3a#:~:text=Facebook%20Prophet%20is%20an%20open-source%20algorithm%20for%20generating,some%20of%20the%20above%20drawbacks%20of%20other%20algorithms.

Molla, R. (2020, December 4). _The pandemic was great for Zoom. What happens when there's a_

_vaccine?_ Vox. Retrieved May 12, 2022, from

https://www.vox.com/recode/21726260/zoom-microsoft-teams-video-conferencing-post-pandemic-coronavirus

Mondal, Arnab. (2021). _Download Financial Dataset Using Yahoo Finance in Python | A_

_Complete Guide_. Retrieved May 10, 2022, from

https://www.analyticsvidhya.com/blog/2021/06/download-

financial-dataset-using-yahoo-finance-in-python-a-complete-guide/

SolarWinds. (2019). _Holt-Winters Forecasting and Exponential Smoothing Simplified_. Retrieved

May 10, 2022, from, https://orangematter.solarwinds.com/2019/12/15/holt-winters-

forecasting-simplified/#:~:text=The%20Holt%2DWinters%20method%20uses,%E2%80%9Csmooth%E2%80%9D%20a%20time%20series.

Vijh, Mehar, et al. "Stock Closing Price Prediction Using Machine Learning Techniques."

_Procedia Computer Science_, Elsevier, 16 Apr. 2020,

https://www.sciencedirect.com/science/article/pii/S1877050920307924.

Namdari, Alireza & Durrani, T.. (2021). A Multilayer Feedforward Perceptron Model in Neural

Networks for Predicting Stock Market Short-term Trends. Operations Research Forum.
