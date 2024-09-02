Dataframe commands can be used in order to find the basic statistical measures of columns or rows in a dataframe - for particular stocks

`cl_price.mean()` gives the mean close price of each of the stocks (each stock is a column, date is the row/index)
`cl_price.std()` gives the standard deviation price of each of the stocks
`cl_price.describe()` gives the basic data like mean median, std, min, max, percentile values for each stock

`cl_price.head(<number>)` displays the first n number of rows of the dataframe cl_price. tail does the same thing with the last rows

