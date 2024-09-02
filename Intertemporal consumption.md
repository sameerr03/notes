Deals with the tradeoff between consumption now $c_1$ and consumption later $c_2$.

The [[vNm Expected utility]] will be$$EU=pu(c_1)+(1-p)u(c_2)$$
Where $u(c_1)$ is independant of $u(c_2)$ but $c_1$ is not independant of $c_2$ as more of $c_1$ implies less of $c_2$

As consumption today is more favourable then consumption tomorrow. As a result the monetary gain of consuming tomorrow has to be greater than the money spendable today. This amount is the **discount factor** $\beta$.

1 dollar tomorrow =  $\beta$ dollars today where $\beta \in (0,1)$ 

If discounting is constant over time (exponential discounting), the utility fuction of consumption will look like
$$U(c_1,c_2,....c_T)=\sum_{t=1}^T\ \beta^{t-1}\ v(c_t)$$
utility function finds the utility from todays refernce. As future consumption is not as favoured, their rates are discounted. v() function is a period utility functiion that is independant across time periods

### Budget Sets

[[Budget sets]] are largely dependant on the endowment of the individual (money recieved now, money guaranteed later). Hovewer the individual has the opportunity to alter their budget set based on savings and credit markets. 

#### Case I: No access - No borrowing, rudimentary savings

$m_1$ is consumed in period 1 and $m_2+$ leftover $m_1$ is consumed in period 2. A maximum of $m_1+m_2$ can be consumed in period 2. 
![[Pasted image 20221116185336.png|400]]
#### Case II: Saving market access, no borrowing

Saving rate is r. The constraints of this case is determined by 
$c_1\le m$, $c_2 \le (1+r)(m_1-c_1)+m_2$

![[Pasted image 20221116190304.png|400]]

#### Case III: Imperfect capital market. (savings rate (r)< borrowing rate(r'))

$c_2=(1+r)(m_1-c_1)+m_2$ for $c_1 \le m_1$
$c_2=(1+r')(m_1-c_1)+m_2$ for $c_1 \ge m_1$

![[Pasted image 20221116190700.png|400]]

#### Case IV: Perfect capital market (borrowing rate=savings rate)

$c_2\le (1+r)(m_1-c_2)+m_2$

![[Pasted image 20221116191019.png|400]]

The budget constrain in this case will be $$c_1+\frac{c_2}{1+r}=m_1+\frac{m_2}{1+r}$$
##### [[Slutsky decomposition]]

If the rate of interest increases and a borrower remained a borrower
![[Pasted image 20221116191625.png]]
### Optimal choice

$$max\ U(c_1,c_2)=v(c_1)+\beta v(c_2)$$
such that $c_1+c_2/(1+r)=m_1+m_2/(1+r)$
$$MRS=\frac{v'(c_1)}{\beta v'(c_2)}=1+r$$
maximising, $$p_1\hat{c}_1=\frac{w_1}{1+\beta}$$
$$p_2\hat{c}_2=\frac{\beta w_1}{1+\beta}$$
If $p_1, p_2=1, 1/(1+r)$
if $\beta=1/(1+r)$
$$\hat{c}_1=\hat{c}_2=\frac{w_1}{1+\beta}$$
