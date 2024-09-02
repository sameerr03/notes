In the [[Decentralized record keeping based solution]], if the cost of maintaining a record $\psi>N_ty$ then record keeping will not be possible. In order to have a decentralized solution to the [[Overlapping generation model]], we can introduce money under the following assumptions:
- The total amount of money is fixed. The nominal stock of it is $M$.
- All the money is fiat money - a form of money that is intrinsically worthless
The structure of time periods and overlapping generations is the same as [[Decentralized record keeping based solution]].

Money circulates in the economy through the old people possessing all the money and then using it to buy goods from the young people's endowments. The young people get money from this and as a result have money going into the next time period. 

**In period** $t$,
for the young agent:
$$c_{1,t}+v_tm_t\le y$$Where:
- $v_t$ is the real value of nominal units of money (what amount of goods can be purchased with one unit of nominal money)
- $m_t$ is the individual demand for nominal money

**In period t+1:**
for the same agent (now old)
$$c_{2,t+1}\le v_{t+1}m_t$$$$\frac1{v_{t+1}}c_{2,t+1}\le m_t$$$$\frac{v_t}{v_{t+1}}c_{2,t+1}\le v_tm_t$$$$c_{1,t}+\frac{v_t}{v_{t+1}}c_{2,t+1}\le c_{1,t}+v_tm_t\le y$$$$c_{1,t}+\frac{v_t}{v_{t+1}}c_{2,t+1}\le y$$This is the lifetime budget constraint.

### Stationary monetary equilibrium
We assume that there is an equal supply and demand for money (monetary equilibrium). 
From the young agent equation,$$c_1+v_tm_t\le y$$with non monotonic preferences,$$c_1+v_tm_t=y$$$$v_tm_t=y-c_1$$in monetary equilibrium, the amount of nominal money individually demanded by all the young agents during a particular period should be equal to the total amount of nominal money supply ($m_tN_t=M$). Substituting this in,$$v_t\frac M{N_t}=y-c_1$$$$v_t=\frac{N_t(y-c_1)}M$$ Since the solution is stationary, $y-c_1$ is in both the numerator and denominator.
$$\frac{v_t}{v_{t+1}}=\frac{N_t/M}{N_{t+1}/M}=\frac 1n$$
From the LTBC, we can get the equation$$c_{1,t}+\frac 1nc_{2,t+1}\le y$$As the utility functions are the same as [[social planner solution]], the SME coincides with the golden rule social planner solution, without the record keeping cost of the decentralized solution. 

#### Price level 
As $v_t$ is the amount of goods for 1 unit of nominal money, the price of one good will be $$p_t=\frac 1{v_t}$$**Inflation rate**
The change in price from one time period to the next gives inflation in this model.$$\frac{p_{t+1}}{p_t}=\frac{v_t}{v_{t+1}}=\frac 1n$$