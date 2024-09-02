OThe Heckscher Ohlin model of trade models the effect of differing factor endowments in otherwise similar countries on trade patterns.

#### Setup
The model is a system of two countries - Home and Foreign. Each of these countries can produce two goods, Food $(F)$ and Cloth $(C)$. 

In order to produce these goods, two inputs are needed Labor $(L)$ and Capital $(K)$. Within each country, both these inputs are perfectly mobile. The endowments are given as 

Home: $(\bar L, \bar K)$
Foreign: $(\bar L^*, \bar K^*)$

We consider the home country **capital abundant** if and only if $$\frac
	{\bar K}{\bar L}>\frac{\bar K^*}{\bar L^*}$$If we assume this to be true, then using the same equation $$\implies \frac
{\bar L^*}{\bar K^*}>\frac{\bar L}{\bar K}$$Meaning that Foreign is **labor abundant**.
#### Factor demand optimization
For cloth, suppose the production function is given by $$F(K,L)=K^\kappa L^{1-\kappa}$$We can make this into an isoquant by fixing the output to an arbitrary value $\bar q$. On the graph of the amount of inputs, the isoquant is the curve 
![[Pasted image 20240321213955.png|400]]
If a firm is producing $\bar q$ units of cloth, they will choose the combination of inputs $(K,L)$ on the isoquant that minimizes cost. We can represent the cost function as $$C(K,L)=wL+rK$$In order to find the optimal inputs, $$\min_{K,L}\ wL+rK\ \text{such that }K^\kappa L^{1-\kappa}=\bar q$$Using lagrangian optimization, $$\mathcal{L}=wL+rK-\lambda(\bar q-K^\kappa L^{1-\kappa})$$Taking the first order conditions, $$\frac{\partial \mathcal L}{\partial L}=w+\frac{\lambda(1-\kappa)K^\kappa}{L^\kappa}=0\implies w=-\lambda(1-\kappa)(\frac KL)^\kappa $$$$\frac{\partial \mathcal L}{\partial K}=r+\lambda\kappa K^{\kappa-1}L^{1-\kappa}=0\implies r=-\lambda\kappa(\frac KL)^{\kappa-1} $$Taking the ratio of wages/rent, $$\frac wr=\frac{1-\kappa}{\kappa}\frac KL\implies \frac {L^C}{K^C}=(\frac{1-\kappa}{\kappa})\frac 1{\frac wr}$$This is the optimal proportion to demand the inputs in order to minimize costs while producing cloth. It is important to note that this optimal ratio is independent of the amount of cloth produced, $\bar q$.  From the derived equation, it is clear that $L/K$ and $w/r$ follow an inverse relationship. Plotting this relationship, we get 
![[Pasted image 20240321215326.png|400]]
This is the relative labor demand for the cloth sector. $w/r$ is the relative cost of labor. If this ratio is high, the relative demand for labor (L/K) is low. if w/r is low, L/K is high. 


##### Labor intensity
The production function for food is given by $$F(K,L)=K^\alpha L^{1-\alpha}$$The constraint is the same as in the cloth sector. Therefore the optimization for cost minimization will yield the same inverse relation between L/K and w/r.$$\frac {L^F}{K^F}=\frac{1-\alpha}{\alpha}\frac 1{\frac wr}$$ If $\alpha>\kappa$,
$$\frac{1-\alpha}{\alpha}<\frac{1-\kappa}{\kappa}$$Multiplying by $w/r$ on both sides, $$\frac{L^F}{K^F}<\frac{L^C}{K^C}$$
Graphically, this inequality is as follows 
![[Pasted image 20240321220212.png|400]]
For any value of $w/r$, $L^F/K^F$ is less than $L^C/K^C$. This means that cloth is **labor intensive**. This implies that food is **capital intensive**. Suppose we represent $L^F/K^F$ and $L^C/K^C$ as functions of $w/r$, then cloth is labor intensive if and only if $$\frac{L^C}{K^C}(\frac wr)>\frac{L^F}{K^C}(\frac wr)\ \ \ \ \forall \frac wr$$We assume that this is the case for the free trade equilibrium.

### Relative labor demand for a country
Suppose $$l=\frac LK$$We know that the production function has constant returns to scale. This means that $$tF(K,L)=F(tK,tL)\ \forall t$$it must be that the marginal product of labor is the same, $$\frac{\partial F(tK,tL)}{\partial L}=\frac{\partial F(K,L)}{\partial L}$$Suppose $t=1/K$. Substituting, $$\frac{\partial F(tK,tL)}{\partial L}=\frac{\partial}{\partial L}F(\frac KK,\frac LK)=\frac{\partial}{\partial L}F(1,\frac LK)$$Therefore,
$$\text{MPL}(K,L)=\text{MPL}(1,l)$$
- $\text{MPL}(1,l)$ is decreasing in $L$
- $\text{MPL}(1,l)$ is increasing in $K$


For given prices $P_F$ and $P_C$, each sector generates an optimum demand for labor and capital in order to minimize costs, as shown from the curves above. Suppose$$l_c=\frac{L_C}{K_C}(\frac wr), l_F=\frac{L_F}{K_F}(\frac wr)$$We are also exogenously given the endowment of the factors to the country. The relative endowment is $\bar L/\bar K$. This is the supply of factors in the economy. Therefore, ![[Pasted image 20240402222545.png|400]]

The overall labor demand for the entire country is given by $$l_H=\frac{L_C+L_F}{K_C+K_F}=\frac{L_C+L_F}K$$
$$=\frac{L_C}{K}+\frac{L_F}K=\frac{K_C}{K}\frac{L_C}{K_C}+\frac{K_F}{K}\frac{L_F}{K_F}$$$$=\frac{K_C}K(l_C)+\frac{K_F}{K}(l_F)$$$$l_H=\frac{K_C}{K}l_C+(1-\frac{K_C}{K})l_F$$
This equation represents the relative labor demand at home in terms of $l_C, l_F$ and $K_C/K$. This is a weighted average of the relative demand of labor in both sectors. Plotting $l_H$, it will be a weighted average between $l_C$ and $l_F$. 
![[Pasted image 20240402224852.png|400]]
This gives us the equilibrium wage to rent ratio, $w'/r'$
#### Comparative Statics
##### Increase in price (Stopler - Samuelson Theorem)
Links relative prices of goods to real income of factors

Consider $P_C$ increases to $P_C'$. This implies that $L_C$ and $K_C$ increase to $L_C'$ and $K_C'$. As there is limited endowment of labor and capital, allocation of labor and capital to the food sector falls. This implies that $$\frac{K_C'}{K}>\frac{K_C}{K}$$In the equation for $l_H$, this makes it such that $l_H$ is graphically closer towards $l_C$ as the weights for $l_C$ are higher.  

![[Pasted image 20240404192558.png|400]]
As the endowment of labor and capital is fixed, In equilibrium the wage to rent ratio increases from $w/r$ to $w'/r'$. As $l_F$ and $l_C$ are functions of the wage to rent ratio, the $l_F^{EQ}$ and $l_C^{EQ}$ in equilibrium are both lower after the increase in price. This implies that firms want to employ relatively less labor and more capital. 

The intuition for this is that when the price of cloth increases, the relative demand for labor shifts towards cloth (labor intensive sector). However, since the wage to rent ratio is higher in the new equilibrium, L/K is lower in both the sectors.

###### Changes to real income
With perfect competition, the marginal cost of producing a good is equal to the marginal benefit. $$r=P_C\times \text{MPK}_C(1,l_C)=P_F\times\text{MPK}_F(1,l_F)\tag 1$$$$w=P_C\times\text{MPL}_C(1,l_C)=P_F\times\text{MPL}_F(1,l_F)\tag 2$$
We know that $l_C$ and $l_F$ fall in equilibrium. 
Due to diminishing marginal returns and factor complementarity, $\text{MPL}(1,l)$ is decreasing in $l$ and $\text{MPK}(1,l)$ is increasing in $l$. This implies that $$\text{MPL}_C(1,l_C')>\text{MPL}_C(1,l_C)$$$$\text{MPL}_F(1,l_F')>\text{MPL}_F(1,l_F$$$$\text{MPK}_C(1,l_C')<\text{MPK}_C(1,l_C)$$$$\text{MPK}_F(1,l_F')<\text{MPK}_F(1,l_F)$$ From substituting the equations from (1) and (2),$$\frac r{P_C}=\text{MPK}_C(1,l_C), \frac r{P_F}=\text{MPK}_F(1,l_F), \frac  w{P_C}=\text{MPL}_C(1,l_C), \frac r{P_F}=\text{MPL}_F(1,l_F)$$Which are the real wages. Therefore, we can conclude that from the change in prices, $$\frac {r'}{P_C'}<\frac{r}{P_C}, \frac{r'}{P_F}<\frac{r}{P_F}, \frac{w'}{P_C'}>\frac{w}{P_C}, \frac{w'}{P_F}>\frac{w}{P_F}$$Therefore, the real income of capital owners fall, and the wages for labor increases. As the demand for cloth increases (labor intensive sector), labor benefits more

##### Increase in factor endowment (Rybczynski Theorem)
Links changes in factor endowments and production of goods, keeping prices constant

Suppose the prices of the goods are fixed, by the labor endowment $\bar L$ doubles. 

As the cloth sector is labor intensive, an increase in labor will result in a larger capacity for cloth production as compared to the increase in food production. Plotting the changes in the PPFs, 
![[Pasted image 20240404202117.png|400]]


If the amount of food to be produced is fixed, the slope of the PPF at that point will be higher after the increase in labor endowment, as the opportunity cost of producing food increases. 

When prices are unchanged, the optimal production shifts towards more cloth and less food when labor endowment has increased. 

##### Heckscher-Ohlin Theorem
Let us consider two countries - Home and Foreign. These countries are exactly identical, except in the endowment of their inputs. Home is endowed with $\bar L, \bar K$ and foreign with $\bar L^*, \bar K^*$ (Home is capital abundant)

In order to understand the trade dynamics, we consider a fictitious economy where home and foreign are endowed with $$(\frac{\bar L+\bar L^*}{2},\frac{\bar K + \bar K^*}{2})$$Given this case, home and foreign are exact copies of each other. As a result, production, consumption and prices in both the countries will be identical. Supposing Home is capital abundant, in order to go from this fictitious situation, we take away capital from foreign and give it to home. Similarly, we take away labor from home and give it to foreign. 

As home has more capital, we know that more of the capital intensive good will be produced compared to the fictitious economy (by [[Heckscher Ohlin Model#Increase in factor endowment (Rybczynski Theorem)|Rybczynski theorem]]). Therefore more food and less cloth is produced compared to the fictitious economy. Similarly, in foreign cloth production goes up and food production goes down compared to the fictitious economy. 

It is assumed that the preferences of consumers in both countries are identical, therefore as home has excess food and foreign has excess cloth, $P_F/P_C$ is less than the relative price in the fictitious economy at home and $P_F^*/P_C^*$ is more than the relative price in the fictitious economy at foreign. 

Therefore, in Autarky, the capital intensive good is relatively cheaper in the capital abundant country. $$\frac{P_F^A}{P_C^A}<\frac{P_F^{*A}}{P_C^{*A}}$$Home has a [[Comparative advantage]] in food production. The capital abundant country exports capital intensive good and the labor abundant country exports labor intensive goods. Home exports food and Foreign imports cloth. 

##### With free trade
As $P_F^A/P_C^A$ is less than the relative price of foreign, in the free trade equilibrium the relative price of food will increase. Similarly, in Foreign, the relative price of food in foreign, it decreases. 

$$\frac{P_F^A}{P_C^A}<\frac{P_F^W}{P_C^W}<\frac{P_F^{*A}}{P_C^{*A}}$$
with the [[Heckscher Ohlin Model#Increase in price (Stopler - Samuelson Theorem)|stopler samuelson theorem]], at home, capital owners will be better off and workers are worse off (demand/price of capital intensive good increases). At foreign, the demand/price of labor intensive good increases, therefore capital owners are worse off and workers are better off. 

