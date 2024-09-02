# Consumer optimization 
The consumer uses the [[Budget sets |budget set]] and their [[indifference curves]](strictly monotone) to arrive at the optimum point of consumption between the two goods.


![[tempFileForShare_20220914-195806.jpg]]

- IC1 is not ideal as improvement is possible within the budget line
- lC3 is not possible (outside the budget set)
- IC2 touches the budget set at the optimum point

The principle behind this is [[Utility]] maximisation. This is at the point where the MRS is equal to the MRT.

## Maximisation
### Using Substitution (2 goods)
Using a standard [[Utility function#Utility functions#Cobb-Douglas function|Cobb-Douglas function]] for two goods, the utility is
$$U(x_1,x_2)=0.5\ln x_1+0.5\ln x_2$$
The budget set determines all feasable conditions of goods that can be purchased (constraint). The function of it is $$m=p_1x_1+p_2x_2$$$$x_2=\frac{m}{p_2}-\frac{p_1}{p_2}x_1$$
Exquivalent utility function V got by doubling U for convenience. Substituting x2 into V(x1,x2) we get $$V(x_1,x_2)=\ln x_1+\ln(\frac{m}{p_2}-\frac{p_1}{p_2}x_1)$$In order to maximise we differentiate the equation and find the point where the slope is 0.
$$\frac{\partial V}{\partial x_1} = \frac{1}{x_1}-\frac{p_1}{m - p_1x_1}$$$$\hat{x}_1=\frac{m}{2p_1}$$ Similarly $$\hat{x}_2=\frac{m}{2p_2}$$
### Using Lagrangian multiplier (N goods)
Using a generic cobb douglas,
$$U(\tilde{x})=\sum^N_{n=1}\alpha_n \ln(x_n)$$ and a generic budget set $\tilde{p}\cdot \tilde{x}=m$, we can find the maxima using a lagrange multiplier $\lambda$ The lagrangian equation is the original U function - the lagrange multiplier into the constraint $$L(\tilde{x},\lambda)=U(\tilde{x})-\lambda(\tilde{p}\cdot \tilde{x}-m)$$
To maximise the partial derivative of each lagrangian =0 and the derivative of the multiplier should be 0 as well.
$$L_n'=MU_n-\lambda p_n=0$$ Where MU is the [[indifference curves|marginal utility]] of the good n.
$$L_\lambda'=\tilde{p}\cdot \tilde{x}-m=0$$ Solving these equations gives us the optimal amounts of all goods. $$\hat{x}_n=\frac{\alpha_n\ m}{p_n}$$