#### 3 Factor Model
Suppose $i$ is an asset or a portfolio. According to the Fama-French 3 factor model, the excess return on $i$ at time $t$ is given by $$R_{it}=\alpha_i+\beta_{iM}R_M+\beta_{i\text{SMB}}\text{SMB}_t+\beta_{i\text{HML}}\text{HML}_t+e_{it}$$Where:
- $R_M$ is the excess returns on an index portfolio (Not the market portfolio, but the index portfolio)
- $\text{SMB}=r_S-r_B$ -> Small minus big. Small is a sufficiently diversified portfolio of small cap stocks and big is a sufficiently diversified portfolio of large cap stocks. Represents the different rates of returns from smaller to larger assets. 
- $\text{HML}=r_H-r_L$ -> high minus low. High is a sufficiently diversified portfolio of assets with a high book to market value ratio and low is a sufficiently diversified portfolio of assets with a low book to market ratio. ([[Balance sheet|Book Value]] = Total Assets - Total Liabilities) 

#### Criticisms of the Fama French
- Not clear what systemic sources of risk HML and SMB factors capture. The model is empirical and atheoretical.
- Because the model has worked in many cases does not mean that it will work everywhere. Some part of the correlations registered could be spurious

#### 5 Factor Model
$$R_{it}=\alpha_i+\beta_{iM}R_M+\beta_{i\text{SMB}}\text{SMB}_t+\beta_{i\text{HML}}\text{HML}_t+\beta_{i\text{CMA}}\text{CMA}_t+\beta_{i\text{RMW}}\text{RMW}_t+e_{it}$$
Where:
- $\text{RMW}=r_R-r_W$ -> Robust minus weak. Excess returns from a diversified portfolio of stocks with robust profitability minus the excess returns from a diversified portfolio of stocks with weak profitability
- $\text{CMA}=r_C-r_A$ -> Conservative minus aggressive. Excess returns from a diversified portfolio of stocks with conservative reinvestment (low reinvestment into their own business) minus excess returns from a diversified portfolio of stocks with aggressive reinvestment (high reinvestment into their own business)

