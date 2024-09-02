### [[Bond Valuation]]
Companies can raise money through selling corporate bonds (debt financing). This is a type of fixed income security. 

Bonds pay a coupon amount periodically. They pay the principal/face value back (1000 here) at the end, when the bond matures. If the price of the bond is $P$, the payoff structure of the bond is ![[Pasted image 20240828151036.png|500]]

We can also calculate the present value of the bond. This is given by $$PV = \sum_{i=1}^{n-1}(\frac{c}{(1+r)^i})+\frac{1000+c}{(1+r)^n}$$We can solve for $r$ such that $PV=P$. The interest rate $\lambda$ that gives us this equality is the yield to maturity (YTM) of the bond.
$$P = \sum_{i=1}^{n-1}(\frac{c}{(1+\lambda)^i})+\frac{1000+c}{(1+\lambda)^n}$$
The relation between the price of the bond and the YTM is as follows:
![[Pasted image 20240828151503.png|400]]
When the bond yield is equal to the coupon rate (c as a percentage of the face value), the price of the bond is equal to the face value. Longer term bonds have a higher sensitivity to interest rate changes, as they have more cash flow streams dependent on them.

### Duration
Duration is a measure of a fixed income securities' sensitivity to interest rates. The duration of a fixed income security is a weighted average of the times in which cash flows are received. The weighting coefficients are the present values of the individual cash flows.$$D =\frac{PV(t_0)t_0+PV(t_1)t_1+\dots+PV(t_n)t_n}{PV}$$Where:
- $PV(t_k)$ is the present value of the cash flow that occurs in time $t_k$. 
- $PV$ is the total present value of the fixed income security

#### Interest duration
Using [[Future and present values#Future value|continuous]] compounding, the present value of a FIS is given by $$PV=e^{-rt_0}x(t_0)+e^{-rt_1}x(t_1)+\dots+e^{-rt_n}x(t_n)$$where $x(t_k)$ is the cash flow from the instrument at time $t_k$. In order to find the effect of interest rates on the present value of the bond, we differentiate with respect to $r$. This gives us$$\frac{dPV}{dr} = -e^{-rt_0}x(t_0)t_0-e^{-rt_1}x(t_1)t_1-\dots-e^{-rt_n}x(t_n)t_n$$$$\frac{dPV}{dr}=-DPV$$Therefore, $$-D = \frac{1}{PV}\frac{dPV}{dr}$$
This shows that duration directly measures the relative sensitivity of the present value of the instrument with respect to the interest rate. 

#### Macaulay Duration
When looking at bonds, it makes sense to look at the sensitivity to the YTM, as it is related to the price of the bond. For a bond with stream of cash flows $x$, compounded $m$ times in a year for $n$ periods with YTM $\lambda$, the price/present value is given by $$PV = \sum_{k=1}^n\frac{x(t_k)}{(1+\lambda/m)^{t_k}}$$The Macaulay duration is given by $$D = \frac{\sum_{k=1}^n(t_k/m)x(t_k)/[1+\lambda/m]^{t_k}}{PV}$$as $\frac{x(t_k)}{(1+\lambda/m)^{t_k}}$ is the PV of the cash flow in $t_k$, and $t_k$ is the time part from the duration definition and it is divided by $m$ as it is compounded $m$ times a year. 

#### Price sensitivity in terms of duration
Taking the derivative w.r.t. $\lambda$,$$\frac{dPV}{d\lambda} = \sum_{k=1}^n\frac{-(t_k/m)x(t_k)}{(1+\lambda/m)^{t_k+1}}=\sum_{k=1}^n\frac{-(t_k/m)}{(1+\lambda/m)}PV(t_k)$$$$\frac{dPV}{d\lambda} = -\frac{1}{1+\lambda/m}DPV$$If we consider $D_M=(1/[1+\lambda/m]D$, then $$\frac{dPV}{d\lambda}=-D_MPV$$but $P= PV$. Therefore $$\frac{dP}{d\lambda}=-D_MP$$$$\frac 1P\frac{dP}{d\lambda}=-D_M\implies\Delta P\approx-D_MP\Delta\lambda$$after discretizing. 
 
#### Sensitivity of a portfolio of bonds
Consider a portfolio $\Pi$ of $k$ bonds. The present value of the portfolio is given by $$PV(\Pi) = \sum_{i=1}^kPV(i)$$The sensitivity of the portfolio to $\lambda$ is given by $$\frac{dPV(\Pi)}{d\lambda} = \sum_{i=1}^k\frac{dPV(i)}{d\lambda}=\sum_{i=1}^k-D_{M,i}PV(i)$$If we consider the weight of each bond in the portfolio $w$ such that$$w_i=\frac{PV(i)}{PV(\Pi)}$$the sensitivity of the portfolio to yields is given by $$\frac{dPV(\Pi)}{d\lambda}=(\sum_{i=0}^k-D_{M,i}w_i)PV(\Pi)$$ The duration of the portfolio is the weighted sum of the duration of the individual assets. 
$$\frac1{PV(\Pi)}\frac{dPV(\Pi)}{d\lambda}=-D_M(\Pi)=\sum_{i=0}^k-D_{M,i}w_i$$
### Immunization and convexity
The procedure of structuring a bond portfolio so that it is protected (hedged) against interest rate risk is called **immunization**. This is done by creating a portfolio of bonds that has the same duration as the desired obligation of payments. If the payment has a duration of 10, we form a portfolio using a linear combination of a bond of higher and lower duration to obtain a portfolio of the same duration. 

**Convexity** is the second derivative of the present value with respect to the interest rates. By including a second order term, we can get an even better hedged portfolio. When the interest rate is $r$, the convexity is given by $$C=\frac{1}{PV}\frac{d^2PV}{dr^2}$$If we take continuous time compounding, the second derivative is given by $$\frac{d^2PV}{dr^2}=e^{-rt_0}x(t_0)t_0^2+e^{-rt_1}x(t_1)t_1^2+\dots+e^{-rt_n}x(t_n)t_n^2$$Therefore, the convexity is given by $$C=\frac1{PV}\sum_{k=0}^N[e^{-rt_k}x(t_k)t_k^2]$$
If we are using semi-annual compounding, the second derivative is given by $$\frac{d^2P}{d\lambda^2}=\sum_{k=0}^N\frac{(t_k/m^2)(t_k+1)x(t_k)}{[1+(\lambda/m)]^{t_k+2}}=\frac{1}{[1+(\lambda/m)]^2}\sum_{k=0}^N\frac{(t_k)(t_k+1)}{m^2}PV(t_k)$$
Putting this together, if $C$ is the convexity, $D_M$ is the modified duration, $\lambda$ is the YTM and $P$ is the price, for a small change in $\lambda$, $$\Delta P\approx-D_MP\Delta \lambda+\frac{P\times C}{2}(\Delta\lambda)^2$$
