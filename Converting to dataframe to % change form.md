the function `DataFrame.pct_change()` creates a new dataframe that calculates the percentage change in each data point from the previous. In the example data frame, 

|Date|AMZN|
|---|---|
|Day 1|$100|
|Day 2| $110|

the function will output a new dataframe

|Date|AMZN|
|---|---|
|Day 1|NaN|
|Day 2|$\frac{110}{100}-1=0.1$|

In quantfin, return data is used much more often than close price. Using close prices, a return dataframe can be found
```
ret_v=cl_prices.pct_change()
```
 as the output is a dataframe [[Basic Statistical Parameters]] can be used on this dataframe for more information on the data.
