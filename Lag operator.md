A linear operator $L$ on a [[Time Series]] such that $$L^iy_t=y_{t-i}$$
#### Properties of the lag operator
1. The lag of a constant term is a constant
2. Distributive:$$(L^i+L^j)y_t=L^iy_t+L^jy_t=y_{t-i}+y_{t-j}$$
3. Associative:$$L^iL^jy_t=L^i(L^jy_t)=L^iy_{t-j}=y_{t-i-j}$$
4. Inverse:$$L^{-i}y_t=y_{t+i}$$
5. If $|a_1|<1,$$$(1+aL+a^2L+a^3L+...)y_t=\frac{y_t}{1-aL}$$
6. If $|a_1|>1$,$$[1+(aL)^{-1}+(aL)^2+(aL)^3+...]y_t=\frac{-aLy_t}{1-aL}$$or $$\frac{y_t}{1-aL}=-(aL)^{-1}\sum_{i=0}^\infty(aL)^{-i}y_t$$
#### Polynomial form
With the equation$$y_t=a_0+a_1y_{t-1}+...+a_py_{t-p}+\epsilon_t$$$$(1-a_1L-a_2L^2-...-a_pL^p)y_t=a_0+\epsilon_t$$Then we define $A(L)=1-a_1L-a_2L^2-...-a_pL^p$,$$A(L)y_t=a_0+\epsilon_t$$

#### Example
Consider$$y_t=a_0+a_1y_{t-1}+\epsilon_1$$$$y_t-a_1Ly_t=a_0+\epsilon_t$$$$(1-a_1L)y_t=a_0+\epsilon_t$$$$y_t=\frac{a_0}{1-aL}+\frac{\epsilon_t}{1-aL}$$as $a_0$ is a constant its lag is constant
$$\frac{\epsilon_t}{1-a_1L}=\epsilon_t+a_1\epsilon_{t-1}+a_1^2\epsilon_{t-2}+...=\sum_{i=0}^\infty a_1^i\epsilon_{t-i}$$Therefore the GS is 
$$y_t=\frac{a_0}{1-aL}+\sum_{i=0}^\infty a_1^i\epsilon_{t-i}$$Which is the same as in [[Difference equations#Backwards iteration]].

#### Stability conditions
For a [[Difference equations]], all roots must lie within the [[Unit root circle]]. Considering the equation$$y_t=a_0+a_1y_{t-1}+a_2y_{t-2}+...+a_ny_{t-n}+\epsilon_t$$Taking the HGNS sln, and assuming $y_t=A\alpha^t$, we simplify and get $$\alpha^n-a_1\alpha^{n-1}-...-a_n=0$$using lagged operators, $$y_t-a_1Ly_t-a_2L^2y_{t}-...-a_nL^ny_t=a_0+\epsilon_t$$$$(1-a_1L-a_2L^2-...-a_nL^n)y_t=a_0+\epsilon_t$$Comparing the two methods, 
$\alpha^n=1$
$\alpha^{n-1}=L$
$\alpha^{n-1}=L^2$
and so on
Taking $\alpha^{n-1}$,$$\alpha^n\times\alpha^{-1}=L$$$$\frac 1\alpha=L$$$$\alpha=\frac 1L$$This is the stability condition. all the lagged values will then lie outside the [[Unit root circle]].