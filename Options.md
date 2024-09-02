Options are contracts between two parties. There are two types of options - Call and put options. 

### Call options
A call option is the right but not the obligation to buy a particular asset at a predetermined price (Strike price) on an agreed date (Expiry date). The contract itself has some value, known as the premium which has to be paid to the option seller in order to get the contract. 

The value of a call option is given by $$V[C_E(S_t,t)]$$where
- $C_E$ is a call option with strike price $E$
- $t$ is the time of purchase
- $S_t$ is the underlying stock price at the time of purchase

#### Long Call (Buying a call option)
If the strike price is $E$, stock price is $S(T$) and the premium of the contract is $P$, at the time of expiry ($t=T$), the payoff of the option is given by 
![[Pasted image 20240419160336.png|500]]
The profit/loss is given by $$\text{Profit} = \begin{cases}0-e^{r(T-t)}V[C_E(S_t,t)]&\text{when }S_T<E\\S_T-E-e^{r(T-t)}V[C_E(S_t,t)]&\text{when }S_T>E\end{cases}$$The exponent term takes into account the time value of the money, as the value of the option is paid upfront. This term is [[Future and present values#Future value|continuously]] compounding at the risk free rate $r$.
#### Short call (Selling an option)
![[Pasted image 20240419160408.png|500]]
The profit/loss is given by $$\text{Profit} = \begin{cases}e^{r(T-t)}V[C_E(S_t,t)]&\text{when }S_T<E\\e^{r(T-t)}V[C_E(S_t,t)]+E-S_T&\text{when }S_T>E\end{cases}$$
### Put options
A put option is the right but not the obligation to sell a particular asset at a predetermined price (Strike price) on an agreed date (Expiry date). The contract itself has some value, known as the premium which has to be paid to the option seller in order to get the contract. 

For a put option, the value is given by $$V[P_E(S_t,t)]$$
#### Long put
![[Pasted image 20240419160507.png|500]]
The profit/loss is given by $$\text{Profit} = \begin{cases}E-S_T-e^{r(T-t)}V[P_E(S_t,t)]&\text{when }S_T<E\\0-e^{r(T-t)}V[C_E(S_t,t)]&\text{when }S_T>E\end{cases}$$
#### Short put
![[Pasted image 20240419160525.png|500]]
The profit/loss is given by $$\text{Profit} = \begin{cases}e^{r(T-t)}V[P_E(S_t,t)]-E+S_T&\text{when }S_T<E\\e^{r(T-t)}V[P_E(S_t,t)]&\text{when }S_T>E\end{cases}$$
#### Straddle
A straddle is when a put and a call option are bought simultaneously with the same strike price and expiration date
![[Pasted image 20240424140650.png|400]]

The profit/loss is given by $$\text{Profit} = \begin{cases}E-S_T-e^{r(T-t)}(V[P_E(S_t,t)]+V[C_E(S_t,t)])&\text{when }S_T<E\\S_T-E-e^{r(T-t)}(V[P_E(S_t,t)]+V[C_E(S_t,t)])&\text{when }S_T>E\end{cases}$$
#### Strangle
A put with a lower strike price and a call with a higher strike price are bought simultaneously with the same expiration date 
![[Pasted image 20240424141313.png|400]]
The profit/loss is given by $$\text{Profit} = \begin{cases}E-S_T-e^{r(T-t)}(V[P_{E_1}(S_t,t)]+V[C_{E_2}(S_t,t)])&\text{when }S_T<E_1\\0-e^{r(T-t)}(V[P_{E_1}(S_t,t)]+V[C_{E_2}(S_t,t)])&\text{when }E_1<S_T<E_2\\S_T-E-e^{r(T-t)}(V[P_{E_1}(S_t,t)]+V[C_{E_2}(S_t,t)])&\text{when }S_T>E_2\end{cases}$$
### Put Call parity
Perfectly hedged positions should have the same value.

Covered Call - Short Call + Stock: This position holds the number of shares specified by the contract, allowing for no undefined losses

Cash secured put - Short Put + Cash: This position allows you to buy into the stock if the put is exercised.

Algebraically, $$-V[C_E(S_t,t)]+S_t = -V[P_E(S_t,t)]+e^{-r(T-t)}E$$
If empirically it is found that $$-V[C_E(S_t,t)]+S_t<-V[P_E(S_t,t)]+Ee^{-r(T-t)}$$Arbitrage can be executed using the following:
- (long greater value hedged portfolio) - borrow $E$ at $r$ and long put
- (short lesser value hedged portfolio) - short call and long stock

**If $S_t<E$** at $T=t$
Put exercised, call not exercised => gain premium
sold stock, used money to pay off loan

**If $S_t>E$**,
Put not exercised, call exercised => use stock to fill order
Use $E$ from sale to pay off loan, which has matured to $E$


Profit is $\alpha$, the difference between the RHS and the LHS


