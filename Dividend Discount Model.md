Dividend refers to **a reward, cash or otherwise, that a company gives to its shareholders**. 

Suppose a company has a timeline of dividends paid as follows:
![[Pasted image 20240413001231.png|700]]

#### constant dividends
In the case when dividends are constant, the valuation of the stock of the company ([[Future and present values|present value]]) is given by $$PV=\frac{D_1^e}{r}$$where
- $D_1^e$ is the expected dividend in period 1
- $r$ is the risk free rate of return

However, $r$ need not be the risk free return as different stocks contain differing amounts of risk. Therefore a **required rate of return/ market capitalization rate** can be used from [[Capital Asset Pricing Model (CAPM)]] where $$k=r_f+\beta[\mathbb E(r_M)-r_f]$$and $$V_0=PV=\frac{D_1^e}k$$where $V_0$ is the intrinsic value of the company at time 0. 

#### Changing dividends
If the dividends are not constant, the valuation is given by $$V_0=PV=\frac{D_1^e}{1+k}+\frac{D_2^e}{(1+k)^2}+\frac{D_3^e}{(1+k)^3}+\dots$$
#### Asset is held only for a finite period
If the asset is held only for $H$ periods and then sold, the intrinsic value of at time 0 is given by $$V_0=\frac{D_1^e}{1+k}+\frac{D_2^e}{(1+k)^2}+\frac{D_3^e}{(1+k)^3}+\dots+\frac{D_H^e+P_H^e}{(1+k)^H}$$where $P_H^e$ is the expected price at the end of $H$. We assume that $P_H^e$ is equal to $V_H$ or the intrinsic value at time $H$. 

#### constant growth dividend
If the dividend grows at the constant rate $g$, then the intrinsic value of the stock is given by $$V_0=\frac{D_0(1+g)}{1+k}+\frac{D_0(1+g)^2}{(1+k)^2}+\frac{D_0(1+g)^3}{(1+k)^3}+\dots$$$$V_0=\frac{D_0(1+g)}{k-g}$$where $k>g$. Therefore, stocks with a growing dividend have a higher intrinsic value than a stock with $g=0$. Companies that implement measures to ensure dividend growth should have higher priced stocks than companies that do not. 

#### Finding dividend growth rates
If a company has [[Ratio analysis#Market Value Ratios|EPS]] of 1, it pays $1-b$ as a dividend, known as the payout ratio and it retains $b$, called the plowback ratio. The company can reinvest retained earnings into projects. 

Suppose the company invests in a project that returns $R$. In the next period, due to the reinvestment of retained earnings, the has an EPS of $$EPS = 1+R\times b$$The dividend paid on this will be $$=(1-b)(1+R\times b)$$$$=(1-b)(1+g)$$where $g=R\times b$

Therefore, a company can increase its dividend by retaining some of its earnings per share rather than paying it out as a dividend. 

if $b=0$, $g=0$ therefore $$V_0=\frac{D_1^e}{k}$$if $1>b>0$, $$V_0=\frac{(1-b)\text{EPS}}{k-g}=\frac{(1-b)\text{EPS}}{k-R\times b}$$where $k>g=R\times b$. $k$ can be found using the [[Capital Asset Pricing Model (CAPM)]] equation$$k=r_f+\beta R_M$$ and $g = b\times ROE$ where $b$ is the plowback ratio and ROE is the [[Ratio analysis#Profitability ratios|Return on Equity]]

