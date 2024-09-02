The [[Overlapping generation model]] with two assets instead one one unlike the [[simple model of money]]. Capital (represented by $k$) and money are used simultaneously.

In an economy with just capital, the budget constraints are given by$$\max_{c_1,c_2} u(c_{1,t},c_{2,t+1} )\text{ s.t. } c_1+k_t\le y\ \&\ c_{2,t+1}\le xk$$ Where:
- $k_t$ is the amount of capital that a young person acquires in time $t$.
- $xk$ is the production function from using $k$ units of capital. 
Finding the lifetime budget constraint,$$c_{1,t}+\frac 1xc_{2,t+1}\le y$$At the SME,$$c_1+\frac 1xc_2\le y$$Plotting the LTBC, 
![[Pasted image 20230922203357.png|400]]

The capital can be used in order to produce goods in the next time period, given by the production function $f(k)$. The rate of return on capital is given by $f'(k)$. If the production function is given as $xk$, then $$f'(k)=x$$Therefore, the rate of return on capital is given by $x$. We are assuming that this production function is non-linear, neo-classical (diminishing marginal returns to capital).
![[Pasted image 20230922204908.png|600]]


At the stationary solution, $k_1=k_2=....=k$

We also know that at the SME, from [[Inflation model]]$$c_1+\frac znc_2\le y$$We know that the rate of return from holding fiat money is given by $$\frac{v_{t+1}}{v_t}=\frac nz$$
In a frictionless economy, if multiple assets coexist, they must have the same rate of return. This is the **Rate of return equality (RORE)** condition. Based on this condition, 

|ROR capital to money| Action|
|---|---|
|$f'(k)>\frac nz$|Only capital is held|
|$f'(k)<\frac nz$|Only money is held|
|$f'(k)=\frac nz$|RORE is met. Agents are indifferent between holding capital and money|

The greater the amount of inflation, the lesser that $\frac nz$ becomes, therefore the more capital that the actors accumulate. This is the **Tobin Effect** i.e., an increase in the growth rate of money supply leads to an increase in the accumulation of capital. 

Consider a permanent increase to the rate of fiat money creation from $z$ to $z'$. In this case, the rate of return to holding fiat money, given by $n/z'$ falls. As this falls below $f'(k)$, agents start accumulating capital as the rate of return is higher. As a result, the capital stock increases from $k$. However, as the capital stock increases, the rate of return for each new unit of capital accumulated decreases due to diminishing marginal returns of the production function. As a result, the rate of return to capital falls till it becomes equal to the rate of return from fiat money, $n/z'$. The capital stock has increased to warrant this, from $k$ to $k^*$, and the system reaches an equilibrium. 

![[Pasted image 20231020141308.png|400]]

#### GDP per capita under the model
The total output of the economy is given by $$\text{GDP}_t=N_ty+N_{t-1}f(k_{t-1})$$In the stationary equilibrium
$$\text{GDP}_t=N_ty+N_{t-1}f(k)$$$$GDP_t=N_t[\ y+\frac{f(k)}n]$$$$\frac{\text{GDP}_t}{N_t+N_{t-1}}=\frac{N_t}{N_t+N_{t-1}}[\ y+\frac{f(k)}n]$$$$\text{Per capita GDP}_t=\frac{1}{1+\frac 1n}[\ y+\frac{f(k)}n]$$
#### Welfare maximization
The social planner's feasibility set is given by$$N_{t-1}c_{2t}+N_tc_{1t}+N_tk_t\le N_ty+N_{t-1}f(k_{t-1})$$Under stationary solutions,
$$N_{t-1}c_{2}+N_tc_{1}+N_tk\le N_ty+N_{t-1}f(k)$$$$\frac{N_{t-1}}{N_t}c_{2}+c_{1}+k\le y+\frac{N_{t-1}}{N_t}f(k)$$$$c_1+\frac 1nc_2\le y+[\frac{f(k)}n-k]$$
The social planner, as a result has to choose $c_1$, $c_2$ and $k$ which all affect the feasibility set. 
![[Pasted image 20230923194006.png|400]]

Larger the feasibility set, the optimum can be on a higher IC (The frontier is pushed out). This is achieved by maximizing the term $f(k)/n-k$. $$\max_k \frac{f(k)}n-k$$$$\frac{f'(k)}n-1=0$$$$f'(k)=n$$This is the optimal amount of capital per young person. 

In the decentralized solution with money, we know that $f'(k)=n/z$. Therefore for welfare maximization in an economy with money, $z=1$. 