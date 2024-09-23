instead of strictly using linear relationships, we can also regress to find a linear combination of a fixed set of nonlinear functions on each of the features. These functions are called **basis functions**. We can represent such a model as $$y(X,W)=w_0+\sum_{i=1}^{M-1}w_i\phi_i(X)$$where:
- $M$ is the total number of params
- $W$ is a vector of weights, $w_0$ is the bias
- $X$ is a vector of features, and the basis function can be applied to a combination of these features

We assume that the target variable $t$ is given by the general regression function plus a random component given by a normal distribution. This is similar to the [[Bayesian curve fitting]]. Therefore, $$p(t|X,W,\beta)=N(t|y(X,W), \beta^{-1})$$Therefore, for the entire dataset, the probability becomes, $$p(T|X,W, \beta)=\prod_{n=1}^NN(t_n|W^T\Phi(X_n), \beta^{-1})$$Taking logs, we get the log likelihood$$\log p(T|W,\beta)=\frac N2\log \beta-\frac N2\log(2\pi)-\beta E_D(W)$$where $$E_D(W)=\frac 12\sum_{i=1}^N(t_n-W^T\Phi(X_n))^2$$which is essentially the sum of squares error function. 

#### Maximizing
$$\nabla \log p(T|W,\beta)=\sum_{n=1}^N(t_n-W^T\Phi(X_n))\Phi(X_n)^T$$Setting this derivative to zero and solving for $W$, we get$$W_{ML}=(\Phi^T\Phi)^{-1}\Phi^TT$$the term $(\Phi^T\Phi)^{-1}\Phi^T$ is called the **Moore Penrose Inverse**. 

We also however, need to minimize the error with respect to the bias. The error with bias is $$E_D(W)=\frac 12\sum_{n=1}^N(t_n-w_0-\sum_{i=1}^{M-1}w_i\phi_i(X_n))^2$$ Therefore we differentiate $E_D$ wrt $w_0$, and get $$w_0=\bar t-\sum_{i=1}^{M-1}w_j\bar\phi_j$$where the bar represents the average. The average of the basis function is just the average of the basis function output over all different datapoints. 