A model that explains the returns of a [[Financial Assets|asset]] in different systematic and non systematic factors. Systematic factors refer to macroeconomic/market related factors and non systematic relates to idiosyncratic or firm specific factors. 

Returns on an asset are modelled as fluctuations around the expected return on the assets. These fluctuations are from the factors mentioned above. $$r_i=\mathbb E(r_i)+\text{Fluctuations}$$Subtracting the risk free rate of return $r_f$ from both sides, $$r_i-r_f=\mathbb E(r_i-r_f)+\text{Fluctuations}\implies R_i=\mathbb E(R_i)+\text{Fluctuations}$$The fluctuations are split into the systemic part, $F$ and the idiosyncratic part $e_i$$$R_i=\mathbb E(R_i)+F+e_i$$However, different assets have different sensitivities to systemic factors. Accounting for this using the [[Simple Linear Regression|OLS]] regression parameter, $$R_i=\mathbb E(R_i)+\tilde \beta_iF+e_i$$
### Assumptions
- $\text{Cov}(F,e_i)=0$ -> systemic and idiosyncratic risk are independent.
- $\text{Cov}(e_i,e_j)=0$ -> idiosyncratic risks are independent between two different assets
- $\mathbb E(F)=0, \mathbb E(e_i)=0$


### Multiple factors
Uses multiple instead of single factors for systemic risk of an asset. The returns of an asset are given by $$R_i=\mathbb E(R_i)_+\tilde\beta_{i1}F_1+\tilde\beta_{i2}F_2+e_i$$where $F_1$ and $F_2$ can be any form of macroeconomic systemic risk variables, or market risk. 