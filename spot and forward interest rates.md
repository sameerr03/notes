The spot interest rate $s_k$ is the interest rate for time $k$ periods (annualized). Since interest can change at any given time, this results in the [[Fixed Income Securities#Bond Valuation|present value]] calculation of the bond being quite different in real life. For a two period bond, the present value is given by $$PV = \frac{c}{1+s_1}+\frac{c+F}{(1+s_2)^2}$$The changing interest rates at each time period is the reason for bond yields being different at different maturities (term structure).

For a zero coupon bond with face value of 1, $$P=\frac{1}{(1+s_T)^T}$$This means that if we are to find the rate of return on this bond, $$r=(\frac 1P)^{1/T}-1=s_T$$This means that the return of a bond is the spot rate. This shows that bond investors are prone to interest rate risk

##### Estimating spot rates
We can represent the price of each currently traded bond as $$P_i=d_{i1}C_i(1)+d_{i2}C_i(2)+\dots+d_{in}C_i(n)$$Using this equation then, we can estimate the discount factors ($d$) using a [[Simple Linear Regression|linear regression]]. $$P=d_1C_i(1)+d_2C_i(2)+\dots+d_nC_i(n)+e_i$$From the discount factors in each period estimated from the regression, we can find out what the spot rate is for each time period. 

#### Forward rates
The forward interest rate is a predetermined interest rate set this period for the next period. $f_{ij}$ is the interest rate for time period $j$, which was agreed upon by two parties in the previous time period $i$. Based on spot rates, if I deposit one dollar in the bank, my return after 2 years will be $$R=(1+s_2)^2$$If the parties instead agree to use spot rates for the first time period and a forward rate for the second period, the return is given by $$R=(1+s_1)(1+f_{12})$$If the two returns do not match, this presents a possibility for infinite risk free arbitrage. Therefore, under the no arbitrage condition, $$(1+s_2)^2=(1+s_1)(1+f_{12})$$therefore, $$f_{12}=\frac{(1+s_2)^2}{(1+s_1)}-1=\frac{DF(1)}{DF(2)}-1$$
This is the forward rate equation for 2 periods. This also means that for any 2 time periods $t_1$ and $t_2$,$$(1+s_{t_1})^{t_1}(1+f_{t_1t_2})^{t_2-t_1}=(1+s_{t_2})^{t_1+t_2}$$

#### [[Fixed Income Securities#Duration|duration]] of a bond and portfolio with spot rates
To the present value/Price calculation, we can add a correction term that will be used to describe the effect of changes in the spot rate on the bond. This is given by
$$P(\delta)=\frac{x(t_1)}{1+s_1+\delta}+\frac{x(t_2)}{(1+s_2+\delta)^2}+\dots$$Then the duration is given by the sensitivity of $P$ with respect to $\delta$ evaluated when $\delta=0$.
$$D(P)=\left. \frac{1}{P(\delta)}\frac{dP(\delta)}{d\delta} \right|_{\delta=0}$$

If we have a portfolio $\Pi$ of $N$ bonds, $$D(\Pi)=\sum_{i=1}^ND(i)w_i$$
