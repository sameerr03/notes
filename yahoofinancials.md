yahoofinancials is another way to get stock data from yahoo! finance. Unlike [[yfinance]], it uses webscraping instead of API - it is more stable and will be more supported but is slower and will not have intraday data.

yahoofinancials provides data in the form of a JSON data structure. A JSON is essentially a bunch of nested dictionary. To extract data, an object has to be created that has the value of the ticker. This is used to create another object from the class YahooFinancials. 

```
from yahoofinancials import YahooFInancials
ticker='HDFCBANK.NS'
yhoofncls=YahooFinancials(ticker)

data=yhoofncls.get_historical_price_data(""<start date YYYY-MM-DD>","<end date>","period")
```

```
from yahoofinancials import YahooFinancials
import pandas as pd
import datetime as dt

stocks =["HDFCBANK.NS","BAJAJFINSV.NS","HINDUNILVR.NS","MAZDA.NS"]
start=(dt.datetime.today()).strftime('%Y-%m-%d')
end = (dt.datetime.today()-dt.timedelta(30)).strftime('%Y-%m-%d')

acl_prices=pd.DataFrame()
for ticker in stocks:
	yahoo_financials=YahooFinancials(ticker, kwargs)
	json_obj=yahoo_financials.get_historical_price_data(start, end, "daily")
	ohlcv =json_obj[ticker]['prices']
	temp=pd.DataFrame(ohlcv)[["formatted_date","adjclose"]]
	temp.set_index("formatted_date", inplace=True)
	temp.dropna(inplace=True)
	acl_prices[ticker]=temp["adjclose"]
```
