Equations of [[Time Series]], where $y$ is subtracted by a lag term. 

Suppose the generic timeseries equation:
$$y_t=a_0+a_1y_{t-1}+\epsilon_t$$$$y_t-y_{t-1}=a_0+a_1y_{t-1}-y_{t-1}+\epsilon_t$$$$\Delta y_t=a_0+(a_1-1)y_{t-1}+\epsilon_t$$This is a **first order difference equation**. Form here we can test the following:
$H_0:a_1=1$ => there is a unit root in the solution, the time series is **not stationary**. 
$H_A:|a_1|<1$ => there is no unit root, the time series is convergent

A second order difference equation will be:
$$\Delta^2y_t=\Delta(\Delta y)$$$$=\Delta(y_1-y_{t-1})$$$$=\Delta y_t-\Delta y_{t-1}$$$$=(y_t-y_{t-1})-(y_{t-1}-y_{t-2})$$$$=y_t-2y_{t-1}+y_{t-2}$$
#### stability conditions of a difference equation
1. $\sum_{i=1}^na_i<1$ => All characteristic roots must lie within the [[Unit root circle]]
2. $\sum_{i=1}^n|a_i|<1$ => since the values of $a_1$ can be negative or positive, this is the sufficient condition
3. $\sum_{i=1}^n a_i=1$=> any sequence that contains one or more characteristic roots equal to unity, is a unit root process. The time series then is said to follow brownian motion. 
### Finding solutions of difference equations
#### Iteration
##### Forward iteration
Suppose the difference equation, $$y_t=a_0+a_1y_{t-1}+\epsilon_0$$given we know the value of $y_0$, the initial value of $y$. Iterating forward, in $t=1$,$$y_1=a_0+a_1y_0+\epsilon_1$$Iterating forward,$$y_2=a_0+a_1(a_0+a_1y_0+\epsilon_1)+\epsilon_2$$$$=a_0+a_0a_1+a_1^2 y_0+a_1\epsilon_1+\epsilon_2$$$$y_3=a_0+a_1y_2+\epsilon_3$$$$=a_0+a_1(a_0+a_0a_1+a_1^2 y_0+a_1\epsilon_1+\epsilon_2)+\epsilon_3$$$$=a_0(1+a_1+a_1^2)+a_1^3y_0+a_1^2\epsilon_1+a_1\epsilon_2+\epsilon_2$$Extrapolating the pattern,
$$y_t=a_0\sum_{i=0}^{t} (a_1^i)+a_1^ty_0+\sum_{i=0}^{t-1}(a_1^i\epsilon_{t-i})$$
##### Backwards iteration
Forward iteration requires $y_0$ to be known, need not always be the case. $$y_t=a_0+a_1y_{t-1}+\epsilon_t$$where $y$ is not known. Iterating backwards, in $t=t-1$,$$y_{t-1}=a_0+a_1y_{t-2}+\epsilon_{t-1}$$Therefore,$$y_t=a_0+a_1(a_0+a_1y_{t-2}+\epsilon_{t-1})+\epsilon_{t}$$$$=a_0+a_0a_1+a_1^2 y_{t-2}+a_1\epsilon_{t-1}+\epsilon_t$$$$y_{t-2}=a_0+a_1y_{t-3}+\epsilon_{t-2}$$$$y_t=a_0+a_0a_1+a_1^2(a_0+a_1y_{t-3}+\epsilon_{t-2})+a_1\epsilon_{t-1}+\epsilon_t$$$$=a_0(1+a_1+a_1^2)+a_1^3y_{t-3}+a_1^2\epsilon_{t-2}+a_1\epsilon_{t-1}+\epsilon_t$$Extrapolating the pattern,
$$y_t=a_0\sum_{i=0}^{n-1} (a_1^i)+a_1^ny_{t-n}+\sum_{i=0}^{n-1}(a_1^i\epsilon_{n-i})\tag 1$$
##### Unit root cases
###### Case 1
If $|a_1|<1$ and $t\to \infty$, then a geometric progression can be applied.
**For forward induction**,
$$y_t=a_0(\frac 1{1-a_1})+a_1^\infty y_0+\sum_{i=0}^{t-1}(a_1^i\epsilon_{t-i})$$
We also know that $a^\infty_1\to 0$. Therefore, taking expectations we get$$\mathbb E(y_t)=\frac{a_0}{1-a_1}+\sum_{i=0}^{t-1}a_1^i\mathbb E(\epsilon_{t-i})$$But $\mathbb E(\epsilon_{t-1})=0$ by definition. Therefore, the series will converge to a value
**For backward induction**,
($n\to\infty$)
$$y_t=a_0(\frac 1{1-a_1})+a_1^\infty y_{t-n}+\sum_{i=0}^{t-1}(a_1^i\epsilon_{t-i})$$Similar result from taking expectations

###### Case 2
$|a_1|\ge 1$, $t\to\infty$
**For forward induction**
$$y_t=a_0(1+a_1+a_1^2+...)+a_1^\infty y_0+\sum_{i=0}^{t-1}a_1^i\epsilon_{t-i}$$However, $a_1^\infty\to \infty$. Therefore the series will explode. 

**For backward induction,**
$$y_t=a_0(1+a_1+a_1^2+...)+a_1^\infty y_{t-n}+\sum_{i=0}^{t-1}a_1^i\epsilon_{t-i}$$The series will explode here as well.

Based on these cases, we can conclude based on the value of $a_1$ that:
- The higher the value of $a_1$ but below 0, the longer the series takes in order to converge to its expected value. 
- Beyond the absolute value of 1, the series is explosive.
- If $a_1$ is negative, it fluctuates between positive and negative in each consecutive iteration.

#### General Solutions
iteration breaks down on difference equations of higher order (more lagged terms).

The general solution is broken down into two parts:
- Homogenous solution: Finds the solution only for the [[Time Series#Noise/Irregular component|irregular component]]
- Particular solution: Finds the solution for the constant terms like $a_0, \epsilon_t$

Suppose the timeseries equation$$y_t-a_1y_{t-1}-a_2y_{t-1}=k$$

##### Homogenous solution
Taking only the irregular component,$$y_t-a_1y_{t-1}-a_2y_{t-1}=0$$Let $y_t=A\alpha^t$. Then substituting all $y$ values,
$$A\alpha^t-a_1A\alpha^{t-1}-a_2A\alpha^{t-2}=0$$Where $A$ is an arbitrary constant
$$A[\alpha^t-a_1\alpha^{t-1}-a_2\alpha^{t-2}]=0$$Since $A\ne 0$,$$\alpha^t-a_1\alpha^{t-1}-a_2\alpha^{t-2}=0$$Dividing on both sides by $\alpha^{t-2}$,$$\alpha^2-a_1\alpha-a_2=0$$Using the quadratic formula, we can find two roots of the equation,$$\alpha_1,\alpha_2=\frac{a_1\pm \sqrt{a_1^2-4a_2}}{2}$$and $\sqrt d=\sqrt{a_1^2-4a_2}$.

Based on the roots obtained in the general solution there are three cases
###### Real and distinct roots
If $d>0$, this implies that $\alpha_1, \alpha_2$ are real and distinct. Then the HS will be$$y_t^h=A_1(\alpha_1)^t+A_2(\alpha_2)^t$$
**Effect of root values on the timeseries**
1. If $\alpha_1,\alpha_2<1$ and  positive, the series will directly converge to a value
2. If either of the roots is negative but $|\alpha_1|,|\alpha_2|<1$ then the series will oscillate and converge to a value
3. If $\alpha_1\ \&\ \alpha_2>0$ and if either is greater than 1 the series will explode
4. if $|\alpha_1|,|\alpha_2|>1$ and at least one is negative the series will oscillate and explode
###### Real and equal roots
$d=0$, implying that $\alpha_1=\alpha_2=a_1/2$. In this case the HS is$$y_t^h=A(\frac{a_1}{2})^t$$
###### Imaginary roots
If $d<0$, $\alpha_1$ and $\alpha_2$ are imaginary - the HS becomes much more complex. Refer running notes

##### Particular solution
We take the regular component of the series. We also assume $y$ as equal to a constant $c$. Therefore, $$c-a_1 c-a_2 c=k$$therefore, $$c=\frac{k}{1-a_1-a_2}$$
###### Particular solution of a deterministic process
Consider the difference equation$$y_t=a_0+a_1y_{t-1}+a_2y_{t-2}+...+a_n y_{t-n}+.....$$To find the particular solution, we assume that $y_t$ is constant such that $y_t=y_{t-1}=y_{t-2}=....=c$. Therefore,$$c=a_0+a_1c+a_2c+...$$$$c=\frac{a_0}{1-a_1-a_2-......-a_n}$$However, if from the [[Difference equations#stability conditions of a difference equation]], $\sum_{i=1}^n a_i=1$, then $c$ is undefined. To get around this issue, we can introduce a trend component $t$ into the unit root process, giving us a trend stationary time series. $$y_t^p=ct$$$$ct=a_0+a_1c(t-1)+...+a_n c(t-n)+...$$$$[1-a_1-a_2-...-a_n-...]ct=a_0-c(a_1+2a_2+3a_3+...na_n+...)$$Since it is a unit root process, $\sum_{i=1}^n a_i=1$. Therefore$$a_0-c(a_1+2a_2+3a_3+...na_n+...)=0$$$$c=\frac{a_0}{a_1+2a_2+3a_3+...na_n+...}$$
###### Particular solution of the stochastic component (Undetermined coefficient method)
Finds the particular solution to the stochastic component of a difference equation - the terms containing the disturbance variables $\epsilon$. From (1) we know that $$y_t=a_0\sum_{i=0}^{n-1} (a_1^i)+a_1^ny_{t-n}+\sum_{i=0}^{n-1}(a_1^i\epsilon_{n-i})$$which is the backwards iteration of $$y_t=a_0+a_1y_{t-1}+\epsilon_t\tag 2$$
If $|a_1|<1$, then we know that $$y_t=\frac{a_0}{1-a_1}+\sum_{i=0}^{\infty}(a_1^i\epsilon_{t-i})$$Taking the stochastic component as a new difference equation, we get $$y_t=b_0+b_1t+\sum_{i=0}^{\infty}(\alpha_i\epsilon_{t-i})\tag 3$$where we have to find out the value of $b_0, b_1, \alpha$. Comparing this with equation (2), we get$$b_0+b_1t+\alpha_0\epsilon_t+\alpha_1\epsilon_{t-1}+...=a_0+a_1(b_0+b_1(t-1)+\alpha_0\epsilon_{t-1}+\alpha_1\epsilon_{t-2+...})+\epsilon_t$$$$0=[b_0-a_0-a_1b_0+a_1b_1]+b_1(1-a_1)t+(\alpha_0-1)\epsilon_t+(\alpha_1-a_0\alpha_0)\epsilon_{t-1}+(\alpha_2-a_1\alpha_1)\epsilon_{t-2}+...$$In order for this equation to hold, all the terms must individually be equal to zero. Therefore taking all terms with a disturbance variable, 
$\alpha_0-1=0\implies \alpha_0=1$
$\alpha_1-a_1\alpha_0\implies \alpha_1=a_1$
$\alpha_2-a_1\alpha_1\implies \alpha_2=a_1^2$
and so on
$\alpha_n-a_1\alpha_{n-1} \implies \alpha_n=a_1^n$
From the general form, the value of $\alpha$ can be found. This is the root of the stochastic part of the difference equation. Can be represented in (3) in the same format as the homogenous solution ($A(\alpha)^t$).

Taking the term with the trend component, 
$b_1(1-a_1)=0$

Taking all other terms,
$b_0-a_0-a_1b_0+a_1b_1=0$

**Case 1:** $|a_1|<1$
From the trend component term we know that $b_1=0$. From the independent terms,$$b_0-a_0-a_1b_0+a_1(0)=0\implies b_0=\frac{a_0}{1-a_1}$$Putting these values into (3), $$y_t=\frac{a_0}{1-a_1}+\sum_{i=0}^{\infty}(\alpha_i\epsilon_{t-i})$$
##### Finding the GS from HS and PS
Typically, the $$\text{GS}=\text{HS}+\text{PS}$$
Suppose that $d>0$. then the General solution is $$y_t=A_1(\frac{a_1+ \sqrt{a_1^2-4a_2}}{2})^t+A_2(\frac{a_1- \sqrt{a_1^2-4a_2}}{2})^t+\frac{k}{1-a_1-a_2}$$this is an equation of $y$, only in terms of $t$. This is the **time path** of $y$ 

