Central banks mandate that banks hold a minimum fraction of their deposits as cash ([[Bank reserve ratios|reserve ratio]]). If a commercial bank falls short of cash needed, the central bank can lend out money to fill this gap. However, the central bank only lends out a fraction of the required cash reserve.

The bank will lower its own cash reserve and invest it into capital, and use the loan money to keep its cash level at the reserve ratio. The [[Intro to Eco (S2022)/balance sheet]] in this scenario will look like. 

|Assets|Liabilities|
|---|---|
|Cash: $(1-\delta)\gamma N_t h_t+\delta\gamma N_th_t$|Deposits: $N_t h_t$|
|Capital: $(1-\gamma) N_th_t+\delta\gamma N_th_t$|Central Bank loan: $\delta\gamma N_th_t$|
|Total: $(1+\delta \gamma) N_th_t$|Total: $(1+\delta \gamma) N_th_t$|

The central bank gives out the loan at the **central bank lending rate**=$\psi$
The one period rate of return of capital = $\sqrt X$. The bank will only invest loan money into capital if $$\psi\le \sqrt X$$Commercial banks give $(1-\delta)\gamma N_th_t$ to the central bank, which gives the commercial bank back $v_tM_t$ of cash in order to keep its minimum cash reserve and also gives the commercial bank the principal loan money $\delta\gamma N_th_t$. Representing this equation,$$\gamma N_th_t=v_tM_t+\text{Additional Loan}$$$$\delta\gamma N_th_t+v_tM_t=\gamma N_th_t$$$$v_t=\frac{(1-\delta)\gamma N_th_t}{M_t}$$$$p_t=\frac{M_t}{(1-\delta)\gamma N_th_t}$$Comparing this to [[Bank reserve ratios]], there is an additional $\delta$ term in the denominator. This indicates that there is a higher price level. This is due to the fact that the additional injection of money from the central bank leads to an increase in the liquidity. However, [[inflation]] rate does not increase, as this term gets cancelled out in subsequent price time equations. There is a temporary increase in the inflation rate which returns to the normal level $n/z$ over time. 

##### Rate of return on deposits
The gross interest rate on deposits is given by $$=\frac{\frac nz[(1-\delta)\gamma+\delta \gamma]N_th_t+\sqrt X[1-\gamma+\delta\gamma]N_th_t-\psi\delta\gamma N_th_t}{N_th_t}$$
Where the $n/z$ term is the cash term, $\sqrt X$ term is the capital term and $\psi$ term is the amount loaned to the commercial bank by the central bank (this is from the balance sheet)$$=\frac nz[(1-\delta)\gamma+\delta\gamma]+\sqrt X[1-\gamma+\delta\gamma]-\psi\delta\gamma$$$$=\frac nz\gamma+\sqrt X[1-\gamma+\delta\gamma]-\psi\delta\gamma$$
