Consider an investor with [[Investor preferences|standard preferences]] who has two [[Financial Assets]] to invest in - a risky portfolio and a risk-free asset. The risk-return profiles of each are given by 

| Asset | Return | Risk |
| ---- | ---- | ---- |
| Risk-free asset | $r_f$ | 0 |
| Risky portfolio | $\mathbb{E}(r)$ | $\sigma_p$ |


![[Pasted image 20240124154401.png|400]]
The investor decides to allocate $y$ of the total capital into the risky portfolio and $1-y$ into the risk free asset. The realized returns of the portfolio are given by $$r=yr_p+(1-y)r_f$$Taking expectations,$$\mathbb{E}(r)=y\ \mathbb{E}(r_p)+(1-y)r_f$$$$=r_f+y[\ \mathbb E(r)-r_f]$$The risk of the portfolio is given by:
$$\text{Var}(r)=\text{Var}(yr_p+(1-y)r_f)$$From [[random variables#Properties]],
$$\text{Var}(r)=y^2\text{Var}(r_p)+(1-y)^2\text{Var}(r_f)+2y(1-y)\text{Cov}(r_p,r_f)$$but $\text{Var}(r_f)=0$ and $\text{Cov}(r_p,r_f)=0$
$$\text{Var}(r)=y^2\sigma^2_p\tag1$$
If $\text{Var}(r)=\sigma^2$, then $$\sigma^2=y^2\sigma^2_p$$$$y=\frac{\sigma}{\sigma_p}\tag2$$
Where:
- $\sigma$ is the standard deviation of the new portfolio
- $\sigma_p$ is the standard deviation of the risky portfolio

From the expected returns of the new portfolio,
$$\mathbb E(r)=r_f+\frac \sigma{\sigma_p}[\ \mathbb E(r_p)-r_f]$$
This equation is the **capital allocation line (CAL)**. Its locus represents all possible combinations of candidate portfolios based on values of $y$. Drawing this line on the $\mathbb E(r)$ $\sigma$ plane, the intercept is $r_f$ and the slope is $\frac {\ \mathbb E(r_p)-r_f}{\sigma_p}$. 
![[Pasted image 20240124160850.png|400]]

The CAL is the feasible set of portfolios between the risk free and risky portfolio. 

The term $\mathbb E(r_p)-r_f$ is the **risk premium** of the risky portfolio. $\sigma_p$ is a measure of risk of the risky portfolio. Therefore the slope of the CAL is a ratio of risk premium to risk. The slope is the [[Sharpe and Sortino Ratio#Sharpe ratio|sharpe ratio]] of the risky portfolio. 
### [[Investor preferences|preference]] optimization (complete portfolio)
Graphically the optimization is given by
![[Pasted image 20240124161032.png|600]]
The Capital allocation line represents the constraint to which the investors preferences need to be maximized. Formally,$$\max_y U(\mathbb E(r),\sigma^2)=\max_y(\mathbb E(r)-\frac 12A\sigma^2)\text{ subject to } E(r)=r_f+\frac \sigma{\sigma_p}[\ \mathbb E(r_p)-r_f]$$Substituting the constraint and (1) into the equation, $$=\max_y (r_f+\frac \sigma{\sigma_p}[\ \mathbb E(r_p)-r_f]-\frac{1}{2}Ay^2\sigma_p^2)$$Substituting (2),$$=\max_y(r_f+y[\ \mathbb E(r_p)-r_f]-\frac{1}{2}Ay^2\sigma_p^2)$$Maximizing,$$0=\mathbb E(r_p)-r_f-Ay\sigma_p^2$$$$y=\frac{\mathbb E(r_p)-r_f}{A\sigma_p^2}$$This is the risky portfolio allocation for the **complete portfolio** that accounts for the investors preferences. $1-y$ is the allocation to the risk free asset. if $A$ is low, $y$ increases. The less risk averse an investor is, the more the allocation of the risky portfolio in the complete portfolio.

#### Leveraged investing
However, $y>1$ by borrowing money and then investing.  On the capital allocation line, this is shown as 
![[Pasted image 20240131151026.png|400]]
if the cost of borrowing (interest rate) is the risk free rate $r_f$. 

In almost all cases, the cost of borrowing will be greater than the risk free rate however due to the banks incentives. If the cost of borrowing is $\hat r_f$, then on the CAL 
![[Pasted image 20240131151318.png|400]]
The slope falls once $y>1$ due to the higher cost of borrowing money. 