Investors form expectations over the performance of company stock. If the stock does not perform at par with these expectations, investors will sell the stock. Therefore the cost of raising equity capital for a company is the **expected return on its stock**. 

On any [[Firm's investment decisions|capital budgeting projects]], the expected return from them must be at least equal to the expected return on a financial asset with comparable risk. 

#### Calculation using CAPM
The [[Capital Asset Pricing Model (CAPM)]] is often used in order to find the cost of equity capital for a firm. The gives us the equation $$\mathbb E(R) = R_f+\beta (\mathbb E(R_M)-R_f)$$where $$\beta = \frac{\text{Cov}(R,R_M)}{\text{Var}(R_M)}$$Projects which have [[Firm's investment decisions#Internal rate of return (IRR)|IRRs]] greater than the cost of capital are chosen. ![[Pasted image 20240408181307.png|400]]

##### Components of CAPM
###### $R_f$
This is the risk free rate of return. Calculated by taking the average yield of short term t-bills, or about 2% less than the 20-year T-Bond

###### $R_M$
$R_M$ can be estimated using either historical data or by using the [[Present Value of a stock#Zero dividend growth]] model. For an individual stock, $$R_i = \frac{D_1}{P_0}+g$$This value can be averaged over many different stocks. While this is a forward looking method, it is very difficult to accurately determine the variables. 

###### $\beta$
The sensitivity of the stock's returns to the market portfolio. It can be found by taking the OLS estimate in a regression with the market risk premium as the independent variable. The issue with this estimation is that the $\beta$ for a stock varies over time, requires a large sample size for unbiased estimation, and can be influenced by changing financial leverage and business risks. 

##### Determinants of $\beta$
- **Cyclicity of Revenues:** Stocks have different tendencies to fluctuate with regards to the business cycle of the economy - automotive stocks will tend to fluctuate with the business cycle as people will not buy cars when the economy is in recession, and pharma stocks will not fluctuate in the same manner. Stocks that are more more cyclical have higher $\beta$. 
- **Operating Leverage:** Degree to which firm can increase operating income by increasing by revenue. $$\text{OL} = \frac{q(\text{P}-\text{VC})}{q(\text{P}-\text{VC})-\text{FC}}$$where $q$ is the quantity, $\text P$ is the price, $\text{FC}$ and $\text{VC}$ are fixed and variable costs. The degree of operating leverage is how sensitive a firm is to fixed costs $$\text{DOL}=\frac{\Delta\text{EBIT}}{\text{EBIT}}\times \frac{\text{Sales}}{\Delta \text{Sales}}$$A high DOL implies greater risk, implying a greater beta
- **Financial Leverage:** The sensitivity to a firms fixed cost of financing. The relation between the betas of the firms debt, equity and assets is given by $$\beta = \frac{\text{Debt}}{\text{Debt}+\text{Equity}}\beta_{\text{Debt}}+\frac{\text{Equity}}{\text{Debt}+\text{Equity}}\beta_{\text{Equity}}$$As debt capital does not contain as much market risk as equity, $\beta_{\text{Debt}}=0$ (approx). Financial leverage always increases the $\beta_{\text{Equity}}$ relative to the $\beta$ of the firms assets.

#### Rationale behind discount rates
![[Pasted image 20240410135310.png|400]]
Using just one discount rate for all projects of a firm increases the risk of the firm. The hurdle rate does not represent the individual risks of each project and thus is not a fair representation of the opportunity costs of those projects.

#### Cost of preferred stock
Preferred stock is equity that behaves like a perpetuity - through dividend (coupon) payments. The price of the PS is the coupon paid/required return. Therefore the cost of the preferred stock is given by $$R_{PS}=\frac{c}{PV}$$
