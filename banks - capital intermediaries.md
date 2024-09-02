A modification of the [[Overlapping generation model]], wherein the agents live for three periods. 

|Period|Consumption|Endowment|
|---|---|---|
|Youth|$c_{1,t}$|$y$|
|Middle age|$c_{2,t+1}$|Nothing|
|Old|$c_{3,t+2}$|Nothing|

We need to maximize the utility of consumption with respect to the following constraints$$c_{1,t}+k_t+v_tm_t\le y$$$$c_{2,t+1}\le v_{t+1}m_t$$$$c_{3,t+2}\le Xk_t$$The agents holds money for their middle age, and the capital created in their youth matures in their old age. Unlike the [[model using capital]], capital takes 2 periods to mature, meaning it is **illiquid**. The other assumption necessary for this structure of consumption is that $X>(n/z)^2$. Otherwise money would be held in the two periods and not capital. 

#### Introducing banks
**In period $t$,**
The young agent can use their endowment for
- consumption ($c_{1,t}$)
- capital ($k_t$)
- Holding money ($v_tm_t$)
- Bank deposits ($h_t$)

The bank offers a 1 period gross rate of return $r_{t+1}\ge v_{t+1}/v_t=n/z$ (at SME). We assume that if $r_{t+1}=v_{t+1}/v_t$ then deposits $\succ$ money for various arbitrary reasons. When the rate of interest offered by the bank is greater than the return on holding fiat money, fiat money is not held by the agents and they finance consumption in their middle age solely through deposits. Thus their budget constraint becomes, $$c_{1,t}+k_t+h_t=y$$The total deposits in banks = $N_th_t$
Banks convert the deposited goods into capital, which gives $XN_th_t$ goods in $t+2$. 

**In $t+1$**,
Banks have to pay $r_{t+1}N_th_t$ to the new middle aged. 
banks use the deposits invested from the current young to pau off the interest and principal of the middle aged$$r_{t+1}N_th_t= N_{t+1}h_{t+1}$$

**In $t+2$**,
Bank gets $XN_th_t$ goods. Bank has to pay off last periods depositors,$$r_{t+2}N_{t+1}h_{t+1}$$$$=r_{t+2}r_{t+1}N_th_t$$using the return from capital. Therefore, the profit of the bank is given by $$\text{profit}=(X-r_{t+1}r_{t+2})N_th_t$$$$\text{per deposit profit}=(X-r_{t+1}r_{t+2})$$
This changes the optimization problem of the agent to maximize utility from the consumption across each time period with the budget constraints:$$c_{1,t}+k_t+h_t\le y$$$$c_{2,t+1}\le r_{t+1}h_t$$$$c_{3,t+2}\le Xk_t$$Presence of banks give higher rate of return than money as $r>n/z$. 
#### SME
At the SME,
$$c_1+k_t+h_t=y$$$$c_2=r_{t+1}h_t$$$$c_3=Xk_t$$As $c_3$ is stationary, this implies that $k_t$ is also stationary in SME. As $k,y$ and $c_1$ are stationary, this means that $h_t$ is also stationary. As $c_2$ is stationary and $h$ is stationary, that implies that $r$ is stationary. Therefore, $$r_t=r_{t+1}=\text{...}=r$$This means that $$\text{profit per deposit}=X-r^2$$Supposing a banking monopoly (1 bank), then in order to maximize profit $$r=\frac nz$$as this is the lowest interest rate possible where people are indifferent between holding fiat money and making deposits. However, due to our assumptions earlier, when the interest rate is equal to the rate of return on holding money people prefer to put it in the banks for reasons of security and so on. 

Supposing more than one bank, the bank with the highest interest rates will gain all the customers. As a result all the banks will increase their interest rates and there will be no profit to be made in the banking space (perfectly competitive). This is somewhat like [[bertrand competition]].

$$r=\sqrt X$$$$\text{profit per deposit}=0$$But as both $h$ and $r$ are stationary, and $rN_th= N_{t+1}h$,$$r=n$$
#### Capital based payments modification
In the earlier model, we run into the problem that the bank uses deposits in one period to pay the deposits of the last period off. This system has contradictions when it comes to what the equilibrium interest rate is. Instead a model can be used where capital invested two periods ago is used to pay off last periods depositors.


Suppose the bank comes into existence in time $\hat t$. Going through the model period by period,

**in $\hat t-1$**

|Generation number|Group|Assets|Liabilities|
|--|---|--|--|
|3|$Y_{\hat t-1}$|$y$|$c_1, k, m$|
|2|$MA_{\hat t-1}$|$0+v_{\hat t-1}m_{\hat t-2}$|$c_2$|
|1|$O_{\hat t-1}$|$0+Xk$|$c_3$|

This time period is in monetary equilibrium. The middle generations finance their consumption through [[simple model of money]]. Suppose the stock of fiat money does not grow. This means that from the market clearing condition,
$$v_{\hat t-1}M=(y-c_1)N_{\hat t-1}$$The rate of holding fiat money will be,$$\frac{v_{\hat t-1}}{v_{\hat t-2}}=\frac{(N_{\hat t-1}(y-c_1))/M}{(N_{\hat t-2}(y-c_1))/M}=n$$
**in $\hat t$, banking starts**

|Gen number|Group|Assets|Liabilities|
|--|---|--|--|
|4|$Y_{\hat t}$|$y$|$c_1, k, m, h$|
|3|$MA_{\hat t}$|$0$|$c_2=0$|
|2|$O_{\hat t}$|$0+Xk$|$c_3$|
|-|Bank|$\bar Y+N_{\hat t}h$|$\bar Y+N_{\hat t}h$ into capital|

The bank offers a rate of return on the deposits $r\ge n$ in order to attract deposits from $Y_{\hat t}$. This means that there is no demand for the money held by $MA_{\hat t}$. The bank converts $N_{\hat t}h$ deposits and its endowment into capital. 

**Alternatively,**
Suppose welfare mechanisms are implemented in order to ensure that gen. 3 will consume. The bank, instead of placing $\bar Y$ into capital, pays off gen 3. with nominal money according to the SME. The bank's profit will be given by$$\text{Bank's profit}=\bar Y-N_{\hat t-1}n(y-c_1-k)$$

**in $\hat t+1$**,

|Gen num|Group|Assets|Liabilities|
|--|---|--|--|
|5|$Y_{\hat t+1}$|$y$|$c_1, k, h$|
|4|$MA_{\hat t+1}$|$0+rh$|$c_2$|
|3|$O_{\hat t+1}$|$0+Xk$|$c_3$|
|-|Bank|$\bar Y+N_{\hat t+1}h$|$N_{\hat t}rh$ paid to $MA_{\hat t+1}$, $N_{\hat t+1}h$ into capital |

The bank has to pay $N_{\hat t}rh$ to gen 4, as they paid deposits in the previous period. The bank's initial endowment is in capital. The bank uses the endowment in this period to pay off the deposits. $$\text{Bank's profit}=\bar Y-N_{\hat t}rh$$
**in ${\hat t+2}$**

|Gen num|Group|Assets|Liabilities|
|--|---|--|--|
|6|$Y_{\hat t+2}$|$y$|$c_1, k, h$|
|5|$MA_{\hat t+2}$|$0+rh$|$c_2$|
|4|$O_{\hat t+2}$|$0+Xk$|$c_3$|
|-|Bank|$0+X(\bar Y+N_{\hat t}h)+N_{\hat t+2}h$|$N_{\hat t+1}rh$ paid to $MA_{\hat t+2}$|

The bank uses the capital that was invested in $\hat t$ in order to pay off current middle aged.
$$\text{Bank's profit}=X(\bar {Y}+N_{\hat t}h)-N_{\hat t+1}rh$$With the **welfare mechanism in place**, the bank's profit will just simply be $$\text{Bank's profit}_{\hat t+2}=XN_{\hat t }h-N_{\hat t+1}rh$$

**in banking equilibrium for general time $t$**,

After the above, the transition from monetary to banking equilibrium is complete. Each generation follows the same pattern. 

|Group|Assets|Liabilities|
|---|--|--|
|$Y_t$|$y$|$c_1, k, h$|
|$MA_t$|$0+rh$|$c_2$|
|$O_t$|$0+Xk$|$c_3$|
|Bank|$0+X(N_{t-2}h)+N_{t}h$|$N_{t-1}rh$ paid to $MA_{t}$|

$$\text{Bank's profit}_t=N_{t-2}h(X-rn)$$
