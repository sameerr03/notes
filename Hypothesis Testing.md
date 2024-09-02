	Make a precise hypothesis and test it instead of a range like in interval estimation

2 hypothesis are made, null and alternative

The Hypothesis is always based on the population parameter

|Null|Alternative|
|---|---|
|Assumed to be given| Needs to be proven |
|Assumed based on the status quo/prior statistical evidence|Rejecion of the assumption|
|Must contain an equality =,$\le$,$\ge$|Must not contain an equality$\ne$,>,<|

The null and the alternative cannot be simultaneously true by design

The outcomes of hypothesis testing is either the rejection of the null hypothesis (alternative is valid) or the faliure to reject the null hypothesis (null is valid)

If the sample mean lies within the critical region (1-[[Estimation of population mean|confidence interval]]=$\alpha$), the hypothesis is rejected. 99% is 2.58sd
![[Pasted image 20221123200333.png]]

The **parameter** is the data point of interest for the entire [[Population|population]]. For the population mean it is $\mu$. For the [[sample]], the same data point is the **statistic or the estimator**. 


In order determine the outcome, the number of standard deviations of the hypothesised parameter is from the statistic is found and then checked with a significance level. If it falls in the critical area, we fail to reject the null. 

### Types of tests
#### Mean test
$H_0$->$\mu=a$ 
$H_a$->$\mu \ne a$
$$Z=\frac{\bar{x}-a}{s/\sqrt{n}}$$
#### Proportion test
$H_0$->$\theta=\theta_0$ 
$H_a$->$\theta\ne \theta_0$
$$Z=\frac{p-\theta_0}{\sqrt{\frac{(\theta_0)(1-\theta_0)}{n}}}$$
#### Difference in mean
$H_0$->$\mu_1-\mu_2=a$ 
$H_a$->$\mu_1-\mu_2\ne a$

If the assumption of normality and homogeneity of variance ($\sigma_1^2=\sigma_2^2$) is correct
$$t=\frac{(X_1-X_2)-a}{\sqrt{\frac{\sigma^2}{n_1}+\frac{\sigma^2}{n_2}}}$$Where $$\sigma^2=\frac{\text {DOF}_1\times \sigma_1^2+\text {DOF}_2\times \sigma_2^2}{\text {DOF}_1+\text {DOF}_2}$$and the degrees of freedom is given by $\text {DOF}_1+\text {DOF}_2$
If the assumption is not held, then $$t=\frac{(X_1-X_2)-a}{\sqrt{\frac{S_{p_1}^2}{n_1}+\frac{S_{p2}^2}{n_2}}}$$where the degree of freedoms are given by $$\text{DOF}=\frac{(\frac{S_1^2}{n_1}+\frac{S_2^2}{n_2})^2}{\frac1{n_1-1}(\frac{S_1^2}{n_1})^2+\frac{1}{n_2-1}(\frac{S_2^2}{n_2})^2}$$
#### Difference in proportion (best fit test)
$H_0$->$\theta_1=\theta_2=\theta_0$ 
$H_a$->$\theta_1\ne \theta_2$
$$Z=\frac{p_1-p_2}{\sqrt{\frac{(\theta_0)(1-\theta_0)}{n_1}+\frac{(\theta_0)(1-\theta_0)}{n_2}}}$$
If $\theta_0$ is not given,
$\hat{\theta}=\frac{x_1+x_2}{n_1+n_2}$
$$Z=\frac{p_1-p_2}{\sqrt{\frac{(\hat{\theta})(1-\hat\theta)}{n_1}+\frac{(\hat\theta)(1-\hat\theta)}{n_2}}}$$
For jointly dist. rvs, Expected frequency table needs to be created using either $\theta_0$ or $\hat\theta$ table multiplied by the sample size to get expected freq. Comparing the frequency table and the expected frequency table by squaring the difference, dividing by the expected frequency and then adding up, we get the error from the expected frequency. This can be approximated into a $\chi^2$ distribution with dof = rc-(r+c+-1). If the value is very high, the error is high and the null is not true. 