|1/2|M|O|X|
|---|---|---|---|
|M|4,2|0,0|0,1|
|O|0,0|2,4|1,3|

**For player 2**

$EU_2(M,\sigma_1)=2p$
$EU_2(O,\sigma_1)=4-4p$
$EU_2(X,\sigma_1)=3-2p$

![[SmartSelect_Pin.jpg|400]]

Looking at various types of equilibriums,

Type A:
Mixes between M,O,X. As the three lines do not intersect, this is not possible. Mathematically, M and O give 2/3 whereas X and M give 3/4.

Type B:
Stratergy is mixed between M and O only. On the graph, this stratergy has less EU than stratergy X at the same value of p. Therefore it is dominated and as a result is not played. At p=2/3, 
$$EU_2(M,\sigma_1)=EU_2(O,\sigma_1)=\frac 4 3\le EU_2(X,\sigma_1)=\frac 5 3$$
This violates the second rule under [[Nash equilibrium#Rules for MSNE]]. Cannot be a MSNE

Type C:
Stratergy is mixed between M and X. This is a possibilty. Stratergy is mixed when p=3/4$$EU_2(M,\sigma_1)=EU_2(X,\sigma_1)=\frac 32\ge EU_2(O,\sigma_1)=1$$
Holds under the rules

Type D:
Statergy is mixed between O and X. Possibility according to graph. Stratergy is mixed when p=1/2$$EU_2(O,\sigma_1)=EU_2(X,\sigma_1)=2\ge EU_2(X,\sigma_1)=1$$
Holds under the rules


**For player 1:**
Player 1 [[Belief|believs]] that player 2 plays $\sigma_2=(q_1,q_2,1-q_1-q_2)$

Type C:
P2 mixes between M and X if p=3/4
$\sigma_2=(q_1,0,1-q_1)$

$EU_1(M,\sigma_1)=4q_1$
$EU_2(O,\sigma_1)=1-q_1$

If player 1 is indifferent between M and O when$$4q_1=1-q_1$$$$q_1=\frac 15$$

Both players are playing a mutual [[Best Response]]. Therefore this is a MSNE.
$$MSNE=((\frac 34,\frac 14),(\frac 15,0,\frac 45))$$

Type D:
P2 mixes between O and X if p=1/2
$\sigma_2=(0,q_2,1-q_2)$

$EU_1(M,\sigma_1)=0$
$EU_2(O,\sigma_1)=q_2+1$

Here this mixed stratergy is clearly not the best response for player 2. Therefore this cannot be a MSNE.

