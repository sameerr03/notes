A model that accounts for preferences for the timing of the resolution of uncertainty.

There are two time periods, $t=1,2$. At each time period there is a set of $X_t$ possible outcomes which contain risk. A [[vNm Expected utility]] maximizer will have preferences over the lotteries in $\Delta(X_1\times X_2)$. Consider the outcomes of the lottery $X_1=X_2=\{C_H,C_L\}$. Then,$$X=X_1\times X_2=\{(C_H,C_L),(C_H,C_H),(C_L,C_L),(C_L,C_H)\}$$The utility will be given by $$\frac 14V(C_H,C_H)+\frac 14V(C_L,C_H)+\frac 14V(C_H,C_L)+\frac 14V(C_L,C_L)$$
Example:
$X_1$ gives 5 for sure, $X_2$ gives $[10,0.5;0,0.5]$
![[Pasted image 20231210021047.png]]s
The utility from this lottery is given by $$\frac 12V(5,10)+\frac12V(5,0)$$
However, uncertainty could be resolved in the second period as well
![[Pasted image 20231210021127.png]]
In this case, the utility is given by 
$$V(5,\frac12u(10)+\frac12u(0))$$
#### Kreps-Porteus Representation
Suppose the DM has the following preferences:
- period 2 preferences $\succsim_2$ over lotteries on period 2 outcomes, $\Delta(X_2)$
- period 1 preferences $\succsim_1$ over lotteries on (period 1 outcome, period 2 lottery) pairs, $\Delta(X_1\times\Delta(X_2))$

$x_1,x_2$ are the pd 1 and pd 2 outcomes. $l_2$ is a typical element in $\Delta(X_2)$ and $L_1$ is a typical element in $\Delta(X_1\times\Delta(X_2))$.

The Kreps-Porteus representation of the preferences $(\succsim_1,\succsim_2)$ is a pair of functions $u:X_2\to\mathbb R$ and $v:X_1\times\mathbb R\to\mathbb R$ such that 
- lotteries in $\Delta(X_2)$ are evaluated by an EU criterion using the function $u$, the [[vNm Expected utility]] representation of $\succsim_2$.
- lotteries in $\Delta(X_1\times\Delta(X_2))$ are evaluated by an EU criterion using the function $v$, that is any $L_1\in \Delta(X_1\times\Delta(X_2))$ is evaluated by:$$\sum_{(x_1,l_2)\in X_1\times\Delta (X_2)}L_1(x_1,l_2)v(x_1,\sum_{x_2\in X_2}l_2(x_2)u(x_2))$$
As seen in the example, uncertainty can be resolved in either time period. Based on this,
Let (u, v) be a Kreps-Porteus representation. Then 
- DM prefers earlier (resp., later) resolution of uncertainty if v is convex (resp. concave) in its second argument 
- DM is indifferent to the timing of resolution of uncertainty if v is linear in its second argument. In this case the Kreps-Porteus representation reduces to a vN-M expected utility representation