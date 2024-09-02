
Consist of two [[random variables]] distributed togetther.

The joint probability is $p(x_i,y_i)$

The probablility of RV X taking the value of $x_i$ is given by 
$$P\{X=x_i\}=\sum_jP\{X=x_i,Y=y_j\}$$
As we are taking pairs, we can get $x_i$ with any $y_j$. Therefore the probability that we get $x_i$ is summed for all possible pairs it can have with any $y_j$. The PMF of Y is similar.

The distribution is read by :
![[Pasted image 20221114165502.png|400]]
### Expected value

The expected value of a jointly distributed random variable is given by $$E(g(x,y))=\sum_x\ \sum_y\ g(x,y)\cdot f(x,y)$$Where 
- $g(x,y)$ is the values taken by the RV
- $f(x,y)$ is the probability at that value

### [[moments]]

The moments around the origin for a jointly distributed RV is given by $$\mu'_{rs}=E(X^r\ Y^s)=\sum_x\ \sum_y\ x^ry^s\cdot f(x,y)$$
The moment arounf the mean is given by
$$\mu_{rs}=E[(X-\mu_x)^r\ (Y-\mu_y)^s]=\sum_x\ \sum_y\ (x-\mu_X)^r\ (y-\mu_Y)^s\cdot f(x,y)$$
#### Covariance
A measure of the dispersion of X and Y values. When X values are far away from the mean, how far away are Y values. 

The first moment around the mean (r=s=1) gives the **covariance** of the jointly distributed rv ($\sigma_{xy}$)$$\sigma_{xy}=\sum_x\ \sum_y\ (x-\mu_X)(y-\mu_Y)\cdot f(x,y)=\sigma_{yx}$$
##### Properties
- $\sigma_{xx}=\sigma^2_x$
- $\sigma_{x,y+c}=\sigma_{xy}$
- $\sigma_{x,cy}=c\ \sigma_{xy}$
- $var(aX+bY)=a^2var(X)+b^2var(Y)+ab\ cov(X,Y)$

##### Covariance theorem
$$\sigma_{xy}=E[(x-\mu_X)(y-\mu_Y)]=E(XY)-E(X)E(Y)$$



### Independance of jointly distributed random variables

RVs X and Y are independant if for any $A,B \in \mathbb{R}$
$$P(X\in A,Y\in B)=P[x\in A]\cdot P[y\in B]$$or
$$F(A,B)=F_X(A)\cdot  F_Y(B),\ E(A,B)=E_X(A)\cdot E_Y(B)$$

### Conditional distributions

The distribution of X given Y is given by$$V(X|Y)=\frac{f(x,y)}{P_y(y)}$$
$$var(Y|X)=E(Y^2|X)-(E(Y|X))^2$$
Where $P_Y(y)$ is the marginal distributon of Y at y.


