Individuals value money today more that money tomorrow. This is due to impatience.

Both these models assume that outcomes realizing at different points in time are evaluated separably and intertemporal effects occur only through impatience or impulsivity. However, there may be situations where DMs evaluate outcomes realizing at different points in time in a non-separable manner. (Eg: preferences for increasing utility profiles (less utility before greater utility), preferences for diversity,etc.). 
#### Exponential discounting model
$t$ is the time period and $u_t$ is the utility at time $t$. $u=(u_0,...,u_T)$ is the utility stream from time 0 to T. $U_0(u)$ is the utility from $u$ evaluated at $t=0$. The exponential discounting model states that $$U_0(u)=u_0\sum_{t=1}^T\delta^tu_t$$Where $\delta$ is the **discount factor**. $\rho$ given by $$\rho=\frac{1-\delta}{\delta}$$ is the discount rate.

This model implies the **dynamic consistency of preferences** -> preferences between 2 choices does not change with just a change in time. For any utility stream $u=(u_0,...,u_T)$ denote $u^t=(u_0,...,u_T)$. For any other time $\tau<t$, $U^\tau(u^t)$ is the utility from utility stream starting at $t$ evaluated at time $\tau$.


A DMs intertemporal preferences are dynamically consistent if for all time periods $\tau<\tau'\le t$, any utility stream $u^t$ and $\tilde u^t$,$$U^\tau(u^t)\ge U^\tau(\tilde u^t)\iff U^{\tau'}(u^t)\ge U^{\tau'}(\tilde u^t)$$**Proposition:** Exponential discounting implies dynamic consistency. Suppose in the time periods, the utility is given by 

|1|2|3|4|
|---|---|---|---|
|||$u_3$|$u_4$|
|||$\tilde u_3$|$\tilde u_4$|

$$U^1(u^3)=\delta^2u_3+\delta^3u_4$$$$U^2(u^3)=\delta u_3+\delta^2u_4$$$$U^1(\tilde u^3)=\delta^2\tilde u_3+\delta^3\tilde u_4$$$$U^2(\tilde u^3)=\delta\tilde u_3+\delta^2\tilde u_4$$If $U^1(u^3)>U^1(\tilde u^3)$$$\delta^2u_3+\delta^3u_4>\delta^2\tilde u_3+\delta^3\tilde u_4$$Dividing by $\delta$ on both sides,
$$\implies \delta u_3+\delta^2u_4>\delta\tilde u_3+\delta^2\tilde u_4$$$$\implies U^2(u^3)>U^2(\tilde u^3)$$Hence dynamic consistency is proven.

#### Quasi - Hyperbolic discounting
It is easier to think of ourselves as patient in the future than at another time. This is a dynamic inconsistency of preferences. This can be accounted for my modifying the exponential discounting model. There are two time related parameters:
- $\delta$ is the measure of impatience (Discount factor)
- $\beta$ is the measure of impulsivity 

The utility $U_0(u)$ for the utility stream $u=(u_0,u_1,...,u_T)$ is :$$U_0(u)=u_0+\sum_{t=1}^T\beta\delta^tu_t$$$\beta$ is independent of time. It is present just once in every term that is not the first in the utility stream. It essentially only affects the today tomorrow tradeoff as it is only discounted one time. Therefore:
- $\beta\delta$ is the today-tomorrow discount factor
- $\delta$ is the tomorrow-dayafter and so on discount factor

###### Dynamic inconsistency example
Suppose the payoffs are given by 

|Decision|Friday|Saturday|Sunday|
|---|---|---|---|
|Cake||4|0|
|No cake||1|6|

Suppose $\beta=1/2,\delta=2/3$
**From friday perspective,**
$$U_F(\text{cake})=u_f+\beta\delta u_s+\beta\delta^2 u_{su}=0+\frac 12\frac 23 (4)+0=\frac 43$$$$U_F(\text{no cake})=u_f+\beta\delta u_s+\beta\delta^2 u_{su}=0+\frac 12\frac 23 (1)+\frac 12 \frac23\frac23(6)=\frac 53$$Therefore, from the perspective of friday, not eating cake $\succ$ eating cake

**From saturday perspective,**
$$U_S(\text{cake})=u_s+\beta\delta u_{su}=4+\frac 12\frac 23 (0)=4$$$$U_S(\text{no cake})=u_s+\beta\delta u_{su}=1+\frac 12\frac 23 (6)=3$$From saturday's perspective, eating cake $\succ$ not eating cake.


Thus preferences are dynamically inconsistent under the quasi hyperbolic discounting model. This dynamic inconsistency can be perhaps dude to self control issues with the DM. 

