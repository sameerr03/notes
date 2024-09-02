Autoregressive moving average is a statistical model that uses [[Time Series]] data to understand the dataset or to forecast future values. An ARIMA equation is given by $$y_t=a_0+\text{AR}(p)+\text{MA}(q)$$Where:
- $a_0$ is an intercept term
- $\text{AR}(p)$ is the autoregressive component, of order $p$. This component is represented as $$a_1y_{t-1}+a_2y_{t-2}+\dots+a_pt_{t-p}$$
- $\text{MA}(q)$ is the moving average component, of order $q$. This component is represented as $$\epsilon_t+\beta_1\epsilon_{t-1}+\beta_2+\dots+\beta_q\epsilon_{t-q}$$$\beta_0$ is normalized as 1. 
- $d$ is the number of times the raw observations are differenced, also called the degree of differencing

The parameters of the model are taken in order to minimize the least squares of the disturbance terms. If the optimal $q=0$, then the process is autoregressive. If the optimal $p=0$, the process is a moving average process. 

#### Stability conditions
If the process is convergent/stable, it is an ARMA process. The degree of differencing $d=0$. The conditions for the process to be stationary is 
- $|a_i|<1\ \forall i=1,2,3,\dots,p$
- $|\beta_i|<1\ \forall i=1,2,3,\dots,q$ and $1-\sum_{i=1}^q\beta_i\ne 0$

#### Equivalence of AR and MA
Consider the [[Difference equations|difference equation]]$$y_t=a_0+a_1y_{t-1}+\epsilon_t\tag{1}$$Using [[Difference equations#Forward iteration|forward iteration]], as $t\to\infty$, $$y_t=\frac{a_0}{1-a_1}+\sum_{i=0}^\infty a_1^i\epsilon_{t-i}\tag{2}$$when $|a_1|<1$. (1) is a AR(1) model and (2) is a MA($\infty$) model. These two are equivalent. Similarly, consider a MA(1) model$$y_t=\epsilon_t+\beta_1\epsilon_{t-1}$$Taking [[Lag operator]]s, $$y_t=(1+\beta L)\epsilon_t$$$$\frac{y_t}{1+\beta L}=\epsilon_t$$if $\beta<0$ and $|\beta|<1$$$y_t+\beta y_{t-1}+\beta^2y_{t-2}+\dots=\epsilon_t$$
if $\beta>0$ and $|\beta|<1$$$y_t-\beta y_{t-1}-\beta^2y_{t-2}-\dots=\epsilon_t$$
In both cases, the process is AR($\infty$). 

#### [[Stationarity]] of a AR process
Consider the AR(1) model$$y_t=a_0+a_1y_{t-1}+\epsilon_t$$The [[Difference equations#Homogenous solution|HGNS]] solution is given by $y_t^h=Aa_1^t$

Iterating forward, the particular solution is given by $$y_t^{\text{PS}}=\frac{a_0}{1-a_1}+\sum_{i=0}^\infty a_1^i\epsilon_{t-i}$$Therefore, the general solution is $$y_t=Aa_1^t+\frac{a_0}{1-a_1}+\sum_{i=0}^\infty a_1^i\epsilon_{t-i}\tag 3$$If we assume that the error terms follow a [[white noise processes|white noise]] process and take expectations, $$\mathbb E(y_t)=Aa_1^t+\frac{a_0}{1-a_1}$$But if $|a_1|<1$ and $t\to\infty$, $y_t^h\to 0$
$$\mathbb E(y_t)=\frac{a_0}{1-a_1}$$which is constant. Finding the variance, $$\text{Var}(y_t)=\mathbb E[(y_t-\mu)^2]=\mathbb E(y_t-\frac{a_0}{1-a_1})^2 $$We know that the homogenous soln. =0 and from (3), $$\text{Var}(y_t)=\mathbb E(\sum_{i=0}^\infty a_1^i\epsilon_{t-i})^2 $$$$=\mathbb E(\epsilon_t^2)+a_1\mathbb E(\epsilon_{t-1}^2)+a_1^2\mathbb E(\epsilon_{t-2}^2)+\dots$$$$=\sigma^2+a_1^2\sigma^2+(a_1^2)^2\sigma^2+\dots$$$$\text{Var}(y_t)=\frac{\sigma^2}{1-a_1^2}$$as $|a_1|<1$. This is a constant variance. Taking the covariance, $$\text{Cov}(y_ty_{t-s})=\mathbb E[(y_t-\mu)(y_{t-s}-\mu)]$$$$=\mathbb E[(\sum_{i=0}^\infty a_1^i\epsilon_{t-i})(\sum_{i=0}^\infty a_1^i\epsilon_{t-s-i})]$$after expanding and simplifying,$$=\sigma^2(a_1)^s[1+(a_1)^2+(a_1^2)^2+\dots]$$$$=\frac{\sigma^2(a_1)^s}{1-(a_1)^2}$$Therefore the stationarity conditions are:
1. $|a_1|<1$
2. $t$ must be large
3. The homogenous solution =0 => $A=0$ or $a_1=0$

#### Autocorrelation Function (ACF)
Consider an AR(1) process. From the above section, we know that$$\mathbb E(y_t)=\frac{a_0}{1-a_1}$$$$\text{Var}(y_t)=\frac{\sigma^2}{1-a_1^2}$$$$\text{Cov}(y_ty_{t-s})=\frac{\sigma^2(a_1)^s}{1-(a_1)^2}$$
If we define $\gamma_s=\text{Cov}(y_ty_{t-s})$, then the ACF is given by the terms $$\rho_0=\frac{\gamma_0}{\gamma_0}; \rho_1=\frac{\gamma_1}{\gamma_0}$$Taking the values of the gammas, $$\rho_1=\frac{\text{Cov}(y_ty_{t-1})}{\text{Cov}(y_ty_t)}=\frac{\text{Cov}(y_ty_{t-1})}{\text{Var}(y_t)}$$which is the [[Simple Linear Regression|OLS]] coefficient. The value of all such $\rho_s$ values is the **ACF function**. Based on the properties of the function, we can identify the number of parameters and they type of ARIMA process. 

##### Finding ACF function for ARMA(2,1) using yule-walker equations
The process is given by:$$y_t=a_1y_{t-1}+a_2y_{t-2}+\epsilon_t$$we assume that the series is stationary, implying that the covariance between any two terms is constant ($\gamma_s$).
Finding the gammas,$$\gamma_0=\mathbb E(y_t^2)=\mathbb E[y_t(a_1y_{t-1}+a_2y_{t-2}+\epsilon_t)]=a_1\mathbb E(y_ty_{t-1})+a_2\mathbb E(y_ty_{t-2})+\mathbb E(y_t\epsilon_t)$$But $\mathbb E(y_ty_{t-2})=\gamma_2$, $\mathbb E(y_ty_{t-1})=\gamma_1$. Further, $$\mathbb E(y_t\epsilon_t)=\mathbb E[\epsilon_t(a_1y_{t-1}+a_2y_{t-2}+\epsilon_t)]=a_1\mathbb E(\epsilon_ty_{t-1})+a_2\mathbb E(\epsilon_ty_{t-2})+\mathbb E(\epsilon_t^2)$$The covariance between $y_{t-s}$ and $\epsilon_t$ where $s>0$ is zero as $\epsilon_t$ is the stochastic component for the time $t$ and is not related to past values of the series. Also the variance of $\epsilon_t$ is $\sigma^2$. 
Therefore$$\gamma_0=a_1\gamma_1+a_2\gamma_2+\sigma^2$$$$\gamma_1=\mathbb E(y_ty_{t-1})=\mathbb E[y_{t-1}(a_1y_{t-1}+a_2y_{t-2}+\epsilon_t)]=a_1\mathbb E(y_{t-1}^2)+a_2\mathbb E(y_{t-1}y_{t-2})+\mathbb E(y_{t-1}\epsilon_t)$$$$\gamma_2=\mathbb E(y_ty_{t-2})=\mathbb E[y_{t-2}(a_1y_{t-1}+a_2y_{t-2}+\epsilon_t)]=a_1\mathbb E(y_{t-1}y_{t-2})+a_2\mathbb E(y_{t-2}^2)+\mathbb E(y_{t-2}\epsilon_t)$$$$\gamma_s=\mathbb E(y_ty_{t-s})=\mathbb E[y_{t-s}(a_1y_{t-1}+a_2y_{t-2}+\epsilon_t)]=a_1\mathbb E(y_{t-1}y_{t-s})+a_2\mathbb E(y_{t-2}y_{t-s})+\mathbb E(y_{t-s}\epsilon_t)$$
Replacing term values with gamma, we find 
$\gamma_1=a_1\gamma_0+a_2\gamma_1$ (constant covariance due to stationarity)
$\gamma_2=a_1\gamma_1+a_2\gamma_1$
$\vdots\ \ \ \ \ \ \ \ \vdots$
$\gamma_s=a_1\gamma_{s-1}+a_2\gamma_{s-2}$

Finding rhos, 
$\rho_0=\gamma_0/\gamma_0=1$
$\rho_1=\gamma_1/\gamma_0=a_1\rho_0+a_2\rho_1\implies \rho_1=\frac{a_1}{1-a_2}$
$\vdots\ \ \ \ \ \ \ \ \vdots$
$\rho_s=a_1\rho_{s-1}+a_2\rho_{s-2}$

##### Finding ACF function for MA(1) using yule-walker equations
Consider the moving average process$$y_t=\epsilon_t+\beta\epsilon_{t-1}$$Taking the YWE, $$\gamma_0=\mathbb E(y_t^2)=\mathbb E[y_t(\epsilon_t+\beta\epsilon_{t-1})]=\mathbb E(y_t\epsilon_t)+\beta\mathbb E(y_t\epsilon_{t-1})$$Substituting $y_t$ into the equation, $$\gamma_0=\mathbb E(\epsilon_t(\epsilon_t+\beta\epsilon_{t-1}))+\beta\mathbb E(\epsilon_{t-1}(\epsilon_t+\beta\epsilon_{t-1}))=\mathbb E(\epsilon_t^2)+\beta\mathbb E(\epsilon_t\epsilon_{t-1})+\beta\mathbb E(\epsilon_t\epsilon_{t-1})+\beta^2\mathbb E(\epsilon_{t-1}^2)$$As $\epsilon$ is a [[white noise processes]], covariance between any terms is 0. Therefore, $$\gamma_0=(1+\beta^2)\sigma^2$$
Similarly, $$\gamma_1=\mathbb E(y_ty_{t-1})=\mathbb E(y_{t-1}\epsilon_t)+\beta\mathbb E(y_{t-1}\epsilon_{t-1})=\mathbb E(\epsilon_t(\epsilon_{t-1}+\beta\epsilon_{t-2}))+\beta\mathbb E(\epsilon_{t-1}(\epsilon_{t-1}+\beta\epsilon_{t-2}))$$$$=\beta\mathbb E(\epsilon_{t-1})^2=\beta\sigma^2$$
$$\gamma_s=\mathbb E(y_ty_{t-s})=\mathbb E(\epsilon_t(\epsilon_{t-s}+\beta\epsilon_{t-s-1}))+\beta\mathbb E(\epsilon_{t-1}(\epsilon_{t-s}+\beta\epsilon_{t-s-1}))=0$$
Finding rhos,
$\rho_0=\gamma_0/\gamma_0=1$
$\rho_1=\gamma_1/\gamma_0=\beta/(1+\beta^2)$
$\vdots\ \ \ \ \ \ \ \ \vdots$
$\rho_s=0$

Plotting this ACF function we find that 
![[Pasted image 20240214025725.png|400]]
There is only one nonzero term.

##### ARMA characteristics based on ACF
- Geometrically decaying ACF => AR process
- Fixed number of ACFs
	- 1 ACF => MA(1) process
	- 2 ACFs => MA(2) process ($\rho_1,\rho_2\ne0, \rho_{3,\dots,s}=0$)
	and so on
- Decaying ACF after $q$ => ARMA($p$,$q$) process

$$\text{ACF}=\rho_s=\frac{\text{Cov}(y_{t-s}, y_{t})}{\text{Var}(y_t)}$$
#### Partial Autocorrelation Function (PACF)
If the mean of the series is $\mu$, we convert the series into a demeaned form.$$y_t-\mu=\phi_{1,1}(y_{t-1}-\mu)+\epsilon_t$$$$y_t^*=\phi_{1,1}y_{t-1}^*+\epsilon_t$$The phi terms are the PACFs.
##### ARMA characteristics based on PACF
- Geometrically decaying PACF => MA process
- Fixed number of pACFs
	- 1 PACF => AR(1) process
	- 2 PACFs => AR(2) process 
	and so on
- Decaying ACF after $p$ => ARMA($p$,$q$) process


