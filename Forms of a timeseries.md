#### Random walk
Day to day changes in the price of a stock should have a mean value of zero. 
If it is known that a stock will yield an expected profit in the next day, efficient speculation will drive the price up. No rational investor would look to hold a stock if it is expected to depreciate in value. The model asserts that the price of the stock should evolve through the following [[Time Series]] difference equation:
$$y_t=y_{t-1}+\epsilon_{t}$$
Taking differences,
$$\Delta y_t=\epsilon_t$$
Compared to the more general difference equation, $$\Delta y_t=\alpha_0+\alpha_1 y_{t-1}+\epsilon_{t}$$this implies that the restriction of $\alpha_0=\alpha_1=0$ has to be tested. Rejecting this restriction implies that random walk theory does not apply to this particular timeseries.

#### Reduced forms and structural equations
Used to collapse a system of difference equations into separate single-equation models. This can be demonstrated by using stochastic variations of Samuelson's 1939 model. In the model:
(SE)$$y_t=c_t+i_t\tag{1}$$Where $y$ is the [[Gross Domestic Product]], $c$ is the consumption and $i$ is the investment. The GDP in this equation is dependent upon the current value of consumption and investment. We also know that:(RF)$$c_t=\alpha y_{t-1}+\epsilon_{ct}\tag{2}$$(RF)$$i_t=\beta(c_t-c_{t-1})+\epsilon_{it}\tag{3}$$A **structural equation** expresses an endogenous variable as being dependent on the current values of other endogenous variables. A **reduced-form equation** expresses the value of a variable in terms of its own lagged values, or the lags of other endogenous variables. 

Substituting 2 into 3,
$$i_t=\beta(\alpha y_{t-1}+\epsilon_{ct}-\alpha y_{t-2}+\epsilon_{ct-1})-\epsilon_{it}\tag{4}$$Substituting 2 and 4 into 1,
$$y_t=\alpha y_{t-1}+\epsilon_{ct}+\beta(\alpha y_{t-1}+\epsilon_{ct}-\alpha y_{t-2}-\epsilon_{ct-1})+\epsilon_{it}$$$$y_t=\alpha y_{t-1}+\epsilon_{ct}+\alpha\beta y_{t-1}+\beta\epsilon_{ct}-\alpha\beta y_{t-2}-\beta\epsilon_{ct-1}+\epsilon_{it}$$$$y_t=\alpha(1+\beta) y_{t-1}-\alpha\beta y_{t-2}+(1+\beta)\epsilon_{ct}-\beta\epsilon_{ct-1}+\epsilon_{it}$$
This is a univariate equation as it only depends on lagged values of $y$.

#### Error correction model
The [[Phillips curve]] is given by $$\pi_t=\mathbb E(\pi_t)+\alpha(y_t-y_e)$$If the central bank has perfect foresight, $$\pi_t=\mathbb E(\pi_t)$$Assume targeted inflation rate $\pi^T$. Then the phillips curve eq becomes,$$\pi_t=\pi^T+\alpha(y_t-y_e)$$$$\pi_t=\pi^T+\epsilon_t$$
If the central bank has not forecasted efficiently and there is a deviation of inflation from the target rate,$$\pi_t\ne\pi^T$$Then the ECM can be used. In the next time period,$$\pi_{t+1}=\pi^T+\alpha(\pi_t-\pi^T)+\epsilon_{t+1}$$
#### Non-linear dynamics
$$i_t=\beta(c_t-c_{t-1})-\lambda_t\beta_2(c_t-c_{t-1})+\epsilon_{it}$$Where $\lambda_t=1$ if $c_t-c_{t-1}<0$, 0 otherwise. Therefore, if $c_t-c_{t-1}>0$$$i_t=\beta(c_t-c_{t-1})+\epsilon_{it}$$else,
$$i_t=(\beta-\beta_2)(c_t-c_{t-1})+\epsilon_{t+1}$$
If $\beta_2>\beta$, this would explain situations where investment expenditure grew despite a fall in consumption spending. 
