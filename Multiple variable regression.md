Builds on the concepts of [[Simple Linear Regression]] but with the ability to control for even more variables. The equation is now of the form$$y_i=\beta_0+\beta_1{x_1}_i+...+\beta_k{x_k}_i+u_i$$The marginal effect of a particular variable on the dependant variable is given by the partial derivative of the variable. Using ordinary least squares, we need to minimise the error squared $(u^2_i)$$$min\ \sum \hat{u_i}^2=\mathcal{L}$$Taking partial derivatives of all the betas, we get all the conditions. This is solved by using matrix differentiating. A simpler way to obtain the formula for 2 variables is to 
1. regress $x_1$ on $x_2$ and intercept. $\hat{r}_1$ is the residual from this regression. The regression is of the formula $$x_1=\hat\pi_0+\hat\pi_2x_2+\hat{r}_1$$
2. Regress $y$ on $\hat{r}_1$. This gives the formula$$y=\beta_0'+\hat{\beta_1}\hat{r}_1+e$$
This two step method isolates the effect of $x_2$ on $x_1$ and then shows the pure effect of $x_1$ on $y$
$$\hat\beta_1=\frac{\sum \hat r_{i1}y_{i1}}{\sum \hat r_{i1}^2}$$

### Goodness of fit test
Any number of variable can be added to the regression to explain all the data points which would ruin the models prediction power outside the sample. Therefore, a measure of fit is needed better than simple [[Simple Linear Regression#Goodness of fit|correlation]]. Adding variables reduce the degrees of freedom, which is accounted for in adjusted r-square. $$AR^2=1-\frac{SSR/(n-(k+1))}{SST/(n-1)}$$

### Variance
How disperesed $\hat\beta_1$ is around the population parameter for each sample 
The variance of the parameter is given by $$Var(\hat\beta_1)=\frac{\sigma^2}{SST_{r_1}}$$$$=\frac{\sigma^2}{SST_{x_1}(1-R_{x_1}^2)}$$ As the variance of the error cannot be found, $\hat\sigma^2$ is used as the estimator, where $$\hat\sigma^2=\frac{\sum\hat{u}^2_i}{n-k-1}$$results in a biased estimate with standard error.$$s.e.(\hat\beta_i)=\frac{\hat\sigma}{\sqrt{SST_i(1-R^2_i)}}$$
### Unbiasedness

#### Assumptions
For unbiasedness of OLS estimator in MLR, an additional assumptions are required compared to [[Simple Linear Regression]]. 
4. No perfect colinearity between the n variables. This implies that $x_1\ne\alpha x_2$ -> would result in identical first order conditions (one variable should not be linear)
5. Homoskedacity: $Var(u|x)=\sigma^2$. OLS estimator becomes inefficient if the sample is heteroskedastic
6. Errors are distributed normally $u\sim N(0,\sigma^2)$

#### Omitted variable bias
$$\hat\beta_1=\frac{\sum(x_i-\bar x)y_i}{\sum(x_i-\bar x)^2}=\frac{\sum(x_i-\bar x)(\beta_0+\beta_1x_1+\beta_2x_2+u)}{\sum(x_i-\bar x)^2}$$
$$\hat\beta_1=\beta_1\frac{\sum x_1(x_i-\bar x)}{SST_x}+\beta_2\frac{\sum x_2(x_i-\bar x)}{SST_x}+\frac{\sum(x_i-\bar x)u_i}{SST_x}$$
We know that $\sum x_1(x_i-\bar x)=\sum(x_i-\bar x)^2$
$$E(\hat \beta_1|x)=\beta_1+\beta_2\frac{\sum x_2(x_i-\bar x)}{SST_x}+0$$$$E(\hat \beta_1|x)=\beta_1+\beta_2\frac{\sum x_2(x_i-\bar x)/n}{SST_x/n}$$$$E(\hat \beta_1|x)=\beta_1+\beta_2\frac{cov(x_1,x_2)}{var(x_1)}$$If the $\beta_2$ term is = 0, or $\pi_1=0$, there is no bias. if the relation between $x_1$ and $x_2$, is true, $\hat \beta_1$ will be an overestimate of the population parameter. In the example case of education ($x_1$) and ability ($x_2$) on wages, the relation of $x_2$ on $x_1$ will be positive as people with higher ability more often are more educated
![[SmartSelect_20230227_205705_Samsung Notes.jpg|400]]

##### Variance
Overestimation of the population parameter results in a stronger relation between $x_1$ and $y$ which results in a higher $R^2$ value, leading to higher [[Multiple variable regression#Variance|variance]].

##### Consistency
When n->$\infty$, $$\hat \beta_1\to\beta_1+\beta_2\frac{cov(x_1,x_2)}{var(x_1)}$$This implies that there will always be bias, even when n is infinity unless $\beta_2=0$
