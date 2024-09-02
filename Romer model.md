An alternative to the [[Solow model - with ideas]]. As opposed to the solow model, the romer model uses 3 sectors in order to determine the labour market. The final equations for steady state values are the same as the [[Solow model - with ideas]], but endogenize parameters that the solow model does not. The three sectors are:
- Final Goods sector - Perfect competition
- Intermediate goods sector - Firms make profits to buy ideas, and sell output using these ideas to the final good sector
- Research sector - Comes up with new ideas

Technology grows at the same rate as [[Solow model - with ideas]], but $s_R$ is now determined endogenously.$$\frac{\dot A}A=\theta\frac{(s_RL)^\lambda}{A^{1-\phi}}$$

#### Final Goods sector
The final goods sector has the production function$$Y=L_Y^{1-\alpha}\int_0^Ax_j^\alpha d_j$$where: 
- $L_Y$ is the number of workers in the final goods sector
- $x_j\ (j\in[0,A])$ are the intermediate goods used in production (a continum that adds upto $A$).
- The expression under the integral replaces the capital goods variable ($K$) used in the solow model

In this model, as technology evolves, $A$ increases. The profit of these final goods sector [[firm]]s are:$$\Pi=L_Y^{1-\alpha}\int_0^Ax_j^\alpha d_j-wL_Y-\int_0^Ap_jx_jd_j$$where:
- $w$ is the wage of the workers in the final goods sector
- $p_j$ is the price of $x_j$.

Maximising profit, the first order conditions are:
$$w=(1-\alpha)L_Y^{-\alpha}\int_0^Ax_j^\alpha d_j$$$$=\frac{(1-\alpha)L_Y^{1-\alpha}\int_0^Ax_j^\alpha d_j}{L_Y}$$$$=(1-\alpha)\frac Y{L_Y}$$and$$p_j=\alpha\ L_Y^{1-\alpha}x^{\alpha-1}_j$$

#### Intermediate goods sector
The principle behind the intermediate goods sector is that the firms in this sector use raw capital and transform it into a finished capital good using [[Ideas]], which is sold to the final goods sector at no cost of production (ideas have low marginal cost).

Once and Idea is bought, no one else can use it. Therefore, the firms act as monopolies for producing the intermediate goods. The price charged for the final intermediate good is the price charged by a monopolist. $$\Pi_j=p_j(x_j)x_j-rx_j$$Where:
- $p_j$ is the price of a finished capital good
- $r$ is the price of raw capital good

The price is a function of quantity (demand function) as if the monopolist increases the production of $j$ arbitrarily, the prices will go down.

Maximizing the profit,$$\frac{d\pi}{dx_j}=p_j'(x_j)x_j+p_j(x_j)-r=0$$$$p_j'(x_j)x_j+p_j(x_j)=r$$$$p_j'(x_j)\frac {x_j}p+1=\frac rp$$$$p=\frac 1{1+\frac{p'(x)x}p}r$$The term in the denominator is the price elasticity of x. Using the price found in the first order condition of the final goods sector firms' profit function($p_j=\alpha\ L_Y^{1-\alpha}x_j^{\alpha-1}$),$$\frac{dp_j}{dx_j}=\alpha(\alpha-1)L_Y^{1-\alpha}x^{\alpha-2}$$$$\frac{x_j}{p_j}\frac{dp_j}{dx_j}=\alpha-1$$as $p_j$ and $x_j$ get cancelled. Putting this value of elasticity into the denominator of the equation for $p$,$$$$$$p=\frac 1\alpha r$$Therefore, the intermediate firm charges $\frac r\alpha$ for the intermediate good. As $\alpha<1$, the price is greater than the marginal cost which means that the intermediate firms make profits. All of these intermediate firms charge the same price as well, as they all go through the same profit maximisation. All intermediate firms also have the same demand function $p_j=\alpha\ L_Y^{1-\alpha}x_j^{\alpha-1}$, which means that the final goods firm buys a fixed quantity of intermediate goods. Therefore $$x_j=x$$If $K$ is the total stock of capital, the sum of all $x$ is the value of $K$. Therefore, $$K=\int_0^Axd_j$$$$K=x\int_0^Ad_j$$$$=xA$$$$x=\frac KA$$Putting this value of $x$ into the final goods output function,$$Y=L_Y^{1-\alpha}\int_0^A(\frac KA)^\alpha d_j$$$$=L_Y^{1-\alpha}A(\frac KA)^\alpha$$$$=K^\alpha(AL_Y)^{1-\alpha}$$

###### Profits made by Intermediate firms
The marginal cost of Labour is given by $$w=(1-\alpha)\frac Y{L_Y}$$This means that $$Y=\alpha Y+(1-\alpha) Y=\alpha Y+wL_Y$$
The other source for expenditure in the economy is from capital goods. We get this from $$\int_0^Ap_jx_jd_j=\alpha Y$$$$\alpha Y=\int_0^A\frac r\alpha\frac KAd_j$$$$rK=\alpha^2Y$$The profits made by intermediate firms all together are$$\int_0^A\pi_jd_j=\int_0^Ap_jx_jd_j-\int_0^Arx_jd_j$$$$=\alpha Y-Axr$$$$=\alpha Y-A\frac KA\frac{\alpha^2 Y}K$$$$=\alpha(1-\alpha)Y$$As all intermediate firms are identical and produce the same output, the profits for each firm is given by $$\pi=\frac{\alpha(1-\alpha)Y}A$$Unlike the solow model, the output of these firms goes into making profits, which is used to buy new ideas.

#### Research sector
Researchers who come up with ideas get a patent, which can be sold for a price $(P_A)$ to intermediate firms. The intermediate firms can use this idea indefinately, which generates a constant stream of profits for them. The price of the patent should be based on this stream of profits. This uses the arbitrage equation$$rP_A=\pi+\dot P_A$$Where:
- $rP_A$ is the alternative to the patent, where the price of the patent is invested into a bank instead, with the rate of return $r$.
- $\pi$ is the profits from the patent
- $\dot P_A$ is the change in the value of the patent (can be sold later for either a profit or a loss).

The price must be the same such that the returns from using the patent and investing the money must be the same. From the equation,$$r=\frac \pi {P_A}+\frac{\dot P_A}{P_A}$$We know from the [[Kaldor facts]] that along the balanced growth path, $r$ remains constant. For $r$ to remain constant, $\frac \pi {P_A}$ must be constant. We know that $\pi=\alpha(1-\alpha)Y/A$, and Y grows at n+g, while A grows at g. This means that $\pi$ grows at n. If $\pi$ grows at n, $P_A$ must also grow at n. This means that $$\frac{\dot P_A}{P_A}=n$$Therefore,$$r=\frac \pi {P_A}+n$$$$P_A=\frac \pi{r-n}$$

#### Labour market equilibirum
$s_r$ is the share of workers working in R&D in an economy. They work with the probability $\bar\theta$ of success of producing a patent. When successful, they earn the price of the patent. However, if they worked in the final sector, they would earn the wage rate, $w$ for certain. In equillibrium,$$w=\bar\theta P_A$$$$(1-\alpha)\frac Y{L_Y}=\bar\theta \frac \pi{r-n}=\frac {\alpha(1-\alpha)Y}{A(r-n)}$$$$\frac 1{L_Y}=\frac{\bar\theta}A\frac\alpha{(r-n)}$$From the [[Solow model - with ideas]], we know that $\dot A/A=\bar\theta L_A/A$. The growth rate of $A$ is $g_A$. Substituting and transforming, we get $\bar\theta/A=g_A/L_A$. Substituting this into the equillibrium equation,$$\frac 1{L_Y}=\frac{\alpha g_A}{L_A(r-n)}$$$$\frac 1{(1-s_R)L}=\frac{\alpha g_A}{s_R(r-n)L}$$$$\frac1{1-s_R}=\frac{\alpha g_A}{s_R(r-n)}$$$$s_R=\frac1{1+\frac{r-n}{\alpha g_A}}$$