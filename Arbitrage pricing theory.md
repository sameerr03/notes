If [[Financial Assets|asset]] returns can be described by using an appropriate [[Factor model]], then in well functioning markets, it is possible to diversify away all the idiosyncratic risk in a portfolio. 

A diversified portfolio that is not affected by idiosyncratic risk is a well diversified portfolio. It is always possible to find a sufficient number of assets to create such a portfolio in a well functioning market. It is important to note that there can be multiple such diversified portfolios. 

Consider $n$ assets such that 
$R_1=\mathbb E(R_1)+\tilde\beta_1F+e_1$
$\vdots$
$R_n=\mathbb E(R_n)+\tilde\beta_n F+e_n$

With a portfolio of equal weights 
$$R_p=\frac 1n\sum_{i=1}^n R_i=\frac 1n\sum_{i=1}^n\mathbb E(R_i)+\frac{\sum_{i=1}^n\tilde\beta_i}{n}F+\frac{\sum_{i=1}^ne_i}{n}$$The overall risk on this portfolio is given by $$\text{Var}(r_p)=\text{Var}(R_p)=(\frac{\sum\tilde\beta_i}{n})^2\sigma^2_F+\frac 1n\sum_{i=1}^n\sum_{j=1}^n\text{Cov}(e_i,e_j)$$In a well diversified portfolio, the term $\frac 1n\sum_{i=1}^n\sum_{j=1}^n\text{Cov}(e_i,e_j)=0$

Suppose the portfolio $p$ is a well diversified portfolio of $n$ assets and $$R_p=\mathbb E(R_p)+\tilde\beta_pF+e_p$$However, by definition, this portfolio does not contain any idiosyncratic risk. Therefore $$R_p=\mathbb E(R_p)+\tilde\beta_pF$$
#### Returns of two different diversified portfolios
Consider two different well diversified portfolios, $R_p, R_q$. The covariance of the returns of these portfolios is given as $$\text{Cov}(R_p,R_q)=\text{Cov}(\mathbb E(R_p),\mathbb E(R_q))+\tilde\beta_p\text{Cov}(\mathbb E(R_p),F)+\tilde\beta_q\text{Cov}(\mathbb E(R_q),F)+\tilde\beta_p\tilde\beta_q\text{Cov}(F,F)$$$$=\tilde\beta_p\tilde\beta_q\sigma_F^2$$We know that the variance of $r_p$ is given by $$\text{Var}(R_p)=(\frac{\sum\tilde\beta_i}{n})^2\sigma^2_F=\tilde\beta_p^2\sigma_F^2$$$$\sigma_{R_p}=\tilde\beta_p\sigma_F$$similarly,$$\sigma_{R_q}=\tilde\beta_q\sigma_F$$Therefore, finding the correlation, $$\rho_{R_p,R_q}=\frac{\text{Cov}(R_p,R_q)}{\sigma_{R_p}\sigma_{R_q}}=1$$Therefore, the returns of two well diversified portfolios have a correlation of 1. This implies that the returns of one can be expressed as a linear relationship of the other $$R_p=a+bR_q$$
#### Deriving the APT Equation
The systemic risk in the returns of the portfolio are not directly observable. Instead, we use a proxy for this. The proxy that can be used for systemic risk is the risk premium of the market $(R_M)$. Therefore, the APT equation becomes $$R_p=\alpha_p+\beta_pR_M$$The excess return not described by the fluctuations of the portfolio is given by $$\alpha_p=\mathbb E(R_p)-\beta_p\mathbb E(R_M)$$Rearranging, $$\mathbb E(R_p)=\alpha_p+\mathbb E(R_M)$$In equilibrium, there should be no arbitrage opportunity, as all the $\alpha$ should be arbitraged away, changing the price of the portfolio and making its alpha = 0. Therefore, $$\mathbb E(R_p)=\beta_p\mathbb E(R_M)$$$$\mathbb E(r_p)-r_f=\beta_p[\mathbb E(r_m)-r_f]$$which is the APT equation. This equation is identical to the [[Capital Asset Pricing Model (CAPM)]] equation. However, it is important to note that CAPM is for individual assets, while APT applies only to well diversified portfolios.

##### Executing arbitrage 
We know that $$\mathbb E(R_p)=\alpha_p+\beta_p\mathbb E(R_M)\tag 1$$$$\mathbb E(R_M)=\alpha_M+\beta_M\mathbb E(R_M)\tag 2$$where $\alpha_M=0$ and $\beta_M=1$

**The combination of two well diversified portfolios is a well diversified portfolio**. Therefore, if empirically $\alpha_p>0$, there is an arbitrage opportunity by creating a new portfolio by combining $M$ and $p$

Since both these portfolios have only systemic risk, they can be combined in a manner that eliminates all systemic risk. Consider this the zero beta portfolio $z$. By selecting weights $w_p$ and $w_M=1-w_p$, for the zero beta portfolio, $$\beta_z=w_p\beta_p+(1-w_p)\beta_M=0$$However we know that $\beta_M=1$. Therefore, $$0=w_p\beta_p+(1-w_p)$$$$w_p=\frac 1{1-\beta_p}$$$$1-w_p=w_M=\frac{-\beta_p}{1-\beta_p}$$The new portfolio is short on the market portfolio, while being long on the portfolio $p$. The return of this portfolio is given by $$R_z=w_pR_p+(1-w_p)R_M$$
$$\alpha_z+\beta_zR_M=w_p\alpha_p+\beta_pw_pR_M+(1-w_p)R_M$$We know that $\beta_z=0$
$$\alpha_z=w_p\alpha_p+\frac{\beta_p}{1-\beta_p}R_M+(\frac{-\beta_p}{1-\beta_p})R_M$$$$\alpha_z=w_p\alpha_p=\frac{1}{1-\beta_p}\alpha_p$$

#### Differences between APT and CAPM
| CAPM                                                                       | APT                                                                                                                                                       |
| -------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Needs the hypothetical market portfolio                                    | Not necessary to have the market portfolio, any portfolio whose constituents are stocks in a broad based index would do (provided it is well diversified) |
| Assumes Mean variance optimized portfolios by every investor in the market | No such claim, stands on the more realistic assumption of exploitation of arbitrage opportunities                                                         |
| Applies to both assets and portfolios                                      | Applies only to well diversified portfolios                                                                                                               |

#### Drawbacks of APT
- Systematic and non-systematic risk may not be [[Factor model#Assumptions|uncorrelated]]
- Non-Systematic risk across firms might not be uncorrelated
- Creation of a well diversified portfolio is practically difficult

#### APT with Multi-Factor Models
Using a multi [[Factor model#Multiple factors|factor]] models to describe asset returns, the returns on an asset is given by $$R_i=\mathbb E(R_i)_+\tilde\beta_{i1}F_1+\tilde\beta_{i2}F_2+e_i$$For many such assets, the well diversified portfolio that can be created is $$R_p=\mathbb E(R_p)+\tilde \beta_pF_1+\tilde\beta_p F_2$$Under the assumptions that the the covariances of $F_1$ and $F_2$, idiosyncratic factors and systemic factors and idiosyncratic factors between assets =0. 

It is not possible to directly observe the effects of $F_1$ and $F_2$ on the returns of a portfolio. Therefore proxies called **factor tracking portfolios** are used. These are specially made portfolios that bear a high correlation with the factor in question. It is important to note that the correlation between the returns of these factor tracking portfolios $R_{F1}$ and $R_{F2}$ are uncorrelated.

Using this, we can obtain the APT equation$$\mathbb E(R_p)=\alpha+\beta_{F1}R_{F1}+\beta_{F2}R_{F2}$$In equilibrium, there is no arbitrage opportunity and $\alpha=0$. Therefore
$$\mathbb E(R_p)=\beta_{F1}R_{F1}+\beta_{F2}R_{F2}$$
##### Example
![[Pasted image 20240322195439.png]]
![[Pasted image 20240322195459.png]]![[Pasted image 20240322195523.png]]
