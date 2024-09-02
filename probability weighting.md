a probability weighting function is a function $w:[0,1]\to[1,0]$ that is non-decreasing and satisfies $w(0)=0$ and $w(1)=1$

It is essentially a function that translates raw probabilities into subjective probabilities (how the probability is perceived by the DM). Eg: Risk of flying is perceived to be much higher than it actually is. 

#### example
For the following choice data![[Pasted image 20231121232249.png|600]]
the weight function can be calculated. Plotting the function 
![[Pasted image 20231121232557.png|400]]

This can be used to calculate a different kind of expected utility using these probability weighting functions. 

#### paradox with this method of EU calculation
$p=[1,\alpha+\beta;0,1-\alpha-\beta]$
$q=[1,\alpha;1+\delta,\beta;0,1-\alpha-\beta]\ \ \ \delta>0$

$q\succ p$ due to first order stochastic dominance (DM prefers $q$ to $p$ regardless of $u$ function). This is due to a higher chance of getting more money. $$U(p)=w(\alpha+\beta)$$$$U(q)=w(\alpha)+(1+\delta)w(\beta)$$$$=w(\alpha)+w(\beta)+\delta w(\beta)$$
For a convex $w$ function,
$$w(\alpha+\beta)\ne w(\alpha)+w(\beta)$$since $w$ is non-linear and $$w(\alpha +\beta)>w(\alpha)+w(\beta)$$$\exists\ \delta$ small enough such that $$w(\alpha+\beta)>w(\alpha)+w(\beta)+\delta w (\beta)$$This implies that $U(p)>U(q)\implies p\succ q$ which violates the first order stochastic dominance.

#### framing effects
$p=[1,\alpha+\beta;0,1-\alpha-\beta]$
$q=[1,\alpha;1,\beta;0,1-\alpha-\beta]$

$$U(p)=w(\alpha+\beta)$$$$U(q)=w(\alpha)+w(\beta)$$$$w(\alpha+\beta)\ne w(\alpha)+w(\beta)$$But $p\iff q$. Therefore this method of EU calculation is subject to framing effects.  