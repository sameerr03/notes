The stock markets cannot be accurately forecasted. The past patterns of market cannot be an indicator of the plausability of the future of the market. Stock markets could be either a Random Walk or an AR-1 model. A random walk is predicted by the equation$$x_t=x_{t-1}+\epsilon_t$$where:
- $x_t$ is the position at time $t$
- $x_{t-1}$ is the position of the object in the previous time period
- $\epsilon_t$ is the randomness or the noise at time $t$ that makes a random walk unpredictable

In a random walk, there can be no prediction for a single random walk. But for infinitely many random walks, a distributuion is followed where the most probable position is the initial one.

An AR-1 (First order Autoregressive) model is given by $$x_t=100+\rho(x_{t-1}-100)+\epsilon_t$$where:
- 100 is the starting point
- $x_t$ is the position at time $t$
- $\rho$ is between -1 and +1

This is a **mean reverting** model. Based on the value of $\rho$, the object moves back to the starting positon, based on the noise and the position in the last period (Do random math to understand it while reviewing). If $\rho$ equals one, the AR-1 is a random walk. However, it is not possible to tell the difference between randomised  

