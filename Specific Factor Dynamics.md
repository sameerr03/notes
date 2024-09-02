#### Setup
- two goods - Food ($F$) and Clothes ($C$)
- 3 inputs for production: Land ($T$) (used only for food production), Capital ($K$) (Used only for Cloth production), Labor ($L$) (Used for both)

Land and Capital here are **specific factors** - they are only useable in one sector. 

Home is endowed with a $(L,T,K)$ amounts of the inputs. 

The production functions are given by:
- Clothes: $Q_C(K,L_C)$
- Food: $Q_F(T,L_F)$
such that $L_F+L_C=L$

##### Assumptions
- The production function has constant returns to scale. $$f(tK,tL)=tf(K,L)$$
- The Marginal product of Capital ($\text{MPK}$), given by $\partial f/\partial K=F_K$ and the Marginal Product of Capital ($\text{MPL}$), given by $\partial f/\partial L=F_L$ must be such that $F_K,F_L\ge 0\ \forall L,K$
- Diminishing marginal returns to a single factor - If the other factors remain constant, the addition of one more unit of factor $A$ results in diminishing returns to each unit of $A$. ($F''_{KK}<0, F''_{LL}<0$)
- Factor complementarity - The marginal product of capital is increasing with each additional unit of labor, and marginal product of labor is increasing with each additional unit of capital. ($F''_{KL}>0, F''_{LK}>0$)

#### Production (Supply side) equilibrium 
![[Pasted image 20240220213141.png|400]]
The [[Ricardian trade model#Welfare (gains from trade)|PPF]] shows the feasibility frontier of the home country. When $C=0$, $L_F=L$ or all labor is allocated to food production and vise versa when $F=0$. 

The slope of the PPF represents the units of cloth that have to be given up for an additional unit of food to be produced. The amount of Food produced from one unit of labor is given by the $\text{MPL}_F$. Therefore, to produce one unit of food, the amount of labor required is given by $1/\text{MPL}_F$. The units of cloth produced form one unit of labor is given by $\text{MPL}_C$. Therefore, from the definition, we can infer that $$\text{slope of PPF}=(\text{MPL}_C)\times(\frac1{\text{MPL}_F})=\frac{\text{MPL}_C}{\text{MPL}_F}$$
which is the amount of cloth lost when food production is increased by one unit. 

##### Return on labor
We assume that production in both sectors is perfectly competitive -> there is no opportunity for profit to be made. This means that the Marginal benefit of production = Marginal cost at equilibrium. Mathematically, for both sectors$$\text{MPL}_F(T,L_F)\times P_F=w$$$$\text{MPL}_C(K,L_C)\times P_C=w$$Therefore, equating these two conditions, we get $$\text{MPL}_F(T,L_F)\times P_F=\text{MPL}_C(K,L_C)\times P_C$$$$\frac{\text{MPL}_C(K,L_C)}{\text{MPL}_F(T,L_F)}=\frac{P_F}{P_C}$$Therefore, in equilibrium, the slope of the PPF is equal to the price ratio of the goods. This gives us the optimal level of production of both goods, and therefore the appropriate labor allocation between food and clothes. 

We know that the marginal product of a factor is diminishing with an increase in the amount of the factor, therefore plotting this relation with respect to both food and clothes, ![[Pasted image 20240222185410.png]]
Note that the graph for food is inverted in its x-axis. Together, we can find the equilibrium wage and labor allocation
![[Pasted image 20240222185520.png|400]]

##### Return on specific factors
If we assume that at equilibrium factor markets are perfectly competitive, then similar to labor, the return per unit of factor (Marginal Cost) = Marginal benefit. Mathematically, $$r_K=\text{MPK}_C(K,L_C)\times P_C$$$$r_T=\text{MPT}_F(T,L_F)\times P_F$$Where $r_K,r_T$ is the income earned from one unit of capital and land respectively.

##### comparative statics
Suppose the home economy is in equilibrium 1, at some relative price $P_F/P_C$. If there is an increase in $P_C\to P_C'$, with food prices remaining constant, then comparing price ratios, $$\frac{P_F}{P_C}>\frac{P_F}{P_C'}$$In the new equilibrium 2, the optimal production is at the point where the slope of the PPF is equal to the price ratio. Therefore, $$\frac{\text{MPL}_C(K,L_C)}{\text{MPL}_F(T,L_F)}>\frac{\text{MPL}_C(K,L_C')}{\text{MPL}_F(T,L_F')}$$as $K,T$ remain constant. Therefore, equilibrium 2 will be at a point where the slope of the PPF is lower. Graphically, 
![[Pasted image 20240222191017.png|400]]
From the graph we can see that equilibrium 2 will have higher cloth and less food production than equilibrium 1. Therefore, the labor allocation will change as follows$$L_C<L_C', L_F>L_F'\tag 1$$
As $L'_F<L_F$, this implies that $$\text{MPL}_F(T,L_F)<\text{MPL}_F(T,L_F')$$due to diminishing marginal products. Similarly, $$\text{MPL}_C(K,L_C)>\text{MPL}_C(K,L_C')$$From [[Specific Factor Dynamics#Return on labor|labor wage relation]], we know that in equilibrium 2, $$w'=P_C'\times \text{MPL}_C(K,L_C')=P_F\times \text{MPL}_F(T,L_F')$$We know that $\text{MPT}_F(T,L_F')$ is greater than $\text{MPT}_F(T,L_F)$ and $P_F$ is constant. Therefore we can conclude that $$w'>w$$However, since $P_C'$ has increased and $\text{MPK}_C(K,L_C')$ has decreased, the increase in $w'$ from $w$ is not the same as the increase in $P_C$ to $P_C'$. 

The **real wage** in terms of cloth is given by $$\lambda_C=\frac{w}{P_C}=\text{MPL}_C(K,L_C)$$The real wages in terms of food is given by $$\lambda_F=\frac{w}{P_F}=\text{MPL}_F(T,L_F)$$From the comparisons of MPL in equilibrium 1 and 2, we can tell that $$\lambda_F<\lambda_F', \lambda_C>\lambda_C'$$However, we cannot make any comment on the welfare due to the change in the equilibrium. This is due to the fact that we do not know the preferences of the consumers (workers).

For capital owners, the return on capital is given by $$r_K=P_C\times \text{MPK}_C(K,L_C)\implies \frac{r_k}{P_C}=\text{MPK}_C(K,L_C)$$This is the amount of clothes that can be bought from one unit of capital. When $P_C$ increases to $P_C'$, from eq(1) and due to factor complementarity, $$\text{MPK}_C(K,L_C)<\text{MPK}_C(K,L_C')\tag 2$$$$\implies \frac{r_k}{P_C}<\frac{r_K'}{P_C'}$$Thus the real income of capital relative to clothes has increased. Since $P_C'>P_C$ and from eq (2) and [[Specific Factor Dynamics#Return on specific factors|return equations]], we can infer that $$r_K<r_K'\implies \frac{r_K'}{P_F}>\frac{r_K}{P_F}$$Thus the real income of capital relative to food has also increased. From this increase in the price of clothes, owners of the specific factor in production of clothes - capital, are better off.

For land owners, the return on land is given by $$r_T=P_F\times \text{MPT}_F(T,L_F)\implies \frac{r_T}{P_F}=\text{MPT}_F(T,L_F)$$This is the amount of food that can be bought from one unit of capital. When $P_C$ increases to $P_C'$, combined with eq (1) and factor complementarity, $$\text{MPT}_F(T,L_F)>\text{MPT}_F(T,L_F')\tag 3$$since $P_F$ is constant, this implies from the [[Specific Factor Dynamics#Return on specific factors|return equations]] that $$\frac{r_T'}{P_F}<\frac{r_T}{P_F}$$Thus the real income of land relative to food has decreased. From (3) and from $P_C<P_C'$, $$r_T'<r_T\implies \frac{r_T'}{P_C'}<\frac{r_T}{P_C}$$Thus the real income of land relative to clothes prices has decreased. Therefore from the increase in price of clothes, owners of the specific factor not used in clothes production - land, are worse off.

Therefore a price change in goods can have unequal effects on different input holders (Labor, land and capital).



