A type of machine learning method use to make a prediction about a categorical variable, but it does so by predicting the probability of a certain event occurring, which is translated into a prediction. 

#### Formulation
We collect the **independent** (assumption) input features into the feature matrix $X$$$X=\begin{bmatrix}x_{11}&\dots&x_{1m}\\x_{21}&\dots&x_{2m}\\\vdots&\ddots&\vdots\\x_{n1}&\dots&x_{nm}\end{bmatrix}$$
The dependent variable $Y$ has a binary value of either 0 (Class 1) or 1 (Class 2). 

#### Regression model
We initially place the features into a linear regression, of the form $$z=WX+b$$where $W$ is a vector of weights, $X$ is the matrix of features and $b$ is the bias (can be thought of as the coefficient)

The value of the function $z$ is passed into the [[Sigmoid Function]](Logit function), which gives us a value bounded between 0 and 1. This is a representation of the probability of each class in $Y$$$p(y=1)=\sigma(z)$$$$p(y=0)=1-\sigma(z)$$
#### Derivation
We use **log odds** (log ratio of probability for to probability against) for this derivation. We can define the odds as $$\frac{p(x)}{1-p(x)}=e^z$$We do this so that we can use log transformations to convert multiplicative probability into linear relations. Applying logs, $$\log[\frac{p(x)}{1-p(x)}]=z=WX+b\tag 1$$Reapplying exponents, $$\frac{p(x)}{1-p(x)}=\exp(WX+b)$$$$p(x)=\exp(WX+b)(1-p(x))=\exp(WX+b)-\exp(WX+b)p(x)$$$$p(x)+\exp(WX+b)p(x)=\exp(WX+b)$$$$p(x)(1+\exp(WX+b)=\exp(WX+b)$$Therefore, $$p(x)=\frac{\exp(WX+b)}{1+\exp(WX+b)}=\frac 1{1+\exp[-(WX+b)]}$$This gives us the sigmoid function, that we can represent as $$p(x)=\sigma(WX+b)$$
#### Log likelihood
The purpose of the likelihood function is to give us the joint probability of observing the data given the parameters (weights $W$ and bias $b$). For the outcomes for a particular datapoint, 
- When $y_i=1$, the likelihood is $p(x_i)$
- When $y_i=0$, the likelihood is $1-p(x_i)$

Therefore (Assuming all samples are independent), the likelihood function is $$L(b,W)=\prod_{i=1}^np(x_i)^{y_i}(1-p(x_i))^{1-y_i}$$This is the expression as if $y_i=1$, we only use $p(x_i)$ and vice versa. This gives us the probability of observing the data given the model parameters. Taking logs on both sides, $$\log L(b,W)=\sum_{i=1}^n[y_i\log p(x_i)+(1-y_i)\log(1-p(x_i))]$$$$=\sum_{i=1}^n[y_i\log p(x_i)+\log(1-p(x_i))-y_i\log(1-p(x_i))]$$$$=\sum_{i=1}^n\log(1-p(x_i))+\sum_{i=1}^ny_i\log\frac{p(x_i)}{1-p(x_i)}$$From (1) we know what the log odds are, $$\log L(b,W)=\sum_{i=1}^n\log(1-p(x_i))+\sum_{i=1}^ny_i(WX+b)$$
###### Maximization
To maximize log likelihood, we need to differentiate with respect to $W$, $$\frac{\partial 
(L(b,W))}{\partial w_j}=-\sum_{i=1}^n\frac{1}{1+\exp(WX_i+b)}\exp(WX+b)x_{ij}+\sum_{i=1}^ny_ix_{ij}$$$$=-\sum_{i=1}^np(x_i)x_{ij}+\sum_{i=1}^ny_ix_{ij}$$$$\frac{\partial\log L(b,W)}{\partial w_j}=\sum_{i=1}^n(y_i-p(x_i))x_{ij}$$
#### Difference with linear regression
![[Pasted image 20240918000620.png]]
