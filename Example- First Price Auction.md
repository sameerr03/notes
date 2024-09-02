[[Auctions]] with sealed bids and private values. The highest bidder wins and pays their own bid. In [[Bayesian Form Game|bayesian form]],

$I=\{1,2\}$
$T_1=t_1,\ T_2=t_2$
$t_i=v_i\in[0,900]$ where $y_i\sim U[0,900]$
$P(v_1,v_2)\sim U[0,900]$
$s_i=b_i\ge0$
where $b_i$ is the bid value made by player $i$.
The payoffs of this game are given by
$u_i(v_i;b_i,b_j)=v_i-b_i$ if $b_i>b_j$
                  $=\frac 12(v_i-b_i)$ if $b_i=b_j$
                  $=0$ if $b_i<b_j$

$s_i=a$ where $a$ is a fraction of the valuation that is bid. The bid will always be lower than the fraction as bidding lower than the valuation is weakly dominant. 

$b_i=av_i$

**For player 1,**
if the amount that player one bids is $x$, and the other player plays the stratergy $b_2=av_2$, then p1 wins if $x>av_2$. Using the cumulative distribution function of a [[types of random variables#Uniform random variables|uniform]] distribution, 
$P(x>av_2)=P(v_2<\frac xa)=\frac x{900a}$

Calculating the expected utility,
$EU_1=P($win$)(v_1-x)+P($loose$)(0)$
$=\frac{x}{900a}(v_1-x)$

A rational player will look to maximise their expected utility. Maximising,
$$\frac{\partial EU_1}{\partial x}=\frac{v_1}{900a}-\frac{2x}{900a}=0$$$$x=\frac 12v_1$$This is the best response of player 1 to player 2's stratergy. By symmetry, the best response of player 2 to player 1 is $$b_2=y=\frac 12v_2$$Therefore, the [[Nash equilibrium#Bayesian Form Game Bayesian Nash Equilibirium|baye's nash equilibrium]] will be $$BNE=(b_1=\frac 12v_1,b_2=\frac 12v_2)$$

#### Game with $n$ bidders
In a game with $n$ bidders, the Expected utility for player 1 will remain the same. 
$EU_1=P($win$)(v_1-x)+P($loose$)(0)$
However, the probabilities will be different. 
$P($win$)=P(v_2<\frac xa\cap v_3<\frac xa\cap...\cap\ v_n<\frac xa)$
As the probabilities of $x/a$ being greated than the valuations of all the other players are independant of each other, 
$P($win$)=P((v_2<\frac xa)\cdot P(v_3<\frac xa)....P((v_n<\frac xa)$
$=(\frac x{900a})^{n-1}$
Therefore the EU function is $$EU_1=(\frac x{900a})^{n-1}(v_1-x)$$Maximizing, $$\frac {\partial EU_1}{\partial x}=\frac{(n-1)(v_1-x)}{(900a)^{n-1}}x^{n-2}-(\frac x{900a})^{n-1}=0$$Solving, we get$$x=(\frac{n-1}n)v_1$$Using symmetry, the BNE will be$$BNE=b_i=(\frac{n-1}n)v_i$$for all $i\in I$
As $n\to\infty$, $b_i\to v_i$. The more players, the closer to truthfull bidding
