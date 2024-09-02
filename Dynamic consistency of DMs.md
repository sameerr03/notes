There are two types of DMs with respect to [[Time preferences|dynamic consistency]].
- Sophisticates: Take into account the dynamic inconsistency of preferences into decision making (exhibit dynamically consistent behavior)
- Naives: Do not take take into account the dynamic inconsistency of preferences into decision making (exhibit dynamically inconsistent behavior)

##### Example

Consider 4 time periods ($t=0,1,2,3$), wherin one movie plays in each time period. The utilities from the movies are $u_0=3,u_1=5,u_2=8,u_3=13$. The DM can only watch 3 movies. Let the discount fator $\delta=1$ and $\beta=1/2$. 

###### Naive DM's decision 
The naive DM will not take into account dynamic inconsistency. From the perspective of the first time period, $t=0$, 

$U_0(\text{skip 0th})=\beta\delta u_1+\beta\delta^2 u_2+\beta\delta^3 u_3=\frac 52+\frac 82+\frac{13}2=13$
$U_0(\text{skip 1st})=u_0+\beta\delta^2 u_2+\beta\delta^3 u_3=3+\frac 82+\frac{13}2=13.5$
$U_0(\text{skip 2nd})=u_0+\beta\delta u_1+\beta\delta^3 u_3=3+\frac 52+\frac{13}2=12$
$U_0(\text{skip 3rd})=u_0+\beta\delta u_1+\beta\delta^2 u_2=3+\frac 52+\frac 82=9.5$

Therefore in time period 0, the naive DM decides to skip the first move and watches the movie in time period 0. From the perspective of the second time period, $t=1$, 

$U_1(\text{skip 1st})=\beta\delta u_2+\beta\delta^2 u_3=\frac 82+\frac{13}2=10.5$
$U_1(\text{skip 2nd})=u_1+\beta\delta^2 u_3=5+\frac{13}2=11.5$
$U_1(\text{skip 3rd})=u_1+\beta\delta u_2=5+\frac 82=9$

Therefore in time period 1, the naive DM decides to skip the second movie and watches the movie in time period 1. From the perspective of the third time period, $t=2$, 

$U_2(\text{skip 2nd})=\beta\delta u_3=\frac{13}2=6.5$
$U_2(\text{skip 3rd})=u_2=8$

Therefore in time period 2, the naive DM decides to skip the third movie and watches the movie in time period 2.

Therefore the naive DM watches the movies in week 0,1,2 and skips out on the best movie in $t=3$.

###### Sophisticated DMs decision
This DM takes into account dynamic inconsistency. Therefore their decision is modelled through a [[extensive form games|extensive form game]] and their final decision is the [[Nash equilibrium#Sub game perfect Nash Equillibrium|SPNE]] of the game.

![[Pasted image 20231209203033.png]]

Using backward induction, we start at $S_3$. At every point that $S_3$ makes a decision, a movie can be watched, which gives higher utility as 
$U_3(\text{watch 3})=u_3=13$
$U_3(\text{dont watch 3})=0$

Therefore at every point, $S_3$ chooses to watch the movie. W is chosen at every node. Inducting backwards,

![[Pasted image 20231209203922.png]]The parenthesis implies that that is the movie watched, not the payoff. For $S_2$, the only non-trivial decision is taken is when 0 and 1 have been watched, as the DM will always watch a total of 3 movies. This is at the node furthest to the right. At this node, 
$U_2(\text{watch 2})=u_2=8$
$U_3(\text{dont watch 2})=\beta\delta u_3=6.5$

Therefore the DM chooses to watch the movie. $W$ is chosen at every node. Inducting backwards,
![[Pasted image 20231209204901.png]]
For $S_1$, the only non-trivial decision is taken is when 0 has been watched, as the DM will always watch a total of 3 movies. This is at the node furthest to the right. At this node, 
$U_1(\text{watch 1})=u_1+\beta\delta u_2=5+\frac 82=9$
$U_1(\text{dont watch 1})=\beta\delta u_2+\beta\delta^2 u_3=\frac 82+\frac {13}2=10.5$

Therefore the DM chooses to skip the movie. $W$ is chosen at every other node. Inducting backwards,
![[Pasted image 20231209205313.png]]
$U_0(\text{watch 0})=u_0+\beta\delta^2 u_2+\beta\delta^3 u_3=3+\frac 82+\frac {13}2=13.5$
$U_0(\text{dont watch 0})=\beta\delta u_1+\beta\delta^2 u_2+\beta\delta^3 u_3=\frac52+\frac 82+\frac {13}2=13$

Therefore the DM chooses $W$ at $S_0$. Therefore the DM watches the movies at time 0,2,3. The SPNE is ($W,DW,W,W$), which is the behavior of the sophisticated DM. 

