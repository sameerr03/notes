`DataFrame.rolling(<parameters>)` provides a rolling window in order to obtain moving calculations for data such as simple moving averages. 

The parameter window determines the size of the rolling window for the calculation - for a 10 day sma, the window=10. 

the parameter min_periods determines how many periods at minimum will be in the rolling window, to account for NaN values. If min_periods=6 and there are 4 NaN values in the window, the rolling window is still created and does not throw an error. By default, min_periods=window

`ret_v.rolling(window=10)` will have no output, as it just creates a dataframe that moves with the specified window and no operations are done to it. The rolling window is simply used for other calculations

A 10day sma is calculated from the return values by the following code
```
sma=ret_v.rolling(window=10).mean()
```

other [[Basic Statistical Parameters]] can be used instead

### Exponential rolling operations
Instead of using rolling, `DataFrame.ewm(<parameters>)` can be used in order to give more weight to recent data - useful for creating an exponential moving average. 

The parameters is based on the method of weighting used for the rolling data. The `com` parameter has the formula $$\alpha=\frac1{1+com}$$for com>=0. Com determines the window equivalent of rolling. 
The span formula is more conventional of a typical ema$$\alpha=\frac 2{1+span}$$
Creating a 10day ema can be done through the following code
```
ema=ret_v.evm(com=10).mean()
```

