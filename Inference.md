Various [[Hypothesis Testing|hypothesis tests]] to find inference in a [[Multiple variable regression|regression]] analysis
#### Test for significance of $x_1$
$H_0:\beta_1=0$
$H_a:\beta_1\ne 0$
As there is no population variance, the test is a [[Hypothesis Testing|t -test]]

Test statistic:$$\frac{\hat \beta_1-0}{\sqrt{\frac{\hat\sigma^2}{SST_1(1-R^2_1)}}}$$

This tests if there is any effect of $x_1$ on $y$

#### Linear combination test
t-test because of no population variance
This test checks for equality between two variables, in order to determine which has a higher effect on $y$. The units of measurement have to be equal for the test to hold.

$H_0:\beta_1-\beta_2=0$
$H_a:\beta_1\ne \beta_2$

Test Statistic:
$$\frac{\hat\beta_1-\hat\beta_2-0}{\sqrt{Var(\hat\beta_1)+Var(\hat\beta_1)-2cov(\hat\beta_1,\hat\beta_2)}}$$

#### Joint conditions test
Simultaneously testing for two hypothesis. Tests if $\beta_1$ and $\beta_2$ are significant in explaining $y$. As the test results in a ratio of 2 $\chi^2$ distributions, the test uses an F-distribution.

$H_0:\beta_1=0, \beta_2=0$

When $H_0$ holds, $$y=\beta_0+u=SSR_{rest}$$When $H_0$ does not, $$y=\beta_0+\beta_1x_1+\beta_2x_2+u=SSR_{unrest}$$

If $\beta_1$ and $\beta_2$ are significant in explaining $y$, the residuals should be more in the $SSR_{rest}$ than in $SSR_{unrest}$ as $\beta_1$ and $\beta_2$ explain parts of $y$.

Test statistic=
$$\frac{[SSR_{rest}-SSR_{unrest}]/q}{SSR_{unrest}/(n-k-1)}=F_{q,\ n-k-1}$$

This test statistic is obtained when we add or subtract two $\chi^2$ distributions, the degrees of freedom get added/subtracted, resulting in $q$ for the numerator, which is the number of restrictions. Since the SST for both the restricted and the unrestricted models is the same, the test statistic can be represented in the $R^2$ form.$$\frac{(R^2_u-R^2_r)/q}{(1-R^2_u)/n-k-1}$$ 

##### Non-zero joint conditions test
In this case one or more of the betas are tested to be any particular number. 
$H_0:\beta_1=1, \beta_2=0$

When $H_0$ holds, the restricted model is $$y_i=\beta_0+x_{1i}+u_i$$$$y_i-x_{1i}=\beta_0+u_i$$When $H_0$ does not hold, the unrestricted model is$$y_i=\beta_0+\beta_1x_{1i}+\beta_2x_{2i}+u_i$$
However, in the restricted model the dependant variable is no longer limited to just $y_i$, therefore the SSTs are not the same, which means that the $R^2$ method does not work. The F statistic is 
$$\frac{[SSR_{rest}-SSR_{unrest}]/q}{SSR_{unrest}/(n-k-1)}=F_{k,\ n-k-1}$$
