
<h1 align="center"> Gold Stock Trend Analysis and Forecasting </h1>  

Gold has long been a cornerstone of financial markets, with its prices reflecting global economic health, investor sentiment, and market trends. However, understanding its behavior and accurately forecasting its movement remains a complex challenge for analysts, researchers, and traders. This project tackles these challenges by leveraging a rich dataset of daily gold prices and advanced analytical techniques to extract insights and create predictive models that aid decision-making.

## Problem statement

The gold market is highly volatile and influenced by various factors, including economic events, geopolitical tensions, and seasonal demand. Analyzing this complexity requires robust data exploration, predictive modeling, and trading strategies to answer critical questions:

- What are the long-term trends in gold prices?
- How can we forecast future movements effectively?
- What strategies can be developed to optimize trading decisions?
  
## Project Objectives 
This project aims to:

- Perform Time Series Analysis to understand historical trends.
- Develop Advanced Modeling techniques for accurate forecasting.
- Create and backtest Trading Strategies to optimize decision-making.
- Conduct Market Sentiment Analysis to understand external influences.
- Use Statistical Methods to analyze relationships within the data.

## About data

[Data Source - Nasdaq](https://www.nasdaq.com/market-activity/commodities/gc:cmx)

- Date: Unique identifier for each trading day.
- Close: Closing price of gold on the respective date.
- Volume: Gold trading volume on the corresponding date.
- Open: Opening price of gold on the respective date.
- High: The highest recorded price of gold during the trading day.
- Low: The lowest price recorded for gold in the trading day.


## Time Series Analysis

### **Long-Term Trend** 

![image](https://github.com/gentallman/gold_stock_trend/assets/78334851/47579b85-4daa-4ba4-8d68-0a1267969609)
Gold prices demonstrate a consistent upward trend over the years, particularly after 2019. Despite temporary dips, prices have steadily risen from around $1200 to nearly $2000, reflecting its resilience as a safe-haven asset.

### **Seasonality and Residuals**   
![image](https://github.com/gentallman/gold_stock_trend/assets/78334851/e118cf7e-0073-4af7-b17f-e2b856b649e0)
- Seasonal events such as Diwali and the wedding season in India contribute to spikes in gold demand.
- Conversely, summer months tend to see reduced activity and lower price movements.

### **Cyclical Patterns**

![image](https://github.com/gentallman/gold_stock_trend/assets/78334851/3f93a324-9563-4c2b-ad6b-0d8142a479a5)

> - The holiday shopping season, spanning from November to December, contributes to a rise in gold demand as consumers seek gifts.
> - The wedding season in India, reaching its peak from October to January, drives heightened demand as gold holds cultural significance in Indian weddings.
> - Additionally, the Hindu festival of Diwali, occurring in October or November, stimulates increased gold purchasing as it is considered auspicious.
> - Conversely, during the summer months between May and August, gold prices may experience a dip or slower activity, potentially due to reduced market participation or seasonal preferences

## Advanced Modeling
Several modeling techniques were implemented to forecast gold prices, including:
- ARIMA & SARIMA: For analyzing seasonality and trends in time-series data.
- Holt-Winters: Applied for exponential smoothing and seasonal forecasting.
- Prophet: Leveraged for its ability to handle holidays, trends, and outliers.
- LSTM (Long Short-Term Memory): Used to capture sequential dependencies and long-term patterns.
- The Prophet model emerged as the most effective, capturing key trends and fluctuations with high accuracy.
- Performance metrics such as Mean Absolute Error (MAE) and Mean Squared Error (MSE) were used to evaluate model effectiveness.

I intend to utilize all available data up to the conclusion of 2023 as our training dataset. Subsequently, we will employ the data from the year 2024 as our test set, aiming to forecast across the entirety of the dataset

#### Different modeling techniques, including ARIMA, SARIMA, Holt-Winters, LSTM, and Prophet, were employed to forecast gold prices. While each model has its strengths, none of them perfectly capture the market dynamics, suggesting the need for continuous refinement and evaluation of forecasting methodologies. Based on actual and predicition graph analysis with performance score `prophet` is best model.

![image](https://github.com/gentallman/gold_stock_trend/assets/78334851/aeeb094d-e9e2-488a-9d14-bac1224a38d0)
> - The real gold prices (black line) go up slowly over time, with some ups and downs now and then. The forecasted prices (orange line) mostly follow the trend of real prices but have some changes because of the ups and downs. Overall, the prophet model's guesses go along with the main trend of gold prices, catching both the rises and falls.

## Trading Strategy Development

### Moving Average Crossover Strategy 
- This strategy likely involves using two moving averages (short-term and long-term) to identify optimal entry and exit points.
- When the short-term moving average crosses above the long-term moving average, it generates a buy signal. Conversely, a cross below indicates a sell signal.
- The consistent portfolio value indicates that this strategy aims for steady growth over time.

### Reverse Trading Strategy
- This strategy might involve counter-trend trading, where positions are taken opposite to prevailing market trends.
- Signals are generated based on volume analysis rather than price analysis. If the current volume exceeds the average volume, a sell signal (-1.0) is generated; otherwise, it's a hold (0.0).
- It could be based on technical indicators, sentiment analysis, or other factors.
- The sharp fluctuations in portfolio value indicate higher risk but also potential for substantial gains.

## Market Sentiment Analysis

### Gold Stock during the Pandemic Years

![image](https://github.com/gentallman/gold_stock_trend/assets/78334851/cd958845-71fc-43b9-8b90-7ba9b9e658c0)
- Gold prices surged during the early months of the pandemic as investors sought safe-haven assets. A notable peak was observed in August 2020.

### Impact of Russia – Ukraine Conflict
![image](https://github.com/gentallman/gold_stock_trend/assets/78334851/c880a4fe-bca2-418f-a5f0-e4f6270e6a74)
- The geopolitical tensions in early 2022 caused significant price fluctuations, with gold initially dipping before recovering to record highs by the end of 2022.

## Key Takeaways
- Resilience of Gold: Gold remains a reliable long-term investment, demonstrating steady growth despite market volatility.
- Seasonal Trends: Cultural and seasonal factors significantly influence short-term price movements.
- Predictive Modeling: While Prophet performed well, refining models with additional features could further enhance accuracy.
- Risk-Return Strategies: The Moving Average Crossover strategy offers stability, while the Reverse Trading strategy caters to higher risk tolerance.

## Recommendations
- Model Enhancement: Incorporate macroeconomic indicators such as interest rates, inflation, and geopolitical news for improved predictions.
- Dynamic Strategies: Combine predictive models with real-time analytics to adjust trading strategies dynamically.
- Broader Analysis: Extend the analysis to include other precious metals or related commodities for diversified insights.
