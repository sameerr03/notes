##### Geometric Brownian Motion

Let us consider a stock $S_t$. The price of this stock evolves according to geometric Brownian motion, a widely used stochastic process for modeling stock prices in financial mathematics. It is characterized by the continuous-time evolution of a stock's price, driven by both deterministic and random components. GBM can be understood as an extension of the classical Brownian motion, adapted to capture the multiplicative nature of returns in financial markets.$$dS_t=\mu S_tdt+\sigma_sS_tdZ_t\tag 1$$Where: 
- $S_t$ is the price of the stock $S$ at time $t$
- $\mu$ is the drift coefficient. This term gives the stock price a drift over time in addition to the random walk process driving the price of the stock.
- $\sigma_s$ the variance coefficient of the stock $S$. This is the variance of the random walk process
- $dZ_t$​ is the increment of a Wiener process (or standard Brownian motion), which models the random component of the stock price movement.

###### Properties
- **Log Normal Distribution:** The solution to the GBM SDE implies that the log of the stock price $\log(S_t)$ is normally distributed. This ensures that the price of the stock can never be negative, unlike Brownian Motion where stock prices can be negative
- **Normal Distribution of Returns:** Assumes that the returns are normally distributed. The returns of a stock for the interval $\Delta t$ is $S_{t+\Delta t}/S_t - 1$. While financial markets do not have this property in general, this assumption is a useful simplification. 
- GBM has **Markov properties**. The future prices are only dependent on current prices.
- **Constant Volatility:** The volatility of the returns of the stock are constant according to GBM, whereas actual financial time series have constantly changing levels of volatility

Graphically,

![[Pasted image 20240514223854.png|500]]Price of $S$ over time

##### Counterpart stock and Ornstein Uhlenbeck process
There then exists a counterpart to this stock, a stock price $Y_t$ such that $$\frac{dY_t}{Y_t}=\alpha dt+\beta\frac{dS_t}{S_t}+dX_t\tag 2$$Where:
- $Y_t$ is the price of the counterpart stock $Y$ at time $t$
- $dY_t/Y_t, dS_t/S_t$ are the returns of $Y$ and $S$ respectively
- $\alpha$ is the return drift coefficient. It gives $Y$ a drift independent of $S$'s drift given by $\mu$
- $\beta$ is the sensitivity of the return of $Y$ to the return of $S$
- $dX_t$ is the residual, given by $$dX_t=\frac{dY_t}{Y_t}-\alpha dt-\beta\frac{dS_t}{S_t}$$

The residuals can be described by an Ornstein–Uhlenbeck process :$$dX_t=\kappa(m-X_t)dt+\sigma dW_t\tag 3$$Where:
- $X_t$ is the value of the OU process at time $t$
- $\kappa$ is the rate of mean reversion
- $\sigma$ is the volatility coefficient of the OU process
- $W_t$ is a Wiener process: ($dW_t\sim N(0, dt)$). We also assume that the wiener processes: $Z_t$ and $W_t$ are uncorrelated

The Ornstein Uhlenbeck process is a mean reverting model. The implications of using it in this context is that the returns of $Y_t$ on average are related to the returns of $S_t$ implying that there are short term, mean reverting fluctuations of the returns of $Y$ from $S$, that can be taken advantage of in a trading algorithm when the price of either asset deviates far from its implied price. 
![[Pasted image 20240514224121.png|500]]Residuals $X_t$

![[Pasted image 20240514225201.png|500]]Stock price $Y_t$
###### Spread of the stocks
Finally, the spread between the two stocks is given by $$\delta_t = Y_t-S_t\tag 4$$Where:
- $\delta_t$ is the value of the spread of the stocks $\delta$ at time $t$. This is the difference in the price of both the stocks at any given time

![[Pasted image 20240514225404.png|500]]spread $\delta_t$

With a pairs trading strategy, trades are made based on the value of the spread, or some metric related to the spread. Thus the spread is of main importance when it comes to executing a successful pairs trading algorithm on real asset pairs.  
#### Expanding $\delta_t$
From equation (1),$$\frac{dS_t}{S_t}=\mu dt+\sigma_sdZ_t\tag 5$$
Substituting (5) into (2),
$$\frac{dY_t}{Y_t} = \alpha dt+\beta[\mu dt+\sigma_sdZ_t]+dX_t\tag 6$$Substituting (3) into (6),
$$\frac{dY_t}{Y_t} = \alpha dt+\beta[\mu dt+\sigma_sdZ_t]+\kappa(m-X_t)dt+\sigma dW_t$$
$$= \alpha dt+\beta\mu dt+\beta\sigma_sdZ_t+\kappa(m-X_t)dt+\sigma dW_t$$$$=[\alpha+\beta\mu+\kappa(m-X_t)]dt +\beta\sigma_sdZ_t+\sigma dW_t$$Multiplying by $Y_t$ on both sides, $$dY_t = Y_t[\alpha+\beta\mu+\kappa(m-X_t)]dt+\beta\sigma_sY_tdZ_t+\sigma Y_tdWt\tag 7$$This is the SDE for the evolution of $Y_t$. From (4) we can conclude that $$d\delta_t = dY_t-dS_t$$Using this relation and plugging in (1) and (7),
$$d\delta_t=Y_t[\alpha+\beta\mu+\kappa(m-X_t)]dt+\beta\sigma_sY_tdZ_t+\sigma Y_tdW_t-(\mu S_tdt+\sigma_sS_tdZ_t)$$$$=Y_t[\alpha+\beta\mu+\kappa(m-X_t)]dt-\mu S_tdt+\beta\sigma_sY_tdZ_t-\sigma_sS_tdZ_t+\sigma Y_tdW_t$$Therefore,$$d\delta_t = [Y_t(\alpha+\beta\mu+\kappa(m-X_t))-\mu S_t]dt+(\beta Y_t-S_t)\sigma_sdZ_t+Y_t\sigma W_t\tag 8$$This is the SDE for the spread. 

#### Results from restricting variables
Let us assume that there is no drift return term for $Y_t$, i.e., $\alpha=0$. We further assume that there is no drift in $S_t$ ($\mu=0$) and the OLS coefficient $\beta=1$.

Applying these restrictions to the SDE, it simplifies to $$d\delta_t = Y_t(\kappa(m-X_t))dt+(Y_t-S_t)\sigma_sdZ_t+Y_t\sigma W_t$$$$=Y_t(\kappa(m-X_t)dt+\sigma W_t)+(Y_t-S_t)\sigma_sdZ_t$$$$d\delta_t =Y_tdX_t+\delta_t\sigma_sdZ_t$$
### Mean, Variance, and distribution - from simulation
From simulations of 10,000 realizations of the spread using the system of SDEs outlined above, with parameters $\alpha = 0, \mu=0.1, \sigma_s=0.3, \sigma = 0.2, \kappa = 40, m=0, S_0 =100, Y_0 = 150, X_0 = 0, \beta = 1.3$,
we find that the spread has a mean and variance that increases with time. The mean and variance both appear to evolve in an approximately linear fashion. The parameters were chosen to replicate observations from asset pairs with highly corelated returns. 

![[Pasted image 20240513235722.png|500]]Evolution of mean over time

![[Pasted image 20240513235808.png|500]]Evolution of variance over time

It is important to note that trades will not be held for as long as a year. The distribution of the final values of the spread at the end of the year is given by 

![[Pasted image 20240513235954.png]]

The starting value of the spread was 50 in this simulation. Final average was 96 at the end of one year. 

Pairs where the spread drifts over time (the stocks diverge a lot or converge a lot) will perform worse compared to pairs where the spread stays around a constant average level. Stationarity tests to ensure this for the spread during trading do not work as well on a day to day basis as spreads fall in and out of stationarity constantly. From analyzing the properties of this SDE a better trading model and pair selection method can be identified, which is not just restricted to cointegrated pairs of assets.
#### Sensitivity analysis with restricted model
Using the restricted model ($\beta = 1, \alpha = 0, \mu =0$), we can see how changes in parameters affect the mean and variance trend of the spread. We look at the slope of the evolution of the mean of the spread SDE and the slope of the evolution of the variance over time of the spread SDE in order to see how changes in these parameters affect the slope. This is done by creating 1000 iterations of the spread for each value of the parameter of interest and then finding the slope of mean and variance trends from these 1000 realizations. We then run a regression with the slope of either the mean or variance evolution as the independent variable and the value of the parameter as the dependent variable. All the other parameters are held constant, thus we can identify the effect a particular parameter has on the spread's trend effects.
#### $\mu$
$$\text{Slope of Mean Evolution}_i = \psi_1\mu_i+e_i$$$$\text{Slope of Variance Evolution}_i = \psi_2\mu_i+e_i$$
For values of $\beta=1, \alpha=0, \sigma = 0.2, \sigma_s=0.3, m=0, \kappa = 40, S_0 = 100, Y_0 = 150, X_0 = 0$,
![[Pasted image 20240514000558.png]]
The rate of increase of the average value appears to have an increasing and linear relation to $\mu$ for the following parameters. The trend of variance increases over time with an increase in $\mu$. Therefore, there is more uncertainty when $\mu$ is higher. The strategy relies on spreads that do not have much trend, therefore $\mu$ values should be low for chosen assets. 

For values of $\beta=0.4, \alpha=0, \sigma = 0.2, \sigma_s=0.3, m=0, \kappa = 40,$

![[Pasted image 20240514000941.png]]

We now notice a decreasing relationship $\mu$ and the rate of evolution of the mean value. the increasing trend with variance still holds. This implies that the effect of mu changes for different values of alpha. Each variable does not have independent effects on the properties of the spread. However, this also implies that for a particular value of $\beta$, mu has minimal effect on the evolution of the spread. 

For values of $\beta=0.6, \alpha=0, \sigma = 0.2, \sigma_s=0.3, m=0, \kappa = 40,$
![[Pasted image 20240514001447.png]]It is important to note that the trend in the variance continues. The linear fit of the slope of mean trend to $\mu$ values seems to degrade as our beta gets closer to the inflection point $\beta_i$ where $\psi_1=0$. The variance of the distribution of the points is higher. 


### $\beta$

$$\text{Slope of Mean Evolution}_i = \phi_1\beta_i+e_i$$$$\text{Slope of Variance Evolution}_i = \phi_2\beta_i+e_i$$
For the values $\mu=0, \alpha=0, \sigma = 0.2, \sigma_s=0.3, m=0, \kappa = 40,$
![[Pasted image 20240514035417.png]]
Both the variance mean trends appear to related in an increasing but non-linear fashion to $\beta$
Taking logs in the regression equations,

$$\log (\text{Slope of Mean Evolution})_i = \phi_3\beta_i+e_i$$$$\log(\text{Slope of Variance Evolution}_i) = \phi_4\beta_i+e_i$$
with the same parameters, ![[Pasted image 20240514035644.png]]
The log of slope of mean trend appears to be linear, whereas the log of slope of variance over time still shows non linear characteristics. However, it is not possible that the mean trend is not distributed logarithmically, as with changes in values of $\mu$ it can be negative. 


For the values $\mu=0.2, \alpha=0, \sigma = 0.2, \sigma_s=0.3, m=0, \kappa = 40,$
![[Pasted image 20240514040311.png]]

#### $\alpha$

$$\text{Slope of Mean Evolution}_i = \gamma_1\alpha_i+e_i$$$$\text{Slope of Variance Evolution}_i = \gamma_2\alpha_i+e_i$$For the values $\mu=0, \beta=1, \sigma = 0 \sigma_s=0.3, m=0, \kappa = 40,$

![[Pasted image 20240514042813.png]]

$\alpha$ has an increasing relation with both the slope of mean and variance trends. 

Interestingly, with the parameters 
$\mu=0, \beta=0.5, \sigma = 0, \sigma_s=0.3, m=0, \kappa = 40,$
![[Pasted image 20240514044308.png]]
The relation between alpha and slope of the variance trend is negative. Further, the relation between the slope of mean trend and alpha appears to be non linear. Extreme points tend to be towards the left of the line of the best fit, and to the right for values of alpha closer to 0. This is persistent for differing iterations of the simulation of the same parameters and with different parameters. 

Further, with the parameters
$\mu=0, \beta=0.65, \sigma = 0, \sigma_s=0.3, m=0, \kappa = 40,$
![[Pasted image 20240514045009.png]]

For this level of beta, the slope of the variance trend is minimized at $\alpha = 0$.

With the parameters
$\mu=0.3, \beta=0.7, \sigma = 0, \sigma_s=0.3, m=0, \kappa = 40,$
![[Pasted image 20240514045556.png]]

With an increase in mu, the value of beta for minimum slope of variance trend where $\alpha = 0$ has increased.

With $\sigma\ne 0$, we get what appears to be a linear trend for various values of $\mu, \beta$
With the parameters
$\mu=0, \beta=1, \sigma = 0.2, \sigma_s=0.3, m=0, \kappa = 40,$
![[Pasted image 20240514050914.png]]

#### $\sigma$
With the parameters
$\alpha = 0, \mu=0, \beta=1, \sigma_s=0.3, m=0, \kappa = 40,$
![[Pasted image 20240514051608.png]]

#### $\sigma_s$
With the parameters
$\alpha = 0, \mu=0, \beta=1, \sigma=0.2, m=0, \kappa = 40,$
![[Pasted image 20240514052102.png]]

### Conclusion
In this document, we have developed a model for the spread evolution between two related stocks using a system of stochastic differential equations (SDEs). The foundation of this model lies in the use of Geometric Brownian Motion (GBM) for individual stock price movements and the Ornstein-Uhlenbeck process for modeling the mean-reverting behavior of the residuals. These mathematical formulations provide a robust framework for understanding the dynamics of asset pairs and their spread, which is critical for pairs trading strategies.

While the model has been detailed with intuitive explanations and step-by-step derivations, it remains in a preliminary stage. The goal is to further investigate the properties of these SDEs, either through computational simulations or more advanced mathematical methods. Specifically, I am seeking insights on:

1. Advanced mathematical techniques that could be employed to analyze the properties of these SDEs.
2. Computational methods that could be used to simulate and better understand the behavior of the model under various conditions.

Given the current state of the model, it is not yet ready for application to real-world stock data or case studies. The focus is on refining the theoretical aspects and ensuring the robustness of the model before considering practical applications.

### References
1. Use of ornstein uhlenbeck to model factor regression residuals https://math.nyu.edu/~avellane/AvellanedaLeeStatArb071108.pdf

Author: Sameer Rangwala
5/2024
