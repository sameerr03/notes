There are different types of [[Cash flows|cash flow]] streams, based on which the calculation of the [[Future and present values#Present value|present value]] is slightly different. 

##### Perpetuity
A **perpetuity** is a constant steam of cash flows that lasts forever. Graphically, ![[Pasted image 20240212210512.png]]
where $C$ is the cash flow at each period, forever. If the appropriate interest/discount rate is $r$, then discounting the cash flows for each period, we get $$PV=\frac{C}{(1+r)}+\frac{C}{(1+r)^2}+\frac{C}{(1+r)^3}+\dots$$in period 0. This forms a infinite geometric series. $$PV = \frac{C}{(1+r)}+\frac 1{(1+r)}[\frac{C}{(1+r)}+\frac{C}{(1+r)^2}+\frac{C}{(1+r)^3}+\dots] $$$$PV = \frac{C}{1+r}+\frac{PV}{1+r}$$$$\frac{(1+r)PV-PV}{1+r}=\frac{C}{1+r}$$$$rPV=C$$$$PV=\frac Cr$$
##### Growing perpetuity
A **growing perpetuity** is a constant stream of cash flows that grow at a constant rate, forever. 
![[Pasted image 20240212210911.png]]
where $g$ is the growth rate in each period. Summing up the discounted cash flows in each period, we get $$PV=\frac{C}{1+r}+\frac{C(1+g)}{(1+r)^2}+\frac{C(1+g)^2}{(1+r)^3}+\dots$$This is another geometric sum. This simplifies into $$PV=\frac C{r-g}$$It is necessary that $r>g$.

###### Annuity
An **Annuity** is a stream of constant cash flows that lasts for a fixed number of periods. Graphically, ![[Pasted image 20240212211305.png]]
The sum of the discounted cash flows gives us the present value$$PV=\frac{C}{(1+r)}+\frac{C}{(1+r)^2}+\frac{C}{(1+r)^3}+\dots +\frac{C}{(1+r)^T}$$In order to condense the calculation, we assume two perpetuities, one starting from period 1 and the other from $T+1$. The difference between the present value of these two perpetuities will give us the present value of the annuity. The first perpetuity has the PV$$PV_1=\frac Cr$$The second has the same PV in period $T$. Therefore to find its PV in period 0, it has to be discounted by $T$ periods. Therefore$$PV_2=\frac{C}{r(1+r)^T}$$Taking the difference, $$PV_A=PV_1-PV_2=\frac Cr[1-\frac1{(1+r)^T}]$$
The term $\frac 1r[1-\frac1{(1+r)^T}]$ is called the **present value interest factor for annuities**. 

##### Growing Annuity
A **growing annuity** is a stream of constant cash flows that grows at a constant rate for a fixed number of periods. Graphically, 
![[Pasted image 20240212212338.png]]
The present value is the sum of discounted cash flows. Therefore, $$PV=\frac{C}{(1+r)}+\frac{C(1+g)}{(1+r)^2}+\frac{C(1+g)^2}{(1+r)^3}+\dots +\frac{C(1+g)^{T-1}}{(1+r)^T}$$Using a similar method to find the condensed form as in the case of the annuity, the present value is given by $$PV=\frac C{r-g}[1-(\frac{1+g}{1+r})^T]$$
where $\frac 1{r-g}[1-(\frac{1+g}{1+r})^T]$ is the present value interest factor for a growing annuity


