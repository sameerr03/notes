### Future value
The total amount due at the end of an investment is the **Future value (FV)** of the investment. Suppose a cash flow $C_0$ is given into the investment in time $t=0$. Then supposing a one period system, the future value is given by $$FV=C_0(1+r)$$Where $r$ is the appropriate interest rate. Over multiple periods, the future value is given by $$FV=C_0(1+r)^T$$Where $T$ is the number of years. If the interest is compounded $m$ times in a year then $$FV=C_0(1+\frac rm)^{m\times T}$$Here $r$ is the Annual percentage rate (APR). The percentage of interest that gives the same FV at the end of $T$ years (compounded annually) is the **effective annual rate (EAR)**$$EAR=(1+\frac rm)^m-1$$The interest can also be **compounded continuously,** that is the interest is continuously compounded over infinitesimally small periods. The FV in this case is given as $$FV=C_0\times e^{rT}$$
### Present value
The current value (at $t=0$) of a future sum of money or stream of cash flows, given a specified rate of return is the **present value (PV)** of the sum of money/stream of cash flows. Suppose the cash flow $C_1$ is given at the end of the one period investment, the present value is given by $$PV=\frac{C_1}{1+r}$$$1+r$ is the discount factor and $r$ is the given interest rate. 

If the cash flows are uncertain, we can use expected cash flows. For the $N$ different scenarios of cash flows, $$\mathbb E(CF) =\sum_{i=1}^NCF_i\times\text{Prob}_i $$and then the one period PV is given by $$PV = \frac{\mathbb E(CF)}{1+r}$$Here, $1/(1+r)$ can be represented as the **discount factor**, $DF$. Therefore, $PV = \mathbb E(CF)\times DF$
### Net present value
Typically investments have a cash inflow, and then a greater cash outflow. Graphically in a one period model, 
![[Pasted image 20240207162658.png|400]]
The **net present value (NPV)** is the present value of future cash flows minus the present value of the cost of investment (Initial investment). In this case, the future cash flow is $C_1$ and the cost of investment is $C_0$. Therefore, the NPV is given by $$NPV=-C_0+PV=-C_0+\frac{C_1}{1+r}$$

