[[aggregate demand]] and [[aggregate supply]] model with time sensitivity.

### DAS (Dynamic Aggregate supply)
Equation:
$$\pi_t=\pi_{t-1}+\phi\ (Y_t-\bar{Y}_t)+\nu_t$$
![[Pasted image 20221220212908.png|400]]
Upward sloping as $\pi_t$ increases with an increase in $Y_t$.
if expectations of inflation go up, inflation today increases at the same $Y_t$. As a result, DAS$_t$ shifts up. A positive supply shock (such as rise in prices) also increases inflation with that same $Y_t$. An increase in the natural level of output will reduce $\pi_t$ at the same Y and DAS$_t$ will shift downwards.

### DAD (Dynamic Aggregate Demand)
Equation:
$$Y_t=\bar{Y}_t-\frac{\alpha\ \theta_\pi}{1+\alpha\ \theta_Y}(\pi_t-\pi_t^*)+\frac{1}{1+\alpha\ \theta_Y}\epsilon_t$$
![[Pasted image 20221220214102.png|400]]
if inflation increases, Y decreases. Therefore DAD is downward sloping.  
if $\bar{Y}_t$ increases, for a fixed $\pi_t$, $Y_t$ increases resulting in the curve shifting outwards  
if $\epsilon_t$ increases, (+ve demand shock → increase in demand), $Y_t$ increases for the same $\pi_t$, therefore the curve shifts outwards. If the central bank's target inflation rate increases, $Y_t$ increases for the same inflation level, the curve shifts outwards.

### DAD-DAS Model
![[Pasted image 20221220214631.png|400]]

#### Supply Shocks
With a positive supply shock(rise in prices) from t-1 to t, the DAS shifts upwards.
![[Pasted image 20221220223513.png|400]]
In time period t->t+1, there is no supply shock. However, there is an inflation, which results in expectations of inflation rising, resulting in (due to adaptive expectations)
$$\pi_{t+1}=\pi_t+\phi(Y_t-\bar{Y}_t)>\pi_{t-1}=\pi_{t-2}+\phi(Y_t-\bar{Y}_t)$$
This results in the DAS not returning completely
![[Pasted image 20221220223920.png]]

#### Demand shocks
With a positive demand shock, DAS moves outwards. In the new equillibrium, inflation increases in time period **t-1->t**. Y increases
![[Pasted image 20221220224137.png|400]]
**Time t->t+1**
The DAS curve moves upwards due to an increase in inflation leading to an increase in expectations of inflation. Suppose there is an additional demand shock, the DAD moves outward again. Y and inflation increase to a further extent. 
![[Pasted image 20221220224454.png|400]]
**Time t+1->t+2**
There is no demand shock any longer, therefore DAD returns back to initial level in t-1. As inflation has increased, the expectations of inflation have increased once again. DAS shifts outward again despite no demand shock. This results in Y falling and inflation increasing.
![[Pasted image 20221220224940.png|400]]

#### Long run equillibrium
Conditions:
1. No External shocks
2. Stable constant inflation rates

This results in
$Y_t=\bar{Y}_t$
$r=\rho$
$\pi_t=\pi_t^*$
$\mathbb{E}_t\pi_{t+1}=\pi_t^*$
$i_t=\rho+\pi_t^*$

### Derivation
##### Equations
Derived from 5 equations
###### IS equation
$$Y_t=\bar{Y}_t-\alpha\ (r_t-\rho)+\epsilon_t$$
Where:
- $Y_t$ is the output of the economy
- $\bar{Y}_t$ is the natural long-run output
- $r_t$ is the real interest rate
- $\alpha$ is the sensitivity of $Y_t$ to $\Delta r_t$
- $\rho$ is the natural rate of interest when $Y_t=\bar{Y}_t$
- $\epsilon_t$ is an exogenous demand shock

As output is inversely related to the interest rate, this equation is synonymous to the IS curve equation

###### Fisher Equation
$$r_t=i_t-\mathbb{E}_t\pi_{t+1}$$
Where:
- $i_t$ is the nominal interest rate
- $\mathbb{E}_t\pi_{t+1}$ is the expectations of inflation in the next time period

###### [[Phillips curve]]
$$\pi_t=\mathbb{E}_{t-1}\pi_t+\phi\ (Y_t-\bar{Y}_t)+\nu_t$$
Where
- $\mathbb{E}_{t-1}\pi_t$ is the expectations of inflation in the previous time period about the current time period
- $\phi\ (Y_t-\bar{Y}_t)$ deviation from natural rate of output (subn. of [[Okun's law]])
- $\nu_t$ is the exogenous supply shock

###### Adaptive expectations
$$\mathbb{E}_t\pi_{t+1}=\pi_t$$
expectations today of inflation tomorrow is the inflation today (Expect inflation to remain constant)

###### Monetary policy rule
$$i_t=\pi_t+\rho\ +\theta_{\pi}\ (\pi_t-\pi_t^*)+\theta_Y(Y_t-\bar{Y}_t)$$
Where
- $\theta_\pi$ is the sensitivity of $i_t$ to $\Delta\pi$
- $\pi^*_t$ is the central bank's target inflation rate
- $\theta_Y$ is the sensitivity of $i_t$ to $\Delta Y$

#### Types of variables:
Endogenous: Changes from within the model: $Y_t,\ \pi_t,\ r_t,\ i_t,\ \mathbb{E}_t\pi_{t+1}$
Exogenous: Changes from outside the model: $\bar{Y}_t,\ \pi^*_t,\ \pi_{t-1},\ \epsilon_t,\ \nu_t$
Parameters: Specefic to a particular economy: $\alpha,\ \rho,\ \phi,\ \theta_Y,\ \theta_\pi$

#### Dynamic Aggregate supply curve
Start with phillips curve
$$\pi_t=\mathbb{E}_{t-1}\pi_t+\phi\ (Y_t-\bar{Y}_t)+\nu_t$$
From adaptive expectations, we know that $\mathbb{E}_{t-1}\pi_t=\pi_{t-1}$. Therefore, 
$$\pi_t=\pi_{t-1}+\phi\ (Y_t-\bar{Y}_t)+\nu_t$$
As Y increases, $\pi$ increases -> graph is upward sloping

#### Dynamic Aggregate Demand curve
Start with IS equation
$$Y_t=\bar{Y}_t-\alpha\ (r_t-\rho)+\epsilon_t$$
From fisher equarion,
$$Y_t=\bar{Y}_t-\alpha\ (i_t-\mathbb{E}_t\pi_{t+1}-\rho)+\epsilon_t$$
Using adaptive expectations,
$$Y_t=\bar{Y}_t-\alpha\ (i_t-\pi_t-\rho)+\epsilon_t$$
Using the monetary policy rule,
$$Y_t=\bar{Y}_t-\alpha(\pi_t+\rho\ +\theta_{\pi}\ (\pi_t-\pi_t^*)+\theta_Y(Y_t-\bar{Y}_t)-\pi_t-\rho)+\epsilon_t$$
Simplifying,
$$Y_t=\bar{Y}_t-\frac{\alpha\ \theta_\pi}{1+\alpha\ \theta_Y}(\pi_t-\pi_t^*)+\frac{1}{1+\alpha\ \theta_Y}\epsilon_t$$
If inflation increases relative to natural rate, Y decreases therefore DAD is downward sloping