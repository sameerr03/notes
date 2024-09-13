Stocks produce cash flows through 2 means - Dividends and Capital gains. Stocks are more risky than bonds typically as bonds have a primary claim on the firm's assets in case of a default. Stocks are traded in the primary (new stock issues) and the secondary (previously issued stocks are traded).
#### [[Future and present values|Present value]] of a stock
The price of a stock at time 0 is given by $$P_0=\frac{\text{Div}_1}{1+R}+\frac{P_1}{1+R}$$Where:
- $\text{Div}_1$ is the expected div at $t=1$
- $P_1$ is the expected price of the stock at $t=1$

At $t=1$,$$P_1=\frac{\text{Div}_2}{1+R}+\frac{P_2}{1+R}$$Together, $$P_0=\frac{\text{Div}_1}{1+R}+\frac{\text{Div}_2}{(1+R)^2}+\frac{P_2}{(1+R)^2}$$Generally, 
$$P_0=\sum_{t=1}^T\frac{\text{Div}_1}{(1+R)^t}+\frac{P_T}{(1+R)^T}$$
There can be 3 cases of dividend value based assumptions:
(supposing the corporation lives forever and 0 capital gains (stock is never sold))
##### Zero dividend growth
$\text{Div}_0=\text{Div}_1=\text{Div}_2=\text{Div}_3=d$
By using the [[Valuing cash flow streams#Perpetuity|perpetuity]] valuation, $$P_0=\frac dR$$
##### Constant growth dividend
Here, $\text{Div}_1=\text{Div}_0(1+g)$, $\text{Div}_2=\text{Div}_1(1+g)=\text{Div}_0(1+g)^2$ and so on. This stream of cash flows from dividends can be valued by using the [[Valuing cash flow streams#Growing perpetuity|growing perpetuity]] valuation$$P_0=\frac{\text{Div}_1}{R-g}$$ It is important to note that the dividend value taken is the expected dividend in the next time period.

##### Differential Growth
This assumes that the dividend of the stock grows at the rate $g_1$ for the first $t$ years, beyond which it grows at $g_2$ forever. This can be valued by using an annuity and perpetuity. For the first $t$ periods, the valuation of the stock will be $$P_t=\frac{\text{Div}_1}{R-g_1}[1-(\frac{1+g_1}{1+R})^t]$$Valued from period $t+1$, the stock is valued by using a growing annuity$$P_{\infty,t+1}=\frac{\text{Div}_{t+1}}{R-g_2}$$Discounting back to present time, $$P_\infty=\frac{\text{Div}_{t+1}}{R-g_2}\times\frac 1{(1+R)^t}$$The final valuation of the stock is given by $$P=P_t+P_\infty=\frac{\text{Div}_1}{R-g_1}[1-(\frac{1+g_1}{1+R})^t]+\frac{\text{Div}_{t+1}}{R-g_2}\times\frac 1{(1+R)^t}$$
#### Determining $g$ and $R$
##### Growth rate of earnings
We know that $$\text{Net Income}=\text{Retained Earnings}+\text{Dividends Paid}$$ from the [[Income statement]]. This amount belongs entirely to the shareholders of the firm. The firm can gain additional income by reinvesting its retained earnings. In this way, we can assume that $$\text{NI}_1=\text{NI}_0+\text{RE}_0\times\text{Returns on Retained Earnings}$$Dividing both sides by $\text{NI}_0$, $$\frac{\text{NI}_1}{\text{NI}_0}=1+\frac{\text{RE}_0}{\text{NI}_0}\times\text{Returns on Retained Earnings}$$We know that Retained Earnings/Net Income is the [[Forecasting financial statements|plowback ratio]] $b$. The LHS is the growth rate in earnings which is $1+g$. Therefore, $$1+g=1+b\times \text{Returns on Retained Earnings}$$We can assume that the future expected return on retained earnings is the [[Ratio analysis#Profitability ratios|Return on Equity]](ROE). Therefore $$1+g=1+b\times\text{ROE}$$


##### Discount rate
Using the growing dividend model, the price of a stock today is $$P_0=\frac{\text{Div}}{R-g}$$Substituting, $$R=\frac{\text{Div}}{P_0}+g$$This tells us that the discount rate has two components, 
- **Dividend yield:** $\text{Div}/P_0$ (similar to [[Bond Valuation|current yield]])
- **Capital Gains yield:** $g$ -> **the dividend growth rate is also the stock prices growth rate** according to this model. We can prove this by taking the ratio of the stock price in 2 periods:$$\frac{P_1}{P_0}=\frac{\text{Div}_2/(r-g)}{\text{Div}_1/(r-g)}=\frac{\text{Div}_1(1+g)}{\text{Div}_1}=1+g$$


