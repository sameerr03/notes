
#### Assumptions
Assumes that every investor is rational. This means that every investor is a mean variance portfolio optimizer ([[n Asset markovitz portfolio]] optimization). All investors have the same set of inputs and homogenous expectations about the future. 

Based on this assumption, we can assume that every investor will come to the same conclusion about the asset and will place the same weight of their portfolio in that asset. If the total portfolio amount for the investor $n$ is $p_n$, then the [[Ratio analysis#Market Value Ratios|market cap]] of asset $A_n$ divided by the total market cap of all assets is given by $$\frac{\text{Market Cap of }A_n}{\text{Total Market Cap}}=\frac{w_np_1+w_np_2+w_np_3+\dots}{p_1+p_2+p_3+\dots}=w_n$$
where $w_n$ is the weight that each investor holds asset $A_n$ in their portfolio. This is because all investors make the same decision. Continuing this logic, the **market portfolio** is a portfolio of all listed assets where the weights on a particular asset is given by $$w_n=\frac{\text{Market Cap of }A_n}{\text{Total Market Cap}}$$
The market portfolio is therefore the optimal portfolio. A "passive" investor could theoretically invest in the market portfolio and obtain the optimal portfolio without exerting any additional effort - this is more efficient than actively finding the optimal portfolio. 

#### Contribution of asset $k$ to risk and return
We denote the market portfolio by $M$. $M$ contains all the assets in the market $A_1,A_2,A_3,\dots,A_n$ which is held in the weight $w_1,w_2,w_3,\dots,w_n$. The return of the market portfolio is given by the weighted average of the returns on the individual assets
$$r_M=w_1r_1+w_2r_2+w_3r_3+\dots+w_nr_n\tag 1$$$$=\sum w_nr_n$$The expected return is given by $$\mathbb E(r_M)=\sum_{i=1}^nw_i\mathbb E(r_i)$$ The variance is given by $$\text{Var}(r_M)=\sum_{i=1}^n\sum_{j=1}^nw_iw_j\text{Cov}(r_i,r_j)$$
Compared to a risk free asset, the excess return is given by
$$R_M=r_M-r_F$$Therefore the risk premium is given by $$\mathbb E(r_M)-r_f=\mathbb E(r_m-r_f)=\mathbb E(R_M)$$Substituting with (1),$$\mathbb E(R_M)=\mathbb E(w_1r_1+w_2r_2+\dots+w_kr_k+\dots+w_nr_n-(w_1+w_2+w_3+\dots+w_n)r_f)$$Therefore, $$\mathbb E(R_M)=w_1\mathbb E(R_1)+w_2\mathbb E(R_2)+\dots+w_k\mathbb E(R_k)+\dots+w_n\mathbb E(r_n)$$Therefore the contribution of the $k$th asset to the risk premium of the market portfolio is $w_k\mathbb E(R_k)$. The contribution of the $k$th asset to the risk of the market portfolio is given by $$w_k[\sum_{i=1}^nw_i\text{Cov}(r_i,r_k)]=w_k[\sum_{i=1}^n\text{Cov}(w_ir_i,r_k)]=w_k\text{Cov}(r_M,r_k)$$Taking differences from both terms, the covariance will not change. Therefore$$w_k\text{Cov}(r_M-r_f,r_k-r_f)=w_k\text{Cov}(R_M,R_k)$$which is the contribution of $k$th asset to the risk. 
#### Deriving the CAPM equation
We use the ratio$$\frac{\text{Contribution of an asset to the risk premium of }M}{\text{Contruibution of an asset to the variance of }M}$$For the asset $k$,$$\frac{w_k\mathbb E(R_k)}{w_k\text{Cov}(R_M,R_k)}=\frac{\mathbb E(R_k)}{\mathrm{Cov}(R_M,R_k)}$$At equilibrium, it must be that $$\frac{\mathbb E(R_1)}{\mathrm{Cov}(R_M,R_1)}=\frac{\mathbb E(R_2)}{\mathrm{Cov}(R_M,R_2)}=\dots=\frac{\mathbb E(R_n)}{\mathrm{Cov}(R_M,R_n)}$$This is because if any asset offered a better ratio, more investors would invest in it, raising the price, therefore lowering the expected return of the asset, bringing the ratio back down. By addendum rule,$$\frac{w_1\mathbb E(R_1)+w_2\mathbb E(R_2)+\dots}{\text{Cov}(R_M,w_1R_1)+\text{Cov}(R_M,w_2R_2)+\dots}=\frac{\mathbb E(R_k)}{\text{Cov}(R_M,R_k)}$$
Therefore based on this equilibrium, for any asset $k$,$$\frac{\mathbb E(R_k)}{\text{Cov}(R_M,R_k)}=\frac{\mathbb E (R_M)}{\sigma^2_M}$$$$\implies\mathbb E(R_k)=\frac{\text{Cov}(R_k,R_M)}{\sigma_M^2}\mathbb E(R_M)$$$$\implies\mathbb E(r_k)-r_f=\beta_k[\mathbb E(r_M)-r_f]$$$$\mathbb E(r_k)=r_f+\beta_k[\mathbb E(r_M)-r_f]$$This is the basic **CAPM equation**
Where:
- $\mathbb E(r_k)$ is the expected return on $k$
- $\beta_k$ is the beta measure of risk (same as [[Simple Linear Regression|OLS]] estimator between market and asset returns): $\text{Cov}(R_k,R_M)/\sigma_M^2$
- $E(r_M-r_f)$ is the risk premium of the market portfolio

Plotting the CAPM line, 
![[Pasted image 20240216163746.png|400]]
The security market line (SML) represents the theoretical returns of the asset based upon the CAPM model for its level of beta. If an asset has returns differing from the SML for the same level of beta, the asset is not efficiently priced in the market. $$\alpha=\text{Observed average return}-\text{Theoretical return}$$A positive $\alpha$ means the stock is underpriced and is giving excess returns. A negative $\alpha$ means that the stock is overpriced and is giving worse returns for its level of beta risk. If the asset is above the SML, it will have a positive $\alpha$ and the system will move towards a higher equilibrium price in the future => likelihood of capital gains. If the asset is below the SML, it will have a negative $\alpha$ and the system will move towards a lower equilibrium price in the future => likelihood of loss. 

#### CAPM for a portfolio
Suppose an investor holds a portfolio different from the market portfolio, with the weights $\tilde w_n$ for asset $n$. Multiplying the CAPM equation for each asset and adding, the overall CAPM for the portfolio becomes$$\sum_{i=1}^n\tilde w_i\mathbb E(r_i)=r_f+(\sum_{i=1}^n\tilde w_i\beta_i)[\mathbb E(r_M)-r_f]$$
#### Estimating $\beta$
There are two methods to estimating the beta of an asset. The fist is by using the standard OLS estimator and running the regression $$\hat \beta_i=\frac{\text{Cov}(R_i,R_M)}{\text{Var}(R_M)}=\frac{\text{Cov}(r_i,r_M)}{\text{Var}(r_M)}$$The second method is to use the risk premiums as the terms of the regression $$(r_i-r_f)=a+b(r_M-r_f)+\epsilon$$therefore $$b=\frac{\text{Cov}(R_i,R_M)}{\text{Var}(R_M)}=\beta_i$$
#### CAPM as a pricing model
To price an asset, we use the expected payoff $\bar Q$ to estimate the price where $$r_k=\frac{\bar Q-P}{P}$$where $P$ is the price of the asset. Therefore by substituting in the CAPM equation, the price becomes$$P=\frac{\bar Q}{1+r_f+\beta[r_M-r_f]}$$Using the idea that beta is the OLS estimator, $$P=\frac{1}{1+r_f}[\bar Q-\frac{\text{Cov}(\bar Q,r_M)[r_M-r_f] }{\sigma_M^2}]$$
#### Zero beta CAPM
We know that $$\beta_i=\frac{\text{Cov}(R_i,R_M)}{\text{Var}(R_M)}$$Therefore, for $\beta_i=0$, it must be that $\text{Cov}(R_i,R_M)=0$. The portfolio $Z$ that achieves this with the market portfolio is the zero beta portfolio, whose returns ($r_{Z}$) are uncorrelated with the returns of market portfolio $M$, $r_M$. If short positions on any asset is **not allowed**, then the CAPM is$$\mathbb E(r_i)-\mathbb E(r_{Z})=\frac{\text{Cov}(r_i,r_M)}{\sigma_M^2}[\mathbb E(r_M)-\mathbb E(r_{Z})]$$
We know that this zero beta portfolio must exist. This is because, if two portfolios lie on the [[n Asset markovitz portfolio#Finding the efficient frontier|efficient frontier]], then any combination of these portfolios lie on the efficient frontier. Furthermore, for any portfolio on the efficient frontier, there lies in the bottom part of the frontier a companion portfolio such that $\text{Cov}(r,r_c)=0$
![[Pasted image 20240228165558.png|400]]

Therefore since all investors select the market portfolio based on mean variance optimization, $r_M$ is on the efficient frontier. Therefore there must be a companion portfolio ($r_{Z}$) such that $\text{Cov}(r_M,r_{Z})=0$

The zero beta capm formula implies that when there is no market risk to a portfolio it will have the same expected return as the zero beta portfolio

#### Intertemporal CAPM (ICAPM)
Given longer time horizons, different sources of risk emerge. These sources are risk factors. Supposing $K$ such risk factors affect the returns of an asset, the ICAPM is built on the formation of $K$ hedged portfolios: $r_{h1}, r_{h2}, r_{h3}, \dots$ 

The return of these hedged portfolios is not affected by the respective risk factor. The risk premium of a hedged portfolio $i$ is given by $$\text{Risk Premium}_{hi}=\mathbb E(r_{hi})-r_f$$For any asset $j$ and a hedged portfolio $i$,$$\beta_{ji}=\frac{\text{Cov}(r_j,r_{hi})}{\text{Var}(r_{hi})}$$incorporating all the different risk factors, the ICAPM is given by, for any asset $j$,$$\mathbb E(r_j)-r_f=\beta_{jM}[\mathbb E(r_M)-r_f]+\sum_{i=1}^K\beta_{ji}[\mathbb E(r_{hi})-r_f]$$If the asset is hedged against a particular risk factor (beta is 1) and has the same level of market risk (beta with market), its expected risk premium is same as that of the hedged portfolio (all other risk factors equally affecting returns across both).

#### CCAPM
Modification of CAPM with the use of many assets, which are used in order to finance lifetime consumption. This relation is expressed as $$\max_{c_{t}} \sum_{t=0}^\infty u(c_t)$$Construct a portfolio called consumption mirroring portfolio, a portfolio whose returns are highly correlated with fluctuations in consumption. The CCAPM says that $$\mathbb E(r_j)-r_f=\beta_{i}[\mathbb E(r_c)-r_f]$$This implies that the risk premium from asset $j$ is equal to the risk premium of the consumption mimicking portfolio if its OLS estimator with it is 1. 

#### Liquidity and CAPM
As liquidity decreases for an asset, its price is discounted in order to compensate for the reduction in liquidity. Moreover, when liquidity for one asset falls, it falls for all the assets. This implies that liquidity risk is correlated.

Therefore, the liquidity of the asset affects the CAPM $\mathbb E(r) \to \beta$ linear relationship.