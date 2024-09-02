#flashcards/stats 
# Types of [[random variables]]
## Discrete types of Random Variables
### Bernoulli random variable
**Bernoulli random variable** ::: captures success or faliure of a trial.
X=1 for sucess and 0 for faliure

$f(X=0)=1-p$ 
$f(X=1)=p$
$F(X=0)=1-p$
$F(1)=1$

$E(X)=0\times (1-p)+p =p$
$\sigma^2=p-p^2=p(1-p)$

### Binomial random variable
**Binomial random variable** ::: The number of successful experiments (i) out of n independant trials
<!--SR:!2022-10-12,1,230-->

$f(X=i)=^nC_ip^i(1-p)^{n-i}$ 
$F(X=i)=\sum_{k=0}^i \ ^nC_kp^k(1-p)^{n-k}$
$E(X)=np$
$\sigma^2=np(1-p)$

### Poisson random variable
**Poisson random variable** ::: Binomial variable only for rare events (large number of trials and very low probability)

$f(X=i)=e^{-\lambda} \frac{\lambda^i}{i!}$ 
$F(X=i)=\sum_{k=0}^i \ e^{-\lambda} \frac{\lambda^k}{k!}$
$E(X)=\lambda$
$\sigma^2=\lambda$

For $n\ge20$ and $p\le0.05$ binomial and poisson RVs are roughly similar. Therefore $\lambda$ = E(X) for a binomial rv for these conditions.

### Negative Binomial random variable
**Negative Binomial random variable** ::: The number of trials needed for r successes
<!--SR:!2022-10-12,1,230-->

$f(X=r)= ^{n-1}C_{r-1}p^r(1-p)^{n-r}$ 
$F(X=i)=\sum_{k=0}^i \ ^{n-1}C_{r-1}p^r(1-p)^{n-r}$
$E(X)=r/p$
$\sigma^2=r(1-p)/p^2$

### Geometric random variables
**Geometric random variables** ::: Probability of success after a series of faliures

$f(X=i)= p(1-p)^{i-1}$ 
$F(X=i)=\sum_{k=0}^i \ p(1-p)^{k-1}$
$E(X)=1/p$
$\sigma^2=(1-p)/p^2$

## Both types of random variables
### Uniform random variables 
Can be discrete or continuous. 
In a uniform RV,:: for each value x of the rv, p(x) is the same. 
![[Pasted image 20221013132141.png|400]]![[Pasted image 20221013132157.png|400]]
Represented as X~U($\alpha, \beta$)

$f(x)=1/(\beta-\alpha)$
$F(x)=(x-\alpha)/(\beta-\alpha)$
$E(X)=\int_\alpha^\beta x\cdot f(x)\ dx=(\alpha+\beta)/2$


## Continuous types of Random Variables

### Normal Random Variable (X~N($\mu,\sigma^2$))

Normal random variable distribution :: density function that is symmetric around the mean (bell curve).
mean = median= mode for a perfect normal distribution

Two parameters that describe a normal distribution
- [[Measures of central tendency|mean]]($\mu$) :: changes the position of the distribution on the X axis
- spread: vertical and horizontal spread. These spreads are related to each other (Inversely proportional). Horizontal spread of the normal distribution is the [[Frequency distributions|standard deviation]] or ($\sigma$).  Higher the SD, higher the spread, flatter the curve.

![[Pasted image 20221018003933.png|300]]![[Pasted image 20221018003947.png|300]]

$f(X)=\frac{ 1} { \sqrt { 2 \pi\sigma ^ z } }e ^ { -( x - \mu ) ^ 2/ 2 \sigma ^ 2 }$

#### Transformations of a normal distribution

If $Y= \alpha X+ \beta$ then the expected value of X, $E(X) \alpha \mu + \beta$ and the variance is $Var(X)= \alpha^ 2 \sigma ^2$.

If $Z=aX+bY$, the variance is 
If two RVs $X_1, X_2$ are distributed normally with means $\mu_1,\mu_2$ and variance $\sigma^2_1,\sigma^2_2$, $X_1-X_2$ will be equal to $$X \equiv X_1-X_2\sim N(\mu_1-\mu_2,\sigma^2_1+\sigma^2_2)$$

A normal distribution can be transformed into a [[types of random variables#Standard normal Random Variable|standard normal distribution]], by :: $$Z=\frac{X-\mu}{\sigma}$$
### Standard normal Random Variable
The standard normal distribution (z distribution) is a distribution where :: $$\mu=0,\sigma=1$$
50 percent of the observations lie below zero. values between standard deviations is taken by subtraction of the cumulative probability at the deviations. 

![[Pasted image 20221018005143.png|400]]

$E(X)=\mu$
$Var(X)=\sigma^2$

![[Pasted image 20221018005347.png|400]]
Z probability values can be identified from a table
### Exponential Random Variable

The random variable associated with amount of time untill an event occurs

$f(X) = \lambda e^ { - \lambda x}$ for $x\ge0$. 0 otherwise
$F(X) = 0$ for $x<0$ . $1- e ^ { - \lambda x }$ for $x\ge0$
$E(x) = \frac { 1} { \lambda }$
$Var(X) = \frac { 1} { \lambda^2}$
MGF of $X = \lambda /(\lambda-t)$