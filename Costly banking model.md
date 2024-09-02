#### Model setup
- Discrete and infinite time ($t=1,2,....,\infty$)
- Agents live forever
- Every time period is divided into **two subperiods** where different activities take place. These differing activities are represented by the existence of two different markets in each time period, called market 1 and market 2. 
![[Pasted image 20231120165022.png|600]]
- In the markets, buyers and sellers trade anonymously (necessitates the use of money as trust based contracts not possible with anonymous trading).
##### In time $t$
for each time $t$,
![[Pasted image 20231120165334.png|400]]
At the end of $M2_{t-1}$/start of $M1_t$, with the probability $\alpha$, some agents become consumers in $M1_t$, that is they do not produce and only consume during the first subperiod of time $t$. With the probability $1-\alpha$ some households become worker households, that is they do not consume during the first subperiod and instead use labor to produce goods demanded by consumers and also provide labor to the banking sector. 

In $M2_{t-1}$ households do not know what their type will be in $M1_t$. Therefore the trades that they make in $M2_{t-1}$ and decisions about $M1_t$ are made under uncertainty. Households in $M2_{t-1}$ will carry some amount of money $m$ with them into the next period in order to participate in market activities in the next period. Assuming the number of households is large enough to fit the law of large numbers, 

$\alpha$ Households -> consumers
$1-\alpha$ Households -> sellers (workers)

###### In subperiod 1, with market $M1_t$
Consumers demand more liquidly (demand more money). Sellers on the other hand, as they do not consume, have excess money that they will not spend money in this subperiod, i.e. they have a liquidity surplus. Thus banks play a role in providing liquidity to the consumers.

1. Sellers make deposits to the bank
2. Bank promises to pay back the sellers at the net rate of interest $r$ in the next period
3. Consumers borrow money from the bank
4. Consumers promise to pay the bank back at the net rate of interest $r_H$ in the next period
5. Consumers pay the sellers with borrowed + their existing money 
6. Sellers exchange this money for goods which the consumers consume

![[Pasted image 20231120170926.png|400]]

For the **consumer**,
If they consume $q$ goods, then their utility is given by $$u(q)\text{ such that }\lim_{q\to 0}u'(q)=\infty,\ \lim_{q\to\infty}u'(q)=0$$(Decreasing marginal utility with an increase in $q$).

For the **producer**,
If they provide $N$ units of labor, their disutility is given by $$c(N)\text{ where }c(0)=0,\ c'>0, c''\ge 0$$(Marginal disutility increases with an increase in $N$)
Here, $$N=n+n_B$$Where:
- $n$ is the labor to produce the market 1 good
- $n_B$ is the labor that the household provides to the banks. This is compensated in $M2_t$ when the bank makes a profit

###### In subperiod 2, with market $M2_t$
In the second market, agents produce $Y$ goods, consume $X$, repay loans, redeem deposits and adjust money balances. Consumers who borrowed money enter the subperiod with debt $l$. They have to pay $r_Hl$ to the bank. Workers who deposited money, enter the subperiod with deposit $d$. They get $rd$ from the bank. Households that provided $n_B$ labor to the bank get paid a wage rate = wage rate of labor working on pure production of $M1$ goods (Perfectly competitive labor market).

In this subperiod, everyone consumes a $M2$ good which is different from the $M1$ good. There is no distinction between workers and consumers in this market. All agents work to produce $Y$ units of M2 goods. If a household consumes $X$ units of the $M2$ good, they gain utility$$u(X) \text{ where }\lim_{X\to0}u'(X)=\infty,\ \lim_{X\to \infty}u'(X)=0$$
The central bank also grows the money supply at the rate $\mu$ in $M2$. The extra money printed is given by $$\text{Money supply increase}=M_t-M_{t-1}$$$$=(\mu-1)M_{t-1}$$This quantity of money is transferred to all households in $M2_{t}$. All debts are settled in M2. Only money is carried into the next period. 


#### Symmetric equilibrium
When transitioning from M1 to M2, the consumer type has $m$ leftover money and $l$ loans taken. The worker type has $m$ money and $d$ bank deposits. This has to be accounted for in the value function for the second market. Optimization in M2 will determine the optimum levels in M1. As the M1 and M2 goods are different, let $$\phi_t M_t=\phi_{t+1}M_{t+1}$$where $\phi_t$ is the real value of money in the second market in period $t$ (1 unit of nominal money in M2 consumption good terms). 

##### M2 optimization
The value function in M2 will be $$W(m,l,d)=\max_{X,Y,m'}[U(X)-Y+\beta V(m')]$$$$\text{s.t. }X+\phi(1+r_H)l+\phi m'=Y+\phi m+\phi(1+r)d+\phi T+\phi pn_B+\phi\zeta$$Where:
- $V(m')$ is the value function of the next M1 for the agent
- $m'$ is the nominal money taken into the M1 of the next period
- $T$ is the transfer from the extra money printed by the central bank
- $\zeta$ is the profit made by the bank
- $n_B$ is the labor provided by the worker to bank

the constraint is from the consumption of M2 good, paying back loans taken from last period and requiring money for the next period. Bank workers get the same wage rate as production of goods in M1. $p$ is the nominal wage rate. 

Taking the constraint in terms of M2 good,$$-Y=\phi m+\phi(1+r)d+\phi T+\phi pn_B+\phi\zeta-X-\phi(1+r_H)l-\phi m'$$Putting this into the value function,$$W(m,l,d)=\max_{X,Y,m'}[U(X)+\phi m+\phi(1+r)d+\phi T+\phi pn_B+\phi\zeta-X-\phi(1+r_H)l-\phi m'+\beta V(m')]$$$$=\phi m+\max_X[U(X)-X]+\max_{m'}[\beta V(m')-\phi m']+\phi(1+r)d+\phi T+\phi pn_B+\phi\zeta-\phi(1+r_H)l$$$$=\phi m+U(X^*)-X^*+\max_{m'}[\beta V(m')-\phi m']+\phi(1+r)d+\phi T+\phi pn_B+\phi\zeta-\phi(1+r_H)l$$Where $X^*\text{ s.t. }\ U'(X^*)-1=0$
$$W(m,l,d)=\phi [m+(1+r)d+pn_B-(1+r_H)l]+U(X^*)-X^*+\max_{m'}[\beta V(m')-\phi m']+\phi T+\phi\zeta$$However, $$W(0,0,0)=U(X^*)-X^*+\phi T+\phi\zeta+\max_{m'}[\beta V(m')-\phi m']$$therefore, from these two equations,$$W(m,l,d)=\phi [m+(1+r)d+pn_B-(1+r_H)l]+W(0,0,0)$$Taking the **first order conditions**
$$\frac{\partial W}{\partial m}=\phi$$$$\frac{\partial W}{\partial d}=\phi(1+r)$$$$\frac{\partial W}{\partial l}=-\phi(1+r_H)$$$$\frac{\partial W}{\partial n_B}=p\phi$$Optimizing the function for the next M1
$$\text{max}_{m'}[\beta V(m')-\phi m']\implies\beta V'(m')-\phi=0$$$$V'(m')=\frac \phi\beta$$
##### M1 optimization
As only money is carried into the M1 period, the value function of a agent in M1 is given by:
$$V(m)=\max_{q,l\ge0}\ \alpha[U(q)+W(m+l-pq,l,0)]+\max_{n,n_B,d\ge0}\ (1-\alpha)[-c(n+n_B)+W(m-d+pn,0,d)]$$Where:
- $q$ is the amount of M1 goods bought
- $m+l$ is the amount of money and loans taken in the first subperiod in order to buy M1 good
- $m+l-pq$ is the total amount of money left over after buying the consumption good, which is taken into the next period
- $m-d+pn$ is the initial money, minus deposits made (will be paid back in the next period)+wage earned from M1 good production
- $W$ is only discounted across periods, not within periods
###### Worker's problem
Focusing on the part of the equation dealing with if the household becomes a worker type,$$V_W(m)=\max_{n,n_B,d\ge0}\ -c(n+n_B)+W(m-d+pn,0,d)$$$$=\max_{n,n_B,d\ge0}\ -c(n+n_B)+\phi[m+pn-d+(1+r)d+pn_B]+W(0,0,0)$$$W(0,0,0)$ is a constant value. Therefore not a part of the maximization$$=\max_{n,n_B,d\ge0}\ -c(n+n_B)+\phi[m+pn+rd+pn_B]+W(0,0,0)$$From this function it is clear that $V_W$ is linear wrt $d$ if all other variables are held constant. This means that the higher value of $d$ leads to higher $V_W$. However, note that $d\le m$ as one cannot deposit more money than one has. Therefore the utility is maximized when $d=m$. Substituting this value into the equation,$$=\max_{n,n_B\ge0}\ -c(n+n_B)+\phi[
(1+r)m+pn+pn_B]+W(0,0,0)$$Taking the **first order conditions,**$$\frac{\partial V_W}{\partial n}=-c'(N)\frac{\partial N}{\partial n}+\phi p\frac{\partial N}{\partial n}=0$$Where $N=n_B+n$$$\implies c'(N)=\phi p$$
###### Consumer's problem
Focusing on the part of the equation dealing with if the household becomes a consumer type,$$V_C(m)=\max_{q,l\ge0}\ U(q)+W(m+l-pq,l,0)$$$$=\max_{q,l\ge0}\ U(q)+\phi[m+l-pq-(1+r_H)l]+W(0,0,0)$$However, the consumer cannot buy goods more than the amount of money that they have + the loans they have taken for consumption. Therefore the constraint is $pq\le m+l$. For all values of $q<q^*$, $q$ is increased until it reaches the optimal level of $q^*$. $q^*=(m+l)/p$ as for any $q<q^*$, $q<(m+l)/p$ implies that more loans have been taken than necessary, which leads to lowering of utility as loans are negatively related to utility. For a value of $q_0$, $l_0=pq_0-m$ is needed. If $l>l_0$ is chosen as the loan amount for the same $q_0$, this will offer lower utility overall. The optimal $l$ is obtained from $l=pq^*-m$. Placing this new constraint into the equation, $$=\max_{q\ge 0}\ U(q)+\phi[m+l-pq-(1+r_H)(pq-m)]+W(0,0,0)$$We know that $l=pq-m\implies m+l-pq=0$. Therefore,$$=\max_{q\ge 0}\ U(q)-\phi[(1+r_H)(pq-m)]+W(0,0,0)$$
Optimizing w.r.t $q$,$$\frac{\partial V_C}{\partial q}=U'(q)-\phi(1+r_H) p=0$$$$U'(q)=\phi(1+r_H)p$$
###### M1 equilibrium
From combining the optimum equations from both worker's and consumer's problems, $$c'(N)=\phi p$$$$U'(q)=\phi(1+r_H)p$$$$\implies U'(q)=(1+r_H)c'(N)$$In equilibrium, all markets clear. The M1 goods market clearance require:
$$(1-\alpha)n=\alpha q$$Where:
- $(1-\alpha)n$ is the amount of M1 good (Linear production with labor (slope=1))
- $\alpha q$ is the total demand for M1 goods

From the M1 consumers problem,$$V_C=\max_{q,l\ge0}\ U(q)+\phi[m+l-pq-(1+r_H)l]+W(0,0,0)$$But, we also know that $pq=m+l$. Therefore,$$V_C=\max_{q,l\ge0}\ U(q)-\phi(1+r_H)l+W(0,0,0)$$From the M1 producers problem$$V_W=\max_{n,n_B\ge0}\ -c(n+n_B)+\phi[
(1+r)m+pn+pn_B]+W(0,0,0)$$Therefore, $V(m)$ becomes$$V(m)=\alpha[U(q)-\phi(1+r_H)l^*]+(1-\alpha)[-c(n+n_B)+\phi[
(1+r)m+pn+pn_B]]$$We know that $pq=m+l\implies q=(m+l)/p$

$$V(m)=\alpha[U(\frac{m+l^*}{p})-\phi(1+r_H)l^*]+(1-\alpha)[-c(n+n_B)+\phi[(1+r)m+pn+pn_B]]$$$$V'(m)=\alpha U'(\frac{m+l^*}{p})\cdot \frac 1p+(1-\alpha)\phi(1+r)$$$$=\phi[\frac{\alpha U'(q)}{\phi p}+(1-\alpha)(1+r)]$$From the optimization of the consumer's problem, we know that $U'(q)=\phi(1+r_H)p$
$$V'(m)=\phi[\alpha(1+r_H)+(1-\alpha)(1+r)]$$$$=\phi[1+\alpha(r_H-r)+r]$$
##### bank's profit maximization
The representative bank makes,$$=r_HL-rD-p\lambda$$$$\text{s.t. }L\le D$$where:
- $L$ is the total amount of loans
- $D$ is the total amount of deposits
- $\lambda$ is the total amount of labor provided to the bank
- $p$ is the nominal wage rate

There is a production function that uses labor and deposits from customers to generate loans. this is given by $$L=pF(\lambda)$$ where $F$ is a concave function and $F(0)=0$. The profit maximization equation is given by $$P=\max_{L,D,\lambda}\ r_HL-rD-\lambda p$$In equilibrium, the loans market clears. This means that $L=D$. Therefore,$$P=\max_{L,\lambda}\ r_HL-rL-\lambda p$$$$=\max_{\lambda}\ (r_H-r)pF(\lambda)-\lambda p$$Taking FOC,$$(r_H-r)pF'(\lambda)-p=0$$$$r_H-r=\frac 1{F'(\lambda)}$$
##### Finding equilibrium interest rates
From the [[DAD-DAS framework#Fisher Equation|fisher equation]], we know that $$(1+i)=(1+R)(1+\pi)$$Where:
- $i$ is the net nominal interest rate or the interest rate offered on an illiquid bond
- $R$ is the net real interest rate
- $\pi$ is the net inflation rate

From the [[simple model of money]], we know that inflation in the model is given by $$\frac{\text{Price tomorrow}}{\text{Price today}}=\frac{P_{t+1}}{P_t}=\frac{v_t}{v_{t+1}}$$In this model, $v_t=\phi$ and $v_{t+1}=\phi'$, the price of market 2 good in the next period. Therefore, from these two equations,$$\frac{v_{t}}{v_{t+1}}=\frac{\phi}{\phi'}=1+\pi$$Substituting this into the fisher equation,$$(1+i)=(1+R)\frac{\phi}{\phi'}$$The discount rate is based on the net real interest rate ($\beta=1/(1+R)$). This implies that$$1+i=\frac{\phi}{\phi'\beta}$$From M2 optimization, we know that 
$$V'(m')=\frac \phi\beta$$From the equilibrium in M1, we know that
$$V'(m)=\phi[1+r+\alpha(r_h-r)]$$From the banks profit maximization, we know that $$r_H-r=\frac{1}{F'(\lambda)}$$Applying stationarity, the condition $$\phi M=\phi'M'$$ has to be met. (This is the same condition as $v_tM_t=v_{t+1}M_{t+1}$ under stationarity in [[simple model of money]]). This condition implies that$$\frac{\phi}{\phi'}=\frac{M'}{M}$$$$(1+\pi)=\frac{\phi}{\phi'}=\frac{M'}{M}=\mu$$Replacing $m$ with $m'$ in the equilibrium M1 equation, we find that $$V'(m')=\phi'[1+r+\alpha(r_H-r)]$$This is because all other terms are time independent. Therefore with the M2 optimization equation,$$\frac \phi\beta=\phi'[1+r+\alpha(r_H-r)]$$$$\frac{\phi}{\beta\phi'}=1+r+\alpha(r_H-r)$$$$1+i=1+r+\alpha(r_H-r)$$$$1+i=1+r+\frac{\alpha}{F'(\lambda)}$$$$r=i-\frac{\alpha}{F'(\lambda)}$$Where $F'(\lambda)$ is the marginal product of the banking sector loan production. It is an indicator of the productivity of the banking sector. A higher MP implies that labor is used more efficiently. More efficient labor => higher $r$. higher $i$ => higher $r$. We know that $\phi/\phi'=\mu$. Therefore,$$1+i=\frac{\phi}{\phi'\beta}=\frac\mu\beta$$$$1+i=\frac\mu\beta$$Therefore if $\mu$ increases, $i$ increases. If the central bank reduces $i\to 0$ or $\mu\to\beta$, then this would mean that the interest rate on deposits would be negative for the same level of productivity of the banking sector. Therefore, at equilibrium, the net nominal interest rate on deposits is given by$$r^*=\text{max}(i-\frac{\alpha}{F'(\lambda)},0)$$In the bank's profit maximization condition,$$r_H-r^*=\frac{1}{F'(\lambda)}$$$$r_H=\frac{1}{F'(\lambda)}+r^*$$In case 1,$$r_H=\frac{1}{F'(\lambda)}+i-\frac{\alpha}{F'(\lambda)}$$$$r_H=i+\frac{1-\alpha}{F'(\lambda)}$$In case 2, $$r_H=\frac{1}{F'(\lambda)}$$Substituting this into the case 1 equation,
$$r_H=i+(1-\alpha)r_H$$$$r_H-(1-\alpha)r_H=i$$$$r_H-r_H+\alpha r_H=i$$$$r_H=\frac  i\alpha$$
Therefore, in both cases,$$r_H>i$$ as $\alpha<1$. The full condition is $r_H>i>r^*$. $r=0$ was one of the two cases. However, if $r=0$ is offered on bank deposits, no one will make deposits, will prefer to just hold money.$$r\le 0\implies i\le\frac{\alpha}{F'(\lambda)}$$We know that $i=\phi/(\phi'\beta)$ and at SME, $i=\mu/\beta-1$. Adding one two both sides of the equation,$$1+ i\le1+\frac{\alpha}{F'(\lambda)}$$$$\frac\mu\beta\le1+\frac\alpha{F'(\lambda)}$$$$\mu\le \beta(1+\frac\alpha{F'(\lambda)})$$Therefore, for very low rates of inflation, banking equilibrium does **not exist.**

#### Equilibrium Equations
**Borrowing constraint:**$$L=\alpha(pq-m)$$Where:
- $L$ is the nominal total loans
- $pq$ is the total amount spent on consumption good in M1
- $m$ is the money already in hand of each household

Substituting in the loan production function, we get$$pF(\lambda)=\alpha(pq-m)$$
**Lending constraint:**
$$\alpha(pq-m)=(1-\alpha)m$$Where:
- $\alpha(pq-m)$ is the total amount that is borrowed (loan demand)
- $(1-\alpha)m$ is the total amount that is available for lending (loan supply)

Simplifying,$$\alpha pq-\alpha m=m-\alpha m$$$$m=\alpha pq$$
**M1 optimization equation**
Putting this into the borrowing constraint,  $$pF(\lambda)=\alpha(pq-m)$$$$pF(\lambda)=\alpha(pq-\alpha pq)$$$$F(\lambda)=\alpha(1-\alpha)q$$
**Labor market clearing for banking sector:**
$$(1-\alpha)n_B=\lambda$$Where:
- $(1-\alpha)n_B$ is the total amount of labor given to the bank.
- $\lambda$ is the total labor demanded by the bank

**M1 goods market clearing:**$$(1-\alpha)n=\alpha q$$Where:
- $(1-\alpha)n$ is the total amount of labor used to produce goods (linear prod func.)
- $\alpha q$ is the total consumption goods bought.

**Equilibrium loan production function:**
As $(1-\alpha)n=\lambda$,$$F((1-\alpha)n_B)=(1-\alpha)\alpha q$$We know that $(1-\alpha)n=\alpha q$. Therefore,$$F((1-\alpha)n_B)=(1-\alpha)^2n$$This equation gives us a relation between $n$ and $n_B$.  

###### Steps for finding the eq (not asked in exam)
1. $n=g(n_B)$ using functional form of $F$
2. $N=n+n_B$
3. $C'(N)=\phi p$
4. $U'(q)=(1+r_H)C'(g(n_B)+n_B)$

#### Welfare
Welfare in this model is given as the present value of discounted  utility flows from every period. In each period, the utility is $$v=\alpha u(q)-(1-\alpha)c(N)+U(X^*)-X^*$$Therefore$$\text{Welfare}=v+\beta v+\beta^2v+...=\frac{v}{1-\beta}$$(Sum of convergent series). When welfare in this banking model - welfare without banks is plotted against inflation rate, we get the following graph:![[Pasted image 20231201233534.png|400]]
This shows that only above a certain level of inflation do banks have a positive impact on welfare.

#### Takeaways from the model
- Banking improves welfare, but only above a certain inflation rate
- Banks fail at Friedman rule ($i=0$)
- There is a spread between $r_H$ and $r$ around $i$ that arises from the cost of banking

