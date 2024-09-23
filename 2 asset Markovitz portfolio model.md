Assume that there are two risky [[Financial Assets]], $A$ and $B$. They both form a risky portfolio $P$ with these assets purchased with the respective weights $w_A, w_B$. The information about the assets is given as follows:

| Asset | Return | Mean | Variance |
| ---- | ---- | ---- | ---- |
| $A$ | $r_A$ | $\mathbb E(r_A)=\mu_A$ | $\sigma_A^2$ |
| $B$ | $r_B$ | $\mathbb E(r_B)=\mu_B$ | $\sigma_B^2$ |
Where 
$\text{Corr}(r_A,r_B)=\rho$
$\text{Cov}(r_A,r_B)=\rho \sigma_A\sigma_B$
$A$ is more risky than $B$ => $\mu_A>\mu_B$ and $\sigma_A>\sigma_B$
Assume normal  [[Jointly distributed random variables|joint distribution]] of returns:$$\begin{pmatrix} r_A\\ r_B\end{pmatrix}\sim N(\begin{pmatrix}\begin{pmatrix} \mu_A\\\mu_B \end{pmatrix}\begin{pmatrix}\sigma_A^2&\rho\sigma_A\sigma_B\\\rho\sigma_A\sigma_B&\sigma^2_B\end{pmatrix}\end{pmatrix}$$on the return risk graph, the two assets are given by ![[Pasted image 20240203193901.png|400]]


#### Expected return of risky portfolio
The [[Return of a portfolio|return of a risky portfolio]] holding the two assets in the weight is given by $$r_p=w_Ar_A+w_Br_B$$but we know that $w_A+w_B=1$. Therefore, $$r_p=w_Ar_A+(1-w_A)r_B$$Taking expectations, $$\mathbb E(r_p)=\mathbb E(r_B)+w_A[\mathbb E(r_A)-\mathbb E(r_B)]$$Similarly, in terms of $w_B$,$$\mathbb E(r_p)=w_B\mathbb E(r_B)+(1-w_B)\mathbb E(r_A)$$$$\mathbb E(r_p)=\mathbb E(r_A)-w_B[\mathbb E(r_A)-\mathbb E(r_B)]$$as $\mu_A>\mu_B$. 

The weights can be negative. If $w_B$ is negative, it implies that the asset $B$ has been short sold and the money from selling it has been used to buy asset $A$. Plotting the expected return of the risky portfolio against the weight of asset $A$ and $B$ in the portfolio, we get
![[Pasted image 20240203194519.png|400]]
#### Variance of risky portfolio
The variance of the risky portfolio is given by $$\text{Var}(r_p)=\text{Var}(w_Ar_A+w_Br_B)$$$$=w_A^2\sigma_A^2+w_B^2\sigma_B^2+2w_Aw_B(\rho\sigma_A\sigma_B)$$$$=w_A^2\sigma_A^2+(1-w_A)^2\sigma_B^2+2w_A(1-w_A)(\rho\sigma_A\sigma_B)\tag {1}$$If the correlation of the returns of the two assets ,$\rho=1$ then,
$$\text{Var}(r_p)=w_A^2\sigma_A^2+(1-w_A)^2\sigma_B^2+2w_A(1-w_A)\sigma_A\sigma_B$$$$=[w_A\sigma_A+(1-w_A)\sigma_B]^2$$$$=[\sigma_B+w_A(\sigma_A-\sigma_B)]^2$$Therefore the standard deviation is $$\sqrt{\text{Var}(r_p)}=\sigma_B+w_A(\sigma_A-\sigma_B)$$Plotting the standard deviation of the portfolio with respect to $w_A$,
![[Pasted image 20240203195743.png|400]]
If the correlation of the returns of the two assets $\rho=-1$, then from (1)$$\text{Var}(r_p)=w_A^2\sigma_A^2+(1-w_A)^2\sigma_B^2-2w_A(1-w_A)\sigma_A\sigma_B$$However, depending on the values of $w_A$, we might get negative standard deviations, which is not possible $(\sigma_A>\sigma_B)$. Therefore, there are two cases. If the value of $w_A$ is sufficiently small, $$\text{Var}(r_p)=((1-w_A)\sigma_B-w_A\sigma_A)^2\tag2$$If the value of $w_A$ is sufficiently large, $$\text{Var}(r_p)=(w_A\sigma_A-(1-w_A)\sigma_B)^2\tag 3$$There are these two cases as $(a-b)^2=(b-a)^2$

Based on these equations, we can find the threshold value of $w_A$ -> there must be a point where the s.d. becomes zero if we were to use only one out of (2) or (3). $$0=(1-w_A)\sigma_B-w_A\sigma_A\implies w_A(\sigma_A+\sigma_B)=\sigma_B\implies w_A=\frac{\sigma_B}{\sigma_A+\sigma_B}$$Therefore, when $w_A=\frac{\sigma_B}{\sigma_A+\sigma_B}$, $\text{StDev}(r_p)=0$. So that the standard deviation remains positive, when $w_A<\frac{\sigma_B}{\sigma_A+\sigma_B}$, then $$\text{StDev}(r_p)=(1-w_A)\sigma_B-w_A\sigma_A=\sigma_B+w_A(\sigma_B-\sigma_A)$$ and when $w_A>\frac{\sigma_B}{\sigma_A+\sigma_B}$ then, $$\text{StDev}(r_p)=w_A\sigma_A-(1-w_A)\sigma_B=-\sigma_B+w_A(\sigma_B+\sigma_A)$$Plotting this function for standard deviation against $w_A$, we get 
![[Pasted image 20240203201858.png|400]]


**typically**, correlations are not 1 or -1, but somewhere in between making the graph a curved form of what we see in the -1 correlation case. 

#### Portfolio allocation
By varying the value of $w_A$ we can find the standard deviation and risk of the candidate portfolio from the derived equations
![[Pasted image 20240203202237.png|400]]
This gives us a curve that shows all possible combinations of the two assets in the candidate portfolio.
##### Minimum variance portfolio allocation
The portfolio obtained by taking the combination of assets that results in the lowest possible risky portfolio variance. This is obtained by selecting the weights after minimizing the portfolio variance. From (1) we know that the variance is$$\text{Var}(r_p)=w_A^2\sigma_A^2+(1-w_A)^2\sigma_B^2+2w_A(1-w_A)(\rho\sigma_A\sigma_B)$$The minimum variance portfolio is obtained by $$\min_{w_A}\text{Var}(r_p)\implies 2w_A\sigma_A^2-2(1-w_A)\sigma_B^2+2\rho\sigma_A\sigma_B-4w_A\rho\sigma_A\sigma_B=0$$$$2w_A\sigma_A^2-2\sigma_B^2+2w_A\sigma_B^2+2\rho\sigma_A\sigma_B-4w_A\rho\sigma_A\sigma_B=0$$$$2w_A(\sigma_A^2+\sigma_B^2-2\rho\sigma_A\sigma_B)-2\sigma_B^2+2\rho\sigma_A\sigma_B=0$$$$w_A=\frac{\sigma_B^2-\rho\sigma_A\sigma_B}{\sigma_A^2+\sigma_B^2-2\rho\sigma_A\sigma_B}$$$$w_B=1-w_A$$
##### Optimal portfolio allocation
 In order to find the optimal portfolio, the slope of a point in the curve to the risk free asset $(0,r_f)$ is taken. Just as in the case of the [[Capital allocation line]], this gives us the [[Sharpe and Sortino Ratio|sharpe]] ratio of the candidate portfolio at that point. The point where this $p$-$r_F$ line is tangential to the risk return curve is the highest sharpe ratio attainable, which is the optimal risky portfolio $\hat r_P$ according to the sharpe ratio.   
![[Pasted image 20240203202858.png|400]]

Alternatively, the [[Investor preferences]] can be optimized instead to find portfolio allocation. We know that the expected return of the risky portfolio of two risky assets is given by $$\mathbb E(r_p)=w_A\mu_A+(1-w_A)\mu_B$$And from equation (1) we know the variance. Putting these terms into the utility function for investor preferences, $$U(\mathbb E(r_p),\sigma_p^2)=w_A\mu_A+(1-w_A)\mu_B-\frac 12A(w_A^2\sigma_A^2+(1-w_A)^2\sigma_B^2+2w_A(1-w_A)(\rho\sigma_A\sigma_B))$$To optimize investor preferences, we maximize utility. $$\max_{w_A}U\implies\mu_A-\mu_B-Aw_A\sigma_A^2+A(1-w_A)\sigma_B^2-A\rho\sigma_A\sigma_B+2Aw_A\rho\sigma_A\sigma_B=0$$$$\mu_A-\mu_B-Aw_A\sigma_A^2+A\sigma_B^2-Aw_A\sigma_B^2-A\rho\sigma_A\sigma_B+2Aw_A\rho\sigma_A\sigma_B=0$$$$Aw_A(\sigma_A^2+\sigma_B^2-2\rho\sigma_A\sigma_B)=\mu_A-\mu_B+A(\sigma_B^2-\rho\sigma_A\sigma_B)$$$$w_A=\frac{\mathbb E(r_A)-\mathbb E(r_B)+A(\sigma_B^2-\rho\sigma_A\sigma_B)}{A(\sigma_A^2+\sigma_B^2-2\rho\sigma_A\sigma_B)}$$$$w_B=1-w_A$$This is the optimal allocation according to investor preferences. 