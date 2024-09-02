Consider the [[Difference equations]]
$$y_t=3+0.9y_{t-1}-0.2y_{t-2}+\epsilon_t\tag 1$$
the [[Difference equations#Homogenous solution|HGNS solution]] is given by:
taking the irregular part of the equation
$$y_t-0.9y_{t-1}+0.2y_{t-2}=0$$Assuming $y_t=Aa_1^t$,
$$Aa_1^t-0.9a_1^{t-1}+0.2a_1^{t-2}=0$$Dividing both sides by $Aa_1^{t-2}$,
$$a_1^2-0.9a_1+0.2=0$$Using the quadratic formula we get the solutions $$a_1=0.5, 0.4$$Therefore, taking the discrete roots case, $$y_t^h=A_1(0.5)^t+A_2(0.4)^t$$
the [[Difference equations#Particular solution of a deterministic process|particular solution for the deterministic component]] is given by:
Assuming $y_t=c$ and not considering the stochastic component (disturbance term),
$$y_t=3+0.9y_{t-1}-0.2y_{t-2}$$$$c=3+0.9c-0.2c$$$$c=10$$Therefore, $$y_t^{\text{PSD}}=10$$
the [[Difference equations#Particular solution of the stochastic component (Undetermined coefficient method)|particular solution for the stochastic component]] is given by:
assuming $$y_t=b_0+b_1t+\sum_{i=0}^\infty\alpha_i\epsilon_{t-i}$$the characteristic roots from the homogenous equation are given by $a_1=0.5,0.4$ which is less than 1. Therefore $b_1=0$. $b_0$ is deterministic and thus is solved in the PSD. Therefore, removing the deterministic component, $$y_t=\sum_{i=0}^\infty \alpha_i\epsilon_{t-i}\tag 2$$Similarly, removing the deterministic component from (1),
$$y_t=0.9y_{t-1}-0.2y_{t-2}+\epsilon_t\tag 3$$
From (2) and (3), $$\alpha_0\epsilon_t+\alpha_1\epsilon_{t-1}+\alpha_2\epsilon_{t-2}+...=0.9[\alpha_0\epsilon_{t-1}+\alpha_1\epsilon_{t-2}+\alpha_2\epsilon_{t-3}+...]-0.2[\alpha_0\epsilon_{t-2}+\alpha_1\epsilon_{t-3}+...]+\epsilon_t$$$$(\alpha_0-1)\epsilon_t+(\alpha_1-0.9\alpha_0)\epsilon_{t-1}+(\alpha_2-0.9\alpha_1+0.2\alpha_0)\epsilon_{t-2}+(\alpha_3-0.9\alpha_2+0.2\alpha_1)\epsilon_{t-3}+...=0$$
Ensuring that all terms are equal to 0, 
$\alpha_0-1=0\implies \alpha_0=1$
$\alpha_1-0.9\alpha_0=0\implies \alpha_1=0.9$
$\alpha_2-0.9\alpha_1+0.2\alpha_0=0$
and so on 
$\alpha_i-0.9\alpha_{i-1}+0.2\alpha_{i-2}=0$
This forms a new difference equation. Assuming $\alpha_i=A\beta^i$, $$A\beta^i-0.9\beta^{i-1}+0.2\beta^{i-2}=0$$Dividing on both sides by $A\beta^{i-2}$ we get$$\beta^2-0.9\beta+0.2=0$$Solving the quadratic equation, we get $$\beta=0.5,0.4$$Therefore the solution is $$\alpha_i=A_3(0.5)^i+A_4(0.4)^i$$When $i=0$, $A_3+A_4=1$
When $i=1$, $0.5A_3+0.4A_4=0.9$
Solving this system, we get $A_3=5, A_4=-4$. Therefore the PS of $\epsilon_t$ is $$\alpha_i=5(0.5)^i-4(0.4)^i$$
Finding the [[Difference equations#General Solutions]], $$y_t=y_t^h+y_t^{\text{PSD}}+y_t^{\text{PSS}}$$$$y_t=A_1(0.5)^t+A_2(0.4)^t+10+\sum_{i=0}^\infty\alpha_i\epsilon_{t-i}$$where $\alpha_i=5(0.5)^i-4(0.4)^i$
