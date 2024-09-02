The [[Overlapping generation model]] with the [[simple model of money]], that uses a changing amount of nominal currency. 

Assume that the stock of money is growing at a constant rate $z$. This is represented as$$M_{t+1}=zM_t$$Based on the value of $z$, the amount of nominal money is either increasing ($z>1$), decreasing ($z<1$) or constant ($z=1$) (which is the [[simple model of money]]).

At the beginning of each period $t$, before any trade commences, the monetary authority print $M_{t}-M_{t-1}$ nominal units of money and transfer it to the $N_{t-1}$ old people in $t$.

**For an agent born in period t**
Budget constraint when young ($t$):
$$c_{1,t}+v_tm_t\le y$$
Budget constraint when old ($t+1$):$$c_{2,t}\le v_{t+1}m_t+a_{t+1}$$Where $a$ is the real value of monetary transfer to each old person. $$a_{t+1}=v_{t+1}\frac{(M_{t+1}-M_t)}{N_t}$$$$=\frac{(1-\frac 1z)v_{t+1}M_{t+1}}{N_t}$$as $z=M_{t+1}/M_t$ 

From the budget constraint in the second period,
$$c_{2,t}\le v_{t+1}m_t+a_{t+1}$$$$\frac 1{v_{t+1}}c_{2,t}\le m_t+\frac1{v_{t+1}}a_{t+1}$$From the budget constraint of the first period,
$$m_t\le\frac y{v_t}-\frac{c_{1,t}}{v_t}$$As $m_t$ is greater than $\frac 1{v_{t+1}}c_{2,t}$ and less than $\frac y{v_t}-\frac{c_{1,t}}{v_t}$, we can combine the two equations to get$$\frac1{v_t}c_{1,t}+\frac 1{v_{t+1}}c_{2,t}\le\frac1{v_{t+1}}a_{t+1}+\frac y{v_t}$$$$c_{1,t}+\frac {v_t}{v_{t+1}}c_{2,t}\le y+\frac{v_t}{v_{t+1}}a_{t+1}$$This is the lifetime budget constraint

### at the stationary monetary equilibrium
$$c_{1,t}=c_{1,t+1}=\text{........}=c_1$$$$c_{2,t}=c_{2,t+1}=\text{........}=c_2$$
from the market clearing condition,
$$\text{Total endowment left after consumption}=N_t(y-c_1)$$$$\text{Amount of money exchanged}=v_tM_t$$In equilibrium, these two are equal and people use all of their money$$v_tM_t=N_t(y-c_1)$$$$v_t=\frac{N_t(y-c_1)}{M_t}$$We can also get $v_{t+1}$,$$v_{t+1}=\frac{N_{t+1}(y-c_1)}{M_{t+1}}$$Dividing,$$\frac {v_t}{v_{t+1}}=\frac{(N_t(y-c_1))/M_t}{(N_{t+1}(y-c_1))/M_{t+1}}$$$$=\frac{N_t\cdot M_{t+1}}{N_{t+1}\cdot M_t}$$$$\frac {v_t}{v_{t+1}}=\frac zn$$ as $M_{t+1}/M_t=z$  and $N_{t+1}/N_t=n$

Also at the stationary SME,$$a_t=\frac{(1-\frac 1z)v_{t}M_{t}}{N_{t-1}}$$$$a_{t+1}=\frac{(1-\frac 1z)v_{t+1}M_{t+1}}{N_t}$$$$\frac{a_t}{a_{t+1}}=\frac{\frac{(1-\frac 1z)v_{t}M_{t}}{N_{t-1}}}{\frac{(1-\frac 1z)v_{t+1}M_{t+1}}{N_t}}$$$$\frac{a_t}{a_{t+1}}=\frac{v_t}{v_{t+1}}\times \frac{M_t}{M_{t+1}}\times \frac{N_t}{N_{t-1}}$$$$=\frac zn \times \frac 1z\times n=1$$From this we can extrapolate that$$a_{t}=a_{t+1}=\text{........}=a$$
### Lifetime budget constraint at the SME
From all the SME conditions, the LTBC is$$c_1+\frac znc_2\le y+\frac zn a$$![[Pasted image 20230908221343.png|400]]

### Feasibility and affordability
Budget set describes the affordability, and the feasibility set describes what is available for consumption. The overlap determines all the allocations possible in the model. The feasibility set is given by the [[social planner solution]].$$c_{1,t}+\frac1nc_{2,t}\le y$$Plotting both simultaneously,
![[Pasted image 20230908221800.png|600]]
green - feasible set
blue - budget set

The overlapping quadrilateral is the set of all allocations that are possible. In this quadrilateral, point X has the highest utility (will be on the highest indifference curve). This is different from the [[social planner solution]], however.![[Pasted image 20230908222100.png|400]]
With a growing or shrinking money supply ($z\ne 1$) the solution deviates from the optimal social planner allocation (Welfare loss). ($z=1$ is the optimal solution, i.e., no inflation)

From the solutions, we can see that with inflation, people tend to overconsume in the first period of their lives. This is because inflation reduces the real value of the money in the next period, therefore as a protective measure, they choose to overconsume in the first period and underconsume in the second. 