An [[Auctions]] with private valuations and sealed bids. Sealed bids are made by all the players. Bidder with the highest bid wins and the winner pays the second highest price. In [[Bayesian Form Game|Bayesian form]],

$I=\{1,2\}$
$T_1=t_1,\ T_2=t_2$
$t_i=v_i\in[0,900]$ where $y_i\sim U[0,900]$
$P(v_1,v_2)\sim U[0,900]$
$s_i=b_i\ge0$
where $b_i$ is the bid value made by player $i$.
The payoffs of this game are given by
$u_i(v_i;b_i,b_j)=v_i-b_j$ if $b_i>b_j$
                  $=\frac 12(v_i-b_j)$ if $b_i=b_j$
                  $=0$ if $b_i<b_j$

**For player 1,**
if $b_1>v_1$, for the following cases,
- $b_2>b_1$, $u_1=0$. This is the same even if $b_1=v_1$
- $b_1>b_2>v_1,\ u_1=v_1-b_2$. Here the payoff is negative. if $b_1=v_1$, then the payoff would be 0, which is stricty better
- $b_1>v_1>b_2,\ u_1=v_1-b_2$. The payoff would be the same even if $b_1=v_1$.
Therefore, $b_1=v_1$ weakly dominates $b_1>v_1$.

if $b_1<v_1$, for the following cases,
- $b_2>v_1>b_1, \ u_1=0$. This is the same even if $b_1=v_1$
- $v_1>b_1>b_2,\ u_1=v_1-b_2$. Here the payoff is positive. if $b_1=v_1$, then the payoff would be the same.
- $v_1>b_2>b_1,\ u_1=0$. The payoff would be $v_1-b_2$ if $b_1=v_1$, which is strictly better.
Therefore, $b_1=v_1$ weakly dominates $b_1<v_1$.

Same for player 2. Therefore the [[Nash equilibrium#Bayesian Form Game Bayesian Nash Equilibirium|baye's nash equilibrium]] will be$$BNE=(b_1=v_1,b_2=v_2)$$
In a second price auction, the optimal stratergy for the players is to bid **truthfully**.