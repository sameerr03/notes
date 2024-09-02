#### LSTAR (Logistic Smooth Transition Autoregressive) Model
A type of nonlinear time series model that allows the behavior of the series to change smoothly from one regime to another, based on the value of an observable variable - potentially a lagged term. 

The transition between regimes is smooth - as described by a logistic function which allows the model to shift between [[Structural break models|structural breaks]]. The model can be represented as follows 
$$y_t=a_0+a_1y_{t-1}+\dots+a_py_{t-p}+F(y_{t-1}-\mu)[b_0+b_1y_{t-1}+\dots+b_py_{t-p}]+e_t$$Where:
$$F(y_{t-1}-\mu)=\frac 1{1+\exp[-\gamma(y_{t-1}-\mu)]}$$ This is the logistic function that allows for the smooth transition between regimes. 
![[Pasted image 20240323152122.png|500]]

This function smoothly transitions between the two sets of autoregressive parameters in the model. 

##### Fourier Flexible Series 
Mathematical function used to decompose periodic functions into a sum of sine and cosine functions with different frequencies and amplitudes. It allows for the modelling of complex cyclic patterns in time series analysis. $$y_t=a+by_{t-1}+ex_t+\sum_{K=1}^m[\alpha_K\sin(\frac {2\pi Kt}T)+\beta_K\cos(\frac{2\pi K t}{T})]+u_t$$where:
- $K$ is the number of single frequencies
- $m$ the the number of cumulative frequencies
- alpha and beta are magnitude terms

