 A [[Technical Indicators|TI]] that determines the strength of a trend. Results are interpreted into a band
 - 0 to 25 - weak or no trend
 - 25-50 - strong trend
 - 50-75 - very strong trend
 - 75-100 - extremely strong trend

ADX makes no inference about the direction, only about the strength of the trend. The calculation is done by finding the positive and negative directional movement (by comparing successive highs and lows) and then calculating the smoothed average of the difference. 

The ADX is obtained from:
$UM=H_t-H_{t-1}$
$DwM=L_{t-1}-L_t$
(Upmove and Downmove)

If the downward movement of the stock is greater than the upmove, +DM is zero and -DM = Downmove and vice versa

This is used to get the directional indicators
+DI is $100\times$ Exponential moving average of (+DM/[[Average true range (ATR)|ATR]])
-DI is $100\times$ Exponential moving average of (-DM/[[Average true range (ATR)|ATR]])

This can be used to calculate the Directional index,
$$DX=(\frac{|+DI--DI|}{|+DI+-DI|})$$

A 14 day ema of the DX times 100 gives us the ADX 