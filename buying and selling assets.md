Consider a risky asset with the payoffs $x_H$ with probability $\alpha=0.5$ or $x_L$ with probability $1-\alpha=0.5$
The price of the asset is $p$. $u(x)=x$. This is represented in the lotteries
$l_{\text{buy}}=[x_H-p,0.5;x_L-p,0.5]$
$l_{\text{sell}}=[p-x_H,0.5;p-x_L,0.5]$
$l_{\emptyset}=0$
##### For an [[vNm Expected utility]] maximizer
$$U(l_{\emptyset})=u(0)=0$$$$U(l_{\text{buy}})=\frac 12u(x_H-p)+\frac 12u(x_L-p)$$$$U(l_{\text{sell}})=\frac 12u(p-x_H)+\frac 12u(p-x_L)$$The investor is only going to buy the asset if $$U(l_{\text{buy}})\ge U(l_{\text{sell}})$$$$U(l_{\text{buy}})\ge U(l_{\emptyset})$$From the first condition, $$x_H-p+x_L-p\ge p-x_H+p-x_L$$$$ p\le\frac{x_H+x_L}{2}$$From the second condition,
$$x_H-p+x_L-p\ge 0$$$$ p\le\frac{x_H+x_L}{2}$$If $p$ is less than expected return of the asset, it is bought. If $p$ is greater, the asset is sold. Therefore the investor always holds a position in the asset.

##### for a [[Rank dependent utility (RDU)]] maximizer
$$U(l_{\text{buy}})=u(x_H-p)w(\frac 12)+u(x_L-p)(w(1)-w(\frac 12))$$
$$U(l_{\text{sell}})=u(p-x_H)w(\frac 12)+u(p-x_L)(w(1)-w(\frac 12))$$$$U(l_{\emptyset})=0$$
The investor is only going to buy the asset if $$U(l_{\text{buy}})\ge U(l_{\text{sell}})$$$$U(l_{\text{buy}})\ge U(l_{\emptyset})$$Using the first condition,
$$(x_H-p)w(\frac 12)+(x_L-p)(1-w(\frac 12))\ge (p-x_H)w(\frac 12)+(p-x_L)(1-w(\frac 12))$$$$w(0.5)x_H+(1-w(0.5))x_L-p\ge p-w(0.5)x_L-(1-w(0.5))x_H$$$$p\le\frac{x_H+x_L}{2}$$Using the second condition,
$$w(0.5)x_H+(1-w(0.5))w_L-p\ge0$$$$p\le w(0.5)x_H+(1-w(0.5))x_L$$From the first condition,$$p\le0.5x_H+x_L-0.5x_L$$$$p\le x_L+0.5[x_H-x_L]$$From the second condition,
$$p\le w(0.5)x_H+x_L-w(0.5)x_L$$$$p\le x_L+w(0.5)[x_H-x_L]$$As $w(0.5)<0.5$ ($w$ is convex),
$$x_L+w(0.5)[x_H-x_L]< x_L+0.5[x_H-x_L]$$Therefore if the second condition is satisfied, the first is satisfied as well.

##### For a [[Maximin Expected Utility (MEU)]] maximizer
Consider an investor with given amount of wealth. The asset gives 1000 in the good state ($g$)and 0  in the bad state $(b)$. The set of priors over $\{g,b\}$ is given by $$C=\{(\mu,1-\mu):\mu\in[1/4,3/4]\}$$In the lottery that the investor buys/sells the asset, 
$f_{\text{buy}}=[1000-p,\mu;-p,1-\mu]$
$f_{\text{sell}}=[p-1000,\mu;p,1-\mu]$
$f_{\emptyset}=0$

$$EU(f_B,\mu)=1000\mu-p\mu-(1-\mu)p$$$$=1000\mu-p$$$$EU(f_S,\mu)=p\mu-1000\mu+(1-\mu)p$$$$=p-1000\mu$$
Finding the MEU from the EU,$$\text{MEU}(f_B,\mu)=\text{min}(1000\mu-p);\mu\in[1/4,3/4]$$$$=1000\times\frac 14-p$$$$=250-p$$$$\text{MEU}(f_B,\mu)=\text{min}(p-1000\mu);\mu\in[1/4,3/4]$$$$=p-1000\times \frac34$$$$=p-750$$ The investor will only buy the asset if
1. $\text{MEU}(f_B)\ge\text{MEU}(f_S)$
2. $\text{MEU}(f_B)\ge\text{MEU}(f_\emptyset)$

**From the first condition,**$$250-p\ge p-750$$$$\implies p\le500$$**From the second condition,**$$250-p\ge0$$$$\implies p\le 250$$Therefore both theses conditions are satisfied if the 2nd condition is. The investor will only buy the asset for 250 or below.

The investor will sell the asset if
1. $\text{MEU}(f_S)\ge\text{MEU}(f_B)$
2. $\text{MEU}(f_S)\ge\text{MEU}(f_\emptyset)$

**From the first condition,**$$250-p\le p-750$$$$\implies p\ge500$$**From the second condition,**$$p-750\ge0$$$$\implies p\ge 750$$Both these conditions hold if the second condition holds. The investor will sell the asset if the price is greater than or equal to 750. 

Therefore a **bid-ask spread forms**. This is represented through 
![[Pasted image 20231202212833.png|500]]
