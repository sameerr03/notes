Consider the lottery $[x_1,p_1;x_2,p_2;...;x_n,p_n]$ where$$x_1\succsim x_2\succsim ...\succsim x_n$$For any lottery, its decumulative distribution $G:X\to[0,1]$ (w.r.t. DMs preferences) is given by $$G(x)=\sum_{j:x_j\succ x}p_j$$Essentially the probability of the [[Lotteries|lottery]] yielding an outcome that the DM strictly prefers to $x$. Under an RDU, the decision weight attached to the outcome $x_j$ is not the raw probability $p_j$ but$$\pi(x_j)=w(G(x_{j+1}))-w(G(x_{j})$$Convention that $G(x_{n+1})=1$

$\succsim$ has an RDU representation is $\exists\ u$ such that $u:X\to\mathbb{R}$ and a [[probability weighting]] factor $w:[0,1]\to[0,1]$ such that the function $U:\Delta(X)\to\mathbb R$, which assess the lottery $p=[x_1,p_1;x_2,p_2;...;x_n,p_n]$ by$$U(p)=\sum_{j=1}^n[w(G(x_{j+1}))-w(G(x_{j})]u(x_j)$$
#### no framing effects unlike standard [[probability weighting#framing effects]]
$p=[1,\alpha+\beta;0,1-\alpha-\beta]$
$q=[1,\alpha;1,\beta;0,1-\alpha-\beta]$

According to RDU,
$$U(p)=w(\alpha+\beta)u(1)$$$$U(q)=w(\alpha)u(1)+[w(\alpha+\beta)-w(\alpha)]u(1)$$$$=w(\alpha+\beta)u(1)$$Therefore there are no framing effects in this model.

#### [[risk preference]]s in RDU
- Risk preferences in RDU are accommodated by both the $u$ function from the $w$ function
- DM shows an affinity toward risk averse behavior with "pessimistic" probability weighting

**Pessimism** holds if for any $x_i,x_j$ in the support of a lottery satisfying $p_i=p_j$, we have $$x_i\succsim x_j\implies \pi(x_i)\le \pi(x_j)$$
**Optimism** holds if for any $x_i,x_j$ in the support of a lottery satisfying $p_i=p_j$, we have $$x_i\succsim x_j\implies \pi(x_i)\ge\pi(x_j)$$Pessimism holds iff weighting function is convex. Optimism iff concave


