An unexpected change over time in the parameters of regression of a [[Time Series]] model is a structural break. These structural breaks can be modelled using the following methods.

#### [[Dummy variables]] for structural breaks
There are three types of dummy variables to approximate structural breaks. 

##### One-Point Dummy
If the structural break is likely to have a jump in the dependent variable in only one period, after which the system returns to the original setup, a dummy variable with the value 1 in the period of the structural break and 0 otherwise can be used. 
![[Pasted image 20240323140101.png|500]]
$$D_t=\begin{cases}1 & \text{ if }t=T \\ 0& \text{ if $t\ne T$}\end{cases}$$
where $T$ is the period where the structural break occurs. If the model without structural change is $$y_t=a_0+a_1x_t+e_t$$then with the structural change, $$y_t=a_0+a_1x_t+\delta D_t+e_t$$
##### Level shift/Crash Dummy
A dummy variable that is used to represent a permanent change in the level of a time series, often due to a structural break. This change can be either an increase or a decrease in the level. The dummy variable takes the value$$D_t=\begin{cases}0 & \text{ if }t<T \\ 1& \text{ if $t\ge T$}\end{cases}$$where $T$ is the time at which the level shift occurs. The time series model will be given by$$y_t=a_0+a_1x_t+\delta D_t+e_t$$ ![[Pasted image 20240323141301.png|500]]

##### Broken-Trend Dummy
A broken trend dummy is used to model a situation where there is a structural break in the trend of the data, not just a level shift. 
![[Pasted image 20240323144232.png|500]]
The dummy variable takes the values $$D_t=\begin{cases}0 & \text{ if }t<T \\ 1& \text{ if $t\ge T$}\end{cases}$$The regression equation becomes$$y_t=a_o+a_1x_t+\delta(t-T)D_t+e_t$$This changes the trend of the equation after $T$. 

**Multiple dummies can be used for the same series using a dummy vector.** A drawback is that we assume that the break dates are known beforehand. 

#### Bai-Perron Test
A method used to identify multiple structural breaks in a time series - points where patterns of the time series changes. The time series is modeled as $$y_t=a_1x_{1t}+a_2x_{2t}+\dots+a_kx_{kt}+e_t$$The test identifies points where the coefficients $a_{it}$ change significantly, implying structural breaks. In applying the Bai-Perron test, one typically starts with the null hypothesis of no breaks and then tests against the alternative hypothesis of one or more breaks. The test iteratively evaluates the possibility of increasing numbers of breaks until the best number of breaks is identified, based on statistical criteria like the likelihood ratio test, minimizing the sum of squared residuals, or using information criteria (e.g., Bayesian Information Criterion - [[Box-Jenkins Method#Schwartz Bayesian Information Criteria (SBC)|BIC]]).

It is important to note that the BP procedure can only be applied to processes that are $I(0)$ (see [[non-stationary series]]). BP also fails to identify temporary breaks. 

