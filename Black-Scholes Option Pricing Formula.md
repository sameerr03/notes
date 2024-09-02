An equation used to price [[Options]].

#### Assumptions
- Stock prices follow geometric Brownian motion. This is mathematically represented using the following process$$dS = \mu S  dt+\sigma SdW$$where:
	- $S$ is the stock price
	- $dt$ is an infinitesimally small time increment
	- $\mu$ is the drift coefficient
	- $\sigma$ is the volatility
	- $dW$ is the infinitesimally small increment of the Weiner process ($dW\sim N(0, dt))$
- Stock returns as a result follow the following distribution $$r=\frac {dS}S = \mu dt+\sigma dW$$Where $\mathbb E(r) = \mu$ and $\text{Var}(r) = \sigma^2$, $r\sim  N(\mu,\sigma^2)$ - returns are normally distributed. 
- Markets are competitive, no frictions

#### Value of a call option
The value of a call option is given by $$V[C_E(S_t,t)] = S_tN(d_1)-Ee^{-r(T-t)}N(d_2)$$Where:
- $E$ is the strike price, $S_t$ is the stock price at time $t$, $t$ is the current time, $T$ is the time of expiry
- $$d_1 = \frac{\ln(\frac{S_t}{Ee^{-r(T-t)}})+\frac{\sigma^2}{2}(T-t)}{\sigma\sqrt{T-t}}$$
- $$d_2 = d_1-\sigma\sqrt{(T-t)}=\frac{\ln(\frac{S_t}{Ee^{-r(T-t)}})-\frac{\sigma^2}{2}(T-t)}{\sigma\sqrt{T-t}}$$
- $N(\cdot)$ is the CDF of a standard normal distribution

#### Value of a put option 
Using the value of a call option and the [[Options#Put Call parity|Put call parity]] relation, we can find the value of a put$$-V[C_E(S_t,t)]+S_t = -V[P_E(S_t,t)]+Ee^{-r(T-t)}$$$$V[P_E(S_t,t)] = Ee^{-r(T-t)}-S_t+V[C_E(S_t,t)]$$Using the Black-Scholes equation$$= Ee^{-r(T-t)}-S_t+S_tN(d_1)-Ee^{-r(T-t)}N(d_2)$$$$=Ee^{-r(T-t)}(1-N(d_2))-S_t(1-N(d_1))$$we know that the normal distribution is symmetric. Therefore$$V[P_E(S_t,t)]=Ee^{-r(T-t)}N(-d_2)-S_tN(-d_1)$$

#### Comparative statics
We see that As the value of $E$ increases, the value of a put option increases and the value of a call option decreases. 

