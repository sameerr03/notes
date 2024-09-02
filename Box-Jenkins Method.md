A practical method to apply [[ARIMA Model]]s in order to find the best fit of a time-series model to past values of the time series

#### 1. Pre-estimation evaluation
1. The series $\{y_t\}$ is plotted - this gives us information about outliers, structural breaks and so on. 
2. Plot the [[ARIMA Model#Autocorrelation Function (ACF)|ACF]] and [[ARIMA Model#Partial Autocorrelation Function (PACF)|PACF]]s to approximate the most parsimonious model (model with the least number of explanatory variables, with a good explanatory power). 


The conditions of the time series that must be met in this stage are:
1. [[Stationarity]]
2. Invertibility: $\{y_t\}$ is invertible if it can be represented with a finite ARIMA oder - convergent AR process

#### 2. Goodness of fit test
Various selection criteria are used to determine the goodness of fit of ARIMA with various different parameters
##### Akaike Information Criteria (AIC)
$$AIC=T\ln(\text{RSS})+2N$$
where:
- $T$ is the number of useable observations (degrees of freedom)
- $\text{RSS}$ is the sum of square residuals
- $N$ is the number of parameters

As $N$ increases, $T$ falls but RSS increases
##### Schwartz Bayesian Information Criteria (SBC)
$$\text{SBC}=T\ln(\text{RSS})+n\ln(T)$$
Compared to AIC, takes more into account the loss of degrees of freedom by adding more degrees of freedom. This is much better when it comes to making better forecasts. Therefore SBC is always more parsimonious than the AIC

**The model with the smallest AIC/SBC is chosen**

#### 3. Post estimation evaluations
The residuals are plotted to check for outliers. The series can be tested for being [[white noise processes|white noise]] through the [[white noise processes#Q-test|Q stat]]. If the residuals are not white noise, the model is not a good fit.

Another method of testing is calculating standardized residuals $\epsilon_t/\hat\sigma_\epsilon$. The value of these standardized residuals should not be more than 5% outside the band -2 to +2. 

ACF and PACFs should be plotted again

