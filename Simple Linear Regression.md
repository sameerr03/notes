The objective of simple linear regression is to plot a line of best fit for a scatterplot and determine causality in a population. The form of the **population regression function** is $$y=\beta_0+\beta_1x+u$$where:
- $y$ is the dependent variable
- $\beta_0$ is the intercept term 
- $\beta_1$ is the slope term
- $x$ is the independent/explanatory variable
- $u$ is the error. It is the difference between the actual values of $y$ and the predicted values of $y$.

As the regression function cannot be found as we do not have the data for the entire population, samples are used to find the regression equation. The **sample regression function** is given by $$\hat y=\hat{\beta_0}+\hat{\beta_1}x+\hat{u}$$Where $\hat u$ is the residual, $\hat y-y$ 
$$\hat{\beta_0}=\bar{y}-[\frac{\sum_{i=1}^{n}(x_i-\bar{x})(y_i-\bar{y})}{\sum_{i=1}^{n}(x_i-\bar{x})^2}]\bar{x}$$$$\hat{\beta_1}=\frac{\sum_{i=1}^{n}(x_i-\bar{x})(y_i-\bar{y})}{\sum_{i=1}^{n}(x_i-\bar{x})^2}$$The parameters can be hypothesis tested in order to determine whether there is any statistical significance of x on y. If $\beta_1$ can be 0, then x may not have any effect on y. 

### Assumptions
1. $E(u)=0$ -> the error is minimized
2. $E(u|x)=0$ → $u$ and $x$ are independent (no [[Correlation]] between u and x). This accounts for selection bias. Other factors not accounted for in the model are independent from the independent variable (for unbiasedness)
4. $Var(u|x)=\sigma^2$ homoskedacity


### Arithmetic properties of the regression
1. $\sum_{i=0}^n\hat{u_i}=0$ (residual, not error - error for population, residual for sample) First [[Simple Linear Regression#Derivation|FOC]]
2. $\sum_{i=0}^n x_i\hat{u_i}=0$ Second [[Simple Linear Regression#Derivation|FOC]]
3. point $(\bar{x},\bar{y})$ is on the regression line
4. $y_i=\hat{y_i}+\hat{u_i}$ This implies that $\bar{y}=\bar{\hat{y}}$
5. $\sum \hat{y_i}\hat{u_i}=0$, sample covariance is 0
6. SST=SSE+SSR (Total sum of squares=Explained sum of squares+Residual sum of squares $\sum(y_i-\bar{y})^2=\sum(\hat{y_i}-\bar{y})^2+\sum(y_i-\hat{y_i})^2$)

### Goodness of fit
a measure of explaining variations in $y_i$ from the regression line $\hat{y_i}$$$R^2=1-\frac{SSR}{SST}$$R-square is the correlation coefficient. It lies between 0 and 1, the closer it is to 1, the beter the fit. There is less variation from the actual y and the sample y.

### Transformations
#### Linear
A transformation such as a change in units. This results in a change in both $\hat{\beta_0}$ and $\hat{\beta_1}$. If y'=a+cy substituting y with the old regression and new paremeters for y' regression we get, $\beta'_0=a+c\beta_0$ and $\beta_1'=c\beta_1$.
If the dependant variable changes (x'=a+cx), using a similar process, $\beta_0=\beta_0'+a\beta_1'$ and $\beta_1'=\beta_1/c$. In both these cases, $R^2$ remains constant. 

#### Non-Linear
When y increases with a greater level than the increase in x but is still dependant on x, the log-level model is used where $\ln y=\beta_0+\beta_1x$. In order to measure elasticity, the log-log model is used where $\ln y=\beta_0+\beta_1\ln x+u$. The slope remains the same but the intercept changes.

### Estimator unbiasedness and variance
#### Assumptions
1. PRF is linear for x and y
2. A random sample of size n is used to estimate the prf
3. $E(u|x)=0$ -> $u$ and $x$ are independant, the error is not dependant on $x$.
4. There is sample variation in $x_i$
5. Errors are homoskedastic, the variance of errors does not change according to observations $Var(u|x)=\sigma^2$
#### Unbiasedness
![[SmartSelect_20230222_195724_Samsung Notes.jpg|400]]
![[SmartSelect_20230222_195842_Obsidian.jpg|400]]
![[SmartSelect_20230222_200041_Samsung Notes.jpg|400]]
#### Variance
How disperesed β^1 is around the population parameter for each sample
Assumption: As u and x are independant, the variance of u is constant for all values of x.(homoskedacity)$$E(u^2|x)=\sigma^2=E(u^2)$$$$Var(\hat\beta_1|x)=E[(\hat\beta_1-\beta_1)^2|x]$$$$=\frac{\sum(x_i-\bar{x})^2E(u^2|x)}{(SST_x)^2}$$$$=\frac{\sigma^2}{SST_x}$$However, the population variance is not known. We only have the variance of the residual and have to use that to estimate the variance.$$\hat{\sigma}^2=(\sum\hat{u_i}^2)/(n-2)$$As we have 2 first order conditions, we can find out the remaining residuals. Therefore we have 2 less degrees of freedom, resulting in n-2. 

$\hat\sigma$ is not an unbiased estimator of $\sigma$ therefore we have to find the error. Root mean square error:$$\sqrt{\hat \sigma^2}=\hat\sigma=RMSE$$$$s.e.(\hat\beta_1)=\frac{\hat\sigma}{\sqrt{SST_x}}$$this is used to construct a confidence interval for the estimation, and do hypothesis testing for the about parameters. When the assumption 5 is broken however, the model exhibits heteroskedacity - varience differs with each value of x.

### Regression through the origin
$$y=\beta x+u$$
minimising the sum of square residuals,
$$\hat\beta=\frac{\sum x_iy_i}{\sum x_i^2}$$
$\hat\beta$ is a biased estimator of $\beta_1$ that is unbiased only if $\beta_0=0$


### Derivation
The estimation is obtained by minimising the error. As the error can be negative, we need to minimise the sum of squares of the error. $$min\sum_{i=1}^{n}\hat{u_i}^2=min\sum_{i=1}^{n}(y_i-\hat{\beta_0}-\hat{\beta_1}x_i)^2$$Taking the first order conditions:
$$\beta_0:\frac{\partial SSR}{\hat{\beta_0}}=-2\sum_{i=1}^{n}(y_i-\hat{\beta_0}-\hat{\beta_1}x_i)=0$$$$\hat{\beta_1}:\frac{\partial SSR}{\partial\hat{\beta_1}}=-2\sum_{i=1}^{n}x_i(y_i-\hat{\beta_0}-\hat{\beta_1}x_1)=0$$From the first condition,$$\sum_{i=1}^{n}y_i-n\hat{\beta_0}-\hat{\beta_1}\sum_{i=1}^{n}x_i=0$$$$\hat{\beta_0}=\frac{1}{n}\sum_{i=1}^{n}(y_i-\hat{\beta_1}x_i)=\bar{y}-\hat{\beta_1}\bar{x}$$Substituting this into 2,$$\sum_{i=1}^{n}x_i(y_i-\bar{y}+\hat{\beta_1}\bar{x}-\hat{\beta_1}x_i)=0$$$$\sum_{i=1}^{n}x_iy_i-\sum_{i=1}^{n}x_i\bar{y}+\sum_{i=1}^{n}x_i\hat{\beta_1}\bar{x}-\sum_{i=1}^{n}x_i\hat{\beta_1}x_i=0$$$$\sum_{i=1}^{n}x_iy_i-\bar{y}\sum_{i=1}^{n}x_i=\hat{\beta_1}(\sum_{i=1}^{n}x_i^2-\bar{x}\sum_{i=1}^{n}x_i)$$$$\hat{\beta_1}=\frac{\sum_{i=1}^{n}x_iy_i-\bar{y}\sum_{i=1}^{n}x_i}{\sum_{i=1}^{n}x_i^2-\bar{x}\sum_{i=1}^{n}x_i}$$From the formula for calculating means,$$=\frac{\sum_{i=1}^{n}x_iy_i-n\bar{y}\bar{x}}{\sum_{i=1}^{n}x_i^2-n\bar{x}^2}$$$$\hat{\beta_1}=\frac{\sum_{i=1}^{n}(x_i-\bar{x})(y_i-\bar{y})}{\sum_{i=1}^{n}(x_i-\bar{x})^2}$$This is the co-vaiance of (x,y) divided by the variance of x. Using this value,
$$\hat{\beta_0}=\bar{y}-[\frac{\sum_{i=1}^{n}(x_i-\bar{x})(y_i-\bar{y})}{\sum_{i=1}^{n}(x_i-\bar{x})^2}]\bar{x}$$

