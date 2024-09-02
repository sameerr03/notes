yfinance is a library that uses an API to gather financial data from yahoo! finance. The stock data from any stock can be accessed using the following code 
```
import yfinance as yf
data=yf.download("<ticker>",period="1mo",interval="5m")
```

This downloads the intraday data taken every five minutes from the last one month of the ticker.

For downloading Adjusted close data for a very specific time, the code can be used:
```
imort datetime as dt
start = dt.datetime.today()-dt.timedelta(30)
end=dt.datetime.today()
data=yf.download("<ticker>", start, end)["Adj Close"]
```

In order to access data for multiple stocks at the same time, a dataframe can be created. A dataframe is essentially a 2d table that has row and column names. Using a list multiple stocks can be iterated through yfinance in order to get a dataframe with all the information.

```
import pandas as pd
acl_price=pd.DataFrame() #Empty data frame
stocks =["HDFCBANK.NS","BAJAJFINSV.NS","HINDUNILVR.NS","MAZDA.NS"]

for ticker in stocks:
	acl_price[ticker]=yf.download(ticker, start, end)["Adj Close"]
```

Suppose all the data needs to be stored, not just the Adjusted close. For this, a dictionary can be used with the key being each ticker and the value assigned to the key being a DataFrame with all the stock information.

```
ohlcv_data={}

for ticker in stocks:
	ohlcv_data[ticker]=yf.download(ticker, start, end)
```
