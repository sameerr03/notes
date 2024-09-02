For any [[Time Series]], if the number of observations $t$ is sufficiently large,$$\mathbb E(y_t)=0,\ \text{Var}(y_t)=\sigma^2=\text{constant},\ \mathbb{E}(y_ty_{t-s})=\mathbb E(y_{t-j}y_{t-j-s})=0\ \forall i,j,s$$In words, the mean of the values is 0, the variance is constant and the covariance of values across any time points is 0.

#### Determining if a process is white noise
Consider a process $$x_t=\sum_{i=0}^q\beta_i\epsilon_{t-i}$$This is a [[ARIMA Model|MA(q)]] process. If we assume that the disturbance terms $\epsilon_t$ is white noise, and if $\beta_0=1, \beta_1=0.5, \beta_{2,\dots,q}=0$
$$x_t=\epsilon_t+0.5\epsilon_{t-1}$$
Taking expectations$$\mathbb E(x_t)=\mathbb E(\epsilon_t)+0.5\mathbb E(\epsilon_{t-1})=0$$as we have assumed that $\epsilon_t$ is white noise. First condition holds. Finding the variance$$\text{Var}(x_t)=\text{Var}(\epsilon_t+0.5\epsilon_{t-1})=\sigma^2+0.5^2\sigma^2+2(0.5)(\text{Cov}(\epsilon_t\epsilon_{t-1})=1.25\sigma^2$$This is a constant variance. Therefore, the second condition is met. Finding the covariance, $$\text{Cov}(x_tx_{t-1})=\mathbb E[(x_t-\mathbb E(x_t))(x_{t-1}-\mathbb E(x_{t-1}))]$$$$=\mathbb E(x_tx_{t-1})=\mathbb E[(\epsilon_t+0.5\epsilon_{t-1})(\epsilon_{t-1}+0.5\epsilon_{t-2})]$$$$=\mathbb E(\epsilon_t\epsilon_{t-1})+0.5\mathbb E(\epsilon_t\epsilon_{t-2})+0.25\mathbb E(\epsilon_{t-1}\epsilon_{t-2})+0.5\mathbb E(\epsilon_{t-1}^2)$$$$=0+0+0+0.5\sigma^2=0.5\sigma^2$$As the covariance is not 0, the third condition does not hold. The series $x_t$ is not white noise.

#### Q-test
The Q statistic can be used to determine whether a timeseries is white noise. The Q gives us an idea of the autocorrelation of the series. The Q stat calculation is given by $$Q=T\sum_{K=1}^sr_K^2$$where $$r_S=\frac{\sum_{t=S+1}^T(y_t-\bar y)(y_{t-s}-\bar y)}{\sum_{t=1}^T(y-\bar y)^2}$$which is just the [[ARIMA Model#Autocorrelation Function (ACF)|ACF]]. Based on the values of Q, the hypothesis are as follows
$H_0: Q=0$
$H_A:Q>0$
$Q$ is distributed according to a $\chi^2$ with $T-K$ degrees of freedom. 

A failure to reject the null implies that Q is not statistically different from zero - the autocorrelation coefficients are less than 1. The series is considered white noise

Rejection of the null implies that the series is non stationary and the autocorrelation based value decay is very slow.

It is important to note that Q stats can work poorly even with large samples.