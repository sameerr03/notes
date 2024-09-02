Extension of the [[2 asset Markovitz portfolio model]], with $n$ [[Financial Assets]]. In order to find the optimal portfolio, we need a matrix vector of the expected return of each of the assets, as well as a [[Covariance matrix]] for the assets
$$E=\begin{bmatrix}\mathbb E(r_1)\\\mathbb E(r_2)\\\vdots\\\mathbb E(r_n)\end{bmatrix}_{n\times1}$$$$C=\begin{bmatrix}\text{Var}(r_1)&\text{Cov}(r_1,r_2)&\dots&\text{Cov}(r_1,r_n)\\\text{Cov}(r_1,r_2)&\text{Var}(r_2)&\dots& \text{Cov}(r_2,r_n)\\\vdots&\vdots&\ddots&\vdots\\\text{Cov}(r_1,r_n)&\text{Cov}(r_2,r_n)&\dots&\text{Var}(r_n)\end{bmatrix}_{n\times n}$$
To find the weights for each asset, we use the weight matrix$$W=\begin{bmatrix}w_1&w_2&\dots&w_n\end{bmatrix}_{1\times n}$$
We need to maximize the [[Sharpe and Sortino Ratio|Sharpe ratio]], represented by $$\max_W\frac{\mathbb E(r_p)-r_f}{\sqrt{\text{Var}(r_p)}}$$Where $$\mathbb E(r_p)=E\times W$$which gives us a scalar. Similarly, $$\text{Var}(r_p)=W^T\times C\times W$$which is another scalar. 

### Finding the efficient frontier
Finding the efficient frontier is very computationally intensive for many assets. Therefore in order to estimate it, **monte carlo** simulations can be used. The process is as follows
1. Input $E$ and $C$ matrices
2. Generate a large number of weight vectors $W$ - higher number is better but more computationally intensive
3. Calculate the sharpe ratio for each weight vector based candidate portfolio
4. Find the vectors of weights for which the sharpe ratio is maximized

Each candidate is represented as a single point on the $r_p-\sigma_p$ graph. 
![[Pasted image 20240210030008.png|400]]
All candidate portfolios to the right of the frontier will not be employed by a rational investor as they offer the same expected return, but with higher standard deviation and therefore risk. Therefore only portfolios on the minimum variance frontier should be considered.

However, all points below the [[2 asset Markovitz portfolio model#Minimum variance portfolio allocation|minimum variance portfolio]] on the frontier should not be considered as well. This is because there will be another candidate portfolio above the minimum variance portfolio on the frontier that offers higher expected return for the same level of risk. 
![[Pasted image 20240210030840.png|400]]
Therefore the part of the minimum variance frontier above the minimum variance portfolio (including the minimum variance portfolio) is the set of all portfolios that maximize sharpe ratio for a given level of risk. This is the **efficient frontier**. 
### Optimal portfolios
##### Optimal risky portfolio
The optimal portfolio based on the markovitz model is the point on the efficient frontier than maximizes the sharpe ratio. Graphically, this is represented by 
![[Pasted image 20240214204916.png|400]]

However, this portfolio does not necessarily maximize the [[Investor preferences]].

##### Complete Portfolio
The complete portfolio can be found by taking weights between the optimal risky portfolio and the risk free asset, through the [[Capital allocation line]]. A point on the CAL can be selected based upon the maximization of the investors utility function with respect to the constraints of the CAL. This will give us the complete portfolio ($C$) that accounts for the investors preferences.

#### Drawbacks
- The markovitz model only takes past information into account, as a result has short term predictions
- Assumes normal returns, which is not the case for financial returns which are prone to extreme tail events
- Assigns too much weights to very risky stocks
- Cannot input subjective expectations about the future of the assets
- Very sensitive to inputs - Expectations and covariance matrix

