
A model that describes a two-good trade economy between two countries. It says in situations where 
- One country is more efficient in producing both goods
- Large labor wage gap (labor is significantly cheaper in one country)
**Both countries** will benefit from trade.

#### Assumptions
- Perfectly competitive labor and goods market
- Constant returns to production
- One input production technology(Labor ($L$)

#### Unit labor requirement
The number of units of labor required in order to produce one unit of a good. It is equivalent to 1/MPL. $a_G$ is the unit labor requirement for one unit of good $G$ in the home country.

### Autarky equilibrium 
Suppose there are two countries - Home and foreign (foreign represented by $*$). 
Each country produces two goods - Clothes and Food
Both the countries are in Autarky - No trade situation
#### Equilibrium conditions 
- Labor market clears $L_F+L_C=L$ in both countries
- Consumers and firms make optimal choices
- The goods market clears $x_F=Y_F; x_C=Y_C$

##### Derivation
The wage rate is $w$. The cost of production for 1 unit of food is therefore given by $a_Fw$, and cost of production for 1 unit of clothes is $a_Cw$.

We assume competitive goods market. Therefore, the prices must be equal to the cost of production. If the prices are higher, there are positive profits in the space and an there will be an entrant into the market. If the prices are lower, there is no incentive for the firm to remain in production. Therefore, $$P_F=a_Fw$$$$P_C=a_Cw$$
Therefore the relative price of food is $$\frac{P_F}{P_C}=\frac{a_Fw}{a_Cw}=\frac{a_F}{a_C}\tag{1}$$If we assume standard cobb Douglas preferences among goods:$$U(x_F,x_C)=x_F^\alpha x_C^{1-\alpha}$$From the optimization, we know that the ratio of expenditure by a consumer on food to expenditure by a consumer on clothes is in the ratio of $\alpha:(1-\alpha)$. Formally, $$\frac{P_Fx_F}{P_Cx_C}=\frac{\alpha}{1-\alpha}$$Substituting the relative price (eq 1), we get $$\frac{a_F}{a_C}\times\frac{x_F}{x_C}=\frac{\alpha}{1-\alpha}$$Using this we can get the relative demand of food.$$\frac{x_F}{x_C}=\frac{\alpha a_C}{(1-\alpha)a_F}\tag{2}$$
As the goods market clears, $Y_F=x_F$ and $Y_C=x_C$. Therefore, from (2) we can find the relative production$$\frac{Y_F}{Y_C}=\frac{x_F}{x_C}=\frac{\alpha a_C}{(1-\alpha)a_F}\tag{3}$$We also have the production functions - $$Y_F=\frac{L_F}{a_F}$$$$Y_C=\frac{L_C}{a_C}$$$a$ is the units of labor required for one unit of production, 1/MPL * L will give number of units produced. Adding the production functions into (3),
$$\frac{Y_F}{Y_C}=\frac{\alpha a_C}{(1-\alpha)a_F}=\frac{L_F/a_F}{L_C/a_C}$$$$\frac{L_F}{L_C}=\frac{\alpha}{1-\alpha}\tag{4}$$But we also know that the labor market clears. Therefore$$L_F+L_C=L$$$$\implies L_C=L-L_F$$
From (4),$$\alpha(L-L_F)=(1-\alpha)L_F$$$$\alpha L-\alpha L_F=L_F-\alpha L_F$$$$L_F=\alpha L$$$$L_C=(1-\alpha) L$$
Suppose $P_C=1$. Then we can find the wage rate and all other endogenous variables in terms of $P_C$.$$P_F=\frac{a_F}{a_C}\tag{5}$$we also know that $P_F=a_Fw$. Substituting in (5),$$a_Fw=\frac{a_F}{a_C}$$$$w=\frac{1}{a_C}$$
This derivation is identical for the foreign country in variable terms. The price ratios can be compared in order to determine which country has a [[Comparative advantage]].

### free trade equilibrium
##### Assumptions
- Costless trade
- Perfect mobility of labor within countries, but no immigration
- Countries being in the autarky equilibrium

##### Background (arbitrage condition)
Trade is a decentralized coordination of each countries production where decentralized means that this coordination can be achieved and sustained by prices and does not require a central authority. 

A trader could exploit an arbitrage opportunity in these two countries under the assumptions. This is through buying good $G$ in the country that has a [[Comparative advantage]] in production of $G$ and selling it in the other country. This takes advantage of the lower relative prices in the country of production. 

However, this activity will result in an increase in demand, resulting in the lowering of the relative price of the good. The opportunity will close when the relative prices of the good across both countries equalize. 

In the example situation in the autarky equilibrium, this would be represented as $$\frac{P_F}{P_C}=\frac{P_F^*}{P_C^*}$$
##### Equilibrium conditions
 - Relative price of food to clothes is equal in both countries
 - Firms and consumers make optimal choices
 - Individual markets clear ($L_F+L_C=L$, $L_F^*+L_C^*=L^*$)
 - Total production = Total consumption ($x_F+x_F^*=Y_F+Y_F^*$, $x_c+x_c^*=Y_c+Y_c^*$)
 - Trade is balanced (real value of imports = real value of exports)

#### FTE Example
Unit labor requirements:

| Country | Food | Cloth |
| ---- | ---- | ---- |
| Home | 3 | 2 |
| Foreign | 1 | 1 |
$L=L^*=900$
$U(x_C,x_F)=x_F^{2/3}x_C^{1/3}$

Suppose $\frac{P_F^W}{P_C^W}=1$. From the equilibrium conditions, this implies that $$\frac{P_F}{P_C}=\frac{P_F^*}{P_C^*}=1$$Taking $P_C=P_C^*=1$, $P_F=P_C^*=1$. In the home country, $$\frac{P_F}{P_C}=1$$this is the relative benefit from food production. The relative cost is given by $$\frac{a_F}{a_C}=\frac 32$$As the relative cost is greater than the relative production, firms at home only produce cloth. Therefore, $$L_F=0\implies L_C=900$$The production function is given by $$Y_C=\frac{L_C}{a_C}=\frac{900}{2}=450$$
In the foreign country, the relative cost of production =1 = relative benefit. Therefore they are indifferent in how much of each good they consume. $$\frac{a_F^*}{a_C^*}=1=\frac{P_F^*}{P_C^*}$$Therefore to determine production, we need to find the optimal consumption. 

**finding optimal consumption:**
Each worker earns wage $wL$. From the optimization of the utility function we know that $2/3$ of the total expenditure of the consumer is in food. Therefore, $$P_Fx_F=\frac23(wL)$$Since the home country produces only clothes, we use the prices of clothes to find wages. The price is equal to cost of production in a competitive goods market. Therefore $$P_C=wa_C\implies w=\frac{P_C}{a_C}=\frac 12$$Finding the expenditure, $$P_Fx_F=\frac23\frac 12L=\frac{900}3=300\implies x_F=300$$For clothes, $$P_Cx_C=\frac13\frac 12L=\frac{900}6=150\implies x_C=150$$In the foreign country, $$P_F^*=w^*a_F^*\implies w=\frac{P_F^*}{a_F^*}=1$$
Finding the optimal consumption of food, $$P_F^*x_F^*=\frac23(1)L=\frac{2\times 900}3=300\implies x_F^*=600$$For clothes, 
$$P_C^*x_C^*=\frac13(1)L=\frac{ 900}3=300\implies x_C^*=300$$
This is the equilibrium demand of each good. In order to establish this as the equilibrium we must verify the 4th condition - the trade must be balanced. The value of exports at home is given by $$P_C^W(Y_C-x_C)=(450-150)=300$$The value of imports at home is given by $$P_F^W(x_f-Y_F)=(300-0)=300$$Therefore trade is balanced and this demand value is the free trade equilibrium. 

#### Equilibrium setup
The ratios between the unit labor requirements of the goods give us the relative cost of production of that good. $a_F/a_C$ is the relative cost of food to cloth production at the home country. 

The ratios between the world prices (price ratio in both countries converge to world in FTE) give us the relative benefit from production of the good. $P_F^W/P_C^W$ is the relative benefit to food production in both countries at the free trade equilibrium. 

Based on the values of the relative cost and benefits to production, we can identify three cases. 
1. $\frac{P_F^W}{P_C^W}>\frac{a_F}{a_C}$ => Relative benefit of food production is greater than cost, the country only produces food and $L_F=F$
2. $\frac{P_F^W}{P_C^W}=\frac{a_F}{a_C}$ => Relative benefit of food production is equal to cost, the country is indifferent between food and cloth production. $L_F+L_C=L$
3. $\frac{P_F^W}{P_C^W}<\frac{a_F}{a_C}$ => Relative benefit of food production is less than cost, the country only produces cloth.$L_C=L$

Plotting the relative world prices on a line, the cases are represented as follows:
![[Pasted image 20240207014143.png|400]]
The country with the lower relative cost of production of the good has the [[Comparative advantage]] in the production of the good. 

##### Supply curve
The relative supply in the two country system of food to cloth is given by $$\text{RS}^W=\frac{Y_F+Y_F^*}{Y_C+Y_C^*}$$When the relative supply is plotted against the the relative world prices, we get the following supply curve.
![[Pasted image 20240207014525.png|400]]

While $\text{RC}^W<a_F/a_C$ there is no production of food in the system

The vertical portion of the graph is when the home country produces only food (relative benefit>relative cost). As a result, it transfers its entire labor force into food production. The foreign country's relative cost is higher and so it produces only cloth. As a result the relative supply is given by ($Y=L/a$) $$\text{RS}^W=\frac{L/a_F+0}{0+L^*/a_C^*}=(\frac L{a_F})/(\frac{L^*}{a_C^*})$$The entire labor force of the home country produces food. This cannot be increased, food production is at maximum capacity until the foreign country is indifferent to production of food. 

When the foreign country is indifferent, it can allocate more and more of its labor to food production. To do this, it has to take away labor from cloth production. Since the x-axis is in relative terms, the denominator (cloth production) will tend to zero as the foreign country produces more food and less goods. As a result the relative supply curve stretches to infinity

##### Demand curve
The relative world demand of food to cloth is given by $$\text{RD}^W=\frac{X_F+X_F^*}{X_C+X_C^*}$$The relation between the relative world demand and the relative world prices is determined from the optimization of the consumption preferences. 

![[Pasted image 20240207020607.png|400]]

##### Equilibrium
There can be three types of equilibrium based on where the supply and demand curves intersect. 
1. Home produces both goods, Foreign produces its comparative advantage
2. Home produces its comparative advantage, foreign produces both goods
3. Both countries produce their comparative advantage

![[Pasted image 20240207021234.png|400]]

Type one and 2 are incomplete specializations, whereas type 3 is a complete specialization as just one good is produced in both countries, their [[Comparative advantage]]. 

**Case I: Complete specialization**
In this case (3), both countries produce only their comparative advantage. This means that the entire labor force of the country is used in the production of that good. If the home country has a comparative advantage in food production, then
Food production in the world: $L/a_F$
Cloth production in the world: $L^*/a_C^*$

In this case, the labor distribution and world supply are trivially found due to the nature of the equilibrium. However, since only one good is produced in each country, it must be that $$\frac{a_F^*}{a_C^*}>\frac{P_F^W}{P_C^W}>\frac{a_F}{a_C}$$If two countries seem similar in terms of labor endowment and unit labor requirements, then a case 1 equilibrium is likely. 

**Case II: Incomplete specialization**
In this case (1) and (2), one country produces both goods and the other produces only its comparative advantage. This implies that one country is indifferent to producing the good and the other has a benefit. This implies that the world relative price of the good will be equal to the [[Ricardian trade model#Autarky equilibrium|autarky]] relative price in that country that produces both goods (relative unit labor requirement). If the home country has a comparative advantage in food and foreign produces both goods, $$\frac{a_F^*}{a_C^*}=\frac{P_F^W}{P_C^W}>\frac{a_F}{a_C}$$ The labor allocation in the country producing one good is also trivially found (home allocates $L$ to food). The labor allocation in the other country has to be found. 

If the two countries are different in terms of labor endowment and unit labor requirements, then a case 2 equilibrium is likely. 


#### Welfare (gains from trade)
The **Production Possibility Frontier (PPF)** is the frontier that shows the set of goods available to both the home and foreign countries. If home has a comparitive advantage in food production, the PPFs are ![[Pasted image 20240209024651.png]]
As the production functions do not have diminishing marginal returns, the PPF is linear. The slope is given by the unit labor requirement ratio. Higher slope slope implies that $$\frac{a_F}{a_C}<\frac{a_F^*}{a_C^*}$$

The **Consumption Possibility Frontier (CPF)** is the maximum amount of a good that can be consumed given the amount of consumption of the other good in a two good model. It represents the set of all feasible consumption bundles in the country. Supposing the home country has a [[Comparative advantage]] in food production, in the autarky equilibrium, the CPFs of both countries are identical to the PPFs. This is because each can country can only consume a maximum of what it produces, since there is no trade. 

In the free trade situation, if the home country wants to only consume clothes, it can 
1. Produce only food. The amount of food produced is given as $(L/a_F)$
2. Sell the food to the foreign country. The amount of money received then is $\frac L{a_F}P_F^W$
3. Use this money to buy clothes from the foreign country. The amount of clothes received is $\frac L{a_F}\frac {P_F^W}{P_C^W}$

##### Case I equilibrium welfare
In the case I equilibrium, we know that $$\frac{a_F^*}{a_C^*}>\frac{P_F^W}{P_C^W}>\frac {a_F}{a_C}$$Looking only at the case for home, $$\frac{P_F^W}{P_C^W}>\frac {a_F}{a_C}$$Multiplying by $L/a_F$ on both sides,
$$\frac{L}{a_F}\times\frac{P_F^W}{P_C^W}>\frac{L}{a_F}\times\frac {a_F}{a_C}$$$$\frac{L}{a_F}\frac{P_F^W}{P_C^W}>\frac{L}{a_C}$$The LHS is the quantity of cloth in the FTE. RHS is the quantity of cloth that can be produced on by home. 

Similarly for the foreign country only wanting to consume food, in a case 1 FTE, the amount of food that is received by executing the inverted trading strategy as outlined earlier for home is given by $$\frac{L^*}{a_C^*}\frac{P_C^W}{P_F^W}$$From the Case I equilibrium condition, we know that 
 $$\frac{a_F^*}{a_C^*}>\frac{P_F^W}{P_C^W}$$Multiplying by $L^*/a_C^*$ on both sides, $$\frac{L^*}{a_C^*}\times\frac{a_F^*}{a_C^*}>\frac{L^*}{a_C^*}\times\frac{P_F^W}{P_C^W}$$$$\frac{L^*}{a_C^*}\times\frac{P_C^W}{P_F^W}>\frac{L^*}{a_C^*}\times\frac{a_C^*}{a_F^*}$$$$\frac{L^*}{a_C^*}\frac{P_C^W}{P_F^W}>\frac{L^*}{a_F^*}$$Therefore through the trading strategy foreign can gain more units of food than if they produced it themselves. Plotting the autarky and the FTE CPFs, 
 ![[Pasted image 20240213231147.png]]
 Therefore there are more consumption bundles available to both the home and foreign country in the FTE case I. This implies that both countries are better off in FTE than in Autarky. **The Case I equilibrium strictly improves welfare**.

##### Case II equilibrium welfare 
Suppose home has a comparative advantage in food production, but foreign produces both goods in order to meet demand. From the trading strategy, the maximum amount of food consumed by foreign is $$\frac{L^*}{a_C^*}\frac{P_C^W}{P_F^W}$$ From the equilibrium condition, $$\frac{a_F^*}{a_C^*}=\frac{P_F^W}{P_C^W}>\frac{a_F}{a_C}$$For the foreign country, $$\frac{P_F^W}{P_C^W}=\frac{a_F^*}{a_C^*}$$Multiplying on both sides by $L^*/a_C^*$ and simplifying, $$\frac{L^*}{a_C^*}\frac{P_C^W}{P_F^W}=\frac{L^*}{a_F^*}$$Which results in the same CPF as in Autarky. 

From the trading strategy, for the home country it can consume a maximum amount of cloth of $$\frac L{a_F}\frac {P_F^W}{P_C^W}$$From the equilibrium condition, $$\frac{P_F^W}{P_C^W}>\frac{a_F}{a_C}$$Multiplying both sides by $L/a_F$ and simplifying, $$\frac{L}{a_F}\frac{P_F^W}{P_C^W}>\frac{L}{a_C}$$Therefore through trading, home can consume more cloth than it can produce by itself in autarky. Graphically, ![[Pasted image 20240213233535.png]]
Therefore more consumption bundles are available only to the home country in FTE compared to autarky. Unchanged for foreign. Therefore **the case II equilibrium weakly improves welfare**. 


#### Takeaways
- There is almost always an opportunity for mutually beneficial trade
- With costless trade $(\frac{a_F}{a_C}\ne\frac{a_F^*}{a_C^*})$ implies that countries will increase trade
- Countries can benefit from trade even if they are less efficient in the production of all goods. A country with lower productivity, will have lower wages (less total production in a perfectly competitive goods market -> less money to pay workers from revenue -> lower wages ) making the country productive in some goods.
- Trade is an indirect method of production
- Trade causes the destruction of jobs - labor moves out of the relatively inefficient industry and into the relativity efficient industry. However, with goods like apparel and software, there is significant cost of movement of labor. 

