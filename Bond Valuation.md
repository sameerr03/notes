A bond is a legally binding agreement between a borrower and a lender that specifies the 
- Par (Face) Value ($\nu$) -  amount paid at maturity to lender. This amount is typically 1000 USD
- Coupon rate ($c$) -  percentage of the face value that is given at periodic intervals to the lender
- Coupon payment and frequency - How often the coupon is paid (Annually, semi-annually, etc.)
- Maturity date - Date when the face value of the bond has to be paid back to the lender.

A bond's **yield** is the annual rate of return on the bond. This return is from two sources - Capital gains (buying low and selling high in a secondary bond market) and the interest payments by the borrower. The yield takes both of these into account.

The **yield to maturity (YTM)** of a bond is the yearly returns the bond provides if the bond is purchased at a date later than the date issued, till its maturity. 

$$YTM=\text{Current yeild}+\text{Capital Gains yeild}$$
The present value of a bond is given by 
$$PV=\frac{c\nu}{(1+r)}+\frac{c\nu}{(1+r)^2}+\frac{c\nu}{(1+r)^3}+\dots+\frac{(1+c)\nu}{(1+r)^n}$$This can be calculated using the [[Valuing cash flow streams#Annuity|Annuity]] formula. $$PV=\frac{c\nu}{r}[1-\frac{1}{(1+r)^n}]+\frac{\nu}{(1+r)^n}$$
The yield to maturity is the rate of interest $r$ such that at $r$, the price of the bond equals the present value of the bond. 
![[Pasted image 20240305025804.png|700]]

When the yield to maturity is equal to the coupon rate, the face value of the bond is equal to the price of the bond. (Assume that the price of the bond is equal to the present value of the bond, in a perfectly competitive bond market). If the bond is trading at a premium, its capital gains are lower, implying that it will have a lower YTM. 

The **current yield** of a bond is given by $$\text{Current Yield}=\frac{c\nu}{\text{Price paid for the bond}}$$The current yield is equal to the YTM and the coupon rate when PV of the bond equals the price of the bond. 

Bonds of similar risk and maturity will be priced to yield the same return, regardless of the coupon rate. 

#### Bond risks
##### Price risks
Changes in interest rates affect the prices of the bonds. An increase in the interest rate reduces the present value and hence the price of a bond.  

Long term bonds as a result are more susceptible to interest rate fluctuation based price risk, as a change in the interest rates will affect future cash flows, which there are more of in a long term bond, thereby affecting the price more. 

As longer term bonds are more prone to interest rate changes, they have higher YTMs

##### Reinvestment Risk
The discounted valuation of the bond is reliant on the assumption that the cash flows received by the investor from coupon payments is reinvested into another asset at the discount rate (interest rate).

However, with bonds, reinvestment risk comes from the likelihood that the investment cash flows are reinvested for a lower rate of return. The lower coupon repayment reinvestment rate will result in a lower yield to maturity. 

#### Zero Coupon bonds
Bonds with a coupon rate of zero $c=0$. The yield of the bond comes from the difference in purchase price and par value. The price of the bond (present value) is calculated by $$PV=\frac{F}{(1+r)^T}$$
#### Types of bonds
##### Government bonds
**Note:** These bonds are tax exempt
**Treasury/Central**
- Bills: Mature in less than a year
- Bonds: Mature in more than 10 years
- Notes: Mature in 1-10 years

**State and municipal bonds**
Debt of state and local government with varying degrees of default. These bonds typically have higher coupon rates as the carry more default risk. 

##### Corporate bonds
Relative to government bonds, these bonds contain greater default risk. Ratings agencies can rate these bonds on the ability for them to be paid back. The rating scheme is as follows

**High grade bonds**
AAA - Extremely strong capacity to pay
AA - Very strong capacity to pay
**Medium grade**
A - Strong capacity to pay, but susceptible to changes
BBB - Adequate capacity to pay, but more susceptible to changes in circumstances
**Low grade** - speculative in terms of capacity to pay
BB 
B
**very low grade** - in many cases, already in default
C
D

#### Bonds and Interest Rates
The real rate of return of a bond measures the purchasing power of the returns from a bond whereas the nominal rate is quoted rate of interest.

The **ex-ante** nominal interest rate is the desired rate of return + adjustments for expected inflation. This is calculated by the fisher equation $$(1+R)=(1+r)(1+h)$$where:
- $R$ is the nominal interest rate
- $r$ is the real interest rate
- $h$ is the expected inflation rate

With small values of $r$ and $h$, the formula can be approximated as $$R=r+h$$Bonds are subjected to inflation related risks. A higher inflation rate results in a higher $R$, implying lower bond yields. 

#### Yield curves
From the above information, we know that 
- Bonds with the same maturity are priced to get similar YTMs
- Bonds with longer maturity periods have higher YTMs as they are more susceptible to changes in interest rates

The **term structure** of a bond is the relationship between time to maturity and yields, all else remaining equal. The **yield curve** is a graphical representation of the term structure

![[Pasted image 20240319003742.png]]

#### Factors affecting required return of a bond
- Default Risk Premium - The additional reward paid for taking on the risk that the bond issuer might default on interest/principal payments. Government T-Bills are considered risk free and bonds with lower [[Bond Valuation#Corporate bonds|bond ratings]] have to give rates of return above the risk free rate to compensate.
- Taxability Risk premium - Municipal bonds are not taxable. Taxable bonds must offer higher rate of return to account for this
- Liquidity premium - bonds which are more frequently traded will have lower required returns. More liquidity is better, but tradeoff for lower liquidity
- Other factors that may impact the cash flow of the bond

