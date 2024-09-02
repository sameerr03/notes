A non-stationary series, or a **unit root** process (at least one of the characteristic roots of the [[Difference equations|difference equation]] is 1) has no tendency to revert to its historical mean. These processes can be [[trend stationary series|trend stationary]], or have a stochastic trend such as the [[Random walk process]]. The process can also be an integrated process. The order of integration $I(d)$ is the order of differencing $(d)$ required in order to make the series stationary.

#### Spurious Regressions
A time series model $y_t=\alpha +x_t+u_t$ when both $x_t$ and $y_t$ are non stationary and independent can have high $R^2$ and significant t-stats, even though there is no causal link between the two variables. Regressions where 
- $y_t=\alpha+\beta x_t+u_t$ where $y_t, x_t, u_t \sim I(0)$
- $y_t=\alpha+\beta x_t+u_t$ where $y_t, x_t, u_t \sim I(1)$ 
are meaningful, whereas
- $y_t=\alpha+\beta x_t+u_t$ where $y_t, x_t \sim I(1)$ but $u_t=y_t-\alpha-\beta x_t\sim I(0)$ 
- $y_t=\alpha+\beta x_t+u_t$ where $y_t, x_t \sim I(0)$ but $u_t=y_t-\alpha-\beta x_t\sim I(1)$
are meaningless as the error terms are not white noise. 

### Unit root tests
#### Dickey-Fuller unit root test
In order to correct for the autocorrelations and ensure that $u_t$ is a white noise process, three specifications of regressions are run 
1. $\Delta y_t=\beta y_{t-1}+e_t$ (no constant, no trend)
2. $\Delta y_t=a+\beta y_{t-1}+e_t$ (constant, no trend)
3. $\Delta y_t=a+\beta y_{t-1}+bt+e_t$ (constant, trend)

The null hypothesis is that a unit root is present in the time series. The t statistic is given by $$t=\frac{\hat \beta}{\text{S.E.}(\hat \beta)}$$It is important to note that the test uses the **dickey-fuller** distribution, and not the normal or t distributions. The critical value are given as follows 
![[Pasted image 20240301235337.png]]

the test is one tailed, and the null is rejected if the t stat is less than the DF critical values.

#### Phillips-Perron (PP) Test and DF-GLS in notes

