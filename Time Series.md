A dataset that tracks a sample over time
### Components of a time series
#### Trend
The trend component describes the long run behavior of the time series. The trend changes the mean of the series over time. Algebraically,$$\text{Trend}_t=\alpha_1+\alpha_2 t$$Where:
- $t$ is the particular year
- $\alpha_1$ is the intercept
- $\alpha_2$ slope 

#### Seasonality
Captures regular periodic movements in the series. This component could be either deterministic (Has a fixed probabilistic value) or stochastic (probability changes over time). This component is represented through the Fourier equations.$$S_t=\beta_1\sin(\frac{2\pi kt}{T})$$Where:
- $\beta_1$ implies how smooth the data is - the higher the number, the smoother the seasonality component
- $k$ is the frequency of the cyclic component
- $t$ is the time
- $T$ is the number of observations

#### Noise/Irregular component
A stochastic process that is present in a time series, that cannot be described by trend, cycle movement, and seasonal variation. The component can be described using the equation of motion driving the stochastic process. $$I_t=\gamma_1+\gamma_2I_{t-1}+\epsilon_t$$Where:
- $I_{t-1}$ is a lagged value of the series.'
- $\epsilon_t$ is a pure random disturbance at time $t$
- $\gamma_2$ is the lag value coefficient. It determines that the current irregular disturbance in this period is $\gamma_2\times100$% of the last periods irregular disturbance plus the random disturbance term. 

### Forming a difference equation
Putting all the components of the timeseries together,
$$y_t=\alpha_1+\alpha_2t+\beta_1\sin(\frac{2\pi kt}{T})+\gamma_1+\gamma_2y_{t-1}+\epsilon_t$$
Where:
- $\alpha_1+\alpha_2t$ is the trend component
- $\beta_1\sin(\frac{2\pi kt}{T})$ is the cyclic component
- $\gamma_1+\gamma_2y_{t-1}+\epsilon_t$ is the irregular component

