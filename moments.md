
Describes distribution of numbers around a point. Moments are necessary as the [[Measures of central tendency|mean]] can be misleading when comparing two datasets. 

We define the rth moment about the origin of a [[random variables|random Variable]] X as the expected value of $X^r$
$$\mu_r'=E[X^r]=\sum_x x^r\cdot f(x)$$or $$\mu_r'=\int_{-\infty}^{\infty} x^r\cdot f(x)$$for continuous [[random variables]].
The first moment about the origin (r=1), $\mu_r' = E(X)=$ mean

## Moment about the mean
The rth moment about the mean of a random variable X
$$\mu_r'=E[(x-\mu)^r]=\sum_x (x-\mu)^2\cdot f(x)$$
The second moment about the mean (r=2) is the [[Frequency distributions#Variance|variance]]
$$\mu_2'=E[(x-\mu)^2]=E[x^2-2x\mu+\mu^2]=E(x^2)-\mu^2=E(x^2)-[E(x)]^2$$
Third moment: Skewness
Fourth moment: Kurtosis
## Moment generating function
Generates moments around the orgin
$$M_x(t)=E(e^{tX})=\sum_x e^{tx}\cdot f(x)$$
Derivatives give us the moment. Derivative when t=0 = E(X) = mean