The minimum cash reserve requirement by the government for the [[banks - capital intermediaries]]. This is a ratio of the total deposits the bank has. It is implemented in order to mitigate liquidity issues and prevent [[Model of a bank run|bank runs]]. 

$\gamma$ of total real deposits is the reserve ratio ($0<\gamma<1$)

Looking at the [[Intro to Eco (S2022)/balance sheet]] of the bank,

|Assets|Liabilities|
|---|---|
|Cash: $\gamma N_t h_t$|Deposits: $N_t h_t$|
|Capital: $(1-\gamma) N_th_t$||
|Total: $N_th_t$|Total: $N_th_t$|

This cash is obtained from the bank by exchanging a fraction of the goods ($\gamma$) to the government in exchange for fiat money with the same real value. The bank obtains $N_th_t$ from all the depositors. $(1-\gamma)N_th_t$ is used to create capital. $\gamma N_th_t$ is given to the government in exchange for $M_t$ units of nominal money. $$\gamma N_th_t=v_tM_t$$$$v_t=\frac{\gamma N_th_t}{M_t}$$


The reserve ratio affects many macroeconomic factors:
- Price level in the economy
- inflation rate
- Seigniorage revenue
- GDP
- Interest rate offered to depositors

#### Macroeconomic Effects
##### Price level
As shown, $v_t$ is increasing with an increase in $\gamma$. We know that the [[simple model of money#Price level|price level]] in the economy is $$p_t=\frac 1{v_t}$$Therefore, an increase in $\gamma$ leads to a fall in $p_t$. This is because a larger percent of the existing deposits is exchanged for the same amount of real money given by the government, setting the real value of the nominal money. As the real value of the money increases, price level falls. This assumes that all other things remain constant ($r,h_t$)

##### [[inflation]]
Despite the increase in $p_t$, the inflation rate does not permanently increase in the economy. There is only a one period fluctuation during the period of change of $\gamma$. We know this as at [[Inflation model#at the stationary monetary equilibrium|SME]], $$\frac{p_{t+1}}{p_t}=\frac{v_t}{v_{t+1}}=\frac zn$$This does not change with a change in $\gamma$. (Gamma cancels out in $v$ terms).

##### [[seigniorage revenue]]
We know that $$\text{seigniorage revenue}=v_t(M_{t-1}-M_t)$$
$$=(1-\frac 1z)v_tM_t$$$$=(1-\frac 1z)\gamma N_th_t$$
Assuming that $\gamma$ has no effect on $h_t$, an increase in $\gamma$ leads to an increase in Seigniorage rev.

##### GDP
In the 3-generation OLG model, the GDP is given by $$\text{GDP}_t=N_ty+XN_{t-2}k_{t-2}+X(1-\gamma)N_{t-2}h_{t-2}$$Where:
- $XN_{t-2}k_{t-2}$ is the capital created by individuals
- $X(1-\gamma)N_{t-2}h_{t-2}$ is the capital created by the bank. This includes the profits, money to be given to depositors, interest to be given to each depositor

A higher $\gamma$ will result in a lower GDP. This is because banks cannot invest as much of its deposits into capital. 

##### Real rate of return on deposits
One period from now, the banks assets are given by 
Cash: $\frac nz \gamma N_th_t$
Capital: $\sqrt X (1-\gamma)N_th_t$

If we have competitive banking, the bank will pay back the entire amount it harvests as capital back to depositors. The profit of the banking sector will be 0. $$\text{Gross rate of return on deposits}= \frac{\frac nz\gamma N_th_t+\sqrt X(1-\gamma)N_th_t}{N_th_t}$$$$=\gamma\frac nz+(1-\gamma)x$$where $x=\sqrt X$

