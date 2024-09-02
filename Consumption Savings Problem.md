In order to determine how much an individual saves or consumes in optimum, a two period consumption problem is set up. At each of the two periods, a person can either consume or save. At the end of the second period, all the money left over is gone as the person only lives for two periods.

The lifetime value of the household is$$V(c_1,c_2)$$Where:
- $c_1$ is the consumption in period one
- $c_2$ is the consumption in period two

The income of the person in the periods is $y_1, y_2$. In period 1, the person also gains some amount of money already in the bank (take as inheritance) $b_1$. Consumption in period 1 is determined by$$c_1+a_1\le b_1+y_1$$Where $a_1$ is the amount that is saved in period 1. This amount is put into a bank where it accumulates interest at the rate $r$. We take $R=1+r$. Then, consumption in period 2 is determined by$$c_2\le y_2+Ra_1$$These two inequalities form the [[Budget sets|budget constraint]]. There is no reason for the person to waste money in both the periods as they will either save or consume all of their income in period 1 and consume all of the remaining money in the second period. Therefore, the inequalities are replaced by equalities. $$a_1=\frac{c_2-y_2}R$$Substituting this in the constraint for period 1, $$c_1+\frac{c_2-y_2}R=b_1+y_1$$$$c_1+\frac{c_2}R=b_1+y_1+\frac{y_2}R$$This is the intertemporal budget constraint. Here the future income and consumption are [[Intertemporal consumption|discounted]]. Carrying out the maximisation problem using a lagrangian, $$max_{c_1,c_2}\ V(c_1,c_2)$$with respect to the budget constraint $c_2=(b_1+y_1-c_1)R+y_2$
$$\mathcal{L}=V(c_1,c_2)+\lambda[c_2-(b_1+y_1-c_1)R-y_2]$$$$\frac{\partial \mathcal L}{\partial c_1}=V_1'(c_1,c_2)+\lambda R=0$$$$\frac{\partial \mathcal L}{\partial c_2}=V_2'(c_1,c_2)+\lambda=0$$Taking both FOC's in terms of lambda and equating,$$V_1'(c_1,c_2)=V_2'(c_1,c_2)R$$Suppose we take the function $V(c_1,c_2)=u(c_1)+\beta u(c_2)$ where $\beta$ is the discounting factor, then substituting into the equation found above, we get$$u'(c_1)=R\beta u'(c_2)$$This is the **Euler equation.** Links the marginal utility of consumption today to the marginal utility of consumption tomorrow.

Putting in the utility function of $$u(c)=\frac{c^{1-\rho}}{1-\rho}$$Therefore the euler equation is $$c_1^{-\rho}=\beta Rc_2^{-\rho}$$Substituting this into the intertemporal budget constraint,$$c_1=\frac{h_1+b_1}{(1+\frac{(\beta R)^{1/\rho}}{R})}$$This shows that only the sum of wealth matters. Income distribution across the time periods does not matter for optimal $c$, only the sum of wealth. 

-------x------
#### Multiperiod Optimisation
For long run projections of growth more than 2 periods are necessary. Supposing a person lives from period $t=0$ to $t=T$$$V(c_0,c_1,...,c_T)=u(c_0)+\beta u(c_1)+....+\beta^Tu(c_T)$$$$=\sum_{t=0}^T\beta^tu(c_t)$$The income profile of the agent is $y_0,y_1,...,y_T$. In period 0,
$a_0+c_0=y_0$
In period 1,
$a_1+c_1=y_1+a_0R$
In period t,
$a_t+c_t=y_t+a_{t-1}R$

Using all these equations and eliminating the savings terms ($a$), we get the intertemporal budget constraint.$$c_0+\frac{c_0}R+....\frac{c_T}{R^T}=y_0+\frac{y_1}{R}+...+\frac{y_T}{R^T}$$Optimising the utility function, $$\mathcal{L}=\sum_{t=0}^T\beta^tu(c_t)-\lambda[y_0+\frac{y_1}{R}+...+\frac{y_T}{R^T}-(c_0+\frac{c_0}R+....\frac{c_T}{R^T})]$$$$\frac{\partial \mathcal L}{\partial c_0}=u'(c_0)-\lambda=0$$$$\frac{\partial \mathcal L}{\partial c_1}=\beta u'(c_1)-\frac\lambda R=0$$$$\frac{\partial \mathcal L}{\partial c_2}=\beta^2u'(c_2)-\frac\lambda {R^2}=0$$Therefore comparing FOCs,$$u'(c_0)=R\beta u'(c_1)$$and $$u'(c_1)=R\beta u'(c_2)$$Therefore, by induction, for any two periods from $t$ to $t+1$,$$u'(c_t)=\beta Ru'(c_{t+1})$$
