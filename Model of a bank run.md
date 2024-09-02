We assume that agents live for three periods and the young agents only get an endowment $y$ of perishable goods. Let us assume that agents do not wish to consume in the first period.

Agents either consume in their middle age or when they are old. However, they are not aware of which type of agent they are until the second period of their life. At the end of the first period their consumption type is determined exogenously. 
- With a probability $\alpha$, an agent is an early consumer (consumes during Middle age)
- With a probability $1-\alpha$, an agent is a late consumer (Consumes during old age)

To finance their consumption, in period 1, the agent decides to either keep their endowment in storage or create capital

ROR matrix

|Financing vehicle|ROR in pd 1|ROR in pd 2|
|---|---|---|
|Storage|$1$|$1$|
|Capital|$v^k-\theta$|$X$|

Where $\theta$ is the friction of verification cost (the capital has to be verified as giving a return of $X$ in the next period in order for someone else to purchase it - in order to provide liquidity for the early consumer types).

$v^k\le X$ as it is the [[Present Value]] of the capital in period 1. The present value of an asset is given by dividing its final value by the gross rate of return on a safe asset. In this case, the gross rate of return on the safe asset (storage) is $1$. Therefore the present value of capital in period 1 is $$\text{PV of capital in pd 1}=\frac X1=X$$However, due to the friction of verification cost, we assume that $\theta$ is sufficiently large ($\theta>X-1$). This means that$$\theta>X-1\ge v^k-1$$$$\implies v^k-\theta<1$$Capital has a lower return than storage in period 1, and a higher return in period 2.

#### With banks
**Assumptions**
- There is competitive banking, i.e., banks make no profit
- Same 1 and 2 period return

Suppose the population is constant at $N$ per generation. The bank collects $Ny$ total deposits from all the young agents. We assume that $N$ is large enough to satisfy the [[point estimation|law of large numbers]]. Banks know the value of $\alpha$. Therefore, there will be $\alpha N$ and $(1-\alpha)N$ early and late consumption types respectively. 

To account for this, the banks put $\alpha Ny$ into storage and $(1-\alpha)Ny$ into capital. In the next period, $\alpha N$ agents who are found to be early types withdraw their deposits in order to consume. Each agent gets$$\frac{\alpha Ny}{\alpha N}=y$$Giving them a ROR of 1. 

In the next period, $(1-\alpha)N$ agents withdraw their deposits to consume. Each agent gets$$\frac{X(1-\alpha)Ny}{(1-\alpha)N}=Xy$$Therefore they get a ROR of $X$.

Thus the bank solves the problem of illiquidity of capital and makes all agents better off without making anyone worse off. 

#### Bank run
In the business as usual scenario,
**In period 0**
The bank collects $Ny$ deposits, of which it puts $(1-\alpha)Ny$ into capital and $\alpha Ny$ into storage. 

**In period 1**
$\alpha Ny$ early types of people collect their deposits

**In period 2**
$(1-\alpha)XNy$ late types of people collect their deposits

However, supposing a bank panic happens i.e., people feel like the bank is unable to fulfill its obligations. Because of this, everyone wants to withdraw their deposits in period 1, either to consume or to put it into storage incase they are late types. 

The panic results in the bank needing to liquidate its assets (capital) in order to pay back all the customers in period 1. This means that the bank has $$\alpha Ny+(1-\alpha )(v^k-\theta)Ny$$of consumption good after liquidation. This money has to be given to $N$ depositors. 

The maximum amount of people who can be given their deposits at ROR=1 is given by $$\frac{\alpha Ny+(1-\alpha )(v^k-\theta)Ny}{y}=\alpha N+(1-\alpha )(v^k-\theta)N<N$$
This value is less than $N$, which means that all the depositors cannot be paid back what they deposited. 

Supposing the bank instead pays everyone equally, each depositor gets$$\frac{\alpha Ny+(1-\alpha )(v^k-\theta)Ny}{N}=\alpha y+(1-\alpha )(v^k-\theta)y<y$$Therefore each depositor looses out on some consumption good due to the cost of liquidation of capital. $$\text{1pd rate of return}=\frac{\alpha Ny+(1-\alpha )(v^k-\theta)Ny}{Ny}=\alpha+(1-\alpha)(v^k-\theta)<1$$
Bank runs thus cause welfare losses and everyone gets a lower 1pd ROR due to depositor panic (can be caused through other means, such as a change in the 2pd ROR of capital or exogenous change in $\alpha$). These runs can be mitigated somewhat with better regulatory framework - monitoring by a central authority such as a central bank ensuring certain [[Bank reserve ratios|reserve ratios]] to ensure the banks liquidity.