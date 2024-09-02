A process in which the [[Time Series]] can move in either direction from its last position, with an equal probability. This process is represented as the [[Difference equations|difference equation]]$$y_t=y_{t-1}+u_t$$where $u_t$ is a random disturbance term that has an expected value of 0. Using the [[Lag operator]], $$y_t=Ly_t+u_t$$$$(1-L)y_t=u_t$$$$y_t=\frac{u_t}{1-L}=u_1+u_2+\dots+u_{t-2}+u_{t-1}+u_t$$$$y_t=\sum_{j=1}^tu_j$$which is the stochastic trend for a finite sample. 

The mean of the series is given by $$\mathbb E(y_t)=\mathbb E[\sum_{j=1}^t u_j]=0$$as the disturbance in a RWP has an expected value of 0. 

The variance of the series is given by $$\mathbb E(y_t)^2=\mathbb E[\sum_{j=1}^tu_j]^2=\mathbb E[u_1^2+u_2^2+\dots+u_t^2+2u_1u_2+\dots+2u_{t-1}u_t]$$$$=\mathbb E(u_1^2)+\dots+\mathbb E(u_t^2)=\sigma^2+\dots+\sigma^2=t\sigma^2$$
As $\mathbb E(u_1u_2)=\dots=\mathbb E(u_{t-1}u_t)=0$

The covariance between $y_t$ and $y_{t-s}$ is given by $$\mathbb E(y_t\cdot y_{t-s})=\mathbb E[\sum_{i=1}^tu_i\cdot\sum_{j=1}^{t-s}u_j]=\mathbb E[(u_1+u_2+\dots+u_{t-s}+u_{t-(s+1)}+\dots+u_t)(u_1+u_2+\dots+u_{t-s})]$$$$=\mathbb E(u_1^2)+\mathbb E(u_2^2)+\dots+\mathbb E(u_{t-s}^2)$$as $\mathbb E(u_n)=0$ and $\mathbb E(u_n u_{n-m})=0$
$$=\sigma^2+\sigma^2+\dots+\sigma^2=(t-s)\sigma^2$$
the [[ARIMA Model#Autocorrelation Function (ACF)|ACFs]] are given by $$\rho_s=\frac{\text{Cov}(y_t,y_{t-s})}{\text{Var}(y_t)}=\frac{(t-s)\sigma^2}{t\sigma^2}=\frac{t-s}{t}$$Therefore, $\rho_0=1, \rho_1=(t-1)/t, \rho_2=(t-2)/2,\dots$ 
The ACFs slowly decay over time. This process is not [[Stationarity|stationary]] and there is no tendency to return to a historical mean or trend. 

