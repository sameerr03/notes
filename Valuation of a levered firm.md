### Adjusted present value
Adjusted present value or APV is given by $$\text{APV} = \text{NPV}+\text{NPVF}$$where:
- NPV is the [[Future and present values#Net present value|Net present value]]
- NPVF is the NPV of financing effects

The effects of financing included under the NPVF are 
- Tax subsidy/shield
- Costs of issuing new securities (float costs)
- Costs of financial distress (Cost of bankruptcy)
- Subsidies to debt financing (priority sectors, govt policy)

#### APV calculation example
![[Pasted image 20240417220024.png]]
### Flow to equity approach
Discount the cash flows from the project to the equity holders of the levered firm at the cost of levered equity capital $R_S$. This is done through the following steps
- Calculate LCF (levered cash flow)
- Calculate cost of equity ($R_S$)
- Value the LCFs at $R_S$

#### FTE example
![[Pasted image 20240417220824.png]]
![[Pasted image 20240417220842.png]]

### [[Weighted Average Cost of Capital (WACC)|WACC]] method
Discount the unlevered cash flows at the rate of the WACC. 
#### WACC example
![[Pasted image 20240417220955.png]]


### Summary 
All three methods are different valuation techniques of companies with debt financing.

|                             | APV                                  | WACC                                 | FTE                                                                  |
| --------------------------- | ------------------------------------ | ------------------------------------ | -------------------------------------------------------------------- |
| **Initial investment**      | Entire Initial investment is counted | Entire Initial investment is counted | Only the portion of the initial investment paid by equity is counted |
| **CFs**                     | Unlevered cash flow                  | Unlevered cash flows used            | Levered cash flows (UCF - interest payments)                         |
| **Discount** **Rate**       | $R_0$ unlev                          | $R_{\text{WACC}}$                    | $R_S$                                                                |
| **PV of financial effects** | Yes                                  | No                                   | No                                                                   |
$R_S$ and $R_0$ from [[Capital Structure]]. APV is when level of debt is constant, WACC when Debt-Equity ratio is constant and FTE for highly levered firms. 

#### Beta and leverage
##### No taxes and riskless debt
When there are no taxes and debt is riskless, then $$\beta_{\text{Equity}}=\beta_{\text{Asset}}(1+\frac{\text{Debt}}{\text{Equity}})$$
##### With taxes
with [[Corporate income tax]] at the tax rate $T$, $$\beta_{\text{Equity}}=(1+\frac{\text{Debt}}{\text{Equity}}\times (1-T))\beta_{\text{Unlevered Firm}}$$
##### with risky debt
in this case, $\beta_{\text{Debt}}\ne 0$. $$\beta_{\text{Equity}}=\beta_{\text{Unlevered firm}}+(1-T)(\beta_{\text{Unlevered firm}}-\beta_{\text{Debt}})\times \frac BS$$