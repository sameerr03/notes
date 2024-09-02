There is no effect of [[Simple Linear Regression#Transformations|linear transformations]] on the [[Inference]] test statistics of the various tests of beta parameters in a [[Multiple variable regression]].

##### Independant variable change of scale
if $x^*=ax+b$,
$\beta_1^*=\frac{\beta_1}a$
$s.e.(\beta^*_1)=\frac 1a s.e.(\beta_1)$
Test statistic for $H_0:\beta^*_1=0$$$\frac{\beta_1}{s.e.(\beta_1)}$$
Test statistic for $H_0:\beta^*_1=c/a\implies\beta_1=c$$$\frac{\beta_1-c}{s.e.(\beta_1)}$$
##### Dependant variable change of scale
if $y^*=ay+b$,
$\beta_1^*=a\beta_1$
$s.e.(\beta^*_1)=a\ s.e.(\beta_1)$
Test statistic for $H_0:\beta^*_1=0$$$\frac{\beta_1}{s.e.(\beta_1)}$$
Test statistic for $H_0:\beta^*_1=ac\implies\beta_1=c$$$\frac{\beta_1-c}{s.e.(\beta_1)}$$

in this case, the errors are $\epsilon^*=a\epsilon$
For a joint test this remains the same as well

##### Log transformation
The log form is used when the dependant variable is positively skewed. Using log makes the transformed variable normally distributed.
Suppose we take a [[Multiple variable regression]] as $$\log y=\beta_0+\beta_1x_1+\beta_2x_2+u$$In order to find the relation between this dependant variable and just taking $y$ as the dependant variable, we transform the function$$y=exp(\beta_0+\beta_1x_1+\beta_2x_2+u$$$u$ is the only random variable in the term. therefore we take it out$$=exp(\beta_0+\beta_1x_1+\beta_2x_2)\cdot exp(u)$$$$E(y|x)=exp(\beta_0+\beta_1x_1+\beta_2x_2)\cdot E(e^u|x)$$
We know that $u$ is independant of $x$ as we assume that error is homoskedastic. Therefore the expectation conditional on $x$ is just the expectation. $$E(y|x)=exp(\beta_0+\beta_1x_1+\beta_2x_2)\cdot E(e^u)$$This expected value is unclear. We assume the $u$ is a normally distributed random variable. Transforming $u$ into a standard normal distribution $Z$, we get $$Z=\frac{u-\mu}\sigma$$$$u=\sigma Z+\mu$$Putting this value into the expectation, and using the CDF formula for a normal distribution, $$E(e^u)=\int_{-\infty}^\infty e^{\sigma Z+\mu}\ \phi(Z)dZ$$$$E(e^u)=\int_{-\infty}^\infty e^{\sigma Z+\mu}\ \frac 1{\sqrt {2\pi}}e^{-\frac{Z^2}{2}}dZ$$$$E(e^u)=\int_{-\infty}^\infty \frac 1{\sqrt {2\pi}}e^{\sigma Z+\mu -\frac{Z^2}{2}}dZ$$Completing the square in the power,$$=e^\mu\int_{-\infty}^\infty \frac 1{\sqrt {2\pi}}e^{-(\frac{Z^2}{2}-\sigma Z
+\frac{\sigma^2}2-\frac{\sigma^2}2)}dZ$$$$=e^\mu\int_{-\infty}^\infty \frac 1{\sqrt {2\pi}}e^{-(\frac{Z}{\sqrt 2}-\frac{\sigma}{\sqrt 2})^2+\frac{\sigma^2}2}dZ$$$$=e^{\mu+\frac{\sigma^2}2}\int_{-\infty}^\infty \frac 1{\sqrt {2\pi}}e^{-\frac{(Z-\sigma)}{ 2}^2}dZ$$The term inside the integral is of the form of CDF of a normal distribution with mean $\sigma$ and variance 1. The area under the entire normal distribution is 1. Therefore $$E(e^u)=e^{\mu+\frac{\sigma^2}2}$$Putting this into the expected equation,$$E(y|x)=exp(\beta_0+\beta_1x_1+\beta_2x_2)\cdot e^{\mu+\frac{\sigma^2}2}$$The expected value of $y$ conditional on $x$ is $\hat y$. similarly the expected value for the term in the exponent is $\hat{\log y}$. By FOC's we know that the average of errors is 0. Therefore,$$\hat y=exp(\hat {\log y})\ e^{\frac{\hat\sigma^2}2}$$Replacing the estimated $\hat y$ with the population $y$ and adding an error term, we get $$y=exp(\hat {\log y})e^{\frac{\hat\sigma^2}2}+\epsilon$$Regressing this formula, (exponent term is the $\beta$), we get the correllation ($R^2$) between y and hat log(y), hat y and X. This can be used to determine whether it is appropriate to take the log of y in a regression. We can compare this as the dependant variable is the same as opposed to comparing $R^2$ directly between regression with and without log.

##### Standardizing variables transformation
$$log(y)=\beta_0^*+\beta_1^*(\frac{x_{i1}-\bar x_1}{S_{x_1}})+\beta_2^*(\frac{x_{i2}-\bar{x}_2}{S_{x_2}})+u^*$$This means that an increase in $x_1$ by one standard deviation leads to a $100\times \beta_1$% change in $y$. This is used to compare effect of different variables on $y$ or on $\log(y)$. Comparing to the normal regression form, $$\beta_1^*=S_{x_1}\beta_1$$Further,$$\Delta\log(y)=\beta_1\Delta x_1$$$$\%\Delta y=100\times [exp(\beta_1\Delta x_1)-1]$$
##### Quadratic transformation
$$y=\beta_0+\beta_1x+\beta_2x^2+u$$Suppose $\beta_1>0$ and $\beta_2<0$, this implies that beyond some value of $x$, an increase in $x$ leads to a decrease in $y$. 

##### Interaction among variables form
$$y=\beta_0+\beta_1x_1+\beta_2x_2+\beta_3x_1x_2+u$$Beta 3 shows the interaction between $x_1$ and $x_2$. Finding the marginal effects, $$\frac{\partial y}{\partial x_2}=\beta_2+\beta_3x_1$$This means that the increase of $y$ due to $x_2$ is greater, the greater value of $x_1$. If $x_2$ is experience and $x_1$ is education, this means that the returns to experience (wages) from someone with more education is more than someone with lower education. 