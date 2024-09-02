#### Zero Sum Game
Game where there are no clear winners. Matching pennies game
Players: N={P1,P2}
Action Spaces: $A_{P1}=\{H,T\}$,$A_{P2}=\{H,T\}$

Using a **payoff matrix**,

|P1/P2|H|T|
|---|---|---|
|H|1,-1|-1,1|
|T|-1,1|1,-1|

The game has no pure stratergy [[Nash equilibrium]]s. Instead MSNE is required. In order to find the mixed stratergy Nash equillibriums, 

**From player 1's point of view**
Player 1 [[Game Theory#Determining outcomes|believes]] that player 2 chooses a mixed stratergy $\sigma_2*=(q,1-q)$ for heads, tails. Therefore, based on the belief and payoffs, we can calculate [[vNm Expected utility]] for player 1.

Fixing player 1, as playing H
$$EU_1(H,\sigma_2*)=1(q)+(-1)(1-q)$$
$$=2q-1$$

Fixing player 1 as playing T,
$$EU_1(T,\sigma_2*)=(-1)(q)+1(1-q)$$
$$=1-2q$$

When EU of playing H and T are equal, player 1 is indifferent between H and T.
$$2q-1=1-2q$$$$4q=2$$$$q=\frac 1 2$$

At q=1/2 the player is indifferent. At this belief, player 1 can mixes the two stratergies with any probability. Plotting the expected utility functions, we get

![[SmartSelect_20230314_203852_Samsung Notes.jpg|400]]

Based on this, the best response function of player 1 is
$B_1(\sigma_2*)=H$ if $q>\frac 1 2$ => $p=1$
$\  \ \ \ \ \ \ \ \ \ \ \ \ \ =T$ if $q<\frac 1 2$ => $p=0$
$\  \ \ \ \ \ \ \ \ \ \ \ \ \ =H$~$T$ if $q=\frac 1 2$ => $p\in[0,1]$

**From player 2's point of view**
Player w [[Game Theory#Determining outcomes|believes]] that player 2 chooses a mixed stratergy $\sigma_1*=(p,1-p)$ for heads, tails. Therefore, based on the belief and payoffs, we can calculate [[vNm Expected utility]] for player 2.

Fixing player 2 as playing H,
$$EU_2(H,\sigma_1*)=1(p)+(-1)(1-p)$$
$$=1-2p$$

Fixing player 2 as playing T,
$$EU_2(T,\sigma_1*)=(-1)(p)+1(1-p)$$
$$=2p-1$$

When EU of playing H and T are equal, player 1 is indifferent between H and T.
$$2p-1=1-2p$$$$4p=2$$$$p=\frac 1 2$$

At p=1/2 the player is indifferent. At this belief, player 1 can mixes the two stratergies with any probability. 

Based on this, the best response function of player 1 is
$B_2(\sigma_1*)=H$ if $p<\frac 1 2$ => $q=1$
$\  \ \ \ \ \ \ \ \ \ \ \ \ \ =T$ if $p>\frac 1 2$ => $q=0$
$\  \ \ \ \ \ \ \ \ \ \ \ \ \ =H$~$T$ if $p=\frac 1 2$ => $q\in[0,1]$

Plotting the mutual best responses,
![[SmartSelect_20230314_204214_Samsung Notes.jpg|400]]
In case pure stratergy nash equilibria exist, they will also appear on the mutual best respone curves under certain probabilites.

From the Mutual best response graph we can see that the equillibrium is at $$NE(\sigma_1^*,\sigma_2^*)=((p,1-p),(q,(1-q))$$$$=((\frac 1 2, \frac 1 2),(\frac 1 2,\frac 1 2))$$
