3 decision game, rock-paper-scissors

|1/2|R|P|C|
|---|---|---|---|
|R|0,0|-1,1|1,-1|
|P|1,-1|0,0|-1,1|
|C|-1,1|1,-1|0,0|

No [[Nash equilibrium#Pure stratergy Nash Equilibrium (PSNE)|PSNE]]. Finding the expected utilities using mixed stratergies,

**For player 1**
$\sigma_2=q_1,q_2,1-q_1-q_2$
$EU_1(R,\sigma_2)=1-q_1-2q_2$
$EU_1(P,\sigma_2)=2q_1+q_2-1$
$EU_1(C,\sigma_2)=-q_1+q_2$

**For player 2**
$\sigma_1=p_1,p_2,1-p_1-p_2$
$EU_2(R,\sigma_1)=1-p_1-2p_2$
$EU_2(P,\sigma_1)=2p_1+p_2-1$
$EU_2(C,\sigma_1)=-p_1+p_2$

**Case A:** All three stratergies are mixed
For player 1,
$$EU_1(R,\sigma_2)=EU_1(P,\sigma_2)=EU_1(C,\sigma_2)$$
Substituting the equations, this is possible at $q_1=q_2=1/3$. At this mixed stratergy of P2, P1 can play $p_1,p_2\in[0,1]$

For player 2, under case 0,  $p_1,p_2\in[0,1]$. Player 2 mixes all 3 stratergies when $$EU_2(R,\sigma_1)=EU_2(P,\sigma_1)=EU_2(C,\sigma_1)$$
Subsitituting equations, they choose this stratergy when $p_1=p_2=1/3$, which is within the interval that P1 uses for $\sigma_1$. Therefore this stratergy is valid, and is a mutual best response as 
$\sigma_1=1/3,1/3,1/3$
$BR_2(\sigma_1)=q_1,q_2\in[0,1]$
$\sigma_2=1/3,1/3,1/3$
$BR_1(\sigma_2)=p_1,p_2\in[0,1]$

$$MSNE=((\frac 13,\frac 13,\frac 13),(\frac 13,\frac 13,\frac 13))$$

**Case B:** Stratergies mixed between R and P
in this case, $p_1+p_2=1$ and $q_1+q_2=1$

For player 1,$$EU_1(R,\sigma_2)=EU_1(P,\sigma_2)\ge EU_1(C,\sigma_2)$$
Substituting the restrictions on the mixed stratergy based on the case into EU functions, we get 
$EU_1(R)=-q_2$
$EU_1(P)=q_1=1-q_2$
As $q_2\in[0,1]$, $EU_1(P)$ [[dominant stratergy#Strictly dominant stratergy|strictly dominates]] $EU_1(R)$. This means that P1 never plays $R$ by [[Rationalizability]]. This means that $q_1=0$

For Player 2, if $p_1=0$,
$EU_2(R)=1-2p_2$
$EU_2(P)=p_2-1$
$EU_2(C)=p_2$

Here, $EU_2(C)$ strictly dominates $EU_2(P)$ which violates condition for [[Nash equilibrium#Rules for MSNE|MSNE]] stated earlier. This type of equillibrium does not exist.



**Case C:** Stratergies mixed between P and C
in this case, $p_1=0$ and $q_1=0$

For player 1,$$EU_1(C,\sigma_2)=EU_1(P,\sigma_2)\ge EU_1(R,\sigma_2)$$
Substituting the restrictions on the mixed stratergy based on the case into EU functions, we get 
$EU_1(R)=1-2q_2$
$EU_1(P)=q_2-1$
$EU_1(C)=q_2$
As $q_2\in[0,1]$, $EU_1(C)$ strictly dominates $EU_1(P)$. This means that P1 never plays $P$ by [[Rationalizability]]. This means that $p_2=0$

For Player 2, if $p_2=0$,
$EU_2(R)=1-p_1$
$EU_2(P)=2p_1-1$
$EU_2(C)=-p_1$

Here, $EU_2(R)$ strictly dominates $EU_2(C)$ which violates condition for [[Nash equilibrium#Rules for MSNE|MSNE]]. This type of equillibrium does not exist. 


**Case D:** Stratergies mixed between R and C
In this case, $p_2=0$ and $q_2=0$

For player 1,$$EU_1(C,\sigma_2)=EU_1(R,\sigma_2)\ge EU_1(P,\sigma_2)$$
Substituting the restrictions on the mixed stratergy based on the case into EU functions, we get 
$EU_1(R)=1-q_1$
$EU_1(P)=2q_1-1$
$EU_1(C)=-q_1$
As $q_1\in[0,1]$, $EU_1(R)$ strictly dominates $EU_1(C)$. This means that P1 never plays $C$ by [[Rationalizability]]. This means that $p_1+p_2=1$

For Player 2, if $p_2+p_1=1$,
$EU_2(R)=-p_2$
$EU_2(P)=p_1=1-p_2$
$EU_2(C)=2q_2-1$

Here, $EU_2(P)$ strictly dominates $EU_2(R)$ which violates condition for [[Nash equilibrium#Rules for MSNE|MSNE]]. This type of equillibrium does not exist. 

Therefore, there is only one MSNE of type A.


