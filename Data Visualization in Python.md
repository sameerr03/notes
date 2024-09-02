dataframes can be graphed in python by using the `DataFrame.plot()` function. 

The default plot method is a line plot. 

The subplot parameter (booleanj) can be used to plot separate columns independently In order to subplot effectively, using the layout parameter is necessary. Layout takes input in a tuple format - (rows,columns)

The title parameter creates a title for the entire plot. 

Plotting the close prices of a few stocks uses the following code (for 4 stocks)
```
cl_price.plot(subplots=True, layout=(2,2), title="Stock Price Evolution")
```

### Plotting percentage change graphs
Using the [[Converting to dataframe to % change form]] as the source of plot can lead to noisy and incomprehensible graphs. Since the dataset has daily percentage changes, there is a lot of fluctuation as it depends on only the day before. As a result the percentage does not account for the compounding nature of stock returns. In theory, suppose the daily returns are 10%, 5% and -5% over three days. The compounded return of a dollar will be
$$1(1+\frac{10}{100})(1+\frac5{100})(1-\frac5{100})=1.097$$
In order to execute the transformation in python to capture this effect the following code is used
```
(1+ret_v).cumprod().plot()
```
This finds the cumulative product of all the returns, essentially finding the compounding rate of return. This gives us a much more understandable plot that captures compounding returns
