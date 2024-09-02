NaN stands for Not a Number - occurs in Dataframes on when financial data is not available for particular days or in case there are not enough datapoints for a particular metric (for instance the first 9 datapoints for a 10 day simple moving average)

### Fill NaN
The `DataFrame.fillna(<parametrers>)` function as a part of the dataframe library fills in values into the NaN positions. In a dataframe that contains stock price data of AMZN, MSFT, FB, GOOG from 2010 onwards - FB values until 2012 are NaN as FB was not publicly listed on a stock exchange until 2012.

```
cl_price.fillna({"FB":0})
```

This creates a new dataframe where all the NaN values under FB are filled with 0. Instead of a dictionary, just putting in a number will replace ALL NaN values in the dataframe with that number in a new dataframe. 

Methods can also be used to determine the fill values. Backfill or bfill uses the next valid observation to fill all the NaN values. For FB, all values before 2012 will be filled with its IPO value. ffill uses the last valid observation for all fill values

The axis parameter determines which axis to use ffill or bfill. =0 (default) uses the vertical axis to determine what to fill (evaluates row values in a specific column) 1 evaluates column values in a particular column.

`inplace=True` will replace the NaN values in the DataFrame that the `fillna()` function is used on.

Example for changing the NaN values in the cl_price dataframe using backfill
```
cl_price.fillna(method='bfill', inplace=True)
```

### Drop NaN
The `DataFrame.dropna(<parameters>)` function drops the datapoints that have NaN values in them rather than replace the specific values. 

Inplace works the same as it does for fillna

The axis parameter drops rows if there is a NaN value in them if `axis=0` and drops columns if `axis=1`

The how parameter determines under what condition a datapoint is dropped. If `how='any'` the datapoint is dropped if any value in the row/column (depending on axis) is NaN. If `how='all'` the datapoint is dropped only if all the rows/columns (depending on axis) are NaN. 

Example for using dropna to drop NaN values in the cl_price dataframe
```
cl_price.dropna(how='any',inplace=True)
```